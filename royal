-- [[ ROYAL HUB V6.0 - DEVELOPER CUSTOM EDITION ]] --
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")
local TweenService = game:GetService("TweenService")
local Lighting = game:GetService("Lighting")

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "RoyalHub_DeveloperEdition"
ScreenGui.Parent = LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ResetOnSpawn = false

local CORRECT_KEY = "RoyalInTSB"

local BlurEffect = Instance.new("BlurEffect")
BlurEffect.Size = 24
BlurEffect.Parent = Lighting

local function setSmoothCorners(obj, amount)
    local corner = Instance.new("UICorner")
    corner.CornerRadius = UDim.new(0, amount)
    corner.Parent = obj
end

-- ==========================================
-- 🔑 واجهة المفتاح (PURE BLACK & WHITE KEY UI)
-- ==========================================
local KeyFrame = Instance.new("Frame")
KeyFrame.Size = UDim2.new(0, 380, 0, 220)
KeyFrame.Position = UDim2.new(0.5, -190, 0.5, -110)
KeyFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
KeyFrame.Parent = ScreenGui
setSmoothCorners(KeyFrame, 10)

local KeyStroke = Instance.new("UIStroke")
KeyStroke.Thickness = 2
KeyStroke.Color = Color3.fromRGB(255, 255, 255)
KeyStroke.Parent = KeyFrame

local KeyTitle = Instance.new("TextLabel")
KeyTitle.Size = UDim2.new(1, 0, 0, 50)
KeyTitle.Text = "ROYAL HUB • DEVELOPER VERIFICATION"
KeyTitle.Font = Enum.Font.GothamBold
KeyTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
KeyTitle.TextSize = 15
KeyTitle.BackgroundTransparency = 1
KeyTitle.Parent = KeyFrame

local KeyInput = Instance.new("TextBox")
KeyInput.Size = UDim2.new(0.8, 0, 0, 40)
KeyInput.Position = UDim2.new(0.1, 0, 0.35, 0)
KeyInput.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
KeyInput.Text = ""
KeyInput.PlaceholderText = "Paste developer key here..."
KeyInput.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
KeyInput.TextColor3 = Color3.fromRGB(255, 255, 255)
KeyInput.Font = Enum.Font.Code
KeyInput.TextSize = 14
KeyInput.Parent = KeyFrame
setSmoothCorners(KeyInput, 5)

local KeyBtn = Instance.new("TextButton")
KeyBtn.Size = UDim2.new(0.8, 0, 0, 40)
KeyBtn.Position = UDim2.new(0.1, 0, 0.65, 0)
KeyBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
KeyBtn.Text = "LAUNCH DEVELOPER SYSTEM"
KeyBtn.Font = Enum.Font.GothamBold
KeyBtn.TextColor3 = Color3.fromRGB(0, 0, 0)
KeyBtn.TextSize = 13
KeyBtn.Parent = KeyFrame
setSmoothCorners(KeyBtn, 5)

-- ==========================================
-- 🎨 الواجهة الرئيسية (PURE BLACK MAIN MENU)
-- ==========================================
local MainFrame = Instance.new("Frame")
MainFrame.Size = UDim2.new(0, 720, 0, 460)
MainFrame.Position = UDim2.new(0.5, -360, 0.5, -230)
MainFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
MainFrame.Visible = false
MainFrame.Parent = ScreenGui
setSmoothCorners(MainFrame, 12)

local RGBStroke = Instance.new("UIStroke")
RGBStroke.Thickness = 2.5
RGBStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
RGBStroke.Parent = MainFrame

coroutine.wrap(function()
    while true do
        for i = 0, 1, 0.002 do
            RGBStroke.Color = Color3.fromHSV(i, 0.9, 0.9)
            task.wait(0.01)
        end
    end
end)()

local MinimizeBtn = Instance.new("TextButton")
MinimizeBtn.Size = UDim2.new(0, 30, 0, 30)
MinimizeBtn.Position = UDim2.new(1, -35, 0, 10)
MinimizeBtn.BackgroundTransparency = 1
MinimizeBtn.Text = "—"
MinimizeBtn.Font = Enum.Font.GothamBold
MinimizeBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
MinimizeBtn.TextSize = 18
MinimizeBtn.Parent = MainFrame

local MiniFrame = Instance.new("TextButton")
MiniFrame.Size = UDim2.new(0, 55, 0, 55)
MiniFrame.Position = UDim2.new(0.05, 0, 0.05, 0)
MiniFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
MiniFrame.Text = "ROYAL"
MiniFrame.Font = Enum.Font.GothamBold
MiniFrame.TextSize = 10
MiniFrame.TextColor3 = Color3.fromRGB(255, 255, 255)
MiniFrame.Visible = false
MiniFrame.Parent = ScreenGui
setSmoothCorners(MiniFrame, 27.5)

