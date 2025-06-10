local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/VisualRoblox/Roblox/main/UI-Libraries/Visual%20Command%20UI%20Library/Source.lua', true))()

local Window = Library:CreateWindow({
    Name = 'تيك توك hasssssssss71',
    IntroText = 'سكربت روبيرتو | Script Roberto Hub',
    IntroIcon = 'rbxassetid://14001480246',
    IntroBlur = true,
    IntroBlurIntensity = 15,
    Theme = Library.Themes.dark,
    Position = 'bottom',
    Draggable = true,
    Prefix = ';'
})


Wait(0.5)
game.StarterGui:SetCore("SendNotification", {
    Title = "تـم تـفـعـيـل سـكـربـت روبيرتو★";
    Text = "انـتـظـر قـلـيـلاً"; -- ARAB TEAM
    Duration = 10;
})


game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName", "Script ROBERTO Hub | 0.1V")


local args = {
    [1] = "RolePlayBio",
    [2] = "استمتع"
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1RPNam1eTex1t"):FireServer(unpack(args))

local function sendChatMessage(message)
    if game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents") then
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")
    elseif game:GetService("TextChatService"):FindFirstChild("TextChannels") then
        local channel = game:GetService("TextChatService").TextChannels:FindFirstChild("RBXGeneral")
        if channel then
            channel:SendAsync(message)
        end
    else
        warn("Chat system not found!")
    end
end

local messagestart = ""
sendChatMessage(messagestart)

loadstring(game:HttpGet(("https://raw.githubusercontent.com/SYELE0/Color-White/main/And-Black")))()

MakeWindow({
  Hub = {
    Title = "roberto | SCRIPT Roberto 0.1V",
    Animation = "Roberto 0.1V"
  },
  Key = {
    KeySystem = false,
    Title = "Key System",
    Description = "",
    KeyLink = "",
    Keys = {"1234"},
    Notifi = {
      Notifications = true,
      CorrectKey = "Running the Script...",
      Incorrectkey = "The key is incorrect",
      CopyKeyLink = "Copied to Clipboard"
    }
  }
})
MinimizeButton({
  Image = "rbxassetid://14886426786",
  Size = {50, 50},
  Color = Color3.fromRGB(10, 10, 10),
  Corner = true,
  Stroke = false,
  StrokeColor = Color3.fromRGB(128, 0, 128)
})

local Main = MakeTab({Name = "مـعـلـومـات الـمـطـور"})
local Image = AddImageLabel(Main, {
  Name = "roberto HU",
  Image = "rbxassetid://14001480246"
})
AddButton(Main, {
  Name = "اضغط لنسخ حساب تيك توك المطور",
  Callback = function()
    setclipboard('saii_note0')
  end
})

AddButton(Main, {
  Name = "اضغط لنسخ حساب روب المطور",
  Callback = function()
    setclipboard('ROBLOX_ACO1')
       end
})

local Main = MakeTab({Name = "سـبـام شـات"})


AddSection(Main, {"انـتـبـه مـن خـطـر الـبـانـد  ! "})


AddSection(Main, {"سبام سرعة 0.2"})

local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration.TargetTextChannel
function sendchat(msg)
  if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
    game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg,"All")
  else
    chat:SendAsync(msg)
  end
end
AddTextBox(Main, {
  Name = "اكتب رسالتك",
  Description = "اكتب الرسالة",
  Flag = "هنا",
  Default = false,
  Callback = function(text)
    TextSave = text
  end
})



AddToggle(Main, {
  Name = "بدء السبام",
  Description = "سبام كتابتك",
  Flag = ".",
  Default = false,
  Callback = function(Value)
    getgenv().RaelHubSpawnText = Value
    while getgenv().RaelHubSpawnText do
      sendchat(TextSave)
      task.wait(0.2)
    end
  end
})

AddSection(Main, {"سبام سرعة 0.6"})
local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration.TargetTextChannel
function sendchat(msg)
  if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
    game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg,"All")
  else
    chat:SendAsync(msg)
  end
end
AddTextBox(Main, {
  Name = "اكتب رسالتك",
  Description = "اكتب الرسالة",
  Flag = "هنا",
  Default = false,
  Callback = function(text)
    TextSave = text
  end
})



