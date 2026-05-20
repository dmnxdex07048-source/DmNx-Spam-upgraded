-- [[ 👑 DmNx Ji ULTIMATE PRO UPDATE 💀 ]] --
local CoreGui = game:GetService("CoreGui")
local ScreenGui = Instance.new("ScreenGui", CoreGui)
ScreenGui.Name = "DmNx Ji Spam (UPGRADED)"

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
    
    local execMsg = "👑?SCRIPT BY DmNx Ji..💀@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@😰😰Ruk Bkl.."
    task.wait(0.2)
    Chat(execMsg)
    task.wait(5)
    s:Destroy()
end)

-- UI Frame
local Main = Instance.new("Frame", ScreenGui)
Main.Size, Main.Position, Main.BackgroundColor3 = UDim2.new(0, 280, 0, 400), UDim2.new(0.5, -140, 0.5, -200), Color3.new(0,0,0)
Main.BorderSizePixel, Main.Active, Main.Draggable = 3, true, true

task.spawn(function()
    while task.wait() do 
        Main.BorderColor3 = Color3.fromRGB(255, 0, 0):Lerp(Color3.fromRGB(128, 0, 128), math.sin(tick() * 3) * 0.5 + 0.5) 
    end
end)

local Scroll = Instance.new("ScrollingFrame", Main)
Scroll.Size, Scroll.Position, Scroll.BackgroundTransparency = UDim2.new(1, 0, 1, 0), UDim2.new(0, 0, 0, 0), 1
Scroll.CanvasSize = UDim2.new(0, 0, 4.5, 0)
Scroll.ScrollBarThickness = 4

local UIList = Instance.new("UIListLayout", Scroll)
UIList.HorizontalAlignment, UIList.Padding = 1, UDim.new(0, 8)

local function CreateTxt(t, s)
    local l = Instance.new("TextLabel", Scroll)
    l.Size, l.Text, l.TextColor3, l.BackgroundTransparency, l.TextSize = UDim2.new(1, 0, 0, s), t, Color3.new(1,1,1), 1, 11
    l.Font = Enum.Font.Code
    return l
end

CreateTxt("👑 DmNx Spam UPDATED HUB 💀", 30)
CreateTxt([[--------------------------
MADE BY DmNx Ji
DmNx Empire 👑🔥
--------------------------]], 80)

local function Inp(p)
    local b = Instance.new("TextBox", Scroll)
    b.Size, b.PlaceholderText, b.BackgroundColor3, b.TextColor3 = UDim2.new(0.9, 0, 0, 40), p, Color3.fromRGB(20,20,20), Color3.new(1,1,1)
    b.BorderSizePixel = 0
    return b
end

local Tar, Del = Inp("TARGET😈"), Inp("DELAY🤡")

local function Btn(t, c)
    local b = Instance.new("TextButton", Scroll)
    b.Size, b.Text, b.BackgroundColor3, b.TextColor3, b.Font = UDim2.new(0.9, 0, 0, 45), t, c, Color3.new(1,1,1), 3
    b.TextSize = 18
    return b
end

local St = Btn("START SPAM 🙏", Color3.fromRGB(0,100,0))
local Sp = Btn("STOP SPAM 🤡", Color3.fromRGB(100,0,0))

-- [[ 25 LINE STOCK - PURE @ BLOCKS NO SPACE ]] --
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
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] TMKX MAIN DREAM >",
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] BOL DmNx Ji ON TOP.. 😈",
    "👑? SCRIPT BY DmNx Ji. @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ [TARGET] SERVER KI AISI TESI BY DmNx Ji.. 🔥"
}

getgenv().On = false
St.Activated:Connect(function()
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
end)

Sp.Activated:Connect(function() getgenv().On = false end)

local T = Btn("CLOSE", Color3.new(0,0,0))
T.Parent, T.Position, T.Size = ScreenGui, UDim2.new(0, 10, 0.5, 0), UDim2.new(0, 90, 0, 35)
T.Activated:Connect(function() Main.Visible = not Main.Visible end)