local MiniStroke = Instance.new("UIStroke")
MiniStroke.Thickness = 2
MiniStroke.Color = Color3.fromRGB(255, 255, 255)
MiniStroke.Parent = MiniFrame

local TopBar = Instance.new("Frame")
TopBar.Size = UDim2.new(1, 0, 0, 70)
TopBar.BackgroundTransparency = 1
TopBar.Parent = MainFrame

local AvatarImg = Instance.new("ImageLabel")
AvatarImg.Size = UDim2.new(0, 48, 0, 48)
AvatarImg.Position = UDim2.new(0, 20, 0, 11)
AvatarImg.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
AvatarImg.Image = "rbxthumb://type=AvatarHeadShot&id=" .. LocalPlayer.UserId .. "&x=150&y=150"
AvatarImg.Parent = TopBar
setSmoothCorners(AvatarImg, 24)

local NameLabel = Instance.new("TextLabel")
NameLabel.Size = UDim2.new(0, 200, 0, 30)
NameLabel.Position = UDim2.new(0, 80, 0, 20)
NameLabel.BackgroundTransparency = 1
NameLabel.Text = LocalPlayer.DisplayName
NameLabel.Font = Enum.Font.GothamBold
NameLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
NameLabel.TextSize = 15
NameLabel.TextXAlignment = Enum.TextXAlignment.Left
NameLabel.Parent = TopBar

local WelcomeLabel = Instance.new("TextLabel")
WelcomeLabel.Size = UDim2.new(0, 200, 0, 30)
WelcomeLabel.Position = UDim2.new(1, -240, 0, 20)
WelcomeLabel.BackgroundTransparency = 1
WelcomeLabel.Text = "Welcome To Royal Hub"
WelcomeLabel.Font = Enum.Font.GothamBold
WelcomeLabel.TextColor3 = Color3.fromRGB(200, 200, 200)
WelcomeLabel.TextSize = 14
WelcomeLabel.TextXAlignment = Enum.TextXAlignment.Right
WelcomeLabel.Parent = TopBar

local SepLineTop = Instance.new("Frame")
SepLineTop.Size = UDim2.new(1, 0, 0, 1)
SepLineTop.Position = UDim2.new(0, 0, 0, 70)
SepLineTop.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
SepLineTop.BorderSizePixel = 0
SepLineTop.Parent = MainFrame

local Sidebar = Instance.new("Frame")
Sidebar.Size = UDim2.new(0, 190, 1, -71)
Sidebar.Position = UDim2.new(0, 0, 0, 71)
Sidebar.BackgroundColor3 = Color3.fromRGB(5, 5, 5)
Sidebar.BorderSizePixel = 0
Sidebar.Parent = MainFrame

local SearchInput = Instance.new("TextBox")
SearchInput.Size = UDim2.new(0.85, 0, 0, 32)
SearchInput.Position = UDim2.new(0.075, 0, 0, 15)
SearchInput.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
SearchInput.Text = ""
SearchInput.PlaceholderText = "🔍 Search here..."
SearchInput.PlaceholderColor3 = Color3.fromRGB(120, 120, 120)
SearchInput.TextColor3 = Color3.fromRGB(255, 255, 255)
SearchInput.TextSize = 13
SearchInput.Font = Enum.Font.Gotham
SearchInput.Parent = Sidebar
setSmoothCorners(SearchInput, 6)

local TabContainer = Instance.new("Frame")
TabContainer.Size = UDim2.new(1, 0, 1, -60)
TabContainer.Position = UDim2.new(0, 0, 0, 60)
TabContainer.BackgroundTransparency = 1
TabContainer.Parent = Sidebar

local CombatTabBtn = Instance.new("TextButton")
CombatTabBtn.Size = UDim2.new(0.85, 0, 0, 38)
CombatTabBtn.Position = UDim2.new(0.075, 0, 0, 5)
CombatTabBtn.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
CombatTabBtn.Text = "⚔️  Combat"
CombatTabBtn.Font = Enum.Font.GothamBold
CombatTabBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
CombatTabBtn.TextSize = 13
CombatTabBtn.Parent = TabContainer
setSmoothCorners(CombatTabBtn, 6)

local MovementTabBtn = CombatTabBtn:Clone()
MovementTabBtn.Position = UDim2.new(0.075, 0, 0, 50)
MovementTabBtn.Text = "⚡  Movement"
MovementTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
MovementTabBtn.Parent = TabContainer

local ConfigTabBtn = CombatTabBtn:Clone()
ConfigTabBtn.Position = UDim2.new(0.075, 0, 0, 95)
ConfigTabBtn.Text = "⚙️  Config"
ConfigTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
ConfigTabBtn.Parent = TabContainer

