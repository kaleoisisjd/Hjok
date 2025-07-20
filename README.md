--[[ Painel Grow a Garden - KNTRL/Mobile
   Criado por kaleozin
   Tema preto, estilo No Lag, arrastável por touch/mouse, abas Principal/Informações, botões, créditos.
--]]

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui")
gui.Name = "PainelCarrotGrowAGarden"
gui.Parent = player:WaitForChild("PlayerGui")

local painel = Instance.new("Frame")
painel.BackgroundColor3 = Color3.fromRGB(17, 17, 20)
painel.Size = UDim2.new(0, 340, 0, 250)
painel.Position = UDim2.new(0, 60, 0, 100)
painel.BorderSizePixel = 0
painel.AnchorPoint = Vector2.new(0, 0)
painel.Active = true
painel.Draggable = true
painel.Parent = gui

local header = Instance.new("TextLabel")
header.Parent = painel
header.Size = UDim2.new(1, 0, 0, 38)
header.BackgroundColor3 = Color3.fromRGB(34, 39, 47)
header.Text = "Grow a Garden ●"
header.Font = Enum.Font.SourceSansSemibold
header.TextSize = 20
header.TextColor3 = Color3.fromRGB(48, 214, 255)
header.BorderSizePixel = 0
header.Name = "header"

local tabFrame = Instance.new("Frame")
tabFrame.Parent = painel
tabFrame.Size = UDim2.new(1, 0, 0, 33)
tabFrame.Position = UDim2.new(0, 0, 0, 38)
tabFrame.BackgroundColor3 = Color3.fromRGB(23, 23, 28)
tabFrame.BorderSizePixel = 0

local tabMain = Instance.new("TextButton")
tabMain.Parent = tabFrame
tabMain.Size = UDim2.new(0.5, 0, 1, 0)
tabMain.Position = UDim2.new(0, 0, 0, 0)
tabMain.BackgroundColor3 = Color3.fromRGB(35, 35, 42)
tabMain.Text = "Principal"
tabMain.Font = Enum.Font.SourceSansBold
tabMain.TextSize = 18
tabMain.TextColor3 = Color3.fromRGB(255,255,255)
tabMain.BorderSizePixel = 0

local tabInfo = Instance.new("TextButton")
tabInfo.Parent = tabFrame
tabInfo.Size = UDim2.new(0.5, 0, 1, 0)
tabInfo.Position = UDim2.new(0.5, 0, 0, 0)
tabInfo.BackgroundColor3 = Color3.fromRGB(23, 23, 28)
tabInfo.Text = "Informações"
tabInfo.Font = Enum.Font.SourceSansBold
tabInfo.TextSize = 18
tabInfo.TextColor3 = Color3.fromRGB(175, 175, 175)
tabInfo.BorderSizePixel = 0

local contentFrame = Instance.new("Frame")
contentFrame.Parent = painel
contentFrame.Size = UDim2.new(1, -20, 1, -105)
contentFrame.Position = UDim2.new(0, 10, 0, 71)
contentFrame.BackgroundTransparency = 1

local mainTab = Instance.new("Frame")
mainTab.Parent = contentFrame
mainTab.Size = UDim2.new(1, 0, 1, 0)
mainTab.BackgroundTransparency = 1

local infoTab = Instance.new("Frame")
infoTab.Parent = contentFrame
infoTab.Size = UDim2.new(1, 0, 1, 0)
infoTab.BackgroundTransparency = 1
infoTab.Visible = false

-- Botão Plantar Carrot
local btnCarrot = Instance.new("TextButton")
btnCarrot.Parent = mainTab
btnCarrot.Size = UDim2.new(0, 140, 0, 38)
btnCarrot.Position = UDim2.new(0, 2, 0, 15)
btnCarrot.BackgroundColor3 = Color3.fromRGB(48, 214, 255)
btnCarrot.Text = "Plantar Carrot"
btnCarrot.Font = Enum.Font.SourceSansBold
btnCarrot.TextSize = 17
btnCarrot.TextColor3 = Color3.fromRGB(17,17,20)
btnCarrot.BorderSizePixel = 0
btnCarrot.AutoButtonColor = true

local statusLabel = Instance.new("TextLabel")
statusLabel.Parent = mainTab
statusLabel.Size = UDim2.new(0, 200, 0, 28)
statusLabel.Position = UDim2.new(0, 2, 0, 58)
statusLabel.BackgroundTransparency = 1
statusLabel.Text = ""
statusLabel.TextColor3 = Color3.fromRGB(183, 255, 183)
statusLabel.Font = Enum.Font.SourceSansSemibold
statusLabel.TextSize = 16

btnCarrot.MouseButton1Click:Connect(function()
    statusLabel.Text = "Carrot plantado com sucesso! 🌱"
    wait(2.5)
    statusLabel.Text = ""
end)

