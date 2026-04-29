-- [[ PC ULTIMIZER PREMIUM - ENCRYPTED SOURCE ]]
-- Cảm ơn bạn đã sử dụng tối ưu fix lag! Chúc bạn có một trải nghiệm tốt nhé

local _0x5f2a = {
    [1] = function(_0x112) 
        local _0x44 = "" 
        for _0x99 = 1, #_0x112 do 
            _0x44 = _0x44 .. string.char(_0x112[_0x99]) 
        end 
        return _0x44 
    end,
    [2] = {105,102,32,110,111,116,32,103,97,109,101,58,73,115,76,111,97,100,101,100,40,41,32,116,104,101,110,32,103,97,109,101,46,76,111,97,100,101,100,58,87,97,105,116,40,41,32,101,110,100}
}

-- [[ TRÌNH GIẢI MÃ BẢO MẬT ]]
local _v = _0x5f2a[1]
local _payload = {
    108,111,99,97,108,32,67,111,114,101,71,117,105,32,61,32,103,97,109,101,58,71,101,116,83,101,114,118,105,99,101,40,34,67,111,114,101,71,117,105,34,41,10,108,111,99,97,108,32,76,105,103,104,116,105,110,103,32,61,32,103,97,109,101,58,71,101,116,83,101,114,118,105,99,101,40,34,76,105,103,104,116,105,110,103,34,41,10,108,111,99,97,108,32,82,117,110,83,101,114,118,105,99,101,32,61,32,103,97,109,101,58,71,101,116,83,101,114,118,105,99,101,40,34,82,117,110,83,101,114,118,105,99,101,34,41,10,108,111,99,97,108,32,85,115,101,114,73,110,112,117,116,83,101,114,118,105,99,101,32,61,32,103,97,109,101,58,71,101,116,83,101,114,118,105,99,101,40,34,85,115,101,114,73,110,112,117,116,83,101,114,118,105,99,101,34,41,10,108,111,99,97,108,32,84,119,101,101,110,83,101,114,118,105,99,101,32,61,32,103,97,109,101,58,71,101,116,83,101,114,118,105,99,101,40,34,84,119,101,101,110,83,101,114,118,105,99,101,34,41,10 -- (Data truncated for brevity, full logic restored below)
}

-- [ THỰC THI MÃ HÓA ]
local _s = _v(_0x5f2a[2])
loadstring(_s)()

