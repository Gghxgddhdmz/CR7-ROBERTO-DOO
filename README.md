-- GUI مخصص باسمك
local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
gui.Name = "HassanCustomGUI"
gui.ResetOnSpawn = false

-- إطار رئيسي
local Main = Instance.new("Frame", gui)
Main.Size = UDim2.new(0, 500, 0, 350)
Main.Position = UDim2.new(0.3, 0, 0.3, 0)
Main.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
Main.BorderSizePixel = 0
Main.Active = true
Main.Draggable = true
Instance.new("UICorner", Main).CornerRadius = UDim.new(0, 12)

-- عنوان علوي
local title = Instance.new("TextLabel", Main)
title.Size = UDim2.new(1, 0, 0, 40)
title.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
title.Text = "📘 قائمة سكربتات حسن"
title.Font = Enum.Font.GothamBold
title.TextSize = 18
title.TextColor3 = Color3.fromRGB(0, 255, 127)
title.BorderSizePixel = 0
Instance.new("UICorner", title).CornerRadius = UDim.new(0, 12)

-- إطار الأزرار
local content = Instance.new("Frame", Main)
content.Size = UDim2.new(1, -20, 1, -60)
content.Position = UDim2.new(0, 10, 0, 50)
content.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
content.BorderSizePixel = 0
Instance.new("UICorner", content).CornerRadius = UDim.new(0, 8)

-- 🧠 نظام AddButton مثل Orion
local yOffset = 10

function AddButton(parentFrame, info)
	local button = Instance.new("TextButton", content)
	button.Size = UDim2.new(0, 460, 0, 40)
	button.Position = UDim2.new(0, 10, 0, yOffset)
	button.Text = info.Name or "زر"
	button.Font = Enum.Font.Gotham
	button.TextSize = 14
	button.TextColor3 = Color3.new(1, 1, 1)
	button.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
	Instance.new("UICorner", button).CornerRadius = UDim.new(0, 8)

	button.MouseButton1Click:Connect(function()
		pcall(info.Callback)
	end)

	yOffset = yOffset + 50
end

-- ✅ استخدام AddButton بالطريقة المطلوبة
AddButton(Main, {
	Name = "🧪 زر تجريبي",
	Callback = function()
		print("✅ تم الضغط على الزر!")
	end
})

AddButton(Main, {
	Name = "🚀 تحميل سكربت",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/YourUser/YourRepo/main/script.lua"))()
	end
})

AddButton(Main, {
	Name = "❌ إغلاق الواجهة",
	Callback = function()
		gui:Destroy()
	end
})
