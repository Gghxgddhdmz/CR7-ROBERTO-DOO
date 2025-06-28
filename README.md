local GUI = {}

local Player = game.Players.LocalPlayer local ScreenGui = Instance.new("ScreenGui", Player:WaitForChild("PlayerGui")) ScreenGui.Name = "TabbedHubGUI" ScreenGui.ResetOnSpawn = false

local Main, TabHolder, ContentHolder local Tabs = {}

function GUI.MakeWindow(settings) local hub = settings.Hub or {}

Main = Instance.new("Frame", ScreenGui)
Main.Size = UDim2.new(0, 600, 0, 400)
Main.Position = UDim2.new(0.3, 0, 0.3, 0)
Main.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Main.BackgroundTransparency = 1
Main.BorderSizePixel = 0
Main.Active = true
Main.Draggable = true
Instance.new("UICorner", Main).CornerRadius = UDim.new(0, 12)

local Title = Instance.new("TextLabel", Main)
Title.Size = UDim2.new(1, 0, 0, 40)
Title.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Title.BackgroundTransparency = 1
Title.Text = "🌐 " .. (hub.Title or "My Hub")
Title.Font = Enum.Font.GothamBold
Title.TextSize = 18
Title.TextColor3 = Color3.fromRGB(0, 255, 127)
Title.TextXAlignment = Enum.TextXAlignment.Left
Instance.new("UICorner", Title).CornerRadius = UDim.new(0, 12)

local collapseBtn = Instance.new("ImageButton", Title)
collapseBtn.Size = UDim2.new(0, 24, 0, 24)
collapseBtn.Position = UDim2.new(1, -30, 0.5, -12)
collapseBtn.Image = "rbxassetid://15507434243"
collapseBtn.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
collapseBtn.BackgroundTransparency = 1
Instance.new("UICorner", collapseBtn).CornerRadius = UDim.new(1, 0)

local collapsed = false
collapseBtn.MouseButton1Click:Connect(function()
	collapsed = not collapsed
	if TabHolder then TabHolder.Visible = not collapsed end
	if ContentHolder then ContentHolder.Visible = not collapsed end
end)

TabHolder = Instance.new("Frame", Main)
TabHolder.Size = UDim2.new(0, 150, 1, -40)
TabHolder.Position = UDim2.new(0, 0, 0, 40)
TabHolder.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TabHolder.BackgroundTransparency = 1
Instance.new("UICorner", TabHolder).CornerRadius = UDim.new(0, 12)

ContentHolder = Instance.new("Frame", Main)
ContentHolder.Size = UDim2.new(1, -160, 1, -50)
ContentHolder.Position = UDim2.new(0, 160, 0, 50)
ContentHolder.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ContentHolder.BackgroundTransparency = 1
Instance.new("UICorner", ContentHolder).CornerRadius = UDim.new(0, 12)

end

function GUI.NewTab(tabName) local Tab = {} local y = 10

