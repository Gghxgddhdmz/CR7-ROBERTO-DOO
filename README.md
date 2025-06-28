local GUI = {}

local Player = game.Players.LocalPlayer
local ScreenGui = Instance.new("ScreenGui", Player:WaitForChild("PlayerGui"))
ScreenGui.Name = "TabbedHubGUI"
ScreenGui.ResetOnSpawn = false

local Main, TabHolder, ContentHolder, Title
local Tabs = {}

function GUI.MakeWindow(settings)
	local hub = settings.Hub or {}

	-- Main Frame
	Main = Instance.new("Frame", ScreenGui)
	Main.Size = UDim2.new(0, 600, 0, 400)
	Main.Position = UDim2.new(0.3, 0, 0.3, 0)
	Main.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
	Main.BorderSizePixel = 0
	Main.Active = true
	Main.Draggable = true
	Instance.new("UICorner", Main).CornerRadius = UDim.new(0, 12)

	-- Title
	Title = Instance.new("TextLabel", Main)
	Title.Size = UDim2.new(1, 0, 0, 40)
	Title.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
	Title.Text = "🌐 " .. (hub.Title or "My Hub")
	Title.Font = Enum.Font.GothamBold
	Title.TextSize = 18
	Title.TextColor3 = Color3.fromRGB(0, 255, 127)
	Title.TextXAlignment = Enum.TextXAlignment.Left
	Instance.new("UICorner", Title).CornerRadius = UDim.new(0, 12)

	-- Tab Buttons Holder (Left)
	TabHolder = Instance.new("Frame", Main)
	TabHolder.Size = UDim2.new(0, 150, 1, -40)
	TabHolder.Position = UDim2.new(0, 0, 0, 40)
	TabHolder.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	Instance.new("UICorner", TabHolder).CornerRadius = UDim.new(0, 12)

	-- Tab Content Holder (Right)
	ContentHolder = Instance.new("Frame", Main)
	ContentHolder.Size = UDim2.new(1, -160, 1, -50)
	ContentHolder.Position = UDim2.new(0, 160, 0, 50)
	ContentHolder.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
	Instance.new("UICorner", ContentHolder).CornerRadius = UDim.new(0, 12)
end

-- ✅ إنشاء تبويب جديد
function GUI.NewTab(tabName)
	local Tab = {}
	local y = 10

	local button = Instance.new("TextButton", TabHolder)
	button.Size = UDim2.new(1, -20, 0, 40)
	button.Position = UDim2.new(0, 10, 0, 10 + #Tabs * 45)
	button.Text = tabName
	button.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
	button.TextColor3 = Color3.new(1, 1, 1)
	button.Font = Enum.Font.Gotham
	button.TextSize = 14
	Instance.new("UICorner", button).CornerRadius = UDim.new(0, 8)

	local frame = Instance.new("Frame", ContentHolder)
	frame.Name = tabName
	frame.Size = UDim2.new(1, 0, 1, 0)
	frame.BackgroundTransparency = 1
	frame.Visible = (#Tabs == 0)

	button.MouseButton1Click:Connect(function()
		for _, t in pairs(ContentHolder:GetChildren()) do
			if t:IsA("Frame") then t.Visible = false end
		end
		frame.Visible = true
	end)

	function Tab:AddButton(info)
		local btn = Instance.new("TextButton", frame)
		btn.Size = UDim2.new(0, 400, 0, 40)
		btn.Position = UDim2.new(0, 20, 0, y)
		btn.Text = info.Name or "زر"
		btn.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
		btn.TextColor3 = Color3.new(1, 1, 1)
		btn.Font = Enum.Font.Gotham
		btn.TextSize = 14
		Instance.new("UICorner", btn).CornerRadius = UDim.new(0, 8)

		btn.MouseButton1Click:Connect(function()
			pcall(info.Callback)
		end)

		y = y + 50
	end

	table.insert(Tabs, Tab)
	return Tab
end

-- ✅ زر الإغلاق/الفتح داخل العنوان
function GUI.MinimizeButton(config)
	if not Main or not Title then return end

	local btn = Instance.new("ImageButton")
	btn.Size = UDim2.new(0, config.Size[1], 0, config.Size[2])
	btn.Position = UDim2.new(1, -config.Size[1] - 10, 0, (40 - config.Size[2]) / 2)
	btn.Image = config.Image
	btn.BackgroundColor3 = config.Color or Color3.fromRGB(30, 30, 30)
	btn.BackgroundTransparency = 0.1
	btn.Parent = Title

	if config.Corner then
		Instance.new("UICorner", btn).CornerRadius = UDim.new(1, 0)
	end

	if config.Stroke then
		local stroke = Instance.new("UIStroke", btn)
		stroke.Color = config.StrokeColor or Color3.fromRGB(255, 255, 255)
	end

	local hidden = false
	btn.MouseButton1Click:Connect(function()
		hidden = not hidden
		TabHolder.Visible = not hidden
		ContentHolder.Visible = not hidden
	end)
end

return GUI
