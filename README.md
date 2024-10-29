# Roblox-one-shot-boss
-- One-Shot Boss Script for Roblox "Soul"

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local workspace = game:GetService("Workspace")
local bossName = "The Gero King" -- Replace with actual boss name
local damageAmount = 999999 -- Set this to the desired damage amount

local function oneShotBoss()
    local boss = workspace:FindFirstChild(bossName)

    if boss and boss:FindFirstChild("Humanoid") then
        -- Deal damage to the boss
        boss.Humanoid:TakeDamage(damageAmount)

        -- Optional: Display a message or effect
        print(bossName .. " has been defeated!")
    else
        print("Boss not found!")
    end
end

-- Execute the one-shot function
oneShotBoss()