local button = Instance.new("TextButton", TabHolder)
button.Size = UDim2.new(1, -20, 0, 40)
button.Position = UDim2.new(0, 10, 0, 10 + #Tabs * 45)
button.Text = tabName
button.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
button.BackgroundTransparency = 1
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
	btn.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	btn.BackgroundTransparency = 1
	btn.TextColor3 = Color3.new(1, 1, 1)
	btn.Font = Enum.Font.Gotham
	btn.TextSize = 14
	Instance.new("UICorner", btn).CornerRadius = UDim.new(0, 8)
	btn.MouseButton1Click:Connect(function()
		pcall(info.Callback)
	end)
	y = y + 50
end

function Tab:AddSection(info)
	local title = Instance.new("TextLabel", frame)
	title.Size = UDim2.new(0, 400, 0, 20)
	title.Position = UDim2.new(0, 20, 0, y)
	title.Text = info.Name or "قسم"
	title.TextColor3 = Color3.new(1, 1, 1)
	title.BackgroundTransparency = 1
	title.Font = Enum.Font.GothamBold
	title.TextSize = 16
	y = y + 25
end

function Tab:AddSlider(info)
	local label = Instance.new("TextLabel", frame)
	label.Size = UDim2.new(0, 400, 0, 20)
	label.Position = UDim2.new(0, 20, 0, y)
	label.Text = info.Name .. ": " .. info.Default
	label.TextColor3 = Color3.new(1, 1, 1)
	label.BackgroundTransparency = 1
	label.Font = Enum.Font.Gotham
	label.TextSize = 14
	y = y + 25

	local slider = Instance.new("TextButton", frame)
	slider.Size = UDim2.new(0, 400, 0, 10)
	slider.Position = UDim2.new(0, 20, 0, y)
	slider.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	slider.BackgroundTransparency = 0.6
	Instance.new("UICorner", slider).CornerRadius = UDim.new(1, 0)

	local value = info.Default or info.Min
	local increment = info.Increase or 1
	local dragging = false

	local function update(inputX)
		local relX = math.clamp((inputX - slider.AbsolutePosition.X) / slider.AbsoluteSize.X, 0, 1)
		value = math.floor((info.Min + (info.Max - info.Min) * relX) / increment + 0.5) * increment
		label.Text = info.Name .. ": " .. tostring(value)
		if info.Callback then pcall(info.Callback, value) end
	end

	slider.InputBegan:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 then
			dragging = true
		end
	end)
	slider.InputEnded:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 then
			dragging = false
		end
	end)
	game:GetService("UserInputService").InputChanged:Connect(function(input)
		if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
			update(input.Position.X)
		end
	end)
	y = y + 30
end

function Tab:AddTextBox(info)
	local box = Instance.new("TextBox", frame)
	box.Size = UDim2.new(0, 400, 0, 40)
	box.Position = UDim2.new(0, 20, 0, y)
	box.PlaceholderText = info.PlaceholderText or "..."
	box.Text = info.Default or ""
	box.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	box.BackgroundTransparency = 1
	box.TextColor3 = Color3.new(1, 1, 1)
	box.Font = Enum.Font.Gotham
	box.TextSize = 14
	Instance.new("UICorner", box).CornerRadius = UDim.new(0, 8)

	box.FocusLost:Connect(function(enter)
		if enter and info.Callback then
			pcall(info.Callback, box.Text)
			if info.ClearText then
				box.Text = ""
			end
		end
	end)
	y = y + 50
end

function Tab:AddKeybind(info)
	local key = Enum.KeyCode[info.KeyCode or "E"]
	local btn = Instance.new("TextButton", frame)
	btn.Size = UDim2.new(0, 400, 0, 40)
	btn.Position = UDim2.new(0, 20, 0, y)
	btn.Text = "[ " .. key.Name .. " ] " .. info.Name
	btn.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	btn.BackgroundTransparency = 1
	btn.TextColor3 = Color3.new(1, 1, 1)
	btn.Font = Enum.Font.Gotham
	btn.TextSize = 14
	Instance.new("UICorner", btn).CornerRadius = UDim.new(0, 8)
	local toggled = info.Default or false
	game:GetService("UserInputService").InputBegan:Connect(function(input, gpe)
		if not gpe and input.KeyCode == key then
			toggled = not toggled
			if info.Callback then pcall(info.Callback, toggled) end
		end
	end)
	y = y + 50
end

function Tab:AddDropdown(info)
	local dropdown = Instance.new("TextButton", frame)
	dropdown.Size = UDim2.new(0, 400, 0, 40)
	dropdown.Position = UDim2.new(0, 20, 0, y)
	dropdown.Text = info.Name .. ": " .. (info.Default or "")
	dropdown.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	dropdown.BackgroundTransparency = 1
	dropdown.TextColor3 = Color3.new(1, 1, 1)
	dropdown.Font = Enum.Font.Gotham
	dropdown.TextSize = 14
	Instance.new("UICorner", dropdown).CornerRadius = UDim.new(0, 8)
	local open = false
	local optionsFrame = Instance.new("Frame", frame)
	options

