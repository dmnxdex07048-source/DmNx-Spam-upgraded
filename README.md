-- [[ 👑 DmNx Ji ULTIMATE PRO UPDATE 💀 ]] --
local CoreGui = game:GetService("CoreGui")
local RunService = game:GetService("RunService")
local ScreenGui = Instance.new("ScreenGui", CoreGui)
ScreenGui.Name = "DmNx Ji Spam (UPGRADED)"
ScreenGui.ResetOnSpawn = false

-- [[ CHAT FUNCTIONALITY ]] --
local function Chat(m)
    pcall(function()
        local t = game:GetService("TextChatService")
        if t.ChatVersion == Enum.ChatVersion.TextChatService then
            t.TextChannels.RBXGeneral:SendAsync(m)
        else
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(m, "All")
        end
    end)
end

-- [[ NEW SOUND ID & EXECUTE TEXT ]] --
task.spawn(function()
    local s = Instance.new("Sound", CoreGui)
    s.SoundId = "rbxassetid://259816079"
    s.Volume = 50
    s:Play()
    
    local execMsg = "👑?SCRIPT BY DmNx Ji..💀________________________________________________________________ᗪ爪几乂 丂卩卂爪 ㄥㄖ卂ᗪ乇ᗪ💀🔥.."
    task.wait(0.2)
    Chat(execMsg)
    task.wait(5)
    s:Destroy()
end)

-- [[ MODERN FRAME CREATION ]] --
local MainFrame = Instance.new("Frame")
MainFrame.Size = UDim2.new(0, 280, 0, 420)
MainFrame.Position = UDim2.new(0.5, -140, 0.5, -210)
MainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
MainFrame.BorderSizePixel = 0
MainFrame.Active = true
MainFrame.Draggable = true
MainFrame.Parent = ScreenGui

-- Rainbow Border effect integrated from the original design
task.spawn(function()
    local border = Instance.new("UIStroke", MainFrame)
    border.Thickness = 3
    while task.wait() do
        border.Color = Color3.fromRGB(255, 0, 0):Lerp(Color3.fromRGB(128, 0, 128), math.sin(tick() * 3) * 0.5 + 0.5)
    end
end)

local UICorner = Instance.new("UICorner")
UICorner.CornerRadius = UDim.new(0, 12)
UICorner.Parent = MainFrame

-- Top UI Elements
local Title = Instance.new("TextLabel")
Title.Size = UDim2.new(1, 0, 0, 40)
Title.Text = "DmNx Spam Hub 💀"
Title.TextSize = 22
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.BackgroundTransparency = 1
Title.Font = Enum.Font.SourceSansBold
Title.Parent = MainFrame

local FPSCounter = Instance.new("TextLabel")
FPSCounter.Size = UDim2.new(1, 0, 0, 20)
FPSCounter.Position = UDim2.new(0, 0, 0, 40)
FPSCounter.Text = "FPS: 0"
FPSCounter.TextColor3 = Color3.fromRGB(200, 200, 200)
FPSCounter.BackgroundTransparency = 1
FPSCounter.Font = Enum.Font.SourceSans
FPSCounter.TextSize = 16
FPSCounter.Parent = MainFrame

RunService.RenderStepped:Connect(function(dt)
    FPSCounter.Text = "FPS: " .. tostring(math.floor(1 / dt))
end)

-- Buttons and Interaction Container
local ButtonsContainer = Instance.new("Frame")
ButtonsContainer.Size = UDim2.new(0.9, 0, 0.68, 0)
ButtonsContainer.Position = UDim2.new(0.05, 0, 0, 75)
ButtonsContainer.BackgroundTransparency = 1
ButtonsContainer.ClipsDescendants = true
ButtonsContainer.Parent = MainFrame

local UIListLayout = Instance.new("UIListLayout")
UIListLayout.FillDirection = Enum.FillDirection.Vertical
UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
UIListLayout.Padding = UDim.new(0, 8)
UIListLayout.Parent = ButtonsContainer

-- User Inputs (Target and Delay fields)
local Tar = Instance.new("TextBox")
Tar.Size = UDim2.new(1, 0, 0, 38)
Tar.PlaceholderText = "TARGET😈"
Tar.Text = ""
Tar.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Tar.TextColor3 = Color3.new(1,1,1)
Tar.BorderSizePixel = 0
Tar.Font = Enum.Font.SourceSans
Tar.TextSize = 18
Tar.Parent = ButtonsContainer
local UICornerTar = Instance.new("UICorner", Tar)
UICornerTar.CornerRadius = UDim.new(0, 6)

local Del = Instance.new("TextBox")
Del.Size = UDim2.new(1, 0, 0, 38)
Del.PlaceholderText = "DELAY🤡"
Del.Text = ""
Del.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Del.TextColor3 = Color3.new(1,1,1)
Del.BorderSizePixel = 0
Del.Font = Enum.Font.SourceSans
Del.TextSize = 18
Del.Parent = ButtonsContainer
local UICornerDel = Instance.new("UICorner", Del)
UICornerDel.CornerRadius = UDim.new(0, 6)