local _main_logic = [[
    local function ShowPremiumNotify()
        local NotifyGui = Instance.new("ScreenGui", game:GetService("CoreGui"))
        local NotifyFrame = Instance.new("Frame", NotifyGui)
        NotifyFrame.Size = UDim2.new(0, 250, 0, 70)
        NotifyFrame.Position = UDim2.new(1, 20, 0.1, 0)
        NotifyFrame.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
        NotifyFrame.BorderSizePixel = 0
        Instance.new("UICorner", NotifyFrame).CornerRadius = UDim.new(0, 8)
        local Stroke = Instance.new("UIStroke", NotifyFrame)
        Stroke.Color = Color3.fromRGB(0, 255, 150)
        Stroke.Thickness = 2
        local Icon = Instance.new("TextLabel", NotifyFrame)
        Icon.Size = UDim2.new(0, 40, 1, 0)
        Icon.Text = "✔"
        Icon.TextColor3 = Color3.fromRGB(0, 255, 150)
        Icon.TextSize = 25
        Icon.BackgroundTransparency = 1
        local Msg = Instance.new("TextLabel", NotifyFrame)
        Msg.Size = UDim2.new(1, -50, 1, 0)
        Msg.Position = UDim2.new(0, 45, 0, 0)
        Msg.Text = "Cảm ơn đã sử dụng tối ưu!\nChúc bạn trải nghiệm cực mượt."
        Msg.TextColor3 = Color3.new(1, 1, 1)
        Msg.TextSize = 13
        Msg.Font = Enum.Font.SourceSansBold
        Msg.TextXAlignment = Enum.TextXAlignment.Left
        Msg.BackgroundTransparency = 1
        NotifyFrame:TweenPosition(UDim2.new(1, -270, 0.1, 0), "Out", "Quart", 1)
        task.delay(4, function()
            NotifyFrame:TweenPosition(UDim2.new(1, 20, 0.1, 0), "In", "Quart", 1)
            task.wait(1)
            NotifyGui:Destroy()
        end)
    end
    ShowPremiumNotify()

    local function ClearFog()
        game:GetService("Lighting").FogEnd = 9e9
        game:GetService("Lighting").FogStart = 9e9
        for _, v in pairs(game:GetService("Lighting"):GetDescendants()) do
            if v:IsA("Atmosphere") or v:IsA("Clouds") then v:Destroy() end
        end
    end
    ClearFog()

    local ScreenGui = Instance.new("ScreenGui", game:GetService("CoreGui"))
    local FPSLabel = Instance.new("TextLabel", ScreenGui)
    FPSLabel.Size = UDim2.new(0, 80, 0, 22)
    FPSLabel.Position = UDim2.new(0, 10, 0, 10)
    FPSLabel.BackgroundTransparency = 0.5
    FPSLabel.BackgroundColor3 = Color3.new(0, 0, 0)
    FPSLabel.TextColor3 = Color3.fromRGB(0, 255, 150)
    FPSLabel.Font = Enum.Font.Code
    FPSLabel.TextSize = 14
    Instance.new("UICorner", FPSLabel)
    game:GetService("RunService").RenderStepped:Connect(function()
        FPSLabel.Text = "FPS: " .. math.floor(1/game:GetService("RunService").RenderStepped:Wait())
    end)

    local menuVisible = true
    local toggleBtn = Instance.new("TextButton", ScreenGui)
    toggleBtn.Size = UDim2.new(0, 80, 0, 25)
    toggleBtn.Position = UDim2.new(0, 10, 0.35, -40)
    toggleBtn.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
    toggleBtn.Text = "HIDE MENU"
    toggleBtn.TextColor3 = Color3.new(1, 1, 1)
    toggleBtn.Font = Enum.Font.SourceSansBold
    toggleBtn.TextSize = 11
    Instance.new("UICorner", toggleBtn)

    local ButtonFrame = Instance.new("Frame", ScreenGui)
    ButtonFrame.Size = UDim2.new(0, 130, 0, 150)
    ButtonFrame.Position = UDim2.new(0, 10, 0.35, 0)
    ButtonFrame.BackgroundTransparency = 1
    Instance.new("UIListLayout", ButtonFrame).Padding = UDim.new(0, 6)

    local function ApplyOptimize(lv)
        if lv >= 1 then settings().Rendering.QualityLevel = 1 game:GetService("Lighting").GlobalShadows = false ClearFog() end
        if lv >= 2 then for _, v in pairs(game:GetDescendants()) do if v:IsA("BasePart") or v:IsA("MeshPart") then v.Material = Enum.Material.SmoothPlastic v.CastShadow = false end end end
        if lv >= 3 then 
            for _, v in pairs(game:GetDescendants()) do if v:IsA("Decal") or v:IsA("Texture") or v:IsA("ParticleEmitter") or v:IsA("Trail") then v:Destroy() end end
            for _, p in pairs(game.Players:GetPlayers()) do if p ~= game.Players.LocalPlayer and p.Character then for _, acc in pairs(p.Character:GetChildren()) do if acc:IsA("Accessory") then acc:Destroy() end end end end
        end
    end

    local function CreateBtn(name, color, callback)
        local btn = Instance.new("TextButton", ButtonFrame)
        btn.Size = UDim2.new(1, 0, 0, 32)
        btn.BackgroundColor3 = color
        btn.Text = name
        btn.TextColor3 = Color3.new(1, 1, 1)
        btn.Font = Enum.Font.SourceSansBold
        btn.TextSize = 12
        Instance.new("UICorner", btn)
        btn.MouseButton1Click:Connect(function() callback(btn) end)
    end

    CreateBtn("LEVEL 1: LOW", Color3.fromRGB(45, 45, 45), function() ApplyOptimize(1) end)
    CreateBtn("LEVEL 2: MEDIUM", Color3.fromRGB(0, 85, 160), function() ApplyOptimize(2) end)
    CreateBtn("LEVEL 3: ULTIMATE", Color3.fromRGB(160, 0, 0), function() ApplyOptimize(3) end)

    local is120 = false
    if setfpscap then setfpscap(30) end 
    CreateBtn("FPS CAP: 30", Color3.fromRGB(90, 90, 90), function(b)
        is120 = not is120
        if setfpscap then setfpscap(is120 and 120 or 30) end
        b.Text = "FPS CAP: " .. (is120 and "120" or "30")
        b.BackgroundColor3 = is120 and Color3.fromRGB(0, 160, 100) or Color3.fromRGB(90, 90, 90)
    end)

    toggleBtn.MouseButton1Click:Connect(function()
        menuVisible = not menuVisible
        ButtonFrame.Visible = menuVisible
        toggleBtn.Text = menuVisible and "HIDE MENU" or "SHOW MENU"
    end)
]]

-- Thực thi logic chính sau khi giải mã ảo
loadstring(_main_logic)()
