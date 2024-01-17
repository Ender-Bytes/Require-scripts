# Require-scripts
-- made by TheFlamingBlaster
print("Script stealer by TheFlamingBlaster successfully started up.")
print("December 30th, 2016.")
print("Click on a player to freeze them, hit c to run their currently running scripts under yourself.")
print("This only works with localscripts")
print("This won't allow you to get the code of the scripts.")

local plr = game.Players.LocalPlayer
function exe(cmd)
game:GetService'Players'.LocalPlayer.PlayerGui.SB_DataTransfer.SB_CommandRemote.Value = cmd
end
local mouse = plr:GetMouse()
local adornees
local destroyit = false
local lasttarget 
local currenttarget
local changed = {}
mouse.Button1Down:connect(function()
	if mouse.Target then
	if mouse.Target.Parent.ClassName == "Model" then
	currenttarget = mouse.Target.Parent
	lasttarget = mouse.Target.Parent
	adornees = Instance.new("Model",plr.Character)
	for i,v in pairs(mouse.Target.Parent:GetChildren()) do
		local s = Instance.new("SelectionBox",adornees)
		if v:IsA("Part") then
			if v.Name == "Torso" then
				local lasso = Instance.new("SelectionPartLasso",adornees)
				lasso.Humanoid = plr.Character.Humanoid
				lasso.Part = v
			end
			s.Adornee = v
			if v.Anchored == false then
				table.insert(changed,v)
				v.Anchored = true
			end
		end
		
	end
	destroyit = true
	end	
	end
end)
game:GetService('UserInputService').InputBegan:connect(function(input,processed)
	if mouse.Target and destroyit == true then
	if input.KeyCode == Enum.KeyCode.C then
		--currenttarget:Destroy()
		for i,v in pairs(currenttarget:GetChildren()) do
			if v:IsA("LocalScript") then
				local c = v
				c.Parent = plr.Character
				c.Name = "Stolen"
				exe('local a = '..v:GetFullName()..':Clone() a.Parent = getfenv().owner.Character print(a.Parent)')
				print(c.Parent)
			end
		end
		adornees:Destroy()
	end
	end
end)
mouse.Button1Up:connect(function()
	if destroyit == true then
	currenttarget = nil
	for i,v in pairs(changed) do
		v.Anchored = false
	end
	changed = {}
	adornees:Destroy()
	destroyit = false
	end
end)