local SepLineVertical = Instance.new("Frame")
SepLineVertical.Size = UDim2.new(0, 1, 1, -71)
SepLineVertical.Position = UDim2.new(0, 190, 0, 71)
SepLineVertical.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
SepLineVertical.BorderSizePixel = 0
SepLineVertical.Parent = MainFrame

local ContentFrame = Instance.new("Frame")
ContentFrame.Size = UDim2.new(1, -191, 1, -71)
ContentFrame.Position = UDim2.new(0, 191, 0, 71)
ContentFrame.BackgroundTransparency = 1
ContentFrame.Parent = MainFrame

local CombatPage = Instance.new("ScrollingFrame")
CombatPage.Size = UDim2.new(1, 0, 1, 0)
CombatPage.BackgroundTransparency = 1
CombatPage.CanvasSize = UDim2.new(0, 0, 3.0, 0) -- كبرنا المساحة عشان تشيل كل الأزرار الجديدة مرتاحة
CombatPage.ScrollBarThickness = 3
CombatPage.ScrollBarImageColor3 = Color3.fromRGB(80, 80, 80)
CombatPage.Visible = true
CombatPage.Parent = ContentFrame

local MovementPage = CombatPage:Clone()
MovementPage.Visible = false
MovementPage.Parent = ContentFrame

local ConfigPage = CombatPage:Clone()
ConfigPage.Visible = false
ConfigPage.Parent = ContentFrame

local allTogglesForConfig = {}

-- دالة التوجيل المحدثة: تنور أخضر فاقع عند التشغيل، وأبيض عند الإيقاف
local function createToggle(parent, name, text, callback)
    local frame = Instance.new("Frame")
    frame.Name = name
    frame.Size = UDim2.new(0.94, 0, 0, 50)
    frame.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
    frame.Parent = parent
    setSmoothCorners(frame, 6)
    
    local label = Instance.new("TextLabel")
    label.Size = UDim2.new(0.7, 0, 1, 0)
    label.Position = UDim2.new(0, 15, 0, 0)
    label.BackgroundTransparency = 1
    label.Text = text
    label.TextColor3 = Color3.fromRGB(255, 255, 255)
    label.Font = Enum.Font.GothamBold
    label.TextSize = 13
    label.TextXAlignment = Enum.TextXAlignment.Left
    label.Parent = frame
    
    local toggleBtn = Instance.new("TextButton")
    toggleBtn.Size = UDim2.new(0, 42, 0, 20)
    toggleBtn.Position = UDim2.new(1, -55, 0.5, -10)
    toggleBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255) -- الباكجراوند الأساسي أبيض عالي
    toggleBtn.Text = ""
    toggleBtn.Parent = frame
    setSmoothCorners(toggleBtn, 10)
    
    local circle = Instance.new("Frame")
    circle.Size = UDim2.new(0, 14, 0, 14)
    circle.Position = UDim2.new(0, 3, 0.5, -7)
    circle.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    circle.Parent = toggleBtn
    setSmoothCorners(circle, 7)
    
    local active = false
    local keybind = "None"
    
    local function updateVisuals()
        if active then
            -- تنور أخضر فاقع عند التفعيل
            TweenService:Create(circle, TweenInfo.new(0.15), {Position = UDim2.new(1, -17, 0.5, -7), BackgroundColor3 = Color3.fromRGB(255, 255, 255)}):Play()
            TweenService:Create(toggleBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.fromRGB(0, 200, 0)}):Play()
        else
            -- ترجع أبيض عادي عند الإيقاف
            TweenService:Create(circle, TweenInfo.new(0, 3, 0.5, -7), {Position = UDim2.new(0, 3, 0.5, -7), BackgroundColor3 = Color3.fromRGB(0, 0, 0)}):Play()
            TweenService:Create(toggleBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.fromRGB(255, 255, 255)}):Play()
        end
    end
    
    local function fire()
        active = not active
        updateVisuals()
        callback(active)
    end
    
    toggleBtn.MouseButton1Click:Connect(fire)
    table.insert(allTogglesForConfig, {name = name, text = text, parentName = parent.Name, trigger = fire, setKey = function(k) keybind = k end, getKey = function() return keybind end})
    return frame, fire
end

local function applyListLayout(page)
    local layout = Instance.new("UIListLayout")
    layout.Padding = UDim.new(0, 8)
    layout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    layout.SortOrder = Enum.SortOrder.LayoutOrder
    layout.Parent = page
    
    local padding = Instance.new("UIPadding")
    padding.PaddingTop = UDim.new(0, 12)
    padding.Parent = page
end
applyListLayout(CombatPage)
applyListLayout(MovementPage)
applyListLayout(ConfigPage)