-- Navigation Buttons
local PageLeft = Instance.new("TextButton")
PageLeft.Size = UDim2.new(0.5, 0, 0, 35)
PageLeft.Position = UDim2.new(0, 0, 1, -35)
PageLeft.Text = "<"
PageLeft.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
PageLeft.Font = Enum.Font.SourceSansBold
PageLeft.TextColor3 = Color3.new(1,1,1)
PageLeft.TextSize = 22
PageLeft.Parent = MainFrame
local UICornerPL = Instance.new("UICorner", PageLeft)

local PageRight = Instance.new("TextButton")
PageRight.Size = UDim2.new(0.5, 0, 0, 35)
PageRight.Position = UDim2.new(0.5, 0, 1, -35)
PageRight.Text = ">"
PageRight.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
PageRight.Font = Enum.Font.SourceSansBold
PageRight.TextColor3 = Color3.new(1,1,1)
PageRight.TextSize = 22
PageRight.Parent = MainFrame
local UICornerPR = Instance.new("UICorner", PageRight)

-- [[ SPAM ARRAYS AND DATA RUNNERS ]] --
local msgs = { 
    "[TARGET] MADARCH4D BH3NXHODI XAL3 KU6TE K6 A8NDH @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX KI PHATU 🥶", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN COLD >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN VOID >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN SPAMMER >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAINSCRIPT >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN DIRT >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN SHARK >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN NAAL >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN MOAT >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN ROBUX >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN FAST >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN MOBILE >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN BALI >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN FEAR >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN DOOM >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN SKY >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN CLOUD >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN GOD >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN HOT >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] B5TA BOL DmNx Ji PA9A >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN NEWEST >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN RELATIONSHIP >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN KURKURE >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] P4P4 BOLO B3T4 >", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] BOL DmNx Ji ON TOP.. 😈", 
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] SERVER KI AISI TESI BY DmNx Ji.. 🔥" 
}

getgenv().On = false

-- Configured UI Layout Button Actions mapped into table array logic 
local buttons = {
    {
        name = "START SPAM 🙏", 
        type = "button", 
        color = Color3.fromRGB(0, 100, 0),
        callback = function() 
            if getgenv().On then return end 
            getgenv().On = true 
            local t, w = Tar.Text, tonumber(Del.Text) or 1.5 
            task.spawn(function() 
                while getgenv().On do 
                    for _, m in pairs(msgs) do 
                        if not getgenv().On then break end 
                        Chat(m:gsub("%[TARGET%]", t)) 
                        task.wait(w) 
                    end 
                end 
            end) 
        end
    },
    {
        name = "STOP SPAM 🤡", 
        type = "button", 
        color = Color3.fromRGB(100, 0, 0),
        callback = function() 
            getgenv().On = false 
        end
    },
    {
        name = "CREDITS 🔥", 
        type = "button", 
        color = Color3.fromRGB(45, 45, 45),
        callback = function() 
            print("MADE BY DmNx Ji - DmNx Empire 👑🔥") 
        end
    }
}

local currentPage = 1
local itemsPerPage = 3

local function renderPage(page)
    -- Remove old buttons while retaining Target and Delay input text boxes
    for _, child in ipairs(ButtonsContainer:GetChildren()) do
        if child:IsA("TextButton") then child:Destroy() end
    end
    
    local startIndex = (page - 1) * itemsPerPage + 1
    local endIndex = math.min(page * itemsPerPage, #buttons)
    
    for i = startIndex, endIndex do
        local item = buttons[i]
        local btn = Instance.new("TextButton", ButtonsContainer)
        btn.Size = UDim2.new(1, 0, 0, 42)
        btn.Text = item.name
        btn.BackgroundColor3 = item.color or Color3.fromRGB(200, 200, 200)
        btn.TextColor3 = Color3.fromRGB(255, 255, 255)
        btn.Font = Enum.Font.SourceSansBold
        btn.TextSize = 18
        
        local UICornerBtn = Instance.new("UICorner")
        UICornerBtn.CornerRadius = UDim.new(0, 6)
        UICornerBtn.Parent = btn
        
        btn.MouseButton1Click:Connect(item.callback)
    end
end

PageLeft.MouseButton1Click:Connect(function()
    if currentPage > 1 then
        currentPage = currentPage - 1
        renderPage(currentPage)
    end
end)

PageRight.MouseButton1Click:Connect(function()
    if currentPage < math.ceil(#buttons / itemsPerPage) then
        currentPage = currentPage + 1
        renderPage(currentPage)
    end
end)

renderPage(currentPage)

-- Dynamic External Independent Close Toggle Action (Kept intact from original format logic)
local T = Instance.new("TextButton")
T.Text = "CLOSE"
T.BackgroundColor3 = Color3.new(0,0,0)
T.TextColor3 = Color3.new(1,1,1)
T.Font = Enum.Font.SourceSansBold
T.TextSize = 14
T.Parent = ScreenGui
T.Position = UDim2.new(0, 10, 0.5, 0)
T.Size = UDim2.new(0, 90, 0, 35)

local UICornerClose = Instance.new("UICorner", T)
UICornerClose.CornerRadius = UDim.new(0, 6)

T.Activated:Connect(function() 
    MainFrame.Visible = not MainFrame.Visible 
end)
