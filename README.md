local OrionLib = ...
local Window = OrionLib:MakeWindow({Name = "اسم سكربتك", ...})

-- OrionLib مخصص ومحلي
local OrionLib = {}

    function OrionLib:MakeWindow(settings)
    local gui = Instance.new("ScreenGui", game.Players.LocalPlayer:WaitForChild("PlayerGui"))
    gui.Name = settings.Name or "OrionCustom"
    gui.ResetOnSpawn = false

    -- الإطار الرئيسي
    local mainFrame = Instance.new("Frame", gui)
    mainFrame.Size = UDim2.new(0, 500, 0, 350)
    mainFrame.Position = UDim2.new(0.3, 0, 0.3, 0)
    mainFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
    mainFrame.BorderSizePixel = 0
    Instance.new("UICorner", mainFrame).CornerRadius = UDim.new(0, 12)

    -- العنوان
    local titleBar = Instance.new("TextLabel", mainFrame)
    titleBar.Size = UDim2.new(1, 0, 0, 40)
    titleBar.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
    titleBar.Text = "🌟 " .. (settings.Name or "Window")
    titleBar.Font = Enum.Font.GothamBold
    titleBar.TextColor3 = Color3.fromRGB(0, 255, 127)
    titleBar.TextSize = 16
    titleBar.BorderSizePixel = 0
    titleBar.TextXAlignment = Enum.TextXAlignment.Center
    Instance.new("UICorner", titleBar).CornerRadius = UDim.new(0, 12)

    -- محتوى رئيسي
    local content = Instance.new("Frame", mainFrame)
    content.Position = UDim2.new(0, 0, 0, 40)
    content.Size = UDim2.new(1, 0, 1, -40)
    content.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
    content.BorderSizePixel = 0
    Instance.new("UICorner", content).CornerRadius = UDim.new(0, 12)

    local y = 10

    -- دالة لإضافة زر
    function OrionLib:AddButton(text, callback)
        local button = Instance.new("TextButton", content)
        button.Size = UDim2.new(0, 460, 0, 40)
        button.Position = UDim2.new(0, 20, 0, y)
        button.Text = text
        button.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
        button.TextColor3 = Color3.new(1, 1, 1)
        button.Font = Enum.Font.Gotham
        button.TextSize = 14
        Instance.new("UICorner", button).CornerRadius = UDim.new(0, 8)

        button.MouseButton1Click:Connect(function()
            pcall(callback)
        end)

        y = y + 50
    end

    return OrionLib
end

-- ✅ استخدام المكتبة:
local Window = OrionLib:MakeWindow({
    Name = "🔧 سكربت ألفا",
    SaveConfig = false
})

Window:AddButton("🧪 تجربة زر", function()
    print("تم الضغط على الزر!")
end)

Window:AddButton("🚀 تحميل سكربت", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/yourname/project/main/script.lua"))()
end)


---

📦 ماذا يقدم هذا السكربت:

الميزة	وصف

MakeWindow()	ينشئ واجهة تشبه Orion GUI
AddButton(text, callback)	تضيف زر مع حدث عند الضغط
تصميم احترافي	ألوان + حدود دائرية + تنظيم
