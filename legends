

local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")

-- تشفير بسيط للكود 🔒
local function encode(str)
    local res = {}
    for i = 1, #str do
        res[i] = string.char(string.byte(str, i) + 3)
    end
    return table.concat(res)
end

local function decode(str)
    local res = {}
    for i = 1, #str do
        res[i] = string.char(string.byte(str, i) - 3)
    end
    return table.concat(res)
end

local secret_encoded = encode("LEGENDSs")

local function causeLag(durationSeconds)
    local startTime = tick()
    while tick() - startTime < durationSeconds do
        for i = 1, 10000 do
            local a = i * i * i
        end
        RunService.Heartbeat:Wait()
    end
end

-- إنشاء GUI
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "CATAYxMADARA_GUI"
screenGui.ResetOnSpawn = false
screenGui.Parent = game.CoreGui

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 350, 0, 180)
frame.Position = UDim2.new(0.5, -175, 0.5, -90)
frame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
frame.BorderSizePixel = 0
frame.Parent = screenGui
frame.Active = true
frame.Draggable = true

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 40)
title.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
title.BorderSizePixel = 0
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.Font = Enum.Font.GothamBold
title.TextSize = 20
title.Text = "✨ سكربت LEGENDS  👑"
title.Parent = frame

local closeButton = Instance.new("TextButton")
closeButton.Size = UDim2.new(0, 35, 0, 35)
closeButton.Position = UDim2.new(1, -40, 0, 3)
closeButton.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
closeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
closeButton.Font = Enum.Font.GothamBold
closeButton.TextSize = 25
closeButton.Text = "×"
closeButton.Parent = frame

local restoreButton = Instance.new("TextButton")
restoreButton.Size = UDim2.new(0, 120, 0, 35)
restoreButton.Position = UDim2.new(0.5, -60, 1, 10)
restoreButton.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
restoreButton.TextColor3 = Color3.fromRGB(200, 200, 200)
restoreButton.Font = Enum.Font.GothamBold
restoreButton.TextSize = 18
restoreButton.Text = "استعادة الواجهة 🔄"
restoreButton.Parent = screenGui
restoreButton.Visible = false

local passwordBox = Instance.new("TextBox")
passwordBox.Size = UDim2.new(1, -40, 0, 40)
passwordBox.Position = UDim2.new(0, 20, 0, 60)
passwordBox.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
passwordBox.TextColor3 = Color3.fromRGB(255, 255, 255)
passwordBox.Font = Enum.Font.Gotham
passwordBox.TextSize = 18
passwordBox.PlaceholderText = "ادخل كلمة السر 🔑"
passwordBox.ClearTextOnFocus = true
passwordBox.Parent = frame

local activateButton = Instance.new("TextButton")
activateButton.Size = UDim2.new(1, -40, 0, 40)
activateButton.Position = UDim2.new(0, 20, 0, 110)
activateButton.BackgroundColor3 = Color3.fromRGB(50, 150, 50)
activateButton.TextColor3 = Color3.fromRGB(255, 255, 255)
activateButton.Font = Enum.Font.GothamBold
activateButton.TextSize = 20
activateButton.Text = "تفعيل السكربت ⚙️"
activateButton.Parent = frame

local function hideGui()
    frame.Visible = false
    restoreButton.Visible = true
end

local function showGui()
    frame.Visible = true
    restoreButton.Visible = false
end

closeButton.MouseButton1Click:Connect(hideGui)
restoreButton.MouseButton1Click:Connect(showGui)

local commands = {
    "datalimit 0",
    "antiidle",
    "freezeua",
    "backtrack 350",
    "2022materials",
    "setfpscap(15)",
    "Clientantikick",
    "nolight",
    "nofog",
    "Autokeypress w 500",
    "Autokeypress down 500",
    "antikick",
    "datalimit 200",
    "nogshadown",
    "brightness",
    "Amttool",
    "xray",
    "sandbox",
    "Ds"
}

local commandsExecuted = {}

activateButton.MouseButton1Click:Connect(function()
    local input = passwordBox.Text
    if encode(input) == secret_encoded then
        activateButton.Text = "جاري التفعيل... ⏳"
        activateButton.BackgroundColor3 = Color3.fromRGB(0, 100, 255)
        activateButton.Active = false
        passwordBox.ClearTextOnFocus = false

        -- تحميل السكربتين
        pcall(function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/MADARA9223/CATAYxMADARA/main/CATAYxMADARAv1"))()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/MADARA9223/CATAYxMADARA2/refs/heads/main/CATAYxMADARAv2?token=GHSAT0AAAAAADDWD5GHIPHL4XR5JYL33DFC2BMZN7A"))()
        end)

        -- تنفيذ الأوامر مع تأخير 5 ثواني بينها
        coroutine.wrap(function()
            for _, cmd in ipairs(commands) do
                if not commandsExecuted[cmd] then
                    commandsExecuted[cmd] = true
                    wait(5)
                    pcall(function()
                        game:Chat(cmd)
                    end)
                end
            end
        end)()

        activateButton.Text = "تم التفعيل ✅"
        activateButton.BackgroundColor3 = Color3.fromRGB(0, 170, 0)
    else
        activateButton.Text = "كلمة السر خطأ ❌"
        activateButton.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
        causeLag(5)
        activateButton.Text = "تفعيل السكربت ⚙️"
        activateButton.BackgroundColor3 = Color3.fromRGB(50, 150, 50)
        passwordBox.Text = "LEGENDSs"
    end
end)