CombatTabBtn.MouseButton1Click:Connect(function()
    CombatPage.Visible = true; MovementPage.Visible = false; ConfigPage.Visible = false
    CombatTabBtn.BackgroundColor3 = Color3.fromRGB(25, 25, 25); MovementTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10); ConfigTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
end)
MovementTabBtn.MouseButton1Click:Connect(function()
    CombatPage.Visible = false; MovementPage.Visible = true; ConfigPage.Visible = false
    CombatTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10); MovementTabBtn.BackgroundColor3 = Color3.fromRGB(25, 25, 25); ConfigTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
end)
ConfigTabBtn.MouseButton1Click:Connect(function()
    CombatPage.Visible = false; MovementPage.Visible = false; ConfigPage.Visible = true
    CombatTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10); MovementTabBtn.BackgroundColor3 = Color3.fromRGB(10, 10, 10); ConfigTabBtn.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
end)

local function makeDraggable(frame)
    local dragging, dragInput, dragStart, startPos
    frame.InputBegan:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
            dragging = true; dragStart = input.Position; startPos = frame.Position
            input.Changed:Connect(function() if input.UserInputState == Enum.UserInputState.End then dragging = false end end)
        end
    end)
    frame.InputChanged:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then dragInput = input end
    end)
    RunService.RenderStepped:Connect(function()
        if dragging and dragInput then
            local delta = dragInput.Position - dragStart
            frame.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
        end
    end)
end
makeDraggable(MainFrame)
makeDraggable(MiniFrame)

MinimizeBtn.MouseButton1Click:Connect(function() MainFrame.Visible = false; MiniFrame.Visible = true; MiniFrame.Position = MainFrame.Position end)
MiniFrame.MouseButton1Click:Connect(function() MiniFrame.Visible = false; MainFrame.Visible = true; MainFrame.Position = MiniFrame.Position end)

-- ==========================================
-- 🛠️ نظام تشغيل الميزات المتكامل والمعدل
-- ==========================================
local Flags = { 
    AimBot = false, BlockV1 = false, BlockV2 = false, AntiRagdoll = false, 
    SideDashCounter = false, FrontDashCounter = false, KillAura = false, VisualUlt = false,
    SpeedHack = false, InfJump = false, Fly = false, WalkCharacter = false, Underground = false
}
local ConfigValues = { Speed = 16, FlySpeed = 50, TargetPlayer = "" }

-- ⚔️ صفحة الـ COMBAT كاملة (بأنوار الإضاءة الخضراء والأبيض المحدثة)
createToggle(CombatPage, "AimBot", "🎯 Aim Bot Lock-On (Auto Camera Track)", function(val) Flags.AimBot = val end)
createToggle(CombatPage, "BlockV1", "Shield Auto Block V1 (Reactive)", function(val) Flags.BlockV1 = val end)
createToggle(CombatPage, "BlockV2", "Shield Auto Block V2 (Perfect Simulation)", function(val) Flags.BlockV2 = val end)
createToggle(CombatPage, "SideDashCounter", "⚡ Auto Side-Dash Counter (Behind Enemy)", function(val) Flags.SideDashCounter = val end)
createToggle(CombatPage, "FrontDashCounter", "💥 Auto Front-Dash Counter (Push Attack)", function(val) Flags.FrontDashCounter = val end)
createToggle(CombatPage, "KillAura", "😈 Kill Aura (Close Range Auto M1)", function(val) Flags.KillAura = val end)
createToggle(CombatPage, "AntiRagdoll", "Anti Ragdoll (Instant Recovery)", function(val) Flags.AntiRagdoll = val end)
createToggle(CombatPage, "VisualUlt", "👑 Infinite Visual Ultimate (Flex Clip)", function(val) Flags.VisualUlt = val end)