AddToggle(Main, {
  Name = "بدء السبام",
  Description = "سبام كتابتك",
  Flag = ".",
  Default = false,
  Callback = function(Value)
    getgenv().RaelHubSpawnText = Value
    while getgenv().RaelHubSpawnText do
      sendchat(TextSave)
      task.wait(0.6)
    end
  end
})
AddSection(Main, {"سبام سرعة 0.8"})

local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration.TargetTextChannel
function sendchat(msg)
  if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
    game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg,"All")
  else
    chat:SendAsync(msg)
  end
end
AddTextBox(Main, {
  Name = "اكتب رسالتك",
  Description = "اكتب الرسالة",
  Flag = "هنا",
  Default = false,
  Callback = function(text)
    TextSave = text
  end
})



AddToggle(Main, {
  Name = "بدء السبام",
  Description = "سبام كتابتك",
  Flag = ".",
  Default = false,
  Callback = function(Value)
    getgenv().RaelHubSpawnText = Value
    while getgenv().RaelHubSpawnText do
      sendchat(TextSave)
      task.wait(0.8)
    end
  end
})
local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration.TargetTextChannel
function sendchat(msg)
  if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
    game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg,"All")
  else
    chat:SendAsync(msg)
  end
end

AddSection(Main, {"سبام سرعة 1.0"})

local TextSave
local tcs = game:GetService("TextChatService")
local chat = tcs.ChatInputBarConfiguration.TargetTextChannel
function sendchat(msg)
  if tcs.ChatVersion == Enum.ChatVersion.LegacyChatService then
    game:GetService("ReplicatedStorage"):FindFirstChild("DefaultChatSystemChatEvents").SayMessageRequest:FireServer(msg,"All")
  else
    chat:SendAsync(msg)
  end
end
AddTextBox(Main, {
  Name = "اكتب رسالتك",
  Description = "اكتب الرسالة",
  Flag = "هنا",
  Default = false,
  Callback = function(text)
    TextSave = text
  end
})
AddToggle(Main, {
  Name = "بدء السبام",
  Description = "سبام كتابتك",
  Flag = ".",
  Default = false,
  Callback = function(Value)
    getgenv().RaelHubSpawnText = Value
    while getgenv().RaelHubSpawnText do
      sendchat(TextSave)
      task.wait(1.0)
    end
  end
})

local Main = MakeTab({Name = "تخريب "})
 local section = AddSection(Main, {" قتل كنبه"})

local Players = game:GetService('Players')
local lplayer = Players.LocalPlayer

