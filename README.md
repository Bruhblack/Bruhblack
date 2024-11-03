local OrionLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/shlexware/Orion/main/source"))()
local player = game.Players.LocalPlayer

-- Create the local window
local window = OrionLib:MakeWindow({Name = "Justine Hub | The Mimic", HidePremium = false})

-- Create the first tab for Chapter 1
local tab1 = window:MakeTab({
    Name = "Book 1 Chapter 1",
    Icon = "rbxassetid://4483345998",
    Premium = false
})

-- Teleport positions for Chapter 1
local position1 = Vector3.new(3460.84375, 37.646121978759766, -1541.8065185546875)
local position2 = Vector3.new(1274.013916015625, 199.5399932861328, -2536.854736328125)

-- Create the "Auto win" buttons for Chapter 1
tab1:AddButton({
    Name = "Auto win part 1",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position1))
    end
})
tab1:AddButton({
    Name = "Auto win part 2",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position2))
    end
})

-- Create the second tab for Chapter 2
local tab2 = window:MakeTab({
    Name = "Book 1 Chapter 2",
    Icon = "rbxassetid://4483345998",
    Premium = false
})

-- Teleport positions for Chapter 2
local position3 = Vector3.new(65.12515258789062, 56.40327453613281, -1584.817138671875)
local position4 = Vector3.new(236.37899780273438, 101.94117736816406, -588.1929931640625)
local position5 = Vector3.new(908.4821166992188, 72.8182601928711, -356.0920104980469)

-- Create the "Auto win" buttons for Chapter 2
tab2:AddButton({
    Name = "Auto win part 1",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position3))
    end
})
tab2:AddButton({
    Name = "Auto win part 2",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position4))
    end
})
tab2:AddButton({
    Name = "Auto win part 3",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position5))
    end
})

-- Create the third tab for Chapter 3
local tab3 = window:MakeTab({
    Name = "Book 1 Chapter 3",
    Icon = "rbxassetid://4483345998",
    Premium = false
})

-- Teleport positions for Chapter 3
local position6 = Vector3.new(2411.8251953125, -23.03111457824707, 2276.95361328125)
local position7 = Vector3.new(242.91757202148438, 31.71737289428711, 454.57183837890625)

-- Create the "Auto win" buttons for Chapter 3
tab3:AddButton({
    Name = "Auto win part 1",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position6))
    end
})
tab3:AddButton({
    Name = "Auto win part 2",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position7))
    end
})
tab3:AddButton({
    Name = "Auto win part 3",
    Callback = function()
        local position8 = Vector3.new(0, 0, 0) -- Replace with the correct position
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position8))
    end
})

-- Create the fourth tab for Chapter 4
local tab4 = window:MakeTab({
    Name = "Book 1 Chapter 4",
    Icon = "rbxassetid://4483345998",
    Premium = false
})

-- Teleport position for Chapter 4
local position9 = Vector3.new(89.58648681640625, -50.996978759765625, -1415.93310546875)

-- Add buttons for Chapter 4
tab4:AddButton({
    Name = "chapter 1",
    Callback = function()
        local character = player.Character or player.CharacterAdded:Wait()
        character:SetPrimaryPartCFrame(CFrame.new(position9))
    end
})
tab4:AddButton({
    Name = "Use KtollT",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/KTollT/KTollT/main/README.md"))()
    end
})

-- Create the "Misc" tab
local miscTab = window:MakeTab({
    Name = "Misc",
    Icon = "rbxassetid://4483345998",
    Premium = false
})

-- FullBright Toggle
local FullBrightEnabled = false

local function ToggleFullBright()
    FullBrightEnabled = not FullBrightEnabled
    local lighting = game:GetService("Lighting")

    if FullBrightEnabled then
        lighting.Brightness = 2
        lighting.OutdoorAmbient = Color3.new(1, 1, 1)
        lighting.Ambient = Color3.new(1, 1, 1)
    else
        lighting.Brightness = 1
        lighting.OutdoorAmbient = Color3.new(0, 0, 0)
        lighting.Ambient = Color3.new(0.5, 0.5, 0.5)
    end
end

miscTab:AddButton({
    Name = "Toggle FullBright",
    Callback = ToggleFullBright
})

-- Make the window visible
OrionLib:Init()