local function getClosestPlayer()
    local closest, maxDist = nil, math.huge
    if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
        for _, enemy in pairs(Players:GetPlayers()) do
            if enemy ~= LocalPlayer and enemy.Character and enemy.Character:FindFirstChild("HumanoidRootPart") and enemy.Character:FindFirstChildOfClass("Humanoid") and enemy.Character:FindFirstChildOfClass("Humanoid").Health > 0 then
                local dist = (enemy.Character.HumanoidRootPart.Position - LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                if dist < maxDist then closest = enemy; maxDist = dist end
            end
        end
    end
    return closest, maxDist
end

-- [تثبيت الـ Aim Bot]
RunService.RenderStepped:Connect(function()
    if Flags.AimBot then
        local target, dist = getClosestPlayer()
        if target and dist < 50 then
            local cam = workspace.CurrentCamera
            local targetHrp = target.Character:FindFirstChild("HumanoidRootPart")
            if targetHrp then
                cam.CFrame = CFrame.lookAt(cam.CFrame.Position, targetHrp.Position + Vector3.new(0, 1.5, 0))
            end
        end
    end
end)

-- [نظام التفادي والعدادات الذكية]
local lastCounterTime = 0
RunService.RenderStepped:Connect(function()
    if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
        local myHrp = LocalPlayer.Character.HumanoidRootPart
        local target, dist = getClosestPlayer()
        if target and dist < 20 and (tick() - lastCounterTime > 0.5) then
            local enemyHrp = target.Character.HumanoidRootPart
            local enemyHum = target.Character:FindFirstChildOfClass("Humanoid")
            local isEnemyAttacking = false
            if enemyHum then
                for _, anim in pairs(enemyHum:GetPlayingAnimationTracks()) do
                    local name = anim.Name:lower()
                    if name:find("attack") or name:find("punch") or name:find("swing") or name:find("strike") or name:find("hit") then
                        isEnemyAttacking = true
                        break
                    end
                end
            end
            if isEnemyAttacking then
                if Flags.SideDashCounter then
                    lastCounterTime = tick()
                    local sideKey = math.random(1,2) == 1 and Enum.KeyCode.A or Enum.KeyCode.D
                    game:GetService("VirtualInputManager"):SendKeyEvent(true, sideKey, false, game)
                    game:GetService("VirtualInputManager"):SendKeyEvent(true, Enum.KeyCode.Q, false, game)
                    task.wait(0.01)
                    game:GetService("VirtualInputManager"):SendKeyEvent(false, sideKey, false, game)
                    game:GetService("VirtualInputManager"):SendKeyEvent(false, Enum.KeyCode.Q, false, game)
                    local behindPosition = enemyHrp.CFrame * CFrame.new(0, 0, 3.8)
                    myHrp.CFrame = CFrame.lookAt(behindPosition.Position, enemyHrp.Position)
                elseif Flags.FrontDashCounter then
                    lastCounterTime = tick()
                    game:GetService("VirtualInputManager"):SendKeyEvent(true, Enum.KeyCode.W, false, game)
                    game:GetService("VirtualInputManager"):SendKeyEvent(true, Enum.KeyCode.Q, false, game)
                    task.wait(0.01)
                    game:GetService("VirtualInputManager"):SendKeyEvent(false, Enum.KeyCode.W, false, game)
                    game:GetService("VirtualInputManager"):SendKeyEvent(false, Enum.KeyCode.Q, false, game)
                    task.wait(0.03)
                    myHrp.CFrame = CFrame.lookAt(myHrp.Position, enemyHrp.Position)
                    game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 0)
                    task.wait(0.01)
                    game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 0)
                    if enemyHrp:IsA("Part") then
                        enemyHrp.AssemblyLinearVelocity = (enemyHrp.Position - myHrp.Position).Unit * 85 + Vector3.new(0, 25, 0)
                    end
                end
            end
        end
    end
end)

-- [باقي أنظمة الصد والـ Aura والـ Ragdoll]
RunService.RenderStepped:Connect(function()
    if (Flags.BlockV1 or Flags.BlockV2) and not (Flags.SideDashCounter or Flags.FrontDashCounter) then
        local target, dist = getClosestPlayer()
        if target and dist < 16 and LocalPlayer.Character then
            local isAttacking = false
            local enemyHum = target.Character:FindFirstChildOfClass("Humanoid")
            if enemyHum then
                for _, anim in pairs(enemyHum:GetPlayingAnimationTracks()) do
                    local animName = anim.Name:lower()
                    if animName:find("punch") or animName:find("attack") or animName:find("strike") or animName:find("swing") then isAttacking = true break end
                end
            end
            if isAttacking then game:GetService("VirtualInputManager"):SendKeyEvent(true, Enum.KeyCode.F, false, game) else game:GetService("VirtualInputManager"):SendKeyEvent(false, Enum.KeyCode.F, false, game) end
        end
    end
end)

task.spawn(function()
    while task.wait(0.1) do
        if Flags.KillAura then
            local target, dist = getClosestPlayer()
            if target and dist < 10 then
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 0)
                task.wait(0.04)
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 0)
            end
        end
    end
end)

RunService.RenderStepped:Connect(function()
    if Flags.AntiRagdoll and LocalPlayer.Character then
        local hum = LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
        local hrp = LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
        if hum and hrp then
            if hum:GetState() == Enum.HumanoidStateType.Ragdoll or hum.PlatformStand then
                hum:ChangeState(Enum.HumanoidStateType.GettingUp)
                hum.PlatformStand = false
            end
        end
    end
    if Flags.VisualUlt then
        local screenGui = LocalPlayer:FindFirstChild("PlayerGui")
        if screenGui then
            local hotbar = screenGui:FindFirstChild("Hotbar") or screenGui:FindFirstChild("MainGui")
            local ultBar = hotbar and (hotbar:FindFirstChild("Ultimate", true) or hotbar:FindFirstChild("Gage", true))
            if ultBar and ultBar:IsA("Frame") then ultBar.Size = UDim2.new(1, 0, 1, 0) end
        end
    end
end)