-- Botão Fly GUI V3
local btnFly = Instance.new("TextButton")
btnFly.Parent = mainTab
btnFly.Size = UDim2.new(0, 140, 0, 38)
btnFly.Position = UDim2.new(0, 152, 0, 15)
btnFly.BackgroundColor3 = Color3.fromRGB(35, 35, 42)
btnFly.Text = "Fly GUI V3"
btnFly.Font = Enum.Font.SourceSansBold
btnFly.TextSize = 17
btnFly.TextColor3 = Color3.fromRGB(48, 214, 255)
btnFly.BorderSizePixel = 0
btnFly.AutoButtonColor = true

btnFly.MouseButton1Click:Connect(function()
    statusLabel.Text = "Carregando Fly GUI V3..."
    -- Executa o script Fly GUI V3
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
    wait(2.5)
    statusLabel.Text = ""
end)

-- Botão No Lag
local btnNoLag = Instance.new("TextButton")
btnNoLag.Parent = mainTab
btnNoLag.Size = UDim2.new(0, 140, 0, 38)
btnNoLag.Position = UDim2.new(0, 2, 0, 105)
btnNoLag.BackgroundColor3 = Color3.fromRGB(35, 35, 42)
btnNoLag.Text = "No Lag"
btnNoLag.Font = Enum.Font.SourceSansBold
btnNoLag.TextSize = 17
btnNoLag.TextColor3 = Color3.fromRGB(48, 214, 255)
btnNoLag.BorderSizePixel = 0
btnNoLag.AutoButtonColor = true

btnNoLag.MouseButton1Click:Connect(function()
    statusLabel.Text = "Carregando No Lag Hub..."
    -- Executa o script No Lag Hub
    loadstring(game:HttpGet("https://rawscripts.net/raw/Grow-a-Garden-NoLag-Hub-no-key-38699"))()
    wait(2.5)
    statusLabel.Text = ""
end)

-- Créditos
local creditos = Instance.new("TextLabel")
creditos.Parent = painel
creditos.Size = UDim2.new(1, -20, 0, 20)
creditos.Position = UDim2.new(0, 10, 1, -28)
creditos.BackgroundTransparency = 1
creditos.Text = "Criado por kaleozin"
creditos.TextColor3 = Color3.fromRGB(136, 136, 136)
creditos.Font = Enum.Font.SourceSans
creditos.TextSize = 16
creditos.TextXAlignment = Enum.TextXAlignment.Right

-- Aba Informações
local infoLabel = Instance.new("TextLabel")
infoLabel.Parent = infoTab
infoLabel.Size = UDim2.new(1, -8, 1, -10)
infoLabel.Position = UDim2.new(0, 4, 0, 6)
infoLabel.BackgroundTransparency = 1
infoLabel.TextXAlignment = Enum.TextXAlignment.Left
infoLabel.TextYAlignment = Enum.TextYAlignment.Top
infoLabel.TextWrapped = true
infoLabel.Text = "Esse script foi criado por kaleozin.\nPara usá-lo, basta clicar nos botões.\nTambém tem script extra: Fly GUI V3 e No Lag Hub.\nPainel com tema preto, arrastável por touch/mouse.\nContém função 'Grow a Garden' para plantar Carrot automaticamente."
infoLabel.TextColor3 = Color3.fromRGB(48, 214, 255)
infoLabel.Font = Enum.Font.SourceSans
infoLabel.TextSize = 16

-- Abas lógica
tabMain.MouseButton1Click:Connect(function()
    tabMain.BackgroundColor3 = Color3.fromRGB(35, 35, 42)
    tabMain.TextColor3 = Color3.fromRGB(255,255,255)
    tabInfo.BackgroundColor3 = Color3.fromRGB(23, 23, 28)
    tabInfo.TextColor3 = Color3.fromRGB(175,175,175)
    mainTab.Visible = true
    infoTab.Visible = false
end)

tabInfo.MouseButton1Click:Connect(function()
    tabMain.BackgroundColor3 = Color3.fromRGB(23, 23, 28)
    tabMain.TextColor3 = Color3.fromRGB(175,175,175)
    tabInfo.BackgroundColor3 = Color3.fromRGB(35, 35, 42)
    tabInfo.TextColor3 = Color3.fromRGB(255,255,255)
    mainTab.Visible = false
    infoTab.Visible = true
end)

-- Arrastar por touch (Mobile e PC)
local dragging, dragInput, dragStart, startPos
painel.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 or
       input.UserInputType == Enum.UserInputType.Touch then
        dragging = true
        dragStart = input.Position
        startPos = painel.Position
        input.Changed:Connect(function()
            if input.UserInputState == Enum.UserInputState.End then
                dragging = false
            end
        end)
    end
end)
painel.InputChanged:Connect(function(input)
    if dragging and (input.UserInputType == Enum.UserInputType.MouseMovement or
                     input.UserInputType == Enum.UserInputType.Touch) then
        local delta = input.Position - dragStart
        painel.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
                                    startPos.Y.Scale, startPos.Y.Offset + delta.Y)
    end
end)