function GetPlayer(String)
    local Found = {}
    local strl = String:lower()
    if strl == "all" then
        for _, v in pairs(Players:GetPlayers()) do
            table.insert(Found, v)
        end
    elseif strl == "others" then
        for _, v in pairs(Players:GetPlayers()) do
            if v.Name ~= lplayer.Name then
                table.insert(Found, v)
            end
        end
    elseif strl == "me" then
        table.insert(Found, lplayer)
    else
        for _, v in pairs(Players:GetPlayers()) do
            if v.Name:lower():sub(1, #String) == String:lower() then
                table.insert(Found, v)
            end
        end
    end
    return Found
end

local function isItemInInventory(itemName)
    for _, item in pairs(lplayer.Backpack:GetChildren()) do
        if item.Name == itemName then
            return true
        end
    end
    return false
end

local function equipItem(itemName)
    local item = lplayer.Backpack:FindFirstChild(itemName)
    if item then
        lplayer.Character.Humanoid:EquipTool(item)
    end
end

local function unequipItem(itemName)
    local item = lplayer.Character:FindFirstChild(itemName)
    if item then
        item.Parent = lplayer.Backpack
    end
end

local function ActiveAutoFling(targetPlayer)
    if not isItemInInventory("Couch") then
        local args = { [1] = "PickingTools", [2] = "Couch" }
        game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
    end

    equipItem("Couch")
    getgenv().flingloop = true

    while getgenv().flingloop do
        local function flingloopfix()
            local Players = game:GetService("Players")
            local Player = Players.LocalPlayer
            local AllBool = false

            local SkidFling = function(TargetPlayer)
                local Character = Player.Character
                local Humanoid = Character and Character:FindFirstChildOfClass("Humanoid")
                local RootPart = Humanoid and Humanoid.RootPart
                local TCharacter = TargetPlayer.Character
                local THumanoid, TRootPart, THead, Accessory, Handle

                if TCharacter:FindFirstChildOfClass("Humanoid") then
                    THumanoid = TCharacter:FindFirstChildOfClass("Humanoid")
                end
                if THumanoid and THumanoid.RootPart then
                    TRootPart = THumanoid.RootPart
                end
                if TCharacter:FindFirstChild("Head") then
                    THead = TCharacter.Head
                end
                if TCharacter:FindFirstChildOfClass("Accessory") then
                    Accessory = TCharacter:FindFirstChildOfClass("Accessory")
                end
                if Accessory and Accessory:FindFirstChild("Handle") then
                    Handle = Accessory.Handle
                end

                if Character and Humanoid and RootPart then
                    if RootPart.Velocity.Magnitude < 50 then
                        getgenv().OldPos = RootPart.CFrame
                    end
                    if THumanoid and THumanoid.Sit and not AllBool then
                        unequipItem("Couch")
                        getgenv().flingloop = false
                        return
                    end
                    if THead then
                        workspace.CurrentCamera.CameraSubject = THead
                    elseif not THead and Handle then
                        workspace.CurrentCamera.CameraSubject = Handle
                    elseif THumanoid and TRootPart then
                        workspace.CurrentCamera.CameraSubject = THumanoid
                    end

                    if not TCharacter:FindFirstChildWhichIsA("BasePart") then
                        return
                    end

                    local FPos = function(BasePart, Pos, Ang)
                        RootPart.CFrame = CFrame.new(BasePart.Position) * Pos * Ang
                        Character:SetPrimaryPartCFrame(CFrame.new(BasePart.Position) * Pos * Ang)
                        RootPart.Velocity = Vector3.new(9e7, 9e7 * 10, 9e7)
                        RootPart.RotVelocity = Vector3.new(9e8, 9e8, 9e8)
                    end

                    local SFBasePart = function(BasePart)
                        local TimeToWait = 2
                        local Time = tick()
                        local Angle = 0
                        repeat
                            if RootPart and THumanoid then
                                if BasePart.Velocity.Magnitude < 50 then
                                    Angle = Angle + 100
                                    FPos(BasePart, CFrame.new(0, 1.5, 0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, 0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(2.25, 1.5, -2.25) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(-2.25, -1.5, 2.25) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, 1.5, 0) + THumanoid.MoveDirection, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, 0) + THumanoid.MoveDirection, CFrame.Angles(math.rad(Angle), 0, 0))
                                    task.wait()
                                else
                                    FPos(BasePart, CFrame.new(0, 1.5, THumanoid.WalkSpeed), CFrame.Angles(math.rad(90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, -THumanoid.WalkSpeed), CFrame.Angles(0, 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, 1.5, THumanoid.WalkSpeed), CFrame.Angles(math.rad(90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, 1.5, TRootPart.Velocity.Magnitude / 1.25), CFrame.Angles(math.rad(90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, -TRootPart.Velocity.Magnitude / 1.25), CFrame.Angles(0, 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, 1.5, TRootPart.Velocity.Magnitude / 1.25), CFrame.Angles(math.rad(90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, 0), CFrame.Angles(math.rad(90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, 0), CFrame.Angles(0, 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5 ,0), CFrame.Angles(math.rad(-90), 0, 0))
                                    task.wait()
                                    FPos(BasePart, CFrame.new(0, -1.5, 0), CFrame.Angles(0, 0, 0))
                                    task.wait()
                                end
                            else
                                break
                            end
                        until BasePart.Velocity.Magnitude > 500 or BasePart.Parent ~= TargetPlayer.Character or TargetPlayer.Parent ~= Players or not TargetPlayer.Character == TCharacter or THumanoid.Sit or Humanoid.Health <= 0 or tick() > Time + TimeToWait or getgenv().flingloop == false
                    end

                    workspace.FallenPartsDestroyHeight = 0/0
                    local BV = Instance.new("BodyVelocity")
                    BV.Name = "SpeedDoPai"
                    BV.Parent = RootPart
                    BV.Velocity = Vector3.new(9e8, 9e8, 9e8)
                    BV.MaxForce = Vector3.new(1/0, 1/0, 1/0)
                    Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)

                    if TRootPart and THead then
                        if (TRootPart.CFrame.p - THead.CFrame.p).Magnitude > 5 then
                            SFBasePart(THead)
                        else
                            SFBasePart(TRootPart)
                        end
                    elseif TRootPart and not THead then
                        SFBasePart(TRootPart)
                    elseif not TRootPart and THead then
                        SFBasePart(THead)
                    elseif not TRootPart and not THead and Accessory and Handle then
                        SFBasePart(Handle)
                    end
                    BV:Destroy()
                    Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
                    workspace.CurrentCamera.CameraSubject = Humanoid

                    repeat
                        RootPart.CFrame = getgenv().OldPos * CFrame.new(0, .5, 0)
                        Character:SetPrimaryPartCFrame(getgenv().OldPos * CFrame.new(0, .5, 0))
                        Humanoid:ChangeState("GettingUp")
                        table.foreach(Character:GetChildren(), function(_, x)
                            if x:IsA("BasePart") then
                                x.Velocity, x.RotVelocity = Vector3.new(), Vector3.new()
                            end
                        end)
                        task.wait()
                    until (RootPart.Position - getgenv().OldPos.p).Magnitude < 25

                    workspace.FallenPartsDestroyHeight = getgenv().FPDH
                end
            end

            if not Welcome then
                -- Mensagem de boas-vindas
            end
            getgenv().Welcome = true

            if AllBool then
                for _, x in next, Players:GetPlayers() do
                    SkidFling(x)
                end
            end

            if targetPlayer then
                SkidFling(targetPlayer)
            end

            task.wait()
        end

        wait()
        pcall(flingloopfix)
    end
end

local FlingAdvancedPlayerList = {}
local playerDropdown

local function UMupdatePlayerList()
    FlingAdvancedPlayerList = {}
    for _, player in ipairs(Players:GetPlayers()) do
        table.insert(FlingAdvancedPlayerList, player.Name)
    end
    if playerDropdown then
        playerDropdown:Refresh(FlingAdvancedPlayerList, true)
    end
end

local function teleportToPlayer(playerName)
    local player = Players:FindFirstChild(playerName)
    local localPlayer = Players.LocalPlayer

    if player and player.Character and localPlayer.Character and localPlayer.Character:FindFirstChild("HumanoidRootPart") then
        local targetPosition = player.Character.HumanoidRootPart.Position
        localPlayer.Character:MoveTo(targetPosition)
        print("Teletransportado para o jogador alvo.")
    else
        print("NÃ£o foi possÃ­vel encontrar o jogador alvo ou o HumanoidRootPart.")
    end
end

UMupdatePlayerList()

AddDropdown(Main, {
    Name = "اختار اسم الاعب",
    Default = "",
    Options = FlingAdvancedPlayerList,
    Callback = function(value)
        SelectedPlayer = value
    end    
})

AddButton(Main, {
    Name = "تحديث القائمة ",
    Callback = function()
        UMupdatePlayerList()
    end    
})

local flingToggle

AddToggle(Main, {
    Name = " تخريب كنبة",
    Default = false,
    Callback = function(state)
        if state then
            if SelectedPlayer then
                local targetPlayer = GetPlayer(SelectedPlayer)[1]
                if targetPlayer then
                    ActiveAutoFling(targetPlayer)
                end
            end
        else
            getgenv().flingloop = false
        end
    end    
})

game:GetService("Players").LocalPlayer.Character.Humanoid:GetPropertyChangedSignal("Sit"):Connect(function()
    if lplayer.Character.Humanoid.Sit then
        if flingToggle then
            flingToggle:Set(false)
        end
    end
end)
      
local section = AddSection(Main, {"قتل بالشاحنه السوداء"})

local function ShowPlayerList()
    local playerNames = {}
    for _, player in pairs(game.Players:GetPlayers()) do
        table.insert(playerNames, player.Name)
    end
    
    AddDropdown(Main, {
        Name = "اختار اسم المرحوم",
        Default = playerNames[1],
        Options = playerNames,
        Callback = function(Value)
            selectedPlayer = game.Players:FindFirstChild(Value)
            print("Jogador selecionado: " .. Value)
        end
    })
end

ShowPlayerList()

AddButton(Main, {
    Name = "تحديث القائمة",
    Callback = function()
        UMupdatePlayerList()
    end    
})

local flingToggle

AddButton(Main, {
    Name = "قتل بيت وسياره",
    Callback = function()
        local Player = game.Players.LocalPlayer
    local Backpack = Player.Backpack
    local Character = Player.Character
    local Humanoid = Character:FindFirstChildOfClass("Humanoid")
    local RootPart = Character:FindFirstChild("HumanoidRootPart")
    local Houses = game.Workspace:FindFirstChild("001_Lots")
    local OldPos = RootPart.CFrame
    local Angles = 0
    local Vehicles = Workspace.Vehicles
    local Pos

   
    function Check()
        if Player and Character and Humanoid and RootPart and Vehicles then
            return true
        else
            return false
        end
    end

  
    if selectedPlayer and selectedPlayer.Character then
        if Check() then
            local House = Houses:FindFirstChild(Player.Name.."House")
            if not House then
                local EHouse
                for _,Lot in pairs(Houses:GetChildren()) do
                    if Lot.Name == "For Sale" then
                        for _,num in pairs(Lot:GetDescendants()) do
                            if num:IsA("NumberValue") and num.Name == "Number" and num.Value < 25 and num.Value > 10 then
                                EHouse = Lot
                                break
                            end
                        end
                    end
                end

                local BuyDetector = EHouse:FindFirstChild("BuyHouse")
                Pos = BuyDetector.Position
                if BuyDetector and BuyDetector:IsA("BasePart") then
                    RootPart.CFrame = BuyDetector.CFrame + Vector3.new(0,-6,0)
                    task.wait(.5)
                    local ClickDetector = BuyDetector:FindFirstChild("ClickDetector")
                    if ClickDetector then
                        fireclickdetector(ClickDetector)
                    end
                end
            end

            task.wait(0.5)
            local PreHouse = Houses:FindFirstChild(Player.Name .. "House")
            if PreHouse then
                task.wait(0.5)
                local Number
                for i,x in pairs(PreHouse:GetDescendants()) do
                    if x.Name == "Number" and x:IsA("NumberValue") then
                        Number = x
                    end
                end
                task.wait(0.5)
                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Gettin1gHous1e"):FireServer("PickingCustomHouse","049_House", Number.Value)
            end

            task.wait(0.5)
            local PCar = Vehicles:FindFirstChild(Player.Name.."Car")
            if not PCar then
                if Check() then
                    RootPart.CFrame = CFrame.new(1118.81, 75.998, -1138.61)
                    task.wait(0.5)
                    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Ca1r"):FireServer("PickingCar","SchoolBus")
                    task.wait(0.5)
                    local PCar = Vehicles:FindFirstChild(Player.Name.."Car")
                    task.wait(0.5)
                    local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")
                    if Seat then
                        repeat task.wait()
                            RootPart.CFrame = Seat.CFrame * CFrame.new(0, math.random(-1, 1), 0)
                        until Humanoid.Sit
                    end
                end
            end

            task.wait(0.5)
            local PCar = Vehicles:FindFirstChild(Player.Name.."Car")
            if PCar then
                if not Humanoid.Sit then
                    local Seat = PCar:FindFirstChild("Body") and PCar.Body:FindFirstChild("VehicleSeat")
                    if Seat then
                        repeat task.wait()
                            RootPart.CFrame = Seat.CFrame * CFrame.new(0, math.random(-1, 1), 0)
                        until Humanoid.Sit
                    end
                end

                local Target = selectedPlayer
                local TargetC = Target.Character
                local TargetH = TargetC:FindFirstChildOfClass("Humanoid")
                local TargetRP = TargetC:FindFirstChild("HumanoidRootPart")
                if TargetC and TargetH and TargetRP then
                    if not TargetH.Sit then
                        while not TargetH.Sit do
                            task.wait()
                            local Fling = function(alvo,pos,angulo)
                                PCar:SetPrimaryPartCFrame(CFrame.new(alvo.Position) * pos * angulo)
                            end
                            Angles = Angles + 100
                            Fling(TargetRP,CFrame.new(0, 1.5, 0) + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                            Fling(TargetRP,CFrame.new(0, -1.5, 0) + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                            Fling(TargetRP,CFrame.new(2.25, 1.5, -2.25)  + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                            Fling(TargetRP,CFrame.new(-2.25, -1.5, 2.25) + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                            Fling(TargetRP,CFrame.new(0, 1.5, 0) + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                            Fling(TargetRP,CFrame.new(0, -1.5, 0) + TargetH.MoveDirection * TargetRP.Velocity.Magnitude / 1.10,CFrame.Angles(math.rad(Angles), 0, 0))
                        end

                        task.wait(0.2)
                        local House = Houses:FindFirstChild(Player.Name.."House")
                        PCar:SetPrimaryPartCFrame(CFrame.new(House.HouseSpawnPosition.Position))
                        task.wait(0.2)
                        local pedro = Region3.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(30,30,30),game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(30,30,30))

                        local a = workspace:FindPartsInRegion3(pedro,game.Players.LocalPlayer.Character.HumanoidRootPart,math.huge)

                        for i,v in pairs(a) do
                            if v.Name == "HumanoidRootPart" then
                                local b = game:GetService("Players"):FindFirstChild(v.Parent.Name)
                                local args = {
                                    [1] = "BanPlayerFromHouse",
                                    [2] = b,
                                    [3] = v.Parent
                                }

                                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Playe1rTrigge1rEven1t"):FireServer(unpack(args))

                               
                                local args = {
                                    [1] = "DeleteAllVehicles"
                                }
                                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Ca1r"):FireServer(unpack(args))
                            end
                        end
                    end
                end
            end
        end
    end
    end
})

local section = AddSection(Main, {"قتل باص"})
 local noclipEnabled = false
local runService = game:GetService("RunService")

-- Função para definir CanCollide para todas as partes do personagem
local function setCharacterCanCollide(character, canCollide)
    for _, part in ipairs(character:GetDescendants()) do
        if part:IsA("BasePart") then
            part.CanCollide = canCollide
        end
    end
end

-- Função de callback para o botão de alternância de Noclip
local function onNoclipToggle(value)
    noclipEnabled = value
    print("Noclip Enabled:", noclipEnabled)
    
    local player = game.Players.LocalPlayer
    local character = player.Character

    if noclipEnabled then
        -- Inicia um loop para continuamente definir CanCollide
        noclipLoop = runService.Stepped:Connect(function()
            if character then
                setCharacterCanCollide(character, false)
            end
        end)
    else
        -- Desativa o loop e restaura CanCollide
        if noclipLoop then
            noclipLoop:Disconnect()
        end
        if character then
            setCharacterCanCollide(character, true)
        end
    end
end

local Players = game:GetService("Players")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local selectedPlayerName = nil
local destination = Vector3.new(265.46, -450.83, -59.93)
local originalPosition = nil

local playerNames = {}
for _, player in pairs(Players:GetPlayers()) do
    table.insert(playerNames, player.Name)
end

local selectedPlayerName = nil

local Dropdown = AddDropdown(Main, {
Name = "اختار الاعب",
 Options = playerNames,
    Callback = function(selected)
        selectedPlayerName = selected
    end
})

AddButton(Main, {
    Name = "تحديث القائمة",
    Callback = function()
        UMupdatePlayerList()
    end    
})

local flingToggle

AddButton(Main, {
    Name = "قتل الاعب",
    Callback = function()
        if not selectedPlayerName then
            print("Nenhum jogador selecionado!")
            return
        end

        local player = Players.LocalPlayer
        local character = player.Character or player.CharacterAdded:Wait()
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
        originalPosition = humanoidRootPart.CFrame

        local function GetBus()
            local vehicles = Workspace:FindFirstChild("Vehicles")
            if vehicles then
                return vehicles:FindFirstChild(player.Name.."Car")
            end
            return nil
        end

        local bus = GetBus()

        -- Se o ônibus não existir, tenta spawnar um
        if not bus then
            humanoidRootPart.CFrame = CFrame.new(1118.81, 75.998, -1138.61)
            task.wait(0.5)
            local remoteEvent = ReplicatedStorage:FindFirstChild("RE")
            if remoteEvent and remoteEvent:FindFirstChild("1Ca1r") then
                remoteEvent["1Ca1r"]:FireServer("PickingCar", "SchoolBus")
            end
            task.wait(1)
            bus = GetBus()
        end

        -- Se conseguiu spawnar, tenta sentar no banco do motorista
        if bus then
            local seat = bus:FindFirstChild("Body") and bus.Body:FindFirstChild("VehicleSeat")
            if seat and character:FindFirstChildOfClass("Humanoid") and not character.Humanoid.Sit then
                repeat
                    humanoidRootPart.CFrame = seat.CFrame * CFrame.new(0, 2, 0)
                    task.wait()
                until character.Humanoid.Sit or not bus.Parent
            end

            local function TrackPlayer()
                while true do
                    if selectedPlayerName then
                        local targetPlayer = Players:FindFirstChild(selectedPlayerName)
                        if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
                            local targetHumanoid = targetPlayer.Character:FindFirstChildOfClass("Humanoid")
                            if targetHumanoid and targetHumanoid.Sit then
                                if character.Humanoid then
                                    bus:SetPrimaryPartCFrame(CFrame.new(destination))
                                    print("Jogador sentou, levando ônibus para o void!")

                                    task.wait(0.2)
                                    local function simulateJump()
                                        local humanoid = player.Character and player.Character:FindFirstChildWhichIsA("Humanoid")
                                        if humanoid then
                                            humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
                                        end
                                    end

                                    simulateJump()
                                    print("Simulando pulo!")
                                    task.wait(0.4)
                                    simulateJump()
                                    task.wait(0.5)
                                    humanoidRootPart.CFrame = originalPosition
                                    print("Player voltou para a posição inicial!")
                                end
                                break
                            else
                                local targetRoot = targetPlayer.Character.HumanoidRootPart
                                local time = tick() * 35 -- Aumenta a frequência
                                local lateralOffset = math.sin(time) * 4 -- Movimento lateral rápido
                                local frontBackOffset = math.cos(time) * 20 -- Movimento para frente/trás rápido
                                bus:SetPrimaryPartCFrame(targetRoot.CFrame * CFrame.new(lateralOffset, 0, frontBackOffset))
                            end
                        end
                    end
                    RunService.RenderStepped:Wait()
                end
            end

            spawn(TrackPlayer)
        end
    end
})

AddButton(Main, {
    Name = "سحب الاعب",
    Callback = function()
        if not selectedPlayerName then
            print("Nenhum jogador selecionado!")
            return
        end

        local player = Players.LocalPlayer
        local character = player.Character or player.CharacterAdded:Wait()
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
        originalPosition = humanoidRootPart.CFrame

        local function GetBus()
            local vehicles = Workspace:FindFirstChild("Vehicles")
            if vehicles then
                return vehicles:FindFirstChild(player.Name.."Car")
            end
            return nil
        end

        local bus = GetBus()

        -- Se o ônibus não existir, tenta spawnar um
        if not bus then
            humanoidRootPart.CFrame = CFrame.new(1118.81, 75.998, -1138.61)
            task.wait(0.5)
            local remoteEvent = ReplicatedStorage:FindFirstChild("RE")
            if remoteEvent and remoteEvent:FindFirstChild("1Ca1r") then
                remoteEvent["1Ca1r"]:FireServer("PickingCar", "SchoolBus")
            end
            task.wait(1)
            bus = GetBus()
        end

        -- Se conseguiu spawnar, tenta sentar no banco do motorista
        if bus then
            local seat = bus:FindFirstChild("Body") and bus.Body:FindFirstChild("VehicleSeat")
            if seat and character:FindFirstChildOfClass("Humanoid") and not character.Humanoid.Sit then
                repeat
                    humanoidRootPart.CFrame = seat.CFrame * CFrame.new(0, 2, 0)
                    task.wait()
                until character.Humanoid.Sit or not bus.Parent
            end

            local function TrackPlayerToOriginalPosition()
                while true do
                    if selectedPlayerName then
                        local targetPlayer = Players:FindFirstChild(selectedPlayerName)
                        if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
                            local targetHumanoid = targetPlayer.Character:FindFirstChildOfClass("Humanoid")
                            if targetHumanoid and targetHumanoid.Sit then
                                if character.Humanoid then
                                    bus:SetPrimaryPartCFrame(originalPosition)
                                    print("Jogador sentou, trazendo ônibus para a posição inicial!")

                                    task.wait(0.2)
                                    local function simulateJump()
                                        local humanoid = player.Character and player.Character:FindFirstChildWhichIsA("Humanoid")
                                        if humanoid then
                                            humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
                                        end
                                    end

                                    simulateJump()
                            
                                    task.wait(0.2)
                                    humanoidRootPart.CFrame = originalPosition
                                    print("Player voltou para a posição inicial!")

                                    -- Excluir o ônibus
                                    local args = {
                                        [1] = "DeleteAllVehicles"
                                    }
                                    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Ca1r"):FireServer(unpack(args))
                                end
                                break
                            else
                                local targetRoot = targetPlayer.Character.HumanoidRootPart
                                local time = tick() * 35 -- Aumenta a frequência
                                local lateralOffset = math.sin(time) * 4 -- Movimento lateral rápido
                                local frontBackOffset = math.cos(time) * 20 -- Movimento para frente/trás rápido
                                bus:SetPrimaryPartCFrame(targetRoot.CFrame * CFrame.new(lateralOffset, 0, frontBackOffset))
                            end
                        end
                    end
                    RunService.RenderStepped:Wait()
                end
            end

            spawn(TrackPlayerToOriginalPosition)
        end
    end
})

local section = AddSection(Main, {"اوامر تجسس وتحكم بالاعب"})

-- Function to get all player names
local function getPlayerNames()
    local playerNames = {}
    for _, player in ipairs(game.Players:GetPlayers()) do
        table.insert(playerNames, player.Name)
    end
    return playerNames
end

-- Store selected player for later use
local selectedPlayer = nil
local followHead = false
local connection = nil

-- Function to spectate the selected player
local function spectatePlayer(enable)
    local player = game.Players.LocalPlayer
    local camera = workspace.CurrentCamera

    if selectedPlayer then
        local targetPlayer = game.Players:FindFirstChild(selectedPlayer)
        if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
            if enable then
                -- Set camera to follow the selected player
                camera.CameraSubject = targetPlayer.Character.Humanoid
            else
                -- Reset camera to default (back to the local player)
                camera.CameraSubject = player.Character.Humanoid
            end
        else
            print("Selected player not available or out of game.")
        end
    else
        print("No player selected!")
    end
end

-- Function to float just above the selected player's head without falling
local function floatAbovePlayerHead()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()

    if character and character:FindFirstChild("HumanoidRootPart") then
        local humanoidRootPart = character.HumanoidRootPart

        if selectedPlayer then
            local targetPlayer = game.Players:FindFirstChild(selectedPlayer)

            if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("Head") then
                local targetHead = targetPlayer.Character.Head

                -- Position above the selected player's head
                humanoidRootPart.CFrame = targetHead.CFrame * CFrame.new(0, 3, 0)

                -- Keep updating the position every frame
                connection = game:GetService("RunService").Heartbeat:Connect(function()
                    if followHead and targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("Head") then
                        -- Update to stay above the player's head
                        humanoidRootPart.CFrame = targetPlayer.Character.Head.CFrame * CFrame.new(0, 3, 0)
                    else
                        connection:Disconnect() -- Disconnect if the toggle is off
                    end
                end)
            else
                print("Target player not found or not in the game.")
            end
        else
            print("No player selected!")
        end
    end
end

-- Function to trigger the secondary script
local function triggerCharacterSizeDown()
    local args = {
        [1] = "CharacterSizeDown",
        [2] = 2.4
    }
    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Clothe1s"):FireServer(unpack(args))
end

-- Function to teleport behind the selected player and return after 1.5 seconds
local function moveBehindAndReturn()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local humanoidRootPart = character:FindFirstChild("HumanoidRootPart")

    if humanoidRootPart and selectedPlayer then
        local targetPlayer = game.Players:FindFirstChild(selectedPlayer)
        if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
            local targetHumanoidRootPart = targetPlayer.Character.HumanoidRootPart

            -- Store the original position
            local originalPosition = humanoidRootPart.CFrame

            -- Move behind the selected player
            humanoidRootPart.CFrame = targetHumanoidRootPart.CFrame * CFrame.new(0, 0, 3)

            -- Wait for 1.5 seconds before returning
            wait(1.5)

            -- Return to original position
            humanoidRootPart.CFrame = originalPosition
        else
            print("Selected player not found or not in the game.")
        end
    else
        print("No player or HumanoidRootPart found!")
    end
end

-- Create the dropdown with player names
AddDropdown(Main, {
    Name = "اختار الاعب",
    Default = "",
    Options = getPlayerNames(),
    Callback = function(value)
        selectedPlayer = value
        print("Player selected: " .. value)
    end    
})

AddButton(Main, {
    Name = "تحديث القائمة",
    Callback = function()
        UMupdatePlayerList()
    end    
})

local flingToggle

-- Add a toggle that allows the player to spectate the selected player
AddToggle(Main, {
    Name = "شوف الاعب",
    Default = false,
    Callback = function(value)
        spectatePlayer(value)
    end    
})

-- Add a button to teleport to the selected player
AddButton(Main, {
    Name = "اذهب الى الاعب",
    Callback = function()
        floatAbovePlayerHead()
    end    
})