-- ==========================================
-- ⚡ صفحة الـ MOVEMENT الشاملة للميزات الجديدة
-- ==========================================
local SpeedToggleFrame = createToggle(MovementPage, "SpeedHack", "Speed Hack Bypass", function(val) Flags.SpeedHack = val end)
local SpeedBox = Instance.new("TextBox")
SpeedBox.Size = UDim2.new(0, 60, 0, 25)
SpeedBox.Position = UDim2.new(0, 170, 0.5, -12)
SpeedBox.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
SpeedBox.Text = "16"
SpeedBox.TextColor3 = Color3.fromRGB(255, 255, 255)
SpeedBox.Font = Enum.Font.Code
SpeedBox.Parent = SpeedToggleFrame
SpeedBox.FocusLost:Connect(function()
    local num = tonumber(SpeedBox.Text)
    if num then ConfigValues.Speed = math.clamp(num, 0, 450) else SpeedBox.Text = tostring(ConfigValues.Speed) end
end)

RunService.RenderStepped:Connect(function()
    if Flags.SpeedHack and LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Humanoid") then
        LocalPlayer.Character:FindFirstChildOfClass("Humanoid").WalkSpeed = ConfigValues.Speed
    end
end)

createToggle(MovementPage, "InfJump", "Infinite Jump Engine", function(val) Flags.InfJump = val end)
UserInputService.JumpRequest:Connect(function()
    if Flags.InfJump and LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Humanoid") then
        LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState(Enum.HumanoidStateType.Jumping)
    end
end)

local FlyToggleFrame = createToggle(MovementPage, "Fly", "Premium Flight Controller", function(val) Flags.Fly = val end)
local FlyBox = Instance.new("TextBox")
FlyBox.Size = UDim2.new(0, 60, 0, 25)
FlyBox.Position = UDim2.new(0, 170, 0.5, -12)
FlyBox.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
FlyBox.Text = "50"
FlyBox.TextColor3 = Color3.fromRGB(255, 255, 255)
FlyBox.Font = Enum.Font.Code
FlyBox.Parent = FlyToggleFrame
FlyBox.FocusLost:Connect(function()
    local num = tonumber(FlyBox.Text)
    if num then ConfigValues.FlySpeed = math.clamp(num, 0, 200) else FlyBox.Text = tostring(ConfigValues.FlySpeed) end
end)

local flyAttachment, flyLV, flyAO
RunService.RenderStepped:Connect(function()
    if Flags.Fly and LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
        local hrp = LocalPlayer.Character.HumanoidRootPart
        local cam = workspace.CurrentCamera
        if not flyAttachment then
            flyAttachment = Instance.new("Attachment")
            flyAttachment.Parent = hrp
            flyLV = Instance.new("LinearVelocity")
            flyLV.MaxForce = math.huge
            flyLV.Attachment0 = flyAttachment
            flyLV.Parent = hrp
            flyAO = Instance.new("AlignOrientation")
            flyAO.MaxTorque = math.huge
            flyAO.Attachment0 = flyAttachment
            flyAO.Parent = hrp
        end
        local moveDir = Vector3.new(0,0,0)
        if UserInputService:IsKeyDown(Enum.KeyCode.W) then moveDir = moveDir + cam.CFrame.LookVector end
        if UserInputService:IsKeyDown(Enum.KeyCode.S) then moveDir = moveDir - cam.CFrame.LookVector end
        if UserInputService:IsKeyDown(Enum.KeyCode.A) then moveDir = moveDir - cam.CFrame.RightVector end
        if UserInputService:IsKeyDown(Enum.KeyCode.D) then moveDir = moveDir + cam.CFrame.RightVector end
        if moveDir.Magnitude > 0 then flyLV.VectorVelocity = moveDir.Unit * ConfigValues.FlySpeed else flyLV.VectorVelocity = Vector3.new(0,0,0) end
        flyAO.CFrame = cam.CFrame
    else
        if flyLV then flyLV:Destroy() flyLV = nil end
        if flyAO then flyAO:Destroy() flyAO = nil end
        if flyAttachment then flyAttachment:Destroy() flyAttachment = nil end
    end
end)

-- 🆕 [قالب الميزات الجديدة للاعبين والماتش المخصص]
local CustomMoveFrame = Instance.new("Frame")
CustomMoveFrame.Size = UDim2.new(0.94, 0, 0, 110) -- مساحة تناسب الاختيارات
CustomMoveFrame.BackgroundColor3 = Color3.fromRGB(12, 12, 12)
CustomMoveFrame.Parent = MovementPage
setSmoothCorners(CustomMoveFrame, 6)

local PlayerLabel = Instance.new("TextLabel")
PlayerLabel.Size = UDim2.new(0.4, 0, 0, 35)
PlayerLabel.Position = UDim2.new(0, 15, 0, 10)
PlayerLabel.BackgroundTransparency = 1
PlayerLabel.Text = "👤 Select Target Player:"
PlayerLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
PlayerLabel.Font = Enum.Font.GothamBold
PlayerLabel.TextSize = 12
PlayerLabel.TextXAlignment = Enum.TextXAlignment.Left
PlayerLabel.Parent = CustomMoveFrame

local PlayerInputBox = Instance.new("TextBox")
PlayerInputBox.Size = UDim2.new(0.5, 0, 0, 28)
PlayerInputBox.Position = UDim2.new(0.45, 0, 0, 12)
PlayerInputBox.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
PlayerInputBox.Text = ""
PlayerInputBox.PlaceholderText = "Type part of name..."
PlayerInputBox.TextColor3 = Color3.fromRGB(255, 255, 255)
PlayerInputBox.Font = Enum.Font.Gotham
PlayerInputBox.TextSize = 12
PlayerInputBox.Parent = CustomMoveFrame
setSmoothCorners(PlayerInputBox, 4)

PlayerInputBox.FocusLost:Connect(function()
    local text = PlayerInputBox.Text:lower()
    for _, p in pairs(Players:GetPlayers()) do
        if p ~= LocalPlayer and (p.Name:lower():find(text) or p.DisplayName:lower():find(text)) then
            ConfigValues.TargetPlayer = p.Name
            PlayerInputBox.Text = p.DisplayName
            break
        end
    end
end)

-- زر الالتصاق العادي بظهر اللاعب WALKCHARACTER
local WalkToggleFrame = Instance.new("Frame")
WalkToggleFrame.Size = UDim2.new(0.45, 0, 0, 40)
WalkToggleFrame.Position = UDim2.new(0, 15, 0, 55)
WalkToggleFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
WalkToggleFrame.Parent = CustomMoveFrame
setSmoothCorners(WalkToggleFrame, 5)

local WalkLabel = Instance.new("TextLabel")
WalkLabel.Size = UDim2.new(0.6, 0, 1, 0)
WalkLabel.Position = UDim2.new(0, 8, 0, 0)
WalkLabel.BackgroundTransparency = 1
WalkLabel.Text = "WalkCharacter"
WalkLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
WalkLabel.Font = Enum.Font.GothamBold
WalkLabel.TextSize = 11
WalkLabel.Parent = WalkToggleFrame

local WalkBtn = Instance.new("TextButton")
WalkBtn.Size = UDim2.new(0, 35, 0, 18)
WalkBtn.Position = UDim2.new(1, -43, 0.5, -9)
WalkBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
WalkBtn.Text = ""
WalkBtn.Parent = WalkToggleFrame
setSmoothCorners(WalkBtn, 9)

local WalkCircle = Instance.new("Frame")
WalkCircle.Size = UDim2.new(0, 12, 0, 12)
WalkCircle.Position = UDim2.new(0, 3, 0.5, -6)
WalkCircle.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
WalkCircle.Parent = WalkBtn
setSmoothCorners(WalkCircle, 6)

WalkBtn.MouseButton1Click:Connect(function()
    Flags.WalkCharacter = not Flags.WalkCharacter
    if Flags.WalkCharacter then
        Flags.Underground = false
        TweenService:Create(WalkCircle, TweenInfo.new(0.12), {Position = UDim2.new(1, -15, 0.5, -6)}):Play()
        TweenService:Create(WalkBtn, TweenInfo.new(0.12), {BackgroundColor3 = Color3.fromRGB(0, 200, 0)}):Play()
    else
        TweenService:Create(WalkCircle, TweenInfo.new(0.12), {Position = UDim2.new(0, 3, 0.5, -6)}):Play()
        TweenService:Create(WalkBtn, TweenInfo.new(0.12), {BackgroundColor3 = Color3.fromRGB(255, 255, 255)}):Play()
    end
end)

-- زر الالتصاق تحت الأرض مباشرة Underground Attack
local UgToggleFrame = WalkToggleFrame:Clone()
UgToggleFrame.Position = UDim2.new(0.52, 0, 0, 55)
UgToggleFrame.TextLabel.Text = "Underground"
UgToggleFrame.Parent = CustomMoveFrame

local UgBtn = UgToggleFrame.TextButton
local UgCircle = UgBtn.Frame

UgBtn.MouseButton1Click:Connect(function()
    Flags.Underground = not Flags.Underground
    if Flags.Underground then
        Flags.WalkCharacter = false
        TweenService:Create(UgCircle, TweenInfo.new(0.12), {Position = UDim2.new(1, -15, 0.5, -6)}):Play()
        TweenService:Create(UgBtn, TweenInfo.new(0.12), {BackgroundColor3 = Color3.fromRGB(0, 200, 0)}):Play()
    else
        TweenService:Create(UgCircle, TweenInfo.new(0.12), {Position = UDim2.new(0, 3, 0.5, -6)}):Play()
        TweenService:Create(UgBtn, TweenInfo.new(0.12), {BackgroundColor3 = Color3.fromRGB(255, 255, 255)}):Play()
    end
end)

-- [ماتش الالتصاق المطور والآمن لمابك]
RunService.RenderStepped:Connect(function()
    if ConfigValues.TargetPlayer ~= "" then
        local p = Players:FindFirstChild(ConfigValues.TargetPlayer)
        if p and p.Character and p.Character:FindFirstChild("HumanoidRootPart") and LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
            local enemyHrp = p.Character.HumanoidRootPart
            local myHrp = LocalPlayer.Character.HumanoidRootPart
            
            if Flags.WalkCharacter then
                -- يلتصق بظهره تماماً فوق الأرض
                myHrp.CFrame = enemyHrp.CFrame * CFrame.new(0, 0, 2.5)
            elseif Flags.Underground then
                -- يلتصق بظهره ومختفي تحت الأرض بـ 5.5 خطوات لمنع الدمج
                myHrp.CFrame = enemyHrp.CFrame * CFrame.new(0, -5.5, 2.0)
            end
        end
    end
end)

-- ==========================================
-- ⚙️ صفحة الإعدادات وتأكيد تشغيل الواجهة
-- ==========================================
local function populateConfigPage()
    for _, cfg in pairs(allTogglesForConfig) do
        local configRow = Instance.new("Frame")
        configRow.Size = UDim2.new(0.94, 0, 0, 45)
        configRow.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
        configRow.Parent = ConfigPage
        setSmoothCorners(configRow, 6)
        
        local label = Instance.new("TextLabel")
        label.Size = UDim2.new(0.6, 0, 1, 0)
        label.Position = UDim2.new(0, 15, 0, 0)
        label.BackgroundTransparency = 1
        label.Text = "[" .. cfg.parentName:gsub("Page","") .. "] " .. cfg.text
        label.TextColor3 = Color3.fromRGB(200, 200, 200)
        label.Font = Enum.Font.GothamBold
        label.TextSize = 13
        label.TextXAlignment = Enum.TextXAlignment.Left
        label.Parent = configRow
        
        local bindBtn = Instance.new("TextButton")
        bindBtn.Size = UDim2.new(0, 90, 0, 26)
        bindBtn.Position = UDim2.new(1, -105, 0.5, -11)
        bindBtn.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
        bindBtn.Text = "Bind Key"
        bindBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
        bindBtn.Font = Enum.Font.GothamBold
        bindBtn.TextSize = 11
        bindBtn.Parent = configRow
        setSmoothCorners(bindBtn, 4)
        
        bindBtn.MouseButton1Click:Connect(function()
            bindBtn.Text = "..."
            local conn
            conn = UserInputService.InputBegan:Connect(function(input)
                if input.UserInputType == Enum.UserInputType.Keyboard then
                    cfg.setKey(input.KeyCode.Name)
                    bindBtn.Text = input.KeyCode.Name
                    conn:Disconnect()
                end
            end)
        end)
    end
end

UserInputService.InputBegan:Connect(function(input, gpe)
    if gpe then return end
    if input.UserInputType == Enum.UserInputType.Keyboard then
        for _, cfg in pairs(allTogglesForConfig) do if cfg.getKey() == input.KeyCode.Name then cfg.trigger() end end
    end
end)

SearchInput.Changed:Connect(function()
    local text = SearchInput.Text:lower()
    for _, child in pairs(ContentFrame:GetDescendants()) do
        if child:IsA("Frame") and child:FindFirstChild("TextLabel") then
            child.Visible = (text == "" or child.TextLabel.Text:lower():find(text)) and true or false
        end
    end
end)

KeyBtn.MouseButton1Click:Connect(function()
    if KeyInput.Text == CORRECT_KEY then
        KeyFrame:Destroy()
        TweenService:Create(BlurEffect, TweenInfo.new(0.5), {Size = 0}):Play()
        task.delay(0.5, function() BlurEffect:Destroy() end)
        MainFrame.Visible = true
        populateConfigPage()
    else
        KeyBtn.Text = "INVALID KEY"
        KeyBtn.BackgroundColor3 = Color3.fromRGB(150, 0, 0)
        task.wait(1)
        KeyBtn.Text = "LAUNCH DEVELOPER SYSTEM"
        KeyBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    end
end)
