-- Objects

local MiniGUI = Instance.new("ScreenGui")
local scriptframe = Instance.new("Frame")
local TextButton = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local TextButton_2 = Instance.new("TextButton")
local TextButton_3 = Instance.new("TextButton")
local TextButton_4 = Instance.new("TextButton")
local TextButton_5 = Instance.new("TextButton")
local TextButton_6 = Instance.new("TextButton")
local TextButton_7 = Instance.new("TextButton")
local TextButton_8 = Instance.new("TextButton")

-- Properties

MiniGUI.Name = "Mini GUI"
MiniGUI.Parent = game.Players.LocalPlayer.PlayerGui

scriptframe.Name = "script frame"
scriptframe.Parent = MiniGUI
scriptframe.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
scriptframe.Position = UDim2.new(0, 103, 0, 29)
scriptframe.Size = UDim2.new(0, 313, 0, 449)
scriptframe.Style = Enum.FrameStyle.RobloxRound

TextButton.Parent = scriptframe
TextButton.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton.Position = UDim2.new(0, 157, 0, 99)
TextButton.Size = UDim2.new(0, 123, 0, 50)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "Geno Bendy"
TextButton.TextColor3 = Color3.new(0, 1, 1)
TextButton.TextScaled = true
TextButton.TextSize = 14
TextButton.TextWrapped = true

TextButton.MouseButton1Down:connect(function()
local p = game.Players.LocalPlayer
local char = p.Character
local mouse = p:GetMouse()
local larm = char["Left Arm"]
local rarm = char["Right Arm"]
local lleg = char["Left Leg"]
local rleg = char["Right Leg"]
local hed = char.Head
local torso = char.Torso
local hum = char.Humanoid
local cam = game.Workspace.CurrentCamera
local root = char.HumanoidRootPart
local deb = false
local shot = 0
local debris=game:service"Debris"
local l = game:GetService("Lighting")
local rs = game:GetService("RunService").RenderStepped
for i,v in pairs(char:children()) do
if v:IsA("Shirt") and v:IsA("Pants") and v:IsA("Hat") and v:IsA("Accessory") then
v:Remove()
end
end
shirt = Instance.new("Shirt", char)
shirt.Name = "Shirt"
pants = Instance.new("Pants", char)
pants.Name = "Pants"
char.Shirt.ShirtTemplate = "rbxassetid://716858027"
char.Pants.PantsTemplate = "rbxassetid://687438377"
local p = game.Players.LocalPlayer
local char = p.Character
local mouse = p:GetMouse()
local larm = char["Left Arm"]
local rarm = char["Right Arm"]
local lleg = char["Left Leg"]
local rleg = char["Right Leg"]
local hed = char.Head
local torso = char.Torso
local hum = char.Humanoid
local cam = game.Workspace.CurrentCamera
local root = char.HumanoidRootPart
local rj = root.RootJoint
local deb = false
local shot = 0
local stanceToggle = "Idle1"
local l = game:GetService("Lighting")
local rs = game:GetService("RunService").RenderStepped
local hb = game:GetService("RunService").Heartbeat
local Stepped = game:GetService("RunService").Stepped
hed.face.Texture = "rbxassetid://0"
eye2 = Instance.new("Part", workspace)
eye2.Anchored = false
eye2.Parent = hed
eye2.TopSurface = 0
eye2.BrickColor = BrickColor.new("Royal purple")
eye2.Material = "Neon"
eye2.BottomSurface = 0
eye2m = Instance.new("SpecialMesh", eye2)
eye2m.MeshId = "rbxassetid://862497341"
eye2m.TextureId = "rbxassetid://862497354"
eye2m.Scale = Vector3.new(0.05, 0.05, 0.05)
ogsize = eye2m.Scale
weld = Instance.new("Weld", hed)
weld.Part0 = eye2
weld.Part1 = hed
weld.Name = "eye2Weld"
weld.C1 = CFrame.new(0,.45,0.05)
local shir = Instance.new("Shirt",char)
local pan = Instance.new("Pants",char)
shir.ShirtTemplate = "http://www.roblox.com/asset/?id=870418443"
pan.PantsTemplate = "http://www.roblox.com/asset/?id=772824951"
spawn(function()
	while wait() do
		for i,v in pairs(char:GetChildren()) do
			if v:IsA('Part') then
				v.BrickColor = BrickColor.new("Really black")
			end
		end
	end
end)
--[[Psychopath's waifu
I think ck is going to send me in hell...
Genocider by grgrgry21.
Credit to CKbackup's and idk..
Edit by pika335 n stuff... it okay...
             B
          U     R
         N  I N  H
          E     L
             L
]]--
wait(1 / 60)
Effects = { }
local Player = game.Players.localPlayer
local Character = Player.Character
local Humanoid = Character.Humanoid
local Mouse = Player:GetMouse()
local LeftArm = Character["Left Arm"]
local RightArm = Character["Right Arm"]
local LeftLeg = Character["Left Leg"]
local RightLeg = Character["Right Leg"]
local Head = Character.Head
local Torso = Character.Torso
local Camera = game.Workspace.CurrentCamera
local RootPart = Character.HumanoidRootPart
local RootJoint = RootPart.RootJoint
local attack = false
local Anim = 'Idle'
local attacktype = 1
local delays = false
local play = true
local targetted = nil
local Torsovelocity = (RootPart.Velocity * Vector3.new(1, 0, 1)).magnitude 
local velocity = RootPart.Velocity.y
local sine = 0
local change = 1
local doe = 0
local Create = LoadLibrary("RbxUtility").Create
Humanoid.WalkSpeed = 8
local m = Create("Model"){
	Parent = Character,
	Name = "WeaponModel",
}

Humanoid.Animator.Parent = nil
Character.Animate.Parent = nil

local newMotor = function(part0, part1, c0, c1)
	local w = Create('Motor'){
		Parent = part0,
		Part0 = part0,
		Part1 = part1,
		C0 = c0,
		C1 = c1,
	}
	return w
end

function clerp(a, b, t)
	return a:lerp(b, t)
end

RootCF = CFrame.fromEulerAnglesXYZ(-1.57, 0, 3.14)
NeckCF = CFrame.new(0, 1, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)

local RW = newMotor(Torso, RightArm, CFrame.new(1.5, 0, 0), CFrame.new(0, 0, 0)) 
local LW = newMotor(Torso, LeftArm, CFrame.new(-1.5, 0, 0), CFrame.new(0, 0, 0))
local RH = newMotor(Torso, RightLeg, CFrame.new(.5, -2, 0), CFrame.new(0, 0, 0))
local LH = newMotor(Torso, LeftLeg, CFrame.new(-.5, -2, 0), CFrame.new(0, 0, 0))
RootJoint.C1 = CFrame.new(0, 0, 0)
RootJoint.C0 = CFrame.new(0, 0, 0)
Torso.Neck.C1 = CFrame.new(0, 0, 0)
Torso.Neck.C0 = CFrame.new(0, 1.5, 0)

local rarmc1 = RW.C1
local larmc1 = LW.C1
local rlegc1 = RH.C1
local llegc1 = LH.C1

local resetc1 = false

function PlayAnimationFromTable(table, speed, bool)
	RootJoint.C0 = clerp(RootJoint.C0, table[1], speed) 
	Torso.Neck.C0 = clerp(Torso.Neck.C0, table[2], speed) 
	RW.C0 = clerp(RW.C0, table[3], speed) 
	LW.C0 = clerp(LW.C0, table[4], speed) 
	RH.C0 = clerp(RH.C0, table[5], speed) 
	LH.C0 = clerp(LH.C0, table[6], speed) 
	if bool == true then
		if resetc1 == false then
			resetc1 = true
			RootJoint.C1 = RootJoint.C1
			Torso.Neck.C1 = Torso.Neck.C1
			RW.C1 = rarmc1
			LW.C1 = larmc1
			RH.C1 = rlegc1
			LH.C1 = llegc1
		end
	end
end

ArtificialHB = Create("BindableEvent", script){
	Parent = script,
	Name = "Heartbeat",
}

script:WaitForChild("Heartbeat")

frame = 1 / 30
tf = 0
allowframeloss = false
tossremainder = false
lastframe = tick()
script.Heartbeat:Fire()

game:GetService("RunService").Heartbeat:connect(function(s, p)
	tf = tf + s
	if tf >= frame then
		if allowframeloss then
			script.Heartbeat:Fire()
			lastframe = tick()
		else
			for i = 1, math.floor(tf / frame) do
				script.Heartbeat:Fire()
			end
			lastframe = tick()
		end
		if tossremainder then
			tf = 0
		else
			tf = tf - frame * math.floor(tf / frame)
		end
	end
end)

function swait(num)
	if num == 0 or num == nil then
		ArtificialHB.Event:wait()
	else
		for i = 0, num do
			ArtificialHB.Event:wait()
		end
	end
end

function RemoveOutlines(part)
	part.TopSurface, part.BottomSurface, part.LeftSurface, part.RightSurface, part.FrontSurface, part.BackSurface = 10, 10, 10, 10, 10, 10
end
	
CFuncs = {	
	["Part"] = {
		Create = function(Parent, Material, Reflectance, Transparency, BColor, Name, Size)
			local Part = Create("Part"){
				Parent = Parent,
				Reflectance = Reflectance,
				Transparency = Transparency,
				CanCollide = false,
				Locked = true,
				BrickColor = BrickColor.new(tostring(BColor)),
				Name = Name,
				Size = Size,
				Material = Material,
			}
			RemoveOutlines(Part)
			return Part
		end;
	};
	
	["Mesh"] = {
		Create = function(Mesh, Part, MeshType, MeshId, OffSet, Scale)
			local Msh = Create(Mesh){
				Parent = Part,
				Offset = OffSet,
				Scale = Scale,
			}
			if Mesh == "SpecialMesh" then
				Msh.MeshType = MeshType
				Msh.MeshId = MeshId
			end
			return Msh
		end;
	};
	
	["Mesh"] = {
		Create = function(Mesh, Part, MeshType, MeshId, OffSet, Scale)
			local Msh = Create(Mesh){
				Parent = Part,
				Offset = OffSet,
				Scale = Scale,
			}
			if Mesh == "SpecialMesh" then
				Msh.MeshType = MeshType
				Msh.MeshId = MeshId
			end
			return Msh
		end;
	};
	
	["Weld"] = {
		Create = function(Parent, Part0, Part1, C0, C1)
			local Weld = Create("Weld"){
				Parent = Parent,
				Part0 = Part0,
				Part1 = Part1,
				C0 = C0,
				C1 = C1,
			}
			return Weld
		end;
	};

	["Sound"] = {
		Create = function(id, par, vol, pit) 
			coroutine.resume(coroutine.create(function()
				local S = Create("Sound"){
					Volume = vol,
					Pitch = pit or 1,
					SoundId = id,
					Parent = par or workspace,
				}
				wait() 
				S:play() 
				game:GetService("Debris"):AddItem(S, 6)
			end))
		end;
	};
	
	["ParticleEmitter"] = {
		Create = function(Parent, Color1, Color2, LightEmission, Size, Texture, Transparency, ZOffset, Accel, Drag, LockedToPart, VelocityInheritance, EmissionDirection, Enabled, LifeTime, Rate, Rotation, RotSpeed, Speed, VelocitySpread)
			local fp = Create("ParticleEmitter"){
				Parent = Parent,
				Color = ColorSequence.new(Color1, Color2),
				LightEmission = LightEmission,
				Size = Size,
				Texture = Texture,
				Transparency = Transparency,
				ZOffset = ZOffset,
				Acceleration = Accel,
				Drag = Drag,
				LockedToPart = LockedToPart,
				VelocityInheritance = VelocityInheritance,
				EmissionDirection = EmissionDirection,
				Enabled = Enabled,
				Lifetime = LifeTime,
				Rate = Rate,
				Rotation = Rotation,
				RotSpeed = RotSpeed,
				Speed = Speed,
				VelocitySpread = VelocitySpread,
			}
			return fp
		end;
	};

	CreateTemplate = {
	
	};
}



New = function(Object, Parent, Name, Data)
	local Object = Instance.new(Object)
	for Index, Value in pairs(Data or {}) do
		Object[Index] = Value
	end
	Object.Parent = Parent
	Object.Name = Name
	return Object
end
	

ShadowHead = New("Part",Character,"ShadowHead",{CanCollide = false,BrickColor = BrickColor.new("Really black"),Size = Vector3.new(1.20000005, 0.600000024, 1),CFrame = CFrame.new(68.5999985, 0.700013041, 9.89999962, 1, 0, 0, 0, 1, 0, 0, 0, 1),Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",ShadowHead,"Mesh",{Scale = Vector3.new(1.25999999, 1.5, 1.25999999),})
Weld = New("Weld",ShadowHead,"mot",{Part0 = ShadowHead,Part1 = Character.Head,C1 = CFrame.new(0, 0.200000048, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),})

Handle = New("Part",m,"Handle",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Transparency = 1,Transparency = 1,Size = Vector3.new(1.78105354, 1.21267569, 0.446083069),CFrame = CFrame.new(3.48884702, 1.89424598, -23.6011944, 0.0172098875, -7.30156898e-07, 0.999851942, 0.999853492, 1.19907781e-08, -0.0172098596, -1.80598714e-09, 1.00000083, 1.4975667e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(6,0,0),})
moter = New("Weld",Handle,"mot",{Part0 = RightArm,Part1 = Handle,})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(3.46324158, 2.55061626, -23.0996056, 0.0172099378, 1.26508749e-05, 0.999852061, 0.999856234, 0.000737910799, -0.0172098614, -0.000738026109, 1.00000215, 2.29468287e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("BlockMesh",Part,"Mesh",{Scale = Vector3.new(0.492160469, 0.24608025, 0.123040132),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098838, 0.999853015, -0.000738022442, 1.18836761e-05, 0.000737924012, 1.00000048, 0.999851942, -0.0172098614, 1.52736902e-06),C1 = CFrame.new(0.655831456, 0.501588821, -0.0368974209, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Shape = Enum.PartType.Cylinder,Size = Vector3.new(0.200000003, 0.270688266, 0.270688266),CFrame = CFrame.new(3.47537327, 1.11045444, -23.2953625, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Part,"Mesh",{Scale = Vector3.new(0.123040125, 1, 1),MeshType = Enum.MeshType.Cylinder,})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.783906102, 0.305831909, 1.74045563e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(1.47648132, 0.221472263, 0.344512314),CFrame = CFrame.new(3.48828244, 1.86040294, -23.3093491, 0.0172099452, 3.70001203e-08, 0.999852061, 0.99985671, -3.59708352e-09, -0.0172098596, -4.18887769e-09, 1.0000025, 2.26488032e-06),BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("BlockMesh",Part,"Mesh",{Scale = Vector3.new(1, 1.00999999, 1),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),C1 = CFrame.new(-0.0338476896, 0.291845322, 1.8119812e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.98432076, 0.200000003, 0.24608022),CFrame = CFrame.new(3.48404813, 1.61474013, -23.4433804, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("BlockMesh",Part,"Mesh",{Scale = Vector3.new(1, 0.246080264, 1),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.279546618, 0.157814026, 1.21593475e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Shape = Enum.PartType.Cylinder,Size = Vector3.new(0.984321058, 0.200000003, 0.200000003),CFrame = CFrame.new(3.36101127, 1.61687815, -23.4187717, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Part,"Mesh",{Scale = Vector3.new(1, 0.492160618, 0.492160439),MeshType = Enum.MeshType.Cylinder,})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.279526353, 0.182422638, -0.123043299, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(3.53706741, 2.54934502, -23.0996056, 0.0172099378, 1.26508749e-05, 0.999852061, 0.999856234, 0.000737910799, -0.0172098614, -0.000738026109, 1.00000215, 2.29468287e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("BlockMesh",Part,"Mesh",{Scale = Vector3.new(0.492160469, 0.246080235, 0.123040132),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098838, 0.999853015, -0.000738022442, 1.18836761e-05, 0.000737924012, 1.00000048, 0.999851942, -0.0172098614, 1.52736902e-06),C1 = CFrame.new(0.655830979, 0.501588821, 0.0369393826, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(1.47648132, 0.200000003, 0.200000003),CFrame = CFrame.new(3.48828554, 1.86097884, -23.1606178, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("BlockMesh",Part,"Mesh",{Scale = Vector3.new(1, 0.369120389, 0.7382406),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.0332717896, 0.440576553, 1.14440918e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Partss = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Shape = Enum.PartType.Cylinder,Size = Vector3.new(0.200000003, 0.221472204, 0.221472189),CFrame = CFrame.new(3.47526526, 1.10428262, -23.2953568, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(.0, 0, 0),})
Mesh = New("SpecialMesh",Partss,"Mesh",{Scale = Vector3.new(0.123040125, 1, 1),MeshType = Enum.MeshType.Cylinder,})
mot = New("Weld",Partss,"mot",{Part0 = Partss,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.790078878, 0.305837631, 1.57356262e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(3.49040294, 1.9837563, -23.5174713, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Part,"Mesh",{Scale = Vector3.new(0.615200579, 0.36912033, 0.24608025),MeshId = "http://www.roblox.com/asset/?id=3270017",MeshType = Enum.MeshType.FileMesh,})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(0.0895236731, 0.0837230682, 1.52587891e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.295296252, 0.738240778, 0.369120389),CFrame = CFrame.new(3.49802279, 2.42631888, -23.8138046, 0.0172099452, 3.70001203e-08, 0.999852061, 0.99985671, -3.59708352e-09, -0.0172098596, -4.18887769e-09, 1.0000025, 2.26488032e-06),BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(.0, 0, 0),})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),C1 = CFrame.new(0.532151103, -0.212610245, 1.74045563e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.344512314, 0.78745681, 0.344512314),CFrame = CFrame.new(3.49802279, 2.42631888, -23.8138046, 0.0172099452, 3.70001203e-08, 0.999852061, 0.99985671, -3.59708352e-09, -0.0172098596, -4.18887769e-09, 1.0000025, 2.26488032e-06),BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),C1 = CFrame.new(0.532151103, -0.212610245, 1.74045563e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Part = New("Part",m,"Part",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Shape = Enum.PartType.Cylinder,Size = Vector3.new(0.984321058, 0.200000003, 0.200000003),CFrame = CFrame.new(3.60706425, 1.61264217, -23.4187698, 0.0172099359, 1.26359728e-05, 0.999851942, 0.999856234, 0.000738034665, -0.0172098596, -0.000738148578, 1.00000226, 2.36918868e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Part,"Mesh",{Scale = Vector3.new(1, 0.492160618, 0.492160439),MeshType = Enum.MeshType.Cylinder,})
mot = New("Weld",Part,"mot",{Part0 = Part,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098819, 0.999853015, -0.00073814491, 1.18687749e-05, 0.000738047936, 1.0000006, 0.999851882, -0.0172098596, 1.60187483e-06),C1 = CFrame.new(-0.279527187, 0.182424545, 0.12304616, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(3.47672749, 1.18911982, -23.1232109, 0.999851942, 0.00638213893, 0.0159827713, -0.0172098316, 0.37065956, 0.928613782, 4.44045327e-06, -0.928749561, 0.370713741),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(0.24608025, 0.246080264, 0.615200639),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.999851882, -0.0172098316, 3.67313623e-06, 0.00638283044, 0.370658338, -0.928748012, 0.0159824342, 0.928610861, 0.370713145),C1 = CFrame.new(-0.705229163, 0.477983475, 1.76429749e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.344512254, 0.787456751, 0.200000003),CFrame = CFrame.new(3.50247502, 2.68478155, -23.8132839, 0.999851942, 1.0713723e-05, -0.0172099732, -0.0172098912, 0.000738376984, -0.999856234, 4.21693585e-06, 1.00000226, 0.000738456321),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 1, 0.861280859),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.999851882, -0.0172098912, 3.44961882e-06, 9.9465251e-06, 0.000738390256, 1.0000006, -0.0172099192, -0.999853015, 0.000738452654),C1 = CFrame.new(0.790651679, -0.212089539, 2.07424164e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(3.4904809, 1.98827124, -23.5162678, -0.999852061, -0.0148990965, 0.00861407723, 0.0172099397, -0.865535975, 0.500560343, -4.36594746e-06, 0.500633478, 0.865662456),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(0.24608025, 0.369120389, 0.861280918),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, -0.999851942, 0.0172099397, -3.59863043e-06, -0.0148994327, -0.865533173, 0.500632644, 0.00861338526, 0.500558794, 0.865661025),C1 = CFrame.new(0.0940393209, 0.0849266052, 1.54972076e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.442944348, 0.200000003, 0.200000003),CFrame = CFrame.new(3.37415838, 2.37982368, -23.1609974, 0.0172098633, 1.48413446e-05, 0.999851882, 0.999856234, 0.0007376945, -0.0172097869, -0.000737846654, 1.00000215, 7.44058752e-08),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 0.369120389, 0.492160529),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098093, 0.999853015, -0.000737842987, 1.40741467e-05, 0.000737707771, 1.00000048, 0.999851823, -0.0172097888, -6.92903996e-07),C1 = CFrame.new(0.483531356, 0.440196991, -0.12302804, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.61520052, 0.200000003, 0.200000003),CFrame = CFrame.new(3.35783243, 1.43252242, -23.1602993, 0.0172098633, 1.48413446e-05, 0.999851882, 0.999856234, 0.0007376945, -0.0172097869, -0.000737846654, 1.00000215, 7.44058752e-08),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 0.369120389, 0.492160529),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.0172098093, 0.999853015, -0.000737842987, 1.40741467e-05, 0.000737707771, 1.00000048, 0.999851823, -0.0172097888, -6.92903996e-07),C1 = CFrame.new(-0.463909149, 0.440895081, -0.123048544, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(1.47648132, 0.200000003, 0.200000003),CFrame = CFrame.new(3.61130548, 1.85886192, -23.160614, -0.0172098689, 1.04156998e-05, -0.99985218, -0.999856234, 0.000738191127, 0.0172097925, 0.000738266157, 1.00000238, -4.55221243e-06),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 0.369120389, 0.492160529),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, -0.0172098149, -0.999853075, 0.00073826249, 9.64850187e-06, 0.00073820434, 1.00000072, -0.999852121, 0.0172097944, -3.78489494e-06),C1 = CFrame.new(-0.0332713127, 0.440580368, 0.123049498, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.36912033, 0.738240778, 0.200000003),CFrame = CFrame.new(3.50183868, 2.64789343, -23.8132629, 0.999851942, 1.0818032e-05, -0.017209895, -0.0172098186, 0.000737608876, -0.999856234, 4.13497901e-06, 1.00000238, 0.000737691764),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(.0, 0, 0),})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 1, 0.738240719),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.999851882, -0.0172098186, 3.36766243e-06, 1.00508332e-05, 0.000737622147, 1.00000072, -0.0172098409, -0.999853015, 0.000737688097),C1 = CFrame.new(0.753758311, -0.212068558, 1.93119049e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.344512254, 0.787456751, 0.200000003),CFrame = CFrame.new(3.49357963, 2.16808391, -23.8129005, 0.999852061, -1.05647114e-05, 0.0172100067, -0.0172099303, -0.000737611321, 0.999856114, 4.36594746e-06, -1.00000226, -0.000737689785),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 1, 0.861280859),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.999851942, -0.0172099303, 3.59863043e-06, -9.79751348e-06, -0.000737624592, -1.0000006, 0.0172099527, 0.999852955, -0.000737686118),C1 = CFrame.new(0.273878455, -0.211706161, 1.90734863e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})
Wedge = New("WedgePart",m,"Wedge",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Size = Vector3.new(0.36912033, 0.738240659, 0.200000003),CFrame = CFrame.new(3.49420977, 2.20497489, -23.8129292, 0.999852061, -1.05647114e-05, 0.0172100067, -0.0172099303, -0.000737611321, 0.999856114, 4.36594746e-06, -1.00000226, -0.000737689785),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(.0, 0, 0),})
Mesh = New("SpecialMesh",Wedge,"Mesh",{Scale = Vector3.new(1, 1, 0.738240719),MeshType = Enum.MeshType.Wedge,})
mot = New("Weld",Wedge,"mot",{Part0 = Wedge,Part1 = Handle,C0 = CFrame.new(0, 0, 0, 0.999851942, -0.0172099303, 3.59863043e-06, -9.79751348e-06, -0.000737624592, -1.0000006, 0.0172099527, 0.999852955, -0.000737686118),C1 = CFrame.new(0.310774684, -0.211734772, 1.43051147e-05, 0.0172098875, 0.999853492, -1.80598714e-09, -7.30156898e-07, 1.19907781e-08, 1.00000083, 0.999851942, -0.0172098596, 1.4975667e-06),})

for _,v in pairs(m:children()) do
if v:IsA("Part") then
v.CanCollide = false
end
end
if Character.Name == "grgrgry21" or Character.Name == "Player1" then
for _,v in pairs(Character:children()) do
if v:IsA("Accessory") then
v:Remove()
end
end	
Handle = New("Part",m,"Handle",{CanCollide = false,BrickColor = BrickColor.new("Really black"),FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 1, 1),CFrame = CFrame.new(-27.3000507, 4.79990387, 28.10005, 4.49431016e-21, -6.79974523e-22, -1, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, 4.49431016e-21),CanCollide = false,BottomSurface = Enum.SurfaceType.Smooth,TopSurface = Enum.SurfaceType.Smooth,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",Handle,"Mesh",{Offset = Vector3.new(0, 0.100000001, 0),MeshId = "http://www.roblox.com/asset/?id=62246019",MeshType = Enum.MeshType.FileMesh,})
Decal = New("Decal",Handle,"Decal",{Face = Enum.NormalId.Top,Texture = "http://www.roblox.com/asset/?id=146022204",})
mot = New("Motor",Handle,"mot",{Part0 = Handle,Part1 = Head,C0 = CFrame.new(0, 0, 0, 4.49431016e-21, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, -1, -6.79974523e-22, 4.49431016e-21),C1 = CFrame.new(-0.100000381, 0.0999999046, 0.200000763, 4.49431016e-21, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, -1, -6.79974523e-22, 4.49431016e-21),})
Handle1 = New("Part",m,"Handle1",{CanCollide = false,BrickColor = BrickColor.new("Bright red"),FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 1, 1),CFrame = CFrame.new(-27.3000507, 4.79990387, 28.10005, 4.49431016e-21, -6.79974523e-22, -1, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, 4.49431016e-21),BottomSurface = Enum.SurfaceType.Smooth,TopSurface = Enum.SurfaceType.Smooth,Color = Color3.new(0.768628, 0.156863, 0.109804),})
Mesh = New("SpecialMesh",Handle1,"Mesh",{Offset = Vector3.new(0, 0.100000001, 0),Scale = Vector3.new(0.949999988, 0.949999988, 0.949999988),MeshId = "http://www.roblox.com/asset/?id=62246019",MeshType = Enum.MeshType.FileMesh,})
mot = New("Motor",Handle1,"mot",{Part0 = Handle1,Part1 = Head,C0 = CFrame.new(0, 0, 0, 4.49431016e-21, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, -1, -6.79974523e-22, 4.49431016e-21),C1 = CFrame.new(-0.100000381, 0.0999999046, 0.200000763, 4.49431016e-21, 4.72251821e-22, 1, -6.79974523e-22, 1, -4.72251821e-22, -1, -6.79974523e-22, 4.49431016e-21),})
end


function rayCast(Position, Direction, Range, Ignore)
	return game:service("Workspace"):FindPartOnRay(Ray.new(Position, Direction.unit * (Range or 999.999)), Ignore) 
end 

--[[FindNearestTorso = function(pos)
	local list = (game.Workspace:children())
	local torso = nil
	local dist = 1000
	local temp, human, temp2 = nil, nil, nil
	for x = 1, #list do
		temp2 = list[x]
		if temp2.className == "Model" and temp2.Name ~= Character.Name then
			temp = temp2:findFirstChild("Torso")
			human = temp2:findFirstChild("Humanoid")
			if temp ~= nil and human ~= nil and human.Health > 0 and (temp.Position - pos).magnitude < dist then
				local dohit = true
				if dohit == true then
					torso = temp
					dist = (temp.Position - pos).magnitude
				end
			end
		end
	end
	return torso, dist
end]]
function FindNearestTorso(Position, Distance, SinglePlayer)
	if SinglePlayer then
		return (SinglePlayer.Torso.CFrame.p - Position).magnitude < Distance
	end
	local List = {}
	for i, v in pairs(workspace:GetChildren()) do
		if v:IsA("Model") then
			if v:findFirstChild("Torso") then
				if v ~= Character then
					if (v.Torso.Position - Position).magnitude <= Distance then
						table.insert(List, v)
					end 
				end 
			end 
		end 
	end
	return List
end
function Damage(Part, hit, minim, maxim, knockback, Type, Property, Delay, HitSound, HitPitch)
	if hit.Parent == nil then
		return
	end
	local h = hit.Parent:FindFirstChild("Humanoid")
	for _, v in pairs(hit.Parent:children()) do
		if v:IsA("Humanoid") then
			h = v
		end
	end
	if h ~= nil and hit.Parent.Name ~= Character.Name and hit.Parent:FindFirstChild("Torso") ~= nil then
		if hit.Parent:findFirstChild("DebounceHit") ~= nil then
			if hit.Parent.DebounceHit.Value == true then
				return
			end
		end
		local c = Create("ObjectValue"){
			Name = "creator",
			Value = game:service("Players").LocalPlayer,
			Parent = h,
		}
		game:GetService("Debris"):AddItem(c, .5)
		if HitSound ~= nil and HitPitch ~= nil then
			CFuncs.Sound.Create(HitSound, hit, 1, HitPitch) 
		end
		local Damage = math.random(minim, maxim)
		local blocked = false
		local block = hit.Parent:findFirstChild("Block")
		if block ~= nil then
			if block.className == "IntValue" then
				if block.Value > 0 then
					blocked = true
					block.Value = block.Value - 1
					print(block.Value)
				end
			end
		end
		if blocked == false then
			h.Health = h.Health - Damage
			ShowDamage((Part.CFrame * CFrame.new(0, 0, (Part.Size.Z / 2)).p + Vector3.new(0, 1.5, 0)), -Damage, 1.5, BrickColor.new("Really black").Color)
		else
			h.Health = h.Health - (Damage / 2)
			ShowDamage((Part.CFrame * CFrame.new(0, 0, (Part.Size.Z / 2)).p + Vector3.new(0, 1.5, 0)), -Damage, 1.5, BrickColor.new("Really black").Color)
		end
		if Type == "Knockdown" then
			local hum = hit.Parent.Humanoid
			hum.PlatformStand = true
			coroutine.resume(coroutine.create(function(HHumanoid)
				swait(1)
				HHumanoid.PlatformStand = false
			end), hum)
			local angle = (hit.Position - (Property.Position + Vector3.new(0, 0, 0))).unit
			local bodvol = Create("BodyVelocity"){
				velocity = angle * knockback,
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			local rl = Create("BodyAngularVelocity"){
				P = 3000,
				maxTorque = Vector3.new(500000, 500000, 500000) * 50000000000000,
				angularvelocity = Vector3.new(math.random(-10, 10), math.random(-10, 10), math.random(-10, 10)),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodvol, .5)
			game:GetService("Debris"):AddItem(rl, .5)
		elseif Type == "Normal" then
			local vp = Create("BodyVelocity"){
				P = 500,
				maxForce = Vector3.new(math.huge, 0, math.huge),
				velocity = Property.CFrame.lookVector * knockback + Property.Velocity / 1.05,
			}
			if knockback > 0 then
				vp.Parent = hit.Parent.Torso
			end
			game:GetService("Debris"):AddItem(vp, .5)
		elseif Type == "Up" then
			local bodyVelocity = Create("BodyVelocity"){
				velocity = Vector3.new(0, 20, 0),
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodyVelocity, .5)
		elseif Type == "DarkUp" then
			coroutine.resume(coroutine.create(function()
				for i = 0, 1, 0.1 do
					swait()
					Effects.Block.Create(BrickColor.new("Black"), hit.Parent.Torso.CFrame, 5, 5, 5, 1, 1, 1, .08, 1)
				end
			end))
			local bodyVelocity = Create("BodyVelocity"){
				velocity = Vector3.new(0, 20, 0),
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodyVelocity, 1)
		elseif Type == "Snare" then
			local bp = Create("BodyPosition"){
				P = 2000,
				D = 100,
				maxForce = Vector3.new(math.huge, math.huge, math.huge),
				position = hit.Parent.Torso.Position,
				Parent = hit.Parent.Torso,
			}
			game:GetService("Debris"):AddItem(bp, 1)
		elseif Type == "Freeze" then
			local BodPos = Create("BodyPosition"){
				P = 50000,
				D = 1000,
				maxForce = Vector3.new(math.huge, math.huge, math.huge),
				position = hit.Parent.Torso.Position,
				Parent = hit.Parent.Torso,
			}
			local BodGy = Create("BodyGyro") {
				maxTorque = Vector3.new(4e+005, 4e+005, 4e+005) * math.huge ,
				P = 20e+003,
				Parent = hit.Parent.Torso,
				cframe = hit.Parent.Torso.CFrame,
			}
			hit.Parent.Torso.Anchored = true
			coroutine.resume(coroutine.create(function(Part) 
				swait(1.5)
				Part.Anchored = false
			end), hit.Parent.Torso)
			game:GetService("Debris"):AddItem(BodPos, 3)
			game:GetService("Debris"):AddItem(BodGy, 3)
		end
		local debounce = Create("BoolValue"){
			Name = "DebounceHit",
			Parent = hit.Parent,
			Value = true,
		}
		game:GetService("Debris"):AddItem(debounce, Delay)
		c = Create("ObjectValue"){
			Name = "creator",
			Value = Player,
			Parent = h,
		}
		game:GetService("Debris"):AddItem(c, .5)
	end
end

function ShowDamage(Pos, Text, Time, Color)
	local Rate = (1 / 30)
	local Pos = (Pos or Vector3.new(0, 0, 0))
	local Text = (Text or "")
	local Time = (Time or 2)
	local Color = (Color or Color3.new(1, 0, 1))
	local EffectPart = CFuncs.Part.Create(workspace, "SmoothPlastic", 0, 1, BrickColor.new(Color), "Effect", Vector3.new(0, 0, 0))
	EffectPart.Anchored = true
	local BillboardGui = Create("BillboardGui"){
		Size = UDim2.new(3, 0, 3, 0),
		Adornee = EffectPart,
		Parent = EffectPart,
	}
	local TextLabel = Create("TextLabel"){
		BackgroundTransparency = 1,
		Size = UDim2.new(1, 0, 1, 0),
		Text = Text,
		Font = "SciFi",
		TextColor3 = Color,
		TextScaled = true,
		Parent = BillboardGui,
	}
	game.Debris:AddItem(EffectPart, (Time))
	EffectPart.Parent = game:GetService("Workspace")
	delay(0, function()
		local Frames = (Time / Rate)
		for Frame = 1, Frames do
			wait(Rate)
			local Percent = (Frame / Frames)
			EffectPart.CFrame = CFrame.new(Pos) + Vector3.new(0, Percent, 0)
			TextLabel.TextTransparency = Percent
		end
		if EffectPart and EffectPart.Parent then
			EffectPart:Destroy()
		end
	end)
end

function dmg(dude)
if dude.Name ~= Character then
dude.Humanoid.PlatformStand = true
local bgf = Instance.new("BodyGyro",dude.Head)
bgf.CFrame = bgf.CFrame * CFrame.fromEulerAnglesXYZ(math.rad(-90),0,0)
local val = Instance.new("BoolValue",dude)
val.Name = "IsHit"
for i = 1, 6 do
local blo = Instance.new("Part",game.Workspace)
blo.Size = Vector3.new(.6,.2,.6)
blo.Material = "SmoothPlastic"
blo.BrickColor = BrickColor.new("Crimson")
--blo.Position = dude.Head.Position
blo.CFrame = dude.Head.CFrame
game:GetService("Debris"):AddItem(blo,30)
end
local ds = coroutine.wrap(function()
wait(.2)
dude.Torso:BreakJoints()
end)
ds()
end
end

function mdmg(Part, Magnitude)--, MinimumDamage, MaximumDamage, KnockBack, Type, HitSound, HitPitch)
    --local buddy
	for _, c in pairs(workspace:children()) do
		local hum = c:findFirstChild("Humanoid")
		if hum ~= nil then
			local head = c:findFirstChild("Torso")
			if head ~= nil then
				local targ = head.Position - Part.Position
				local mag = targ.magnitude
				if mag <= Magnitude and c.Name ~= Player.Name then 
				if c.Name ~= Character then
				if c.Name ~= "CKbackup" then
			local asd = Instance.new("ParticleEmitter",c.Torso)
			asd.Color = ColorSequence.new(Color3.new(1, 0, 0), Color3.new(.5, 0, 0))
			asd.LightEmission = .1
			asd.Size = NumberSequence.new(0.2)
			asd.Texture = "http://www.roblox.com/asset/?ID=771221224"
			aaa = NumberSequence.new({NumberSequenceKeypoint.new(0, 0.2),NumberSequenceKeypoint.new(1, 5)})
			bbb = NumberSequence.new({NumberSequenceKeypoint.new(0, 1),NumberSequenceKeypoint.new(0.0636, 0), NumberSequenceKeypoint.new(1, 1)})
			asd.Transparency = bbb
			asd.Size = aaa
			asd.ZOffset = .9
			asd.Acceleration = Vector3.new(0, -5, 0)
			asd.LockedToPart = false
			asd.EmissionDirection = "Back"
			asd.Lifetime = NumberRange.new(1, 2)
			asd.Rate = 1000
			asd.Rotation = NumberRange.new(-100, 100)
			asd.RotSpeed = NumberRange.new(-100, 100)
			asd.Speed = NumberRange.new(6)
			asd.VelocitySpread = 10000
			asd.Enabled=true
					--Damage(head, head, MinimumDamage, MaximumDamage, KnockBack, Type, RootPart, .1, "rbxassetid://" .. HitSound, HitPitch)
					dmg(c)
					CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=206082273", c.Torso, 1.2, .8)
					coroutine.wrap(function()
					wait(.2)
					asd.Enabled = false
					wait(2)
					asd:Remove()
					end)()
				       else
        CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=240429289", c.Torso, 1.5, math.random(1,1.3))		
        Effects.Sphere.Create(BrickColor.new("Bright red"), c.Torso.CFrame, 30, 30, 30, .5, .5, .5, 0.04)

					end
				end
			end
		end
	end
	end
end
EffectModel = Create("Model"){
	Parent = Character,
	Name = "Effects",
}

Effects = {
	Block = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay, Type)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("BlockMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			if Type == 1 or Type == nil then
				table.insert(Effects, {
					prt,
					"Block1",
					delay,
					x3,
					y3,
					z3,
					msh
				})
			elseif Type == 2 then
				table.insert(Effects, {
					prt,
					"Block2",
					delay,
					x3,
					y3,
					z3,
					msh
				})
			end
		end;
	};

		Cylinder = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("CylinderMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Cylinder",
				delay,
				x3,
				y3,
				z3,
				msh
			})
		end;
	};
	Head = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
			local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "Head", "nil", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Cylinder",
				delay,
				x3,
				y3,
				z3,
				msh
			})
		end;
	};
	
	Sphere = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "Sphere", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Cylinder",
				delay,
				x3,
				y3,
				z3,
				msh
			})
		end;
	};
	
	Elect = {
		Create = function(cff, x, y, z)
			local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, BrickColor.new("Lime green"), "Part", Vector3.new(1, 1, 1))
			prt.Anchored = true
			prt.CFrame = cff * CFrame.new(math.random(-x, x), math.random(-y, y), math.random(-z, z))
			prt.CFrame = CFrame.new(prt.Position)
			game:GetService("Debris"):AddItem(prt, 2)
			local xval = math.random() / 2
			local yval = math.random() / 2
			local zval = math.random() / 2
			local msh = CFuncs.Mesh.Create("BlockMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(xval, yval, zval))
			table.insert(Effects, {
				prt,
				"Elec",
				0.1,
				x,
				y,
				z,
				xval,
				yval,
				zval
			})
		end;

	};
	
	Ring = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://3270017", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Cylinder",
				delay,
				x3,
				y3,
				z3,
				msh
			})
		end;
	};


	Wave = {
		Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://20329976", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Cylinder",
				delay,
				x3,
				y3,
				z3,
				msh
			})
		end;
	};

	Break = {
		Create = function(brickcolor, cframe, x1, y1, z1)
			local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new(0.5, 0.5, 0.5))
			prt.Anchored = true
			prt.CFrame = cframe * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
			local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "Sphere", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			local num = math.random(10, 50) / 1000
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Shatter",
				num,
				prt.CFrame,
				math.random() - math.random(),
				0,
				math.random(50, 100) / 100
			})
		end;
	};
	
	Fire = {
		Create = function(brickcolor, cframe, x1, y1, z1, delay)
			local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			msh = CFuncs.Mesh.Create("BlockMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"Fire",
				delay,
				1,
				1,
				1,
				msh
			})
		end;
	};
	
	FireWave = {
		Create = function(brickcolor, cframe, x1, y1, z1)
			local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 1, brickcolor, "Effect", Vector3.new())
			prt.Anchored = true
			prt.CFrame = cframe
			msh = CFuncs.Mesh.Create("BlockMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
			local d = Create("Decal"){
				Parent = prt,
				Texture = "rbxassetid://26356434",
				Face = "Top",
			}
			local d = Create("Decal"){
				Parent = prt,
				Texture = "rbxassetid://26356434",
				Face = "Bottom",
			}
			game:GetService("Debris"):AddItem(prt, 10)
			table.insert(Effects, {
				prt,
				"FireWave",
				1,
				30,
				math.random(400, 600) / 100,
				msh
			})
		end;
	};
	
	Lightning = {
		Create = function(p0, p1, tym, ofs, col, th, tra, last)
			local magz = (p0 - p1).magnitude
			local curpos = p0
			local trz = {
				-ofs,
				ofs
			}
			for i = 1, tym do
				local li = CFuncs.Part.Create(EffectModel, "Neon", 0, tra or 0.4, col, "Ref", Vector3.new(th, th, magz / tym))
				local ofz = Vector3.new(trz[math.random(1, 2)], trz[math.random(1, 2)], trz[math.random(1, 2)])
				local trolpos = CFrame.new(curpos, p1) * CFrame.new(0, 0, magz / tym).p + ofz
				li.Material = "Neon"
				if tym == i then
					local magz2 = (curpos - p1).magnitude
					li.Size = Vector3.new(th, th, magz2)
					li.CFrame = CFrame.new(curpos, p1) * CFrame.new(0, 0, -magz2 / 2)
					table.insert(Effects, {
						li,
						"Disappear",
						last
					})
				else
					do
						do
							li.CFrame = CFrame.new(curpos, trolpos) * CFrame.new(0, 0, magz / tym / 2)
							curpos = li.CFrame * CFrame.new(0, 0, magz / tym / 2).p
							game.Debris:AddItem(li, 10)
							table.insert(Effects, {
								li,
								"Disappear",
								last
							})
						end
					end
				end
			end
		end
	};

	EffectTemplate = {

	};
}

function chatfunc(text)
local chat = coroutine.wrap(function()
if Character:FindFirstChild("TalkingBillBoard")~= nil then
Character:FindFirstChild("TalkingBillBoard"):destroy()
end
local naeeym2 = Instance.new("BillboardGui",Character)
naeeym2.Size = UDim2.new(0,100,0,40)
naeeym2.StudsOffset = Vector3.new(0,3,0)
naeeym2.Adornee = Character.Head
naeeym2.Name = "TalkingBillBoard"
local tecks2 = Instance.new("TextLabel",naeeym2)
tecks2.BackgroundTransparency = 1
tecks2.BorderSizePixel = 0
tecks2.Text = ""
tecks2.Font = "Antique"
tecks2.TextSize = 38
tecks2.TextStrokeTransparency = 0
tecks2.TextColor3 = Color3.new(0,0,0)
tecks2.TextStrokeColor3 = Color3.new(0,0,0)
tecks2.Size = UDim2.new(1,0,0.5,0)
local tecks3 = Instance.new("TextLabel",naeeym2)
tecks3.BackgroundTransparency = 1
tecks3.BorderSizePixel = 0
tecks3.Text = ""
tecks3.Font = "Antique"
tecks3.TextSize = 38
tecks3.TextStrokeTransparency = 0
tecks3.TextColor3 = Color3.new(0,0,0)
tecks3.TextStrokeColor3 = Color3.new(0,0,0)
tecks3.Size = UDim2.new(1,0,0.5,0)
for i = 1,string.len(text),1 do
CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=365786623", Character, .6, .8)
tecks2.Text = string.sub(text,1,i)
tecks3.Text = string.sub(text,1,i)
wait(0.01)
end
wait(2)
for i = 1, 50 do
swait()
tecks2.Position = tecks2.Position - UDim2.new(math.random(-.4,.4),math.random(-5,5),.05,math.random(-5,5))
tecks2.Rotation = tecks2.Rotation - .8
tecks2.TextStrokeTransparency = tecks2.TextStrokeTransparency +.04
tecks2.TextTransparency = tecks2.TextTransparency + .04
tecks3.Position = tecks2.Position - UDim2.new(math.random(-.4,.4),math.random(-5,5),.05,math.random(-5,5))
tecks3.Rotation = tecks2.Rotation + .8
tecks3.TextStrokeTransparency = tecks2.TextStrokeTransparency +.04
tecks3.TextTransparency = tecks2.TextTransparency + .04
end
naeeym2:Destroy()
end)
chat()
end
function onChatted(msg)
chatfunc(msg)
end
Player.Chatted:connect(onChatted)

abss = Instance.new("BillboardGui",Character)
abss.Size = UDim2.new(10,0,10,0)
abss.Enabled = false
imgl = Instance.new("ImageLabel",abss)
imgl.Position = UDim2.new(0,0,0,0)
imgl.Size = UDim2.new(1,0,1,0)
imgl.Image = "rbxassetid://223123319"
imgl.ImageColor3 = Color3.new(0, 0, 255)
imgl.BackgroundTransparency = 1
imgf = Instance.new("ImageLabel",abss)
imgf.Position = UDim2.new(0,0,0,0)
imgf.Size = UDim2.new(1,0,1,0)
imgf.Image = "rbxassetid://418573253"
imgf.ImageColor3 = Color3.new(0, 0, 255)
imgf.BackgroundTransparency = 1
img2 = Instance.new("ImageLabel",abss)
img2.Position = UDim2.new(0,0,0,0)
img2.Size = UDim2.new(1,0,1,0)
img2.Image = "rbxassetid://223123319"
img2.ImageColor3 = Color3.new(0, 0, 255)
img2.BackgroundTransparency = 1
img3 = Instance.new("ImageLabel",abss)
img3.Position = UDim2.new(0,0,0,0)
img3.Size = UDim2.new(1,0,1,0)
img3.Image = "rbxassetid://418573253"
img3.ImageColor3 = Color3.new(0, 0, 255)
img3.BackgroundTransparency = 1

spawn(function()
chatfunc("B E N D Y")
wait(3)
chatfunc("Editted by pika335. Genocider by grgrgry21")
wait(3)
chatfunc("Make on 12/8/2017")
wait(3)
chatfunc("Fixer LuckZinHo and VictoriaChristophe :D")
wait(3)
chatfunc("Have Fun For My Script And Don't Leak it :D")
end)

function attackone()
	attack = true
	Humanoid.WalkSpeed = 0
	if targetted.Name ~= "CKbackup" then
			local partasdeff = Instance.new("ParticleEmitter",targetted.Torso)
			partasdeff.Color = ColorSequence.new(Color3.new(1, 0, 0), Color3.new(.5, 0, 0))
			partasdeff.LightEmission = .1
			partasdeff.Size = NumberSequence.new(0.2)
			partasdeff.Texture = "http://www.roblox.com/asset/?ID=771221224"
			aaa = NumberSequence.new({NumberSequenceKeypoint.new(0, 0.2),NumberSequenceKeypoint.new(1, 5)})
			bbb = NumberSequence.new({NumberSequenceKeypoint.new(0, 1),NumberSequenceKeypoint.new(0.0636, 0), NumberSequenceKeypoint.new(1, 1)})
			partasdeff.Transparency = bbb
			partasdeff.Size = aaa
			partasdeff.ZOffset = .9
			partasdeff.Acceleration = Vector3.new(0, -5, 0)
			partasdeff.LockedToPart = false
			partasdeff.EmissionDirection = "Back"
			partasdeff.Lifetime = NumberRange.new(1, 2)
			partasdeff.Rate = 1000
			partasdeff.Rotation = NumberRange.new(-100, 100)
			partasdeff.RotSpeed = NumberRange.new(-100, 100)
			partasdeff.Speed = NumberRange.new(6)
			partasdeff.VelocitySpread = 10000
			partasdeff.Enabled=false
	for i = 0, 3, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.0150662307, -4.88092428e-06, 0.0148906102, -0.01982099, -1.08002496e-12, 0.999803543, -4.46946984e-07, 1, -8.86181084e-09, -0.999803782, 3.27825546e-07, -0.0198209975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.00189219415, 1.50098944, -0.129972562, 0.0201512501, 0.0765038878, -0.996864021, 0.0566192083, 0.995383799, 0.0775336027, 0.998202145, -0.0580037907, 0.0157258138) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(2.01696348, 0.389823437, -0.060955409, -0.000397110358, -0.999624014, -0.0274192169, 0.00981300231, 0.0274140034, -0.999576092, 0.999951839, -0.0006660074, 0.00979842618) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.64040112, 0.216884568, 1.93210121e-06, 0.962137103, 0.272578239, -7.02217221e-07, -0.272574633, 0.962141275, -9.83368591e-06, -2.00979412e-06, 9.69739631e-06, 1) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.64369607, -1.98395038, 0.206737444, 0.19058302, -0.152998164, -0.969677031, 0.0664296299, 0.987527609, -0.142758414, 0.979424179, -0.0372077115, 0.198368743) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.641120076, -1.92643452, -0.0258421432, 0.848103583, 0.133398816, -0.51276207, -0.0662644878, 0.986892581, 0.147146463, 0.52567035, -0.0908175632, 0.845826566) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .1, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.011209704, -1.63770795, -0.318749219, -0.0172089972, -4.19956632e-06, -0.999852002, 0.999852061, 8.99471343e-06, -0.0172089972, 9.06549394e-06, -1.00000012, 4.04558159e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	Effects.Block.Create(BrickColor.new("Bright red"), Partss.CFrame, 2, 2, 2, 0.9, 0.9, 0.9, 0.05)
    Effects.Block.Create(BrickColor.new("Deep orange"), Partss.CFrame, 2, 2, 2, 0.5, 0.5, 0.5, 0.05)
    CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=136523485", Character, 5.5, .8)
    dmg(targetted)
    wait()
    chatfunc("Got you.")
    partasdeff.Enabled=true
	for i = 0, 1, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.0150662307, -4.88092428e-06, 0.0148906102, -0.01982099, -1.08002496e-12, 0.999803543, -4.46946984e-07, 1, -8.86181084e-09, -0.999803782, 3.27825546e-07, -0.0198209975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0879677385, 1.49240708, -0.127746791, 0.0201510563, -0.100440688, -0.994740784, 0.0566197298, 0.99346137, -0.0991647467, 0.998197258, -0.0543235913, 0.0257058665) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(2.03539443, 0.729742587, 0.0108130341, -0.00389442407, -0.967803538, 0.251676887, 0.0148300035, -0.251707017, -0.967689872, 0.999882519, -3.62247229e-05, 0.0153327845) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.64040112, 0.216884568, 1.93210121e-06, 0.962137103, 0.272578239, -7.02217221e-07, -0.272574633, 0.962141275, -9.83368591e-06, -2.00979412e-06, 9.69739631e-06, 1) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.64369607, -1.98395038, 0.206737444, 0.19058302, -0.152998164, -0.969677031, 0.0664296299, 0.987527609, -0.142758414, 0.979424179, -0.0372077115, 0.198368743) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.641120076, -1.92643452, -0.0258421432, 0.848103583, 0.133398816, -0.51276207, -0.0662644878, 0.986892581, 0.147146463, 0.52567035, -0.0908175632, 0.845826566) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0112083517, -1.63770616, -0.318746239, -0.0172079317, -2.87033617e-06, -0.999851942, 0.999852002, 8.28504562e-06, -0.0172079336, 8.27014446e-06, -1.00000012, 2.72750913e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	partasdeff.Enabled=false
	for i = 0, 2, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.0150662307, -4.88092428e-06, 0.0148906102, -0.01982099, -1.08002496e-12, 0.999803543, -4.46946984e-07, 1, -8.86181084e-09, -0.999803782, 3.27825546e-07, -0.0198209975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.00189219415, 1.50098944, -0.129972562, 0.0201512501, 0.0765038878, -0.996864021, 0.0566192083, 0.995383799, 0.0775336027, 0.998202145, -0.0580037907, 0.0157258138) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(2.01696348, 0.389823437, -0.060955409, -0.000397110358, -0.999624014, -0.0274192169, 0.00981300231, 0.0274140034, -0.999576092, 0.999951839, -0.0006660074, 0.00979842618) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.64040112, 0.216884568, 1.93210121e-06, 0.962137103, 0.272578239, -7.02217221e-07, -0.272574633, 0.962141275, -9.83368591e-06, -2.00979412e-06, 9.69739631e-06, 1) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.64369607, -1.98395038, 0.206737444, 0.19058302, -0.152998164, -0.969677031, 0.0664296299, 0.987527609, -0.142758414, 0.979424179, -0.0372077115, 0.198368743) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.641120076, -1.92643452, -0.0258421432, 0.848103583, 0.133398816, -0.51276207, -0.0662644878, 0.986892581, 0.147146463, 0.52567035, -0.0908175632, 0.845826566) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.011209704, -1.63770795, -0.318749219, -0.0172089972, -4.19956632e-06, -0.999852002, 0.999852061, 8.99471343e-06, -0.0172089972, 9.06549394e-06, -1.00000012, 4.04558159e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	coroutine.wrap(function()
	wait()
	partasdeff:Remove()
	end)()
	else
	sel = math.random(1,4)
	if sel == 1 then	
	chatfunc("...")
	elseif sel == 2 then	
	chatfunc("No...")
	elseif sel == 3 then
	chatfunc("I cant put him on ink...")
        elseif sel == 4 then
        chatfunc("What am I doing?")
	end
	for i = 0, 5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 0.999999881, 5.04870979e-29, -4.21790838e-43, 5.04870979e-29, 1, -5.04870979e-29, -4.21790838e-43, -5.04870979e-29, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.055980958, 1.49253583, -0.318915963, 0.999889553, 0.0107171191, -0.0102898544, -0.00218299939, 0.791040659, 0.611759722, 0.0146959936, -0.61166966, 0.790976703) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0- .4 * math.cos((sine) / 5), 0), 
         CFrame.new(1.54004693, 0.0494250022, 1.90734852e-06, 0.997847795, -0.0655719861, 0, 0.0655719936, 0.997847855, 7.53468894e-22, -4.94064563e-23, -7.51847299e-22, 0.99999994) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.51232088, 0.0410207808, -3.73942044e-06, 0.998558879, 0.053665854, -2.33806347e-07, -0.0536658242, 0.998558939, -1.04548817e-05, -3.27600219e-07, 1.04523697e-05, 0.99999994) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.540300906, -1.99793804, -2.11055158e-06, 0.998698354, -0.0510031469, 6.26438805e-07, 0.0510031544, 0.998698473, -1.04335422e-05, -9.34800966e-08, 1.04519122e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.539562821, -1.99794102, -5.75710146e-09, 0.998630941, 0.0523070693, -1.67712614e-07, -0.0523070768, 0.99863106, -1.0458818e-05, -3.79587107e-07, 1.04532719e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111967381, -1.6377008, -0.318754196, -0.0172117949, 0, -0.999851942, 0.999851942, 0, -0.0172117949, 0, -1, 0) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	end
	Humanoid.WalkSpeed = 10
	attack = false
end
local Grabbed = false

function hedshoot()
	attack = true

	--local GGyro = Instance.new("BodyPosition")
	local grab = nil
	for i, v in pairs(FindNearestTorso(Torso.CFrame.p, 10)) do
		if v:FindFirstChild('Torso') then
			Grabbed = true
			    CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=260430060", v.Torso, 1, .8)
			grab = v
		end
	end
    Effects.Wave.Create(BrickColor.new("White"), RootPart.CFrame * CFrame.Angles(0,math.rad(90),math.rad(90)), .5, .5, .5, 1, .2, 1, 0.07)
CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=200632211", RootPart, 1.5, .5)
		for i = 0, 1, 0.1 do
		swait()
		if Grabbed == true then
			grab.Humanoid.PlatformStand = true
			--GGyro.position = Partss.Position
			--GGyro.Parent = grab.Head
			grab.Torso.CFrame = Partss.CFrame * CFrame.Angles(0,math.rad(-90),0)
		end
		PlayAnimationFromTable({
         CFrame.new(0.104281992, -1.37529127e-22, -0.179345995, 0.249840975, 5.92156003e-22, 0.968286872, -5.57068883e-22, 1, -4.67813147e-22, -0.968286872, -4.22523594e-22, 0.249840975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.0029296279, 1.47845411, -0.120581962, 0.0750327855, 0.428286105, -0.900522709, 0.166523039, 0.885005891, 0.434781253, 0.983178616, -0.18258062, -0.00491504371) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.96751118, 0.433084905, -0.278422326, 0.305184275, -0.951701581, -0.033564698, 0.012345003, 0.0391969904, -0.999155343, 0.952213347, 0.304512084, 0.0237110667) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.66092706, 0.266950369, 2.51774691e-06, 0.876968205, 0.480548859, -2.5331974e-06, -0.480548888, 0.876968026, -7.03267551e-06, -1.13248825e-06, 7.38352537e-06, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.146832585, -1.7542398, 0.105335698, 0.266426086, 0.491796821, -0.828946948, 0.0135936746, 0.8580302, 0.513420045, 0.96375972, -0.148056909, 0.221916124) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.09110987, -1.74702656, 0.342675447, 0.765578806, 0.632523358, 0.117487431, -0.642276406, 0.740949869, 0.196148768, 0.0370163769, -0.225626737, 0.973510265) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		RootPart.Velocity = RootPart.CFrame.lookVector * 90
		
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111932121, -1.63769805, -0.318755955, -0.0172044784, -1.3951445e-05, -0.999852121, 0.999852002, 3.55020165e-06, -0.0172044784, 3.78862023e-06, -1.00000012, 1.38879986e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
		end
		if Grabbed == true then
		Humanoid.WalkSpeed = 0
		for i = 0, 2, 0.1 do
		swait()
		if Grabbed == true then
			grab.Humanoid.PlatformStand = true
			--GGyro.position = Partss.Position
			--GGyro.Parent = grab.Head
			grab.Torso.CFrame = Partss.CFrame * CFrame.Angles(0,math.rad(-90),0)
		end
		PlayAnimationFromTable({
         CFrame.new(0.104281992, -1.37529127e-22, -0.179345995, 0.249840975, 5.92156003e-22, 0.968286872, -5.57068883e-22, 1, -4.67813147e-22, -0.968286872, -4.22523594e-22, 0.249840975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.0029296279, 1.47845411, -0.120581962, 0.0750327855, 0.428286105, -0.900522709, 0.166523039, 0.885005891, 0.434781253, 0.983178616, -0.18258062, -0.00491504371) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.96751118, 0.433084905, -0.278422326, 0.305184275, -0.951701581, -0.033564698, 0.012345003, 0.0391969904, -0.999155343, 0.952213347, 0.304512084, 0.0237110667) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.58139038, 0.176945746, 5.27966768e-06, 0.939729631, 0.341920435, -3.69548798e-06, -0.341920793, 0.93972975, -6.50105221e-06, -5.81145287e-07, 6.40749931e-06, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.569345832, -1.89868093, -0.00942828506, 0.266425997, -0.0769406706, -0.960779786, 0.0135936281, 0.997010291, -0.0760724545, 0.963760078, 0.00720720552, 0.266675085) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.849354744, -2.01616573, 0.241646215, 0.948664129, 0.308412433, 0.0701368451, -0.312046438, 0.948832989, 0.0484089628, -0.0516182035, -0.0678096861, 0.996362925) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111932121, -1.63769805, -0.318755955, -0.0172044784, -1.3951445e-05, -0.999852121, 0.999852002, 3.55020165e-06, -0.0172044784, 3.78862023e-06, -1.00000012, 1.38879986e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
		end
		if grab.Name ~= "CKbackup" then
			local partasdeff = Instance.new("ParticleEmitter",grab.Torso)
			partasdeff.Color = ColorSequence.new(Color3.new(1, 0, 0), Color3.new(.5, 0, 0))
			partasdeff.LightEmission = .1
			partasdeff.Size = NumberSequence.new(0.2)
			partasdeff.Texture = "http://www.roblox.com/asset/?ID=771221224"
			aaa = NumberSequence.new({NumberSequenceKeypoint.new(0, 0.2),NumberSequenceKeypoint.new(1, 5)})
			bbb = NumberSequence.new({NumberSequenceKeypoint.new(0, 1),NumberSequenceKeypoint.new(0.0636, 0), NumberSequenceKeypoint.new(1, 1)})
			partasdeff.Transparency = bbb
			partasdeff.Size = aaa
			partasdeff.ZOffset = .9
			partasdeff.Acceleration = Vector3.new(0, -5, 0)
			partasdeff.LockedToPart = false
			partasdeff.EmissionDirection = "Back"
			partasdeff.Lifetime = NumberRange.new(1, 2)
			partasdeff.Rate = 1000
			partasdeff.Rotation = NumberRange.new(-100, 100)
			partasdeff.RotSpeed = NumberRange.new(-100, 100)
			partasdeff.Speed = NumberRange.new(10)
			partasdeff.VelocitySpread = 20
			partasdeff.Enabled=false
	sel = math.random(1,5)
	if sel == 1 then	
	chatfunc("You're done for.")
	elseif sel == 2 then	
	chatfunc("You asked for it.")
	elseif sel == 3 then
	chatfunc("Goodbye. Killer")
        elseif sel == 4 then
        chatfunc("Game, over for ink.")
        elseif sel == 5 then
        chatfunc("Heh..")
	end
	for i = 0, 2, 0.1 do
		swait()
				if Grabbed == true then
			grab.Humanoid.PlatformStand = true
			--GGyro.position = Partss.Position
			--GGyro.Parent = grab.Head
			grab.Torso.CFrame = Partss.CFrame * CFrame.Angles(0,math.rad(-90),0)
		end
		PlayAnimationFromTable({
         CFrame.new(0.104281992, -1.37529127e-22, -0.179345995, 0.249840975, 5.92156003e-22, 0.968286872, -5.57068883e-22, 1, -4.67813147e-22, -0.968286872, -4.22523594e-22, 0.249840975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0791492164, 1.44711375, -0.0994036943, 0.0100336075, -0.292051941, -0.95634979, -0.000366999942, 0.956396878, -0.29207015, 0.999949574, 0.00328149647, 0.00948894024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.94523025, 1.02494264, -0.272673488, 0.287940055, -0.795002162, 0.533912063, 0.0434400104, -0.546107173, -0.836588264, 0.956662774, 0.264080375, -0.122711219) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.58139038, 0.176945746, 5.27966768e-06, 0.939729631, 0.341920435, -3.69548798e-06, -0.341920793, 0.93972975, -6.50105221e-06, -5.81145287e-07, 6.40749931e-06, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.569345832, -1.89868093, -0.00942828506, 0.266425997, -0.0769406706, -0.960779786, 0.0135936281, 0.997010291, -0.0760724545, 0.963760078, 0.00720720552, 0.266675085) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.849354744, -2.01616573, 0.241646215, 0.948664129, 0.308412433, 0.0701368451, -0.312046438, 0.948832989, 0.0484089628, -0.0516182035, -0.0678096861, 0.996362925) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .1, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111939851, -1.63769794, -0.31875661, -0.0172049776, -1.39437616e-05, -0.999852121, 0.999852002, 5.96046448e-06, -0.0172049757, 6.16908073e-06, -1, 1.38394535e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
    Effects.Block.Create(BrickColor.new("Bright red"), Partss.CFrame, 2, 2, 2, 0.9, 0.9, 0.9, 0.05)
    Effects.Block.Create(BrickColor.new("Deep orange"), Partss.CFrame, 2, 2, 2, 0.5, 0.5, 0.5, 0.05)
    CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=138137702", Character, 1, .5)
    dmg(grab)
		grab.Head.Velocity = grab.Head.CFrame.lookVector * -60
	partasdeff.Enabled=true
	for i = 0, 1, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.104281992, -1.37529127e-22, -0.179345995, 0.249840975, 5.92156003e-22, 0.968286872, -5.57068883e-22, 1, -4.67813147e-22, -0.968286872, -4.22523594e-22, 0.249840975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0791492164, 1.44711375, -0.0994036943, 0.0100336075, -0.292051941, -0.95634979, -0.000366999942, 0.956396878, -0.29207015, 0.999949574, 0.00328149647, 0.00948894024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.95760894, 1.20200562, -0.275867403, 0.278526366, -0.669772983, 0.688351095, 0.0506580099, -0.705469668, -0.706927419, 0.959091723, 0.23176837, -0.162562534) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.58139038, 0.176945746, 5.27966768e-06, 0.939729631, 0.341920435, -3.69548798e-06, -0.341920793, 0.93972975, -6.50105221e-06, -5.81145287e-07, 6.40749931e-06, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.569345832, -1.89868093, -0.00942828506, 0.266425997, -0.0769406706, -0.960779786, 0.0135936281, 0.997010291, -0.0760724545, 0.963760078, 0.00720720552, 0.266675085) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.849354744, -2.01616573, 0.241646215, 0.948664129, 0.308412433, 0.0701368451, -0.312046438, 0.948832989, 0.0484089628, -0.0516182035, -0.0678096861, 0.996362925) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111932531, -1.63769579, -0.318755656, -0.0172050633, -1.61863863e-05, -0.999852121, 0.999851882, 5.15580177e-06, -0.017205067, 5.453825e-06, -1, 1.60960481e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	partasdeff.Enabled=false
	for i = 0, 2.5, 0.1 do
		swait()	
		PlayAnimationFromTable({
         CFrame.new(0.104281992, -1.37529127e-22, -0.179345995, 0.249840975, 5.92156003e-22, 0.968286872, -5.57068883e-22, 1, -4.67813147e-22, -0.968286872, -4.22523594e-22, 0.249840975) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0791492164, 1.44711375, -0.0994036943, 0.0100336075, -0.292051941, -0.95634979, -0.000366999942, 0.956396878, -0.29207015, 0.999949574, 0.00328149647, 0.00948894024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.94523025, 1.02494264, -0.272673488, 0.287940055, -0.795002162, 0.533912063, 0.0434400104, -0.546107173, -0.836588264, 0.956662774, 0.264080375, -0.122711219) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.58139038, 0.176945746, 5.27966768e-06, 0.939729631, 0.341920435, -3.69548798e-06, -0.341920793, 0.93972975, -6.50105221e-06, -5.81145287e-07, 6.40749931e-06, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.569345832, -1.89868093, -0.00942828506, 0.266425997, -0.0769406706, -0.960779786, 0.0135936281, 0.997010291, -0.0760724545, 0.963760078, 0.00720720552, 0.266675085) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.849354744, -2.01616573, 0.241646215, 0.948664129, 0.308412433, 0.0701368451, -0.312046438, 0.948832989, 0.0484089628, -0.0516182035, -0.0678096861, 0.996362925) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .2, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111939851, -1.63769794, -0.31875661, -0.0172049776, -1.39437616e-05, -0.999852121, 0.999852002, 5.96046448e-06, -0.0172049757, 6.16908073e-06, -1, 1.38394535e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	coroutine.wrap(function()	
		wait(2)
	partasdeff:Remove()	
	end)()
		else
	grab.Humanoid.PlatformStand = false
	for i = 0, 3, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.104280457, -1.46030498e-22, -0.179343686, 0.249860913, 5.18448626e-22, 0.968281686, -5.82335151e-22, 1, -5.29395592e-22, -0.968281686, -3.70576914e-22, 0.249860913) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.00671941042, 1.48144531, -0.121562012, 0.0679168552, 0.388981611, -0.918738663, 0.158512011, 0.904961228, 0.394866198, 0.985018492, -0.172449201, -0.000196114182) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.5714488, -0.100437641, -0.219321564, 0.297819793, -0.653239965, -0.696118593, -0.0311920028, 0.722160041, -0.691022456, 0.954112411, 0.227513462, 0.194697708) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.5814501, 0.177012652, 5.41775626e-06, 0.939689815, 0.342028022, -2.68220901e-06, -0.342027992, 0.939689755, -6.1805149e-06, 4.17232513e-07, 6.72787428e-06, 1) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.569012046, -1.89856982, -0.00933695585, 0.266445845, -0.0764764398, -0.960811257, 0.0135949478, 0.997046292, -0.075590536, 0.963754177, 0.00707861409, 0.266698539) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.849534154, -2.01595497, 0.241721377, 0.948572636, 0.308689058, 0.070150286, -0.312330276, 0.948733151, 0.0485308319, -0.0515729487, -0.067945078, 0.996355295) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .1, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111981034, -1.63767779, -0.318741798, -0.0172085222, -1.4077872e-05, -0.999851882, 0.999851942, 7.4505806e-06, -0.0172085222, 7.68899918e-06, -1.00000012, 1.39512122e-05) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
sel = math.random(1,3)
if sel == 1 then	
chatfunc("I'm stupid sorry boris...")
elseif sel == 2 then	
chatfunc("What am I even doing...?")
elseif sel == 3 then
chatfunc("...Boris tell me you here.")
end
		for i = 0, 5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 0.999999881, 5.04870979e-29, -4.21790838e-43, 5.04870979e-29, 1, -5.04870979e-29, -4.21790838e-43, -5.04870979e-29, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0399715528, 1.42130852, -0.217550665, 0.985933542, -0.136098281, -0.097015582, 0.166522697, 0.849608123, 0.500436008, 0.0143167432, -0.509551942, 0.860320628) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0- .4 * math.cos((sine) / 5), 0), 
         CFrame.new(1.57258642, 0.0433240086, 3.83948304e-08, 0.990993857, -0.133906633, -2.60571618e-08, 0.133906662, 0.990993977, 5.96046341e-08, 1.78410318e-08, -6.25570422e-08, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.693957031, 0.999676406, -0.811627388, 0.817211449, -0.569911301, -0.0858340934, -0.499626935, -0.626295447, -0.598442137, 0.287295371, 0.531934083, -0.796558976) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.540301144, -1.99792778, 1.70425119e-06, 0.998698354, -0.0510031469, 6.26438805e-07, 0.0510031544, 0.998698473, -1.04335422e-05, -9.34800966e-08, 1.04519122e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.539563119, -1.99793291, 1.9016752e-06, 0.998630941, 0.0523070693, -1.67712614e-07, -0.0523070768, 0.99863106, -1.0458818e-05, -3.79587107e-07, 1.04532719e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111991819, -1.63769639, -0.318748534, -0.0172109455, -5.96046448e-08, -0.999852002, 0.999852061, -1.19209318e-07, -0.0172108412, 5.96046519e-08, -0.99999994, -1.19209275e-07) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	end
	end
	--GGyro.Parent = nil
	attack = false
	Grabbed = false
	Humanoid.WalkSpeed = 9

end
function moarblood()
	attack = true
	CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=541710285", Character, 1, .8)
    RootPart.CFrame = targetted.Torso.CFrame * CFrame.new(0,0,4)
local k = New("Part",LeftArm,"k",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Neon,Transparency = 1,Transparency = 1,Shape = Enum.PartType.Cylinder,Size = Vector3.new(0.200000003, 0.221472204, 0.221472189),CFrame = CFrame.new(4.93319941, -1.31948221, -45.7696877, 0.141969427, -5.55023435e-05, -0.989871144, 0.989874005, 1.80069164e-05, 0.141970903, 1.06166653e-05, -1.00000143, 5.59078326e-05),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(.6, 0.164706, 0.207843),})
mot = New("Weld",k,"mot",{Part0 = k,Part1 = LeftArm,C0 = CFrame.new(0, 0, 0, 0.141969457, 0.989873946, 1.06166663e-05, -5.55023507e-05, 1.80069164e-05, -1.00000167, -0.989871264, 0.141970903, 5.59078399e-05),C1 = CFrame.new(6.67572021e-06, -1.40000057, -3.81469727e-06, 0.989870846, -0.14197053, -1.2531201e-06, 0.141970515, 0.989870906, 1.03843358e-05, -2.33842215e-07, -1.04570581e-05, 0.99999994),})
wait(.5)
	for i = 0, 1.2, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.0246932413, -0.0966757834, -0.0092370566, 0.713696778, 5.59592329e-22, 0.700454772, -9.27150216e-22, 1, 1.45779223e-22, -0.700454772, -7.53468894e-22, 0.713696778) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.098094359, 1.53651738, -0.281765848, 0.593379974, 0.280785412, -0.754360616, -0.0276839901, 0.943748772, 0.329502523, 0.804446399, -0.174636483, 0.567774832) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.58677018, 0.143787161, 0.0495693758, 0.968102753, -0.250522822, -0.00394502282, 0.250228018, 0.965921044, 0.0662006512, -0.0127741396, -0.0650762022, 0.997798622) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.74332106, 0.446618229, -0.859300971, 0.795205951, 0.606264353, -0.0095520094, -0.0538869984, 0.0549720451, -0.997032762, -0.603940368, 0.793361068, 0.0763838589) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.648194611, -1.97843742, -0.088139981, 0.954304218, -0.129303336, -0.269414723, 0.107585981, 0.989748061, -0.0939367935, 0.278798997, 0.0606590137, 0.958431959) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.671899676, -2.02211809, 0.00866907835, 0.94230175, 0.108399026, -0.316728801, -0.108764999, 0.993929207, 0.0165804606, 0.316603303, 0.0188252106, 0.948371291) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .2, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111978557, -1.63769853, -0.318748116, -0.0172083378, 3.06963921e-06, -0.999852002, 0.999851942, -2.01165676e-07, -0.0172083378, -2.4586916e-07, -1, -3.09944153e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	if targetted.Name ~= "CKbackup" then
	local grab = nil
	for i, v in pairs(FindNearestTorso(Torso.CFrame.p, 7)) do
		if v:FindFirstChild('Head') then
			Grabbed = true
			    CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=260430060", v.Head, 1, .8)
			grab = v
		end
	end
         Humanoid.WalkSpeed = 0
		for i = 0, 2, 0.1 do
		swait()
		if Grabbed == true then
			grab.Humanoid.PlatformStand = true
			--GGyro.position = Partss.Position
			--GGyro.Parent = grab.Head
			grab.Head.CFrame = k.CFrame * CFrame.Angles(0,math.rad(-90),0)
		end
		PlayAnimationFromTable({
         CFrame.new(-0.203895777, -0.0966757089, 0.221102715, 0.860356927, 5.59592329e-22, -0.509691954, -9.74120787e-23, 1, 9.33471908e-22, 0.509691954, -7.53468894e-22, 0.860356927) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0263810754, 1.49789393, -0.36129567, 0.83927381, -0.177804202, 0.513814509, -0.0293880031, 0.928800881, 0.369412124, -0.542914331, -0.325137854, 0.774292946) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.70567894, 0.192227185, 0.324310064, 0.910149336, -0.402004361, -0.100104719, 0.41140601, 0.848634601, 0.332512379, -0.0487190783, -0.343819588, 0.937771142) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.925376594, 0.275374949, -0.912649989, 0.847262561, -0.507846355, 0.155686736, 0.278232396, 0.17463918, -0.944503605, 0.452473402, 0.84355998, 0.289265245) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.648186982, -1.97843516, -0.0881449506, 0.954305232, -0.129303262, -0.269411147, 0.107586049, 0.989748061, -0.0939371213, 0.278795511, 0.0606598109, 0.958432913) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.671897829, -2.02211738, 0.00865991414, 0.942302644, 0.108399101, -0.316726208, -0.108764961, 0.993929207, 0.0165806562, 0.31660068, 0.0188247077, 0.948372126) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .25, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111928731, -1.63769662, -0.318741947, -0.0172089636, 8.2552433e-06, -0.999852061, 0.999852061, 7.4505806e-07, -0.0172089189, 5.66244125e-07, -1.00000012, -8.2552433e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
		end
		if Grabbed == true then
				sel = math.random(1,3)
	if sel == 1 then	
	chatfunc("My turn.")
	elseif sel == 2 then	
	chatfunc("You the next!")
	elseif sel == 3 then
	chatfunc("Hope you full of ink and Die!")
        elseif sel == 4 then
        chatfunc("You're hopeless.")
        elseif sel == 5 then
        chatfunc("Hmph.")
	end
			local partasdeff = Instance.new("ParticleEmitter",targetted.Head)
			partasdeff.Color = ColorSequence.new(Color3.new(1, 0, 0), Color3.new(.5, 0, 0))
			partasdeff.LightEmission = .1
			partasdeff.Size = NumberSequence.new(0.2)
			partasdeff.Texture = "http://www.roblox.com/asset/?ID=771221224"
			aaa = NumberSequence.new({NumberSequenceKeypoint.new(0, 0.2),NumberSequenceKeypoint.new(1, 5)})
			bbb = NumberSequence.new({NumberSequenceKeypoint.new(0, 1),NumberSequenceKeypoint.new(0.0636, 0), NumberSequenceKeypoint.new(1, 1)})
			partasdeff.Transparency = bbb
			partasdeff.Size = aaa
			partasdeff.ZOffset = .9
			partasdeff.Acceleration = Vector3.new(0, -5, 0)
			partasdeff.LockedToPart = false
			partasdeff.EmissionDirection = "Back"
			partasdeff.Lifetime = NumberRange.new(1, 2)
			partasdeff.Rate = 1000
			partasdeff.Rotation = NumberRange.new(-100, 100)
			partasdeff.RotSpeed = NumberRange.new(-100, 100)
			partasdeff.Speed = NumberRange.new(6)
			partasdeff.VelocitySpread = 10000
			partasdeff.Enabled=false	
	for i = 0, 3, 0.1 do
		swait()
		if Grabbed == true then
			grab.Humanoid.PlatformStand = true
			--GGyro.position = Partss.Position
			--GGyro.Parent = grab.Head
			grab.Head.CFrame = k.CFrame * CFrame.Angles(0,math.rad(-90),0)
		end
		PlayAnimationFromTable({
         CFrame.new(-0.203895777, -0.0966757089, 0.221102715, 0.860356927, 5.59592329e-22, -0.509691954, -9.74120787e-23, 1, 9.33471908e-22, 0.509691954, -7.53468894e-22, 0.860356927) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.0996288583, 1.46053851, -0.148588806, 0.834862471, 0.0359686315, 0.549282432, -0.0103890011, 0.998714745, -0.0496083908, -0.550360739, 0.0357096791, 0.83416307) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.70567894, 0.192227185, 0.324310064, 0.910149336, -0.402004361, -0.100104719, 0.41140601, 0.848634601, 0.332512379, -0.0487190783, -0.343819588, 0.937771142) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.5511272, 1.22937977, -0.634234905, 0.785770595, 0.333147645, 0.521131098, 0.522403002, -0.808557391, -0.270795107, 0.331149668, 0.485022962, -0.809378147) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.648186982, -1.97843516, -0.0881449506, 0.954305232, -0.129303262, -0.269411147, 0.107586049, 0.989748061, -0.0939371213, 0.278795511, 0.0606598109, 0.958432913) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.684103072, -2.02189779, 0.0673112273, 0.973016024, 0.108399175, -0.203689545, -0.109960191, 0.993929327, 0.00367253274, 0.202851087, 0.0188243091, 0.979028702) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .1, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111928731, -1.63769662, -0.318741947, -0.0172089636, 8.2552433e-06, -0.999852061, 0.999852061, 7.4505806e-07, -0.0172089189, 5.66244125e-07, -1.00000012, -8.2552433e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	partasdeff.Enabled=true
	grab.Torso.Transparency = 1
	dmg(grab)
	CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=245185986", grab.Head, .8, .8)
	CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=245185986", grab.Head, 1, .7)
	
	coroutine.wrap(function()
	wait(.4)
	partasdeff.Enabled=false
	end)()
	for i = 0, 3.5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(-0.203895777, -0.0966757089, 0.221102715, 0.860356927, 5.59592329e-22, -0.509691954, -9.74120787e-23, 1, 9.33471908e-22, 0.509691954, -7.53468894e-22, 0.860356927) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.0996288583, 1.46053851, -0.148588806, 0.834862471, 0.0359686315, 0.549282432, -0.0103890011, 0.998714745, -0.0496083908, -0.550360739, 0.0357096791, 0.83416307) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.70567894, 0.192227185, 0.324310064, 0.910149336, -0.402004361, -0.100104719, 0.41140601, 0.848634601, 0.332512379, -0.0487190783, -0.343819588, 0.937771142) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.40260935, 1.29555511, -0.560751677, 0.832364976, 0.188659444, 0.521130562, 0.370884001, -0.88832134, -0.2707977, 0.411842346, 0.418681324, -0.809378505) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.648186982, -1.97843516, -0.0881449506, 0.954305232, -0.129303262, -0.269411147, 0.107586049, 0.989748061, -0.0939371213, 0.278795511, 0.0606598109, 0.958432913) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.684103072, -2.02189779, 0.0673112273, 0.973016024, 0.108399175, -0.203689545, -0.109960191, 0.993929327, 0.00367253274, 0.202851087, 0.0188243091, 0.979028702) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111928731, -1.63769662, -0.318741947, -0.0172089636, 8.2552433e-06, -0.999852061, 0.999852061, 7.4505806e-07, -0.0172089189, 5.66244125e-07, -1.00000012, -8.2552433e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	end
	else
         Humanoid.WalkSpeed = 0
	for i = 0, 3, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.0246932413, -0.0966757834, -0.0092370566, 0.713696778, 5.59592329e-22, 0.700454772, -9.27150216e-22, 1, 1.45779223e-22, -0.700454772, -7.53468894e-22, 0.713696778) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.098094359, 1.53651738, -0.281765848, 0.593379974, 0.280785412, -0.754360616, -0.0276839901, 0.943748772, 0.329502523, 0.804446399, -0.174636483, 0.567774832) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.58677018, 0.143787161, 0.0495693758, 0.968102753, -0.250522822, -0.00394502282, 0.250228018, 0.965921044, 0.0662006512, -0.0127741396, -0.0650762022, 0.997798622) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.74332106, 0.446618229, -0.859300971, 0.795205951, 0.606264353, -0.0095520094, -0.0538869984, 0.0549720451, -0.997032762, -0.603940368, 0.793361068, 0.0763838589) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.648194611, -1.97843742, -0.088139981, 0.954304218, -0.129303336, -0.269414723, 0.107585981, 0.989748061, -0.0939367935, 0.278798997, 0.0606590137, 0.958431959) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.671899676, -2.02211809, 0.00866907835, 0.94230175, 0.108399026, -0.316728801, -0.108764999, 0.993929207, 0.0165804606, 0.316603303, 0.0188252106, 0.948371291) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .2, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111978557, -1.63769853, -0.318748116, -0.0172083378, 3.06963921e-06, -0.999852002, 0.999851942, -2.01165676e-07, -0.0172083378, -2.4586916e-07, -1, -3.09944153e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end	
sel = math.random(1,3)
if sel == 1 then	
chatfunc("Bad...")
elseif sel == 2 then	
chatfunc("Something's wrong now what....")
elseif sel == 3 then
chatfunc("Boris...")
end
	for i = 0, 5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 0.999999881, 5.04870979e-29, -4.21790838e-43, 5.04870979e-29, 1, -5.04870979e-29, -4.21790838e-43, -5.04870979e-29, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0399715528, 1.42130852, -0.217550665, 0.985933542, -0.136098281, -0.097015582, 0.166522697, 0.849608123, 0.500436008, 0.0143167432, -0.509551942, 0.860320628) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0- .4 * math.cos((sine) / 5), 0), 
         CFrame.new(1.57258642, 0.0433240086, 3.83948304e-08, 0.990993857, -0.133906633, -2.60571618e-08, 0.133906662, 0.990993977, 5.96046341e-08, 1.78410318e-08, -6.25570422e-08, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.693957031, 0.999676406, -0.811627388, 0.817211449, -0.569911301, -0.0858340934, -0.499626935, -0.626295447, -0.598442137, 0.287295371, 0.531934083, -0.796558976) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.540301144, -1.99792778, 1.70425119e-06, 0.998698354, -0.0510031469, 6.26438805e-07, 0.0510031544, 0.998698473, -1.04335422e-05, -9.34800966e-08, 1.04519122e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.539563119, -1.99793291, 1.9016752e-06, 0.998630941, 0.0523070693, -1.67712614e-07, -0.0523070768, 0.99863106, -1.0458818e-05, -3.79587107e-07, 1.04532719e-05, 0.999999881) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111991819, -1.63769639, -0.318748534, -0.0172109455, -5.96046448e-08, -0.999852002, 0.999852061, -1.19209318e-07, -0.0172108412, 5.96046519e-08, -0.99999994, -1.19209275e-07) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	end
	attack = false
	Grabbed = false	
	k:Remove()
         Humanoid.WalkSpeed = 9
end

function painlessrain()
attack = true
    Humanoid.WalkSpeed = 0
   local ref1 = New("Part",m,"ref",{Transparency = 1,Size = Vector3.new(.2,.2,.2),CFrame = Torso.CFrame,Anchored = true,CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,})

	coroutine.wrap(function()
	for i = 0, 4 do
	wait(.2)
	CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=199145095", RootPart, 1, 1.3)
	end
	end)()
	for i = 0, 4, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.160091802, -3.66497677e-23, -0.0753167868, 0.153125972, 2.95760942e-22, 0.988206744, 9.50910858e-23, 1, -3.14025256e-22, -0.988206744, 1.42055005e-22, 0.153125986) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.115934461, 1.42953098, -0.0387745127, 0.0422455594, -0.156738758, -0.986736298, 0.091215007, 0.984098434, -0.152414545, 0.994934857, -0.083566308, 0.0558707118) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.88563442, 0.849646449, -0.150348112, 0.134151325, -0.917590559, 0.374207288, 0.151069015, -0.354270071, -0.922860146, 0.979378283, 0.180334046, 0.0910937041) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.53188074, 0.0735950321, 2.69606994e-06, 0.978446901, 0.206499115, 2.48849392e-06, -0.2064991, 0.978446841, -1.05276868e-05, -4.61935997e-06, 9.78447497e-06, 1.00000012) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.6596874, -2.0274992, -0.0100709619, 0.00881013274, -0.161221251, -0.986878991, 0.00903601572, 0.986890376, -0.161142424, 0.999920428, -0.0074977763, 0.0101515204) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.56669867, -2.04759455, -0.0995163321, 0.988194227, 0.0786855519, 0.131456956, -0.0635150596, 0.991232872, -0.115859069, -0.139420897, 0.106141761, 0.984528303) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .07, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.00354172289, -1.19249964, -0.318736732, -0.017209189, -1.8668361e-06, -0.999851942, 0.999851882, 1.90734863e-06, -0.0172091946, 1.93715096e-06, -1.00000012, 1.82725489e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, math.rad(doe * 22)), 0.3)
	end
	for i = 0, 1.5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.160091802, -3.66497677e-23, -0.0753167868, 0.153125972, 2.95760942e-22, 0.988206744, 9.50910858e-23, 1, -3.14025256e-22, -0.988206744, 1.42055005e-22, 0.153125986) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.181723118, 1.42154801, -0.0812263489, 0.0422911495, -0.473342478, -0.879862845, 0.0912349299, 0.878800809, -0.468385875, 0.994931221, -0.0604656339, 0.0803508535) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.46608233, 1.280774, -0.0335922651, 0.00761340559, -0.0420075022, 0.999088407, 0.0443810038, -0.998118579, -0.0423049256, 0.998985708, 0.044662632, -0.00573477149) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.53188074, 0.0735950321, 2.69606994e-06, 0.978446901, 0.206499115, 2.48849392e-06, -0.2064991, 0.978446841, -1.05276868e-05, -4.61935997e-06, 9.78447497e-06, 1.00000012) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.6596874, -2.0274992, -0.0100709619, 0.00881013274, -0.161221251, -0.986878991, 0.00903601572, 0.986890376, -0.161142424, 0.999920428, -0.0074977763, 0.0101515204) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.56669867, -2.04759455, -0.0995163321, 0.988194227, 0.0786855519, 0.131456956, -0.0635150596, 0.991232872, -0.115859069, -0.139420897, 0.106141761, 0.984528303) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .2, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0112083405, -1.63769615, -0.31873402, -0.0172121376, -2.89082527e-06, -0.999851882, 0.999851942, 4.58210707e-07, -0.0172121413, 5.06639481e-07, -1.00000012, 2.89082527e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	for i = 0, 3 do
    Effects.Block.Create(BrickColor.new("Bright red"), Partss.CFrame, 2, 2, 2, 0.9, 0.9, 0.9, 0.05)
    Effects.Block.Create(BrickColor.new("Deep orange"), Partss.CFrame, 2, 2, 2, 0.5, 0.5, 0.5, 0.05)
    CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=138137702", Character, 1, .5)
	for i = 0, .5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.160087422, -3.66470256e-23, -0.0753137618, 0.15316838, 2.95750466e-22, 0.988200247, 9.50818972e-23, 1, -3.14019425e-22, -0.988200247, 1.42057819e-22, 0.15316838) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.181723118, 1.42154801, -0.0812263489, 0.0422911495, -0.473342478, -0.879862845, 0.0912349299, 0.878800809, -0.468385875, 0.994931221, -0.0604656339, 0.0803508535) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.46630716, 1.08524323, -0.0336530581, 0.00764143467, -0.0426861309, 0.999059498, 0.0445286781, -0.998082876, -0.0429849848, 0.998979032, 0.0448152684, -0.0057259798) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.53188026, 0.0735908896, 2.69562906e-06, 0.978447855, 0.206495479, 2.48849392e-06, -0.206495419, 0.978447556, -1.05270137e-05, -4.61935997e-06, 9.78633761e-06, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.659685254, -2.0274992, -0.0100700259, 0.00885757804, -0.161218897, -0.986879349, 0.00904085487, 0.986890197, -0.161139548, 0.999920309, -0.00749491528, 0.0101990253) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.566697419, -2.04759264, -0.0995131433, 0.988195002, 0.078684561, 0.131453067, -0.0635149851, 0.991233289, -0.115855575, -0.139416695, 0.106138662, 0.984529436) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0112046078, -1.63744116, -0.318734497, -0.0172122065, 2.46167183e-05, -0.999852002, 0.999850631, -0.00159030408, -0.0172121339, -0.00159040466, -0.999998927, 2.57790089e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	for i = 0, .5, 0.1 do
		swait()
		PlayAnimationFromTable({
         CFrame.new(0.160091802, -3.66497677e-23, -0.0753167868, 0.153125972, 2.95760942e-22, 0.988206744, 9.50910858e-23, 1, -3.14025256e-22, -0.988206744, 1.42055005e-22, 0.153125986) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.181723118, 1.42154801, -0.0812263489, 0.0422911495, -0.473342478, -0.879862845, 0.0912349299, 0.878800809, -0.468385875, 0.994931221, -0.0604656339, 0.0803508535) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.46608233, 1.280774, -0.0335922651, 0.00761340559, -0.0420075022, 0.999088407, 0.0443810038, -0.998118579, -0.0423049256, 0.998985708, 0.044662632, -0.00573477149) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.53188074, 0.0735950321, 2.69606994e-06, 0.978446901, 0.206499115, 2.48849392e-06, -0.2064991, 0.978446841, -1.05276868e-05, -4.61935997e-06, 9.78447497e-06, 1.00000012) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.6596874, -2.0274992, -0.0100709619, 0.00881013274, -0.161221251, -0.986878991, 0.00903601572, 0.986890376, -0.161142424, 0.999920428, -0.0074977763, 0.0101515204) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.56669867, -2.04759455, -0.0995163321, 0.988194227, 0.0786855519, 0.131456956, -0.0635150596, 0.991232872, -0.115859069, -0.139420897, 0.106141761, 0.984528303) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0112083405, -1.63769615, -0.31873402, -0.0172121376, -2.89082527e-06, -0.999851882, 0.999851942, 4.58210707e-07, -0.0172121413, 5.06639481e-07, -1.00000012, 2.89082527e-06) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
	end
	end
attack = false
Humanoid.WalkSpeed = 8
		wait(.4)
	for i = 0, 8 do
		wait(.2)
		mdmg(ref1, 3)
        CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=192410089", Character, 1.5, .7)		
		ref1.Position = Mouse.hit.p
		ref1.CFrame = ref1.CFrame * CFrame.new(math.random(-.5,.5),0,math.random(-.5,.5))
        Effects.Cylinder.Create(BrickColor.new("Deep orange"), ref1.CFrame, .5, 9999, .5, 0.5, 0, 0.5, 0.07)
	end
	ref1:Remove()
end

function TargetSelect(person)
local dd=coroutine.wrap(function()
if targetted ~= person then
targetted = person
img2.Size = UDim2.new(1,0,1,0)
img2.ImageTransparency = 0
img2.Position = UDim2.new(0,0,0,0)
for i = 0, 2, 0.1 do
swait()
img2.Size = img2.Size + UDim2.new(.05,0,.05,0)
img2.Position = img2.Position + UDim2.new(-.025,0,-.025,0)
img2.ImageTransparency = img2.ImageTransparency + 0.05
end
end
end)
dd()
end

function LockOn()
if Mouse.Target.Parent ~= Character and Mouse.Target.Parent.Parent ~= Character and Mouse.Target.Parent:FindFirstChild("Humanoid") ~= nil then
TargetSelect(Mouse.Target.Parent)
CFuncs["Sound"].Create("http://www.roblox.com/asset/?id=263321145", Character, 1, .8)
end
end


function ofmoosic() -- 2 lazi hoh
delays = true
while wait() and kkk and kkk.Volume >= 0.02 do
	kkk.Volume = kkk.Volume - 0.05
end
wait(0.1)
kkk.Pitch = 0
kkk.PlaybackSpeed = 0
play = false
delays = false
end
function onmoosic()
delays = true
kkk.Pitch = .6
kkk.PlaybackSpeed = .6
while wait() and kkk and kkk.Volume <= 1.5 do
	kkk.Volume = kkk.Volume + 0.05
end
wait(0.1)
play = true
delays = false
end
Mouse.Button1Down:connect(function()
	if attack == false and targetted ~= nil then
		attackone()
	end
end)

Mouse.KeyDown:connect(function(k)
	k = k:lower()
	if attack == false and k == 'q' then
	LockOn()
	end
	if k == 'z' and attack == false then	
	hedshoot()
	elseif k == 'x' and attack == false and targetted ~= nil then
	moarblood()
	elseif k == 'c' and attack == false then
	painlessrain()
	elseif k == 'g' and delays == false and Character.Name == "grgrgry21" then
	delays = true
	chatfunc("Hey Sugarie...")
	wait(2)
	chatfunc("Can I ask you something for uhh.....?")
	wait(3)
	chatfunc("Will you be my....")
	wait(1)
	chatfunc("SacrificBy-")
	wait(.5)
	chatfunc("I mean...")
	wait(1)
	chatfunc("Uhh, forget it or i kill you...")
	delays = false
    elseif k == 'm' and play == true and delays == false then
	ofmoosic()
	elseif k == 'm' and play == false and delays == false then
	onmoosic()
	end
end)

kkk = Instance.new("Sound",Character)
kkk.Volume = 100
kkk.PlaybackSpeed = 1
kkk.Pitch = 1
kkk.SoundId = "rbxassetid://681418426"
kkk:Play()
kkk.Name = "a"
kkk.Looped = true


coroutine.wrap(function()
while true do
swait()
	for i, v in pairs(Character.WeaponModel:GetChildren()) do
		if v:IsA("Part") then
		v.Anchored = false
		end
		end
	for i, v in pairs(Character:GetChildren()) do
		if v:IsA("Part") then
		v.Anchored = false
		elseif v:IsA("Accessory") then
		v.Handle.Anchored = false
		end
		end
end
end)()
coroutine.wrap(function()
while 1 do
swait()
if doe <= 360 then
	doe = doe + 2
else
	doe = 0
end
end
end)()
while true do
	swait()
	for i, v in pairs(Character:GetChildren()) do
		if v:IsA("Part") then
			v.Material = "SmoothPlastic"
		elseif v:IsA("Accessory") then
			v:WaitForChild("Handle").Material = "SmoothPlastic"
		end
	end
while true do
swait()
Character.Humanoid.MaxHealth = math.huge
Character.Humanoid.Health = math.huge
imgl.Rotation = imgl.Rotation + 3
img2.Rotation = img2.Rotation + 3
if targetted ~= nil then
abss.Adornee = targetted:FindFirstChild("Torso") or targetted:FindFirstChild("UpperTorso")
abss.Enabled = true
elseif targetted == nil then
abss.Adornee = nil
abss.Enabled = false
end

while true and imgl.Rotation >= 360 do
imgl.Rotation = 0	
img2.Rotation = 0
end
	Torsovelocity = (RootPart.Velocity * Vector3.new(1, 0, 1)).magnitude 
	velocity = RootPart.Velocity.y
	sine = sine + change
	local hit, pos = rayCast(RootPart.Position, (CFrame.new(RootPart.Position, RootPart.Position - Vector3.new(0, 1, 0))).lookVector, 4, Character)
		if RootPart.Velocity.y > 1 and hit == nil then 
			Anim = "Jump"
			if attack == false then
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 1, -2.21689355e-12, -5.11591203e-13, -2.21689355e-12, 1, 7.74860496e-07, -5.11591203e-13, 7.74860496e-07, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0579944476, 1.48445117, -0.000906195492, 0.999631822, -0.0259140469, -0.00804444961, 0.0262291897, 0.998776913, 0.0419151038, 0.0069484422, -0.0421099029, 0.999089062) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.68067598, 0.167780995, 5.50026158e-08, 0.965881884, -0.258982956, -3.41060513e-13, 0.258982956, 0.965881884, 4.47034836e-07, 8.49010675e-08, 3.16640808e-07, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.67620921, 0.188169807, -3.04922651e-07, 0.95698452, 0.290146649, -2.61441073e-07, -0.290146649, 0.95698452, -1.0069979e-05, -2.89639524e-06, 1.04542296e-05, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.537238836, -1.93797374, 0.176598221, 0.998698533, -0.0506777391, -0.00574572897, 0.0510024093, 0.992341697, 0.112511501, -6.35704041e-08, -0.112657718, 0.993634105) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.536944568, -1.94808352, 0.126473114, 0.998626292, 0.0520468242, 0.00521374354, -0.0523067154, 0.993665218, 0.0995327011, -3.84102691e-07, -0.099668026, 0.995023906) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111988392, -1.63769972, -0.318750381, -0.0172117054, 0, -0.999851942, 0.999851942, 0, -0.0172116756, 0, -1, 0) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
					end
		elseif RootPart.Velocity.y < -1 and hit == nil then 
			Anim = "Fall"
			if attack == false then
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 1, -2.21689355e-12, -5.11591203e-13, -2.21689355e-12, 1, 7.74860496e-07, -5.11591203e-13, 7.74860496e-07, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0576509275, 1.50532985, -0.129091382, 0.999631822, -0.0231846143, -0.0140984114, 0.0262298863, 0.958684564, 0.283279002, 0.00694822101, -0.283544153, 0.958935201) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.68622994, 0.21415168, 7.02040666e-08, 0.881990671, -0.471266806, -3.41060513e-13, 0.471266806, 0.881990671, 4.47034836e-07, 1.54493137e-07, 2.89139166e-07, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-1.72513735, 0.240890861, 2.54038241e-07, 0.814108491, 0.58071363, -2.61430017e-07, -0.580713034, 0.814108849, -1.00698489e-05, -6.08482924e-06, 8.98058715e-06, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(0.536720514, -1.92783141, 0.223740995, 0.998698533, -0.0498600565, -0.0107376017, 0.0510031059, 0.976314366, 0.210260883, -3.04512355e-07, -0.210534185, 0.977587521) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.535922825, -1.92850935, 0.222419083, 0.99863112, 0.0512506701, 0.0104565797, -0.0523065142, 0.978474379, 0.199629858, -3.7062793e-07, -0.199902818, 0.97981596) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0112015437, -1.63769758, -0.318750381, -0.0172110498, 0, -0.999851942, 0.999851942, 0, -0.0172110498, 0, -1, 0) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
					end
		elseif Torsovelocity < 1 and hit ~= nil then
			Anim = "Idle"
			if attack == false then
				change = 1
		PlayAnimationFromTable({
         CFrame.new(0, 0, 0, 1, -2.21689355e-12, -5.11591203e-13, -2.21689355e-12, 1, 7.74860496e-07, -5.11591203e-13, 7.74860496e-07, 1.00000048) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0575585738, 1.52553558, -0.218724757, 0.985934377, -0.143356442, -0.0859283879, 0.166522771, 0.886584163, 0.431554198, 0.0143168001, -0.439792335, 0.897985697) * CFrame.new(0, -.05- .05 * math.cos((sine) / 55), 0- .05 * math.cos((sine) / 55)) * CFrame.Angles(math.rad(0 - 5 * math.cos((sine) / 55)), 0, 0), 
         CFrame.new(1.54809988, 0.041232653, 1.35168499e-08, 0.996376455, -0.0850530341, -3.41060513e-13, 0.0850530341, 0.996376455, 4.47034836e-07, 2.78823862e-08, 3.26637689e-07, 1.00000024) * CFrame.new(0- 0.025 * math.cos((sine) / 45), 0, 0) * CFrame.Angles(0, 0, 0- 0.05 * math.cos((sine) / 45)), 
         CFrame.new(-1.53598976, 0.0413191095, -1.86092848e-06, 0.995650649, 0.0931596532, -2.61508148e-07, -0.0931649953, 0.995651186, -1.00695124e-05, -7.49969331e-07, 1.08217946e-05, 1.00000024) * CFrame.new(0+ 0.025 * math.cos((sine) / 45), 0, 0) * CFrame.Angles(0, 0, 0+ 0.05 * math.cos((sine) / 45)), 
         CFrame.new(0.540300786, -1.99793816, -9.82598067e-07, 0.998698533, -0.0510031395, 6.36324955e-07, 0.0510031395, 0.998698533, -1.00461093e-05, -8.35937328e-08, 1.08393433e-05, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.539563596, -1.99794078, 1.12228372e-06, 0.998635888, 0.0523072146, -1.77852357e-07, -0.0523072146, 0.998635888, -1.00715051e-05, -3.89727461e-07, 1.08406466e-05, 1.00000024) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111980997, -1.6377027, -0.318750381, -0.0172109306, 0, -0.999851882, 0.999851882, 0, -0.0172109306, 0, -1, 0) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
			end
		elseif Torsovelocity > 2 and hit ~= nil then
			Anim = "Walk"
			if attack == false then
		PlayAnimationFromTable({		
         CFrame.new(0, 0, 0, 1, -2.21689355e-12, -5.11591203e-13, -2.21689355e-12, 1, 7.74860496e-07, -5.11591203e-13, 7.74860496e-07, 1.00000048) * CFrame.new(0, 0- .08 * math.cos((sine) / 5), 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(-0.0595112406, 1.55331731, -0.0425721854, 0.999631822, -0.0248252042, -0.010953242, 0.0262294486, 0.987443328, 0.155781403, 0.00694842171, -0.156010598, 0.987731278) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 
         CFrame.new(1.54809988, 0.041232653, 1.35168499e-08, 0.996376455, -0.0850530341, -3.41060513e-13, 0.0850530341, 0.996376455, 4.47034836e-07, 2.78823862e-08, 3.26637689e-07, 1.00000024) * CFrame.new(0, 0, 0- .5 * math.cos((sine) / 10)) * CFrame.Angles(math.rad(0 + 30 * math.cos((sine) / 10)), 0, 0), 
         CFrame.new(-1.53598976, 0.0413191095, -1.86092848e-06, 0.995650649, 0.0931596532, -2.61508148e-07, -0.0931649953, 0.995651186, -1.00695124e-05, -7.49969331e-07, 1.08217946e-05, 1.00000024) * CFrame.new(0, 0, 0+ .5 * math.cos((sine) / 10)) * CFrame.Angles(math.rad(0 - 30 * math.cos((sine) / 10)), 0, 0), 
         CFrame.new(0.540300786, -1.99793816, -9.82598067e-07, 0.998698533, -0.0510031395, 6.36324955e-07, 0.0510031395, 0.998698533, -1.00461093e-05, -8.35937328e-08, 1.08393433e-05, 1.00000024) * CFrame.new(0, 0, 0+ .5 * math.cos((sine) / 10)) * CFrame.Angles(math.rad(0 - 30 * math.cos((sine) / 10)), 0, 0), 
         CFrame.new(-0.539563596, -1.99794078, 1.12228372e-06, 0.998635888, 0.0523072146, -1.77852357e-07, -0.0523072146, 0.998635888, -1.00715051e-05, -3.89727461e-07, 1.08406466e-05, 1.00000024) * CFrame.new(0, 0, 0- .5 * math.cos((sine) / 10)) * CFrame.Angles(math.rad(0 + 30 * math.cos((sine) / 10)), 0, 0), 
		}, .3, false)
		moter.C0 = clerp(moter.C0, CFrame.new(0.0111980997, -1.6377027, -0.318750381, -0.0172109306, 0, -0.999851882, 0.999851882, 0, -0.0172109306, 0, -1, 0) * CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0), 0.3)
			end
		end
	if 0 < #Effects then
		for e = 1, #Effects do
			if Effects[e] ~= nil then
				local Thing = Effects[e]
				if Thing ~= nil then
					local Part = Thing[1]
					local Mode = Thing[2]
					local Delay = Thing[3]
					local IncX = Thing[4]
					local IncY = Thing[5]
					local IncZ = Thing[6]
					if Thing[2] == "Shoot" then
						local Look = Thing[1]
						local move = 30
						if Thing[8] == 3 then
							move = 10
						end
						local hit, pos = rayCast(Thing[4], Thing[1], move, m)
						if Thing[10] ~= nil then
							da = pos
							cf2 = CFrame.new(Thing[4], Thing[10].Position)
							cfa = CFrame.new(Thing[4], pos)
							tehCF = cfa:lerp(cf2, 0.2)
							Thing[1] = tehCF.lookVector
						end
						local mag = (Thing[4] - pos).magnitude
						Effects["Head"].Create(Torso.BrickColor, CFrame.new((Thing[4] + pos) / 2, pos) * CFrame.Angles(1.57, 0, 0), 1, mag * 5, 1, 0.5, 0, 0.5, 0.2)
						if Thing[8] == 2 then
							Effects["Ring"].Create(Torso.BrickColor, CFrame.new((Thing[4] + pos) / 2, pos) * CFrame.Angles(1.57, 0, 0) * CFrame.fromEulerAnglesXYZ(1.57, 0, 0), 1, 1, 0.1, 0.5, 0.5, 0.1, 0.1, 1)
						end
						Thing[4] = Thing[4] + Look * move
						Thing[3] = Thing[3] - 1
						if 2 < Thing[5] then
							Thing[5] = Thing[5] - 0.3
							Thing[6] = Thing[6] - 0.3
						end
						if hit ~= nil then
							Thing[3] = 0
							if Thing[8] == 1 or Thing[8] == 3 then
								Damage(hit, hit, Thing[5], Thing[6], Thing[7], "Normal", RootPart, 0, "", 1)
							else
								if Thing[8] == 2 then
									Damage(hit, hit, Thing[5], Thing[6], Thing[7], "Normal", RootPart, 0, "", 1)
									if (hit.Parent:findFirstChild("Humanoid")) ~= nil or (hit.Parent.Parent:findFirstChild("Humanoid")) ~= nil then
										ref = CFuncs.Part.Create(workspace, "Neon", 0, 1, BrickColor.new("Really red"), "Reference", Vector3.new())
										ref.Anchored = true
										ref.CFrame = CFrame.new(pos)
										CFuncs["Sound"].Create("161006093", ref, 1, 1.2)
										game:GetService("Debris"):AddItem(ref, 0.2)
										Effects["Block"].Create(Torso.BrickColor, CFrame.new(ref.Position) * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50)), 1, 1, 1, 10, 10, 10, 0.1, 2)
										Effects["Ring"].Create(BrickColor.new("Bright yellow"), CFrame.new(ref.Position) * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50)), 1, 1, 0.1, 4, 4, 0.1, 0.1)
										MagnitudeDamage(ref, 15, Thing[5] / 1.5, Thing[6] / 1.5, 0, "Normal", "", 1)
									end
								end
							end
							ref = CFuncs.Part.Create(workspace, "Neon", 0, 1, BrickColor.new("Really red"), "Reference", Vector3.new())
							ref.Anchored = true
							ref.CFrame = CFrame.new(pos)
							Effects["Sphere"].Create(Torso.BrickColor, CFrame.new(pos), 5, 5, 5, 1, 1, 1, 0.07)
							game:GetService("Debris"):AddItem(ref, 1)
						end
						if Thing[3] <= 0 then
							table.remove(Effects, e)
						end
					end
					do
						do
							if Thing[2] == "FireWave" then
								if Thing[3] <= Thing[4] then
									Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(0, 1, 0)
									Thing[3] = Thing[3] + 1
									Thing[6].Scale = Thing[6].Scale + Vector3.new(Thing[5], 0, Thing[5])
								else
									Part.Parent = nil
									table.remove(Effects, e)
								end
							end
							if Thing[2] ~= "Shoot" and Thing[2] ~= "Wave" and Thing[2] ~= "FireWave" then
								if Thing[1].Transparency <= 1 then
									if Thing[2] == "Block1" then
										Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
										Mesh = Thing[7]
										Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
										Thing[1].Transparency = Thing[1].Transparency + Thing[3]
									else
										if Thing[2] == "Block2" then
											Thing[1].CFrame = Thing[1].CFrame
											Mesh = Thing[7]
											Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
											Thing[1].Transparency = Thing[1].Transparency + Thing[3]
										else
											if Thing[2] == "Fire" then
												Thing[1].CFrame = CFrame.new(Thing[1].Position) + Vector3.new(0, 0.2, 0)
												Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
												Thing[1].Transparency = Thing[1].Transparency + Thing[3]
											else
												if Thing[2] == "Cylinder" then
													Mesh = Thing[7]
													Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
													Thing[1].Transparency = Thing[1].Transparency + Thing[3]
												else
													if Thing[2] == "Blood" then
														Mesh = Thing[7]
														Thing[1].CFrame = Thing[1].CFrame * CFrame.new(0, 0.5, 0)
														Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
														Thing[1].Transparency = Thing[1].Transparency + Thing[3]
													else
														if Thing[2] == "Elec" then
															Mesh = Thing[10]
															Mesh.Scale = Mesh.Scale + Vector3.new(Thing[7], Thing[8], Thing[9])
															Thing[1].Transparency = Thing[1].Transparency + Thing[3]
														else
															if Thing[2] == "Disappear" then
																Thing[1].Transparency = Thing[1].Transparency + Thing[3]
															else
																if Thing[2] == "Shatter" then
														Thing[1].Transparency = Thing[1].Transparency + Thing[3]
														Thing[4] = Thing[4] * CFrame.new(0, Thing[7], 0)
														Thing[1].CFrame = Thing[4] * CFrame.fromEulerAnglesXYZ(Thing[6], 0, 0)
														Thing[6] = Thing[6] + Thing[5]
																end
															end
														end
													end
												end
											end
										end
									end
								else
									Part.Parent = nil
									table.remove(Effects, e)
								end
							end
						end
					end
				end
			end
		end
	end
end
end
end)

TextLabel.Parent = scriptframe
TextLabel.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextLabel.Size = UDim2.new(0, 302, 0, 50)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Scripts"
TextLabel.TextColor3 = Color3.new(0, 1, 1)
TextLabel.TextScaled = true
TextLabel.TextSize = 14
TextLabel.TextWrapped = true

TextButton_2.Parent = scriptframe
TextButton_2.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_2.Position = UDim2.new(0, 0, 0, 102)
TextButton_2.Size = UDim2.new(0, 123, 0, 50)
TextButton_2.Font = Enum.Font.SourceSans
TextButton_2.Text = "Bendy The Demon"
TextButton_2.TextColor3 = Color3.new(0, 1, 1)
TextButton_2.TextScaled = true
TextButton_2.TextSize = 14
TextButton_2.TextWrapped = true

TextButton_2.MouseButton1Down:connect(function()
---------ONE WITH CHEESEEE------------
---------MAKE BY SKRUBL0RDZI------------
p = game.Players.LocalPlayer
char = p.Character
torso = char.Torso
hed = char.Head
neck = char.Torso.Neck
hum = char.Humanoid
hum.MaxHealth = math.huge
local msg = game:GetService("Chat")
torso.BrickColor = BrickColor.new("Really black")
hed.BrickColor = BrickColor.new("White")
char["Right Arm"].BrickColor = BrickColor.new("Really black")
char["Left Arm"].BrickColor = BrickColor.new("Really black")
char["Left Leg"].BrickColor = BrickColor.new("Really black") 
char["Right Leg"].BrickColor = BrickColor.new("Really black")
ypcall(function()
shirt = Instance.new("Shirt", char)
shirt.Name = "Shirt"
pants = Instance.new("Pants", char)
pants.Name = "Pants"
char.Shirt.ShirtTemplate = "rbxassetid://891120125"
char.Pants.PantsTemplate = "rbxassetid://833114068"
end)
function sbchat(msg,displayname)
        if not displayname then
            displayname = '<Bitch Smoke>'
        end
        for i,v in pairs(game:GetService('Players'):GetChildren()) do
            local st = Instance.new('StringValue')
            st.Name = 'SB_Chat'
            st.Value = displayname..'/'..msg
            delay(0.2,function() st.Parent = v end)
        end
    end
p1 = Instance.new("Part",char)
p1.FormFactor = Enum.FormFactor.Custom
p1.Size = Vector3.new(1.8,0.8,1.8)
p1.CanCollide = false
p1.Locked = true
p1.BottomSurface = Enum.SurfaceType.Smooth
p1.TopSurface = Enum.SurfaceType.Smooth
SMesh = Instance.new("SpecialMesh", p1)
SMesh.MeshId = "http://www.roblox.com/asset/?id=715422528"
SMesh.MeshType = Enum.MeshType.FileMesh
SMesh.Name = "Mesh"
SMesh.TextureId = "http://www.roblox.com/asset/?id=899756769"
w1 = Instance.new("Weld", hed)
w1.Part0 = hed
w1.C0 = CFrame.new(0,0.76,0.2)*CFrame.Angles(0.3,0,0)
w1.Part1 = p1
w1.C1 = CFrame.new(0, 0, 0)
--------------------------------
p1 = Instance.new("Part",char)
p1.FormFactor = Enum.FormFactor.Custom
p1.Size = Vector3.new(1.8,0.8,1.8)
p1.CanCollide = false
p1.Locked = true
p1.BrickColor = BrickColor.new("Really black")
p1.BottomSurface = Enum.SurfaceType.Smooth
p1.TopSurface = Enum.SurfaceType.Smooth
SMesh = Instance.new("SpecialMesh", p1)
SMesh.MeshId = "http://www.roblox.com/asset/?id=0"
SMesh.MeshType = Enum.MeshType.FileMesh
SMesh.Name = "Mesh"
w1 = Instance.new("Weld", hed)
w1.Part0 = hed
w1.C0 = CFrame.new(0,0.2,-0.25)
w1.Part1 = p1
w1.C1 = CFrame.new(0, 0, 0)
-----------
GroundWave3 = function()
	local HandCF = CFrame.new(torso.Position - Vector3.new(0,0,0)) * CFrame.Angles(0,0,0)
		local wave1 = Instance.new("Part", torso)
		wave1.BrickColor = BrickColor.new("Really black")
		wave1.Anchored = true
		wave1.CanCollide = false
		wave1.Locked = true
		wave1.Material = "Neon"
		wave1.Size = Vector3.new(1, 1, 1)
		wave1.TopSurface = "Smooth"
		wave1.BottomSurface = "Smooth"
		wave1.Transparency = 0
		wave1.CFrame = HandCF
		wm = Instance.new("SpecialMesh", wave1)
		wm.Scale = Vector3.new(.1,.1,.1)
		wm.MeshType = "Sphere"
		coroutine.wrap(function()
		for i = 1, 20, 1 do
		wm.Scale = Vector3.new(2 + i*2, 2 + i*2, 2 + i*2)
		--wave1.Size = wm.Scale
		wave1.CFrame = HandCF
		wave1.Transparency = i/10
		wait()
		end
		wait()
		wave1:Destroy()
	end)()
end
-------------------------------
Spawn(function()
	while wait(1) do
		GroundWave3()
		wait(.5)
		GroundWave3()
	end
end)
warn'[Ground Brake]:Connect!'
-----------------------------------
local Plr = game.Players.LocalPlayer --LocalScript
	local Char = Plr.Character
	local Mouse = Plr:GetMouse()
	local ra = Char:FindFirstChild('Right Arm')
	local ts = Char.Torso
	local la = Char:FindFirstChild('Left Arm')
	local ll = Char:FindFirstChild('Left Leg')
	local rl = Char:FindFirstChild('Right Leg')
	local hd = Char.Head
	local root = Char:FindFirstChild('HumanoidRootPart')
	
	rarm = ra
	larm = la
	torso = ts
	hed = hd
	root = root
	lleg = ll
	rleg = rl

FloatPart = function()
	local Part = Instance.new('Part',torso)
	Part.CFrame = CFrame.new(torso.CFrame.X,workspace.Base.CFrame.Y+1,torso.CFrame.Z) * CFrame.fromEulerAnglesXYZ(86.4,0,87)
	Part.Anchored = true
	Part.Material = 'Neon'
	Part.CanCollide = false
	Part.BrickColor = BrickColor.new("Really black")
	local Mesh = Instance.new('SpecialMesh',Part)
	Mesh.Scale = Vector3.new(4,4,.2)
	Mesh.MeshId = 'http://www.roblox.com/asset/?id=0'
	Mesh.VertexColor = Vector3.new(0,170,255)
	spawn(function()
		for i = 1,30 do
			Mesh.Scale = Mesh.Scale + Vector3.new(.04,.04,0)
			Part.Transparency = Part.Transparency + .035
			game["Run Service"].RenderStepped:wait()
		end
		Part:Destroy()
	end)
end;

DubPart = function()
	local Part = Instance.new('Part',torso)
	Part.CFrame = CFrame.new(torso.CFrame.X,workspace.Base.CFrame.Y+1,torso.CFrame.Z) * CFrame.fromEulerAnglesXYZ(86.4,0,87)
	Part.Anchored = true
	Part.CanCollide = false
	Part.Material = 'Neon'
	Part.BrickColor = BrickColor.new("Really black")
	local Mesh = Instance.new('SpecialMesh',Part)
	Mesh.Scale = Vector3.new(7,7,.2)
	Mesh.MeshId = 'http://www.roblox.com/asset/?id=0'
	Mesh.VertexColor = Vector3.new(0,170,255)
	spawn(function()
		for i = 1,30 do
			Mesh.Scale = Mesh.Scale + Vector3.new(.04,.04,0)
			Part.Transparency = Part.Transparency + .035
			game["Run Service"].RenderStepped:wait()
		end
		Part:Destroy()
	end)
end;

OnTouch = function(Toucher)
	if Toucher.Parent.Name ~= Plr.Name and Toucher.Parent:FindFirstChild('Humanoid') then
		local Hum = Toucher.Parent:FindFirstChild('Humanoid')
		Hum.Health = Hum.Health - .7		
	end
end;

Fade = function(Item,t)
	spawn(function()
		for i = 1,20 do
			Item.Transparency = Item.Transparency + .05
			if t then
				wait(t)
			else 
				wait()
			end
		end
		Item:Destroy()
	end)
end

TouchKill = function(Toucher)
	if Toucher.Parent then
		if Toucher.Parent:FindFirstChild('Humanoid') then
			local P = Toucher.Parent:FindFirstChild('Humanoid')
			if P ~= nil and P.Parent.Name ~= Plr.Name then
				P.Health = P.Health - math.random(4,17)
			end
		end
	end
end;

Particle = function()
	local Part = Instance.new('Part',torso)
	Part.Anchored = true
	Part.Transparency = 0
	Part.Material = "Neon"
	Part.Touched:connect(function(I)OnTouch(I)end)
	Part.CanCollide = false
	Part.CFrame = torso.CFrame * CFrame.new(math.random(-10,10),math.random(-15,15),math.random(-10,10)) * CFrame.fromEulerAnglesXYZ(math.random(),math.random(),math.random())
	local Mesh = Instance.new('SpecialMesh',Part)
	Mesh.Scale = Vector3.new(1,1,1)
	Mesh.MeshId = "rbxassetid://0"
	Mesh.TextureId = "rbxassetid://0"
	spawn(function()
		for i = 1,40 do
			Part.Transparency = Part.Transparency + .0125
			Part.CFrame = Part.CFrame * CFrame.new(0,-.07,0)
			game["Run Service"].RenderStepped:wait()
		end
		Part:Destroy()
	end)
end;

Particle2 = function()
	local Part = Instance.new('Part',torso)
	Part.Anchored = true
	Part.Transparency = 0
	Part.Material = "Neon"
	Part.Touched:connect(function(I)OnTouch(I)end)
	Part.CanCollide = false
	Part.CFrame = torso.CFrame * CFrame.new(math.random(-10,10),math.random(-15,15),math.random(-10,10)) * CFrame.fromEulerAnglesXYZ(math.random(),math.random(),math.random())
	local Mesh = Instance.new('SpecialMesh',Part)
	Mesh.Scale = Vector3.new(1.5,1.5,1.5)
	Mesh.MeshId = "rbxassetid://0"
	Mesh.TextureId = "rbxassetid://0"
	spawn(function()
		for i = 1,40 do
			Part.Transparency = Part.Transparency + .0125
			Part.CFrame = Part.CFrame * CFrame.new(0,-.07,0)
			game["Run Service"].RenderStepped:wait()
		end
		Part:Destroy()
	end)
end;

spawn(function()
	while wait() do
		wait(.05)
		FloatPart()
		wait(.08)
		FloatPart()
		wait(.05)
		DubPart()
		wait(.08)
	end
end)
spawn(function()
	while wait() do
		Particle()
		wait(0.75)
		Particle2()
	end
end)
-------------
hed.face.Texture = "http://www.roblox.com/asset/?id=829370852"
game.Chat:Chat(game.Players.LocalPlayer.Character.Head,"I'M BACK CJ. LET'S ME FLOW DAT DAMN TRAIN!", "Red")
sbchat("I'M BACK CJ. LET'S ME FLOW DAT DAMN TRAIN!",'[Bendy The Demon]')
local HBill = Instance.new("BillboardGui", hed)
local HMain, HBarBack, HBar = Instance.new("Frame", HBill), Instance.new("Frame"), Instance.new("Frame")
local HHealth, HName = Instance.new("TextLabel", HBarBack), Instance.new("TextLabel")
HBill.Size = UDim2.new(15,0,2.2,0)
HBill.Name = "Health Display"
HBill.StudsOffset = Vector3.new(0,4,0)
HBill.AlwaysOnTop = true
HBill.Enabled = true
HMain.BackgroundColor3 = Color3.new(0, 0, 0)
HMain.BackgroundTransparency = 0.6
HMain.Size = UDim2.new(1,0,1,0)
HBarBack.Parent = HMain
HBarBack.BackgroundColor3 = Color3.new(0,0,0)
HBarBack.BorderColor3 = Color3.new(0,0,0)
HBarBack.BorderSizePixel = 2
HBarBack.Position = UDim2.new(.025, 0, .55, 0)
HBarBack.Size = UDim2.new(.95, 0, .3, 0)
HHealth.BackgroundTransparency = 1
HHealth.Size = UDim2.new(1,0,1,0)
HHealth.Font = "Code"
HHealth.Text = "1.#INF"
HHealth.TextScaled = true
HHealth.TextColor3 = Color3.new(1,1,1)
HHealth.TextStrokeColor3 = BrickColor.new("Really black").Color
HHealth.TextStrokeTransparency = 0
HName.Parent = HMain
HName.BackgroundTransparency = 1
HName.Size = UDim2.new(1,0,.5,0)
HName.Font = "Code"
HName.Text = "Bendy The Demon"
HName.TextScaled = true
HName.TextColor3 = BrickColor.new("Really black").Color
HName.TextStrokeColor3 = Color3.new(0,0,0)
HName.TextStrokeTransparency = 0
HName.TextYAlignment = "Top"

  plr = game.Players.LocalPlayer
  local s = Instance.new("Sound",plr.Character)
s.Volume = 3
s.Looped = true
s.Pitch = 1
s.SoundId = "rbxassetid://759795246"
s:Play()
  repeat
    wait(0.4)
  until plr.Character
  chr = plr.Character
  human = chr:FindFirstChild("Humanoid")
  mouse = plr:GetMouse()
  cam = workspace.CurrentCamera
  selected = false
  equipd = false
  tors = chr.Torso
  rarm = chr["Right Arm"]
  larm = chr["Left Arm"]
  rleg = chr["Right Leg"]
  lleg = chr["Left Leg"]
  hrp = chr.HumanoidRootPart
  hed = chr.Head
  anim = human.Animator
  activu = false
  ragged = false
  batting = false
  Heartbeat = Instance.new("BindableEvent")
  Heartbeat.Name = "Heartbeat"
  Heartbeat.Parent = script
  frame = 0.03333333333333333
  tf = 0
  game:GetService("RunService").Heartbeat:connect(function(s, p)
    tf = tf + s
    if tf >= frame then
      for i = 1, math.floor(tf / frame) do
        Heartbeat:Fire()
      end
      tf = tf - frame * math.floor(tf / frame)
    end
  end)
  function swait(num)
    if num == 0 or num == nil then
      Heartbeat.Event:wait()
    else
      for i = 1, num do
        Heartbeat.Event:wait()
      end
    end
  end
  tool = Instance.new("Tool")
  tool.CanBeDropped = false
  tool.RequiresHandle = false
  tool.ToolTip = "NANI BIG SMOKE??????"
  tool.Name = "PRESS X TO USING ME BITC"
  tool.Parent = plr.Backpack
  modz = Instance.new("Model")
  modz.Name = "efx"
  modz.Parent = chr
  RSC0 = CFrame.new(1, 0.5, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RSC1 = CFrame.new(-0.5, 0.5, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LSC0 = CFrame.new(-1, 0.5, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  LSC1 = CFrame.new(0.5, 0.5, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  RHC0 = CFrame.new(1, -1, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RHC1 = CFrame.new(0.5, 1, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LHC0 = CFrame.new(-1, -1, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  RJC1 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  LHC1 = CFrame.new(-0.5, 1, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  NC0 = CFrame.new(0, 1, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  NC1 = CFrame.new(0, -0.5, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  RJC0 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  local nscale = Instance.new("NumberValue")
  nscale.Value = 1
  nscale.Parent = nil
  RightShoulderC0 = CFrame.new(1.5 * nscale.Value, 0.5 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RightShoulderC1 = CFrame.new(0, 0.5 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LeftShoulderC0 = CFrame.new(-1.5 * nscale.Value, 0.5 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  LeftShoulderC1 = CFrame.new(0, 0.5 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  RightHipC0 = CFrame.new(0.5 * nscale.Value, -1 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RightHipC1 = CFrame.new(0, 1 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LeftHipC0 = CFrame.new(-0.5 * nscale.Value, -1 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  LeftHipC1 = CFrame.new(0 * nscale.Value, 1 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  RootJointC0 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  RootJointC1 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  NeckC0 = CFrame.new(0, 1 * nscale.Value, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  NeckC1 = CFrame.new(0, -0.5 * nscale.Value, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  nscale.Changed:connect(function()
    RightShoulderC0 = CFrame.new(1.5 * nscale.Value, 0.5 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
    RightShoulderC1 = CFrame.new(0, 0.5 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
    LeftShoulderC0 = CFrame.new(-1.5 * nscale.Value, 0.5 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    LeftShoulderC1 = CFrame.new(0, 0.5 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    RightHipC0 = CFrame.new(0.5 * nscale.Value, -1 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
    RightHipC1 = CFrame.new(0, 1 * nscale.Value, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
    LeftHipC0 = CFrame.new(-0.5 * nscale.Value, -1 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    LeftHipC1 = CFrame.new(0 * nscale.Value, 1 * nscale.Value, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    RootJointC0 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
    RootJointC1 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
    NeckC0 = CFrame.new(0, 1 * nscale.Value, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
    NeckC1 = CFrame.new(0, -0.5 * nscale.Value, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  end)
  RS = tors:FindFirstChild("Right Shoulder")
  LS = tors:FindFirstChild("Left Shoulder")
  RH = tors:FindFirstChild("Right Hip")
  LH = tors:FindFirstChild("Left Hip")
  RJ = hrp:FindFirstChild("RootJoint")
  N = tors:FindFirstChild("Neck")
  cf = CFrame.new
  ang = CFrame.Angles
  rd = math.rad
  rd2 = math.random
  function nooutline(p)
    p.TopSurface, p.BottomSurface, p.LeftSurface, p.RightSurface, p.FrontSurface, p.BottomSurface = 10, 10, 10, 10, 10, 10
  end
  function makepart(color, name, reflec, trans, mater, parnt, cfram)
    local port = Instance.new("Part")
    port.BrickColor = BrickColor.new(color)
    port.Name = name
    port.Transparency = trans
    nooutline(port)
    port.Reflectance = reflec
    port.Material = mater
    port.Anchored = false
    port.CanCollide = false
    port.Locked = true
    port.Size = Vector3.new(0.2, 0.2, 0.2)
    port.Parent = parnt
    return port
  end
  function makemesh(meshtype, scale, meshid, parent)
    local mes = Instance.new("SpecialMesh")
    mes.MeshType = meshtype
    mes.Scale = scale
    if meshtype == "FileMesh" then
      mes.MeshId = meshid
    end
    mes.Parent = parent
    return mes
  end
  function makeweld(parent, p0, p1, c0, c1)
    local wel = Instance.new("Weld")
    wel.Part0 = p0
    wel.Part1 = p1
    wel.C0 = c0
    if c1 ~= nil then
      wel.C1 = c1
    end
    wel.Parent = parent
    return wel
  end
  local lauf1 = Instance.new("Sound")
  lauf1.SoundId = "rbxassetid://138199573"
  lauf1.Volume = 5
  lauf1.Pitch = 1
  lauf1.Parent = hrp
  function lerpz(joint, prop, cfrmz, alp)
    joint[prop] = joint[prop]:lerp(cfrmz, alp)
  end
  lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
  function resetlerp()
    RJ.C0 = RJC0
    RJ.C1 = RJC1
    N.C0 = NC0
    N.C1 = NC1
    RS.C0 = RSC0
    RS.C1 = RSC1
    LS.C0 = LSC0
    LS.C1 = LSC1
    RH.C0 = RHC0
    RH.C1 = RHC1
    LH.C0 = LHC0
    LH.C1 = LHC1
  end
  function test()
    if selected == false or activu == true then
      return
    end
    if ragged == false then
      ragged = true
      human.PlatformStand = true
      if rarm and tors:FindFirstChild("Right Shoulder") then
        tors:FindFirstChild("Right Shoulder"):Destroy()
        makegloo(tors, RightShoulderC0, RightShoulderC1, tors, rarm, "Right Shoulder")
        maketouchy(rarm, rarm, CFrame.new(0, 0.5, 0))
      end
      if larm and tors:FindFirstChild("Left Shoulder") then
        tors:FindFirstChild("Left Shoulder"):Destroy()
        makegloo(tors, LeftShoulderC0, LeftShoulderC1, tors, larm, "Left Shoulder")
        maketouchy(larm, larm, CFrame.new(0, 0.5, 0))
      end
      if rleg and tors:FindFirstChild("Right Hip") then
        tors:FindFirstChild("Right Hip"):Destroy()
        makegloo(tors, RightHipC0, RightHipC1, tors, rleg, "Right Hip")
        maketouchy(rleg, rleg, CFrame.new(0, 0.5, 0))
      end
      if lleg and tors:FindFirstChild("Left Hip") then
        tors:FindFirstChild("Left Hip"):Destroy()
        makegloo(tors, LeftHipC0, LeftHipC1, tors, lleg, "Left Hip")
        maketouchy(lleg, lleg, CFrame.new(0, 0.5, 0))
        HName.Text = "Died"
      end
    elseif ragged == true then
      ragged = false
      human.Jump = true
      if rarm and tors:FindFirstChild("Right Shoulder") then
        tors:FindFirstChild("Right Shoulder"):Destroy()
        makejoint(tors, RSC0, RSC1, tors, rarm, "Right Shoulder")
        rarm:FindFirstChild("touchy"):Destroy()
      end
      if larm and tors:FindFirstChild("Left Shoulder") then
        tors:FindFirstChild("Left Shoulder"):Destroy()
        makejoint(tors, LSC0, LSC1, tors, larm, "Left Shoulder")
        larm:FindFirstChild("touchy"):Destroy()
      end
      if rleg and tors:FindFirstChild("Right Hip") then
        tors:FindFirstChild("Right Hip"):Destroy()
        makejoint(tors, RHC0, RHC1, tors, rleg, "Right Hip")
        rleg:FindFirstChild("touchy"):Destroy()
      end
      if lleg and tors:FindFirstChild("Left Hip") then
        tors:FindFirstChild("Left Hip"):Destroy()
        makejoint(tors, LHC0, LHC1, tors, lleg, "Left Hip")
        lleg:FindFirstChild("touchy"):Destroy()
      end
      RS = tors:FindFirstChild("Right Shoulder")
      LS = tors:FindFirstChild("Left Shoulder")
      RH = tors:FindFirstChild("Right Hip")
      LH = tors:FindFirstChild("Left Hip")
      RJ = hrp:FindFirstChild("RootJoint")
      N = tors:FindFirstChild("Neck")
      HName.Text = "Bendy The Demon"
    end
  end
  function makegloo(paren, co, ci, parto, parti, nam)
    local gloo = Instance.new("Glue")
    gloo.Name = nam
    gloo.C0 = co
    gloo.C1 = ci
    gloo.Part0 = parto
    gloo.Part1 = parti
    gloo.Parent = paren
  end
  function makejoint(paren, co, ci, parto, parti, nam)
    local gloo = Instance.new("Motor6D")
    gloo.Name = nam
    gloo.C0 = co
    gloo.C1 = ci
    gloo.Part0 = parto
    gloo.Part1 = parti
    gloo.Parent = paren
  end
  function maketouchy(parent, limb, cframe)
    local pr = Instance.new("Part")
    pr.Name = "touchy"
    pr.Size = Vector3.new(1 * nscale.Value, 1 * nscale.Value, 1 * nscale.Value)
    pr.Transparency = 1
    pr.CustomPhysicalProperties = PhysicalProperties.new(0.55, 0.3, 0.5)
    pr.CanCollide = true
    pr.Anchored = false
    pr.Parent = parent
    local w = Instance.new("Weld")
    w.Part0 = pr
    w.Part1 = limb
    w.C0 = cframe
    w.Parent = pr
  end
  local clibat, spec
  local dipperhat = chr:FindFirstChild("DXD_DipperHat")
  local dipperrot
  if dipperhat then
    dipperrot = dipperhat.Handle.HatAttachment.Rotation
  end
  function bat()
    if selected == false or activu == true then
      return
    end
    if batting == false then
      batting = true
      do
        local bmod = Instance.new("Model")
        bmod.Name = "bmodel"
        bmod.Parent = chr
        local hnd = makepart("Really black", "hnd", 0, 1, "Neon", bmod, rarm.CFrame)
        local hmes = makemesh("1", Vector3.new(2, 9, 2), nil, hnd)
        local hwel = makeweld(hnd, hnd, rarm, ang(rd(90), rd(0), rd(0)) * cf(0, 1, 0), nil)
        local pt1 = makepart("Really black", "pt1", 0, 1, "Neon", bmod, rarm.CFrame)
        local p1m = makemesh("Sphere", Vector3.new(3,3,3), nil, pt1)
        local p1w = makeweld(pt1, pt1, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, 1, 0), nil)
        local pt3 = makepart("Really black", "pt3", 0, 1, "Neon", bmod, rarm.CFrame)
        local p3m = makemesh("1", Vector3.new(1, 6, 1), nil, pt3)
        local p3w = makeweld(pt3, pt3, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, -1, 0), nil)
        local pt4 = makepart("Really black", "pt4", 0, math.rad(0,1), "Neon", bmod, rarm.CFrame)
        local p4m = makemesh("FileMesh", Vector3.new(2,2,2), "http://www.roblox.com/asset/?id=777371122", pt4)
        p4m.TextureId = "http://www.roblox.com/asset/?id=777371154"
        p4m.Scale = Vector3.new(2,2,2)
        local p4w = makeweld(pt4, pt4, hnd, ang(rd(90), rd(0), rd(0)) * cf(0, -1.5, 0), nil)
        local pt5 = makepart("Really black", "pt5", 0, 1, "Neon", bmod, rarm.CFrame)
        local p5m = makemesh("Cylinder", Vector3.new(25, 1.5, 1.5), nil, pt5)
        local p5w = makeweld(pt5, pt5, hnd, ang(rd(0), rd(0), rd(90)) * cf(0, -4.025, 0), nil)
        local swingwoo = Instance.new("Sound")
        swingwoo.SoundId = "rbxassetid://201858024"
        swingwoo.Pitch = rd2(10, 11) / 10
        swingwoo.Name = "sweae"
        swingwoo.Volume = 1
        swingwoo.Parent = hrp
        clibat = tool.Activated:connect(function()
          if selected == false or activu == true or ragged == true then
            return
          end
          activu = true
          for _ = 1, 5 do
            swait()
            lerpz(RJ, "C0", RJC0 * cf(0, 0.5, 0) * ang(rd(-20), rd(10), rd(-40)), 0.7)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(20), rd(-20), rd(179)), 0.7)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-20), rd(20), rd(30)), 0.7)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-30)), 0.7)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-110)), 0.7)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
          end
          local bon = Instance.new("Sound")
          bon.SoundId = "rbxassetid://201858024"
          bon.Pitch = rd2(10, 12) / 10
          bon.Volume = 1
          bon.Parent = hrp
          game.Debris:AddItem(bon, 1)
          bon:Play()
          swingwoo:Play()
          for X = 1, 5 do
            swait()
            if X > 1 then
              hito(pt5, 5, 80, 0.2, hrp.CFrame.lookVector * 0, Vector3.new(0, rd2(-5, 5), rd2(-40, 40)))
            end
            lerpz(RJ, "C0", RJC0 * cf(0, -0.5, 0) * ang(rd(60), rd(-10), rd(30)), 0.7)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(20), rd(20), rd(40)), 0.7)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-70), rd(20), rd(30)), 0.7)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(20), rd(-40), rd(80)), 0.7)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
            lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(60)), 0.7)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
          end
          activu = false
        end)
        spec = mouse.KeyDown:connect(function(keya)
          if selected == false or activu == true or ragged == true then
            return
          end
          if keya == "]]" then
            activu = true
            local speed = human.WalkSpeed
            human.WalkSpeed = 0
            human:SetStateEnabled(3, false)
            local function expa()
              local sond = Instance.new("Sound")
              sond.Volume = 1.25
              sond.Pitch = 1
              sond.EmitterSize = 15
              sond.SoundId = "rbxassetid://201858024"
              sond.Parent = pt6
              sond:Play()
              for _ = 1, 3 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(6, 27, 6), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(7.5, 7.5, 7.5), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 3, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(7.5, 7.5, 7.5), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -3, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.07500000000000001, 0.07500000000000001, 0.07500000000000001), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -3.75, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(64.5, 18.75, 18.75), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -12.075000000000001, 0), 0.7)
              end
              for _ = 1, 5 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(4, 18, 4), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(5, 5, 5), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 2, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(5, 5, 5), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -2, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.05, 0.05, 0.05), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -2.5, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(63, 12.5, 12.5), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -8.05, 0), 0.7)
              end
              sond.Pitch = 0.75
              sond:Play()
              for _ = 1, 3 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(12, 54, 12), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(15, 15, 15), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 6, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(15, 15, 15), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -6, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.15000000000000002, 0.15000000000000002, 0.15000000000000002), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -7.5, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(156, 37.5, 37.5), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -24.150000000000002, 0), 0.7)
              end
              for _ = 1, 5 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(8, 36, 8), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(10, 10, 10), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 4, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(10, 10, 10), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -4, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.1, 0.1, 0.1), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -5, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(102, 25, 25), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -16.1, 0), 0.7)
              end
              sond.Pitch = 0.4
              sond:Play()
              game.Debris:AddItem(sond, 2)
              for _ = 1, 3 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(18, 81, 18), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(22.5, 22.5, 22.5), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 9, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(22.5, 22.5, 22.5), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -9, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.225, 0.225, 0.225), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -11.25, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(230.2, 56.25, 56.25), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -36.225, 0), 0.7)
              end
              for _ = 1, 5 do
                swait()
                hmes.Scale = hmes.Scale:lerp(Vector3.new(14, 63, 14), 0.7)
                p1m.Scale = p1m.Scale:lerp(Vector3.new(17.5, 17.5, 17.5), 0.7)
                p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 7, 0), 0.7)
                p3m.Scale = p3m.Scale:lerp(Vector3.new(17.5, 17.5, 17.5), 0.7)
                p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -7, 0), 0.7)
                p4m.Scale = p4m.Scale:lerp(Vector3.new(0.17500000000000002, 0.17500000000000002, 0.17500000000000002), 0.7)
                p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -8.75, 0), 0.7)
                p5m.Scale = p5m.Scale:lerp(Vector3.new(400, 43.75, 43.75), 0.7)
                p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -30, 0), 0.7)
              end
            end
            for _ = 1, 3 do
              swait()
              lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(-5), rd(0), rd(0)), 0.5)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.5)
              lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-20), rd(0), rd(-10)), 0.5)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(LS, "C0", LSC0 * cf(0, 0.2, -0.2) * ang(rd(70), rd(-60), rd(-100)), 0.5)
              if dipperhat then
                dipperhat.Handle.HatAttachment.Rotation = dipperhat.Handle.HatAttachment.Rotation:lerp(dipperrot + Vector3.new(0, 0, 0), 0.3)
              end
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-10)), 0.5)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-10), rd(-10)), 0.5)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
            end
            for _ = 1, 3 do
              swait()
              lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(-5), rd(0), rd(0)), 0.5)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.5)
              lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-20), rd(0), rd(-10)), 0.5)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(35), rd(-50), rd(-100)), 0.3)
              if dipperhat then
                dipperhat.Handle.HatAttachment.Rotation = dipperhat.Handle.HatAttachment.Rotation:lerp(dipperrot + Vector3.new(15, 0, 0), 0.3)
              end
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-10)), 0.5)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
              lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-10), rd(-10)), 0.5)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
            end
            for _ = 1, 30 do
              swait()
              lerpz(RJ, "C0", RJC0 * cf(1.1, 0.6, 0) * ang(rd(0), rd(0), rd(-120)), 0.2)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(-20)), 0.2)
              lerpz(RS, "C0", RSC0 * cf(0, 0.4, 0.2) * ang(rd(80), rd(-20), rd(80)), 0.2)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.2)
              lerpz(LS, "C0", LSC0 * cf(0, -0.2, -0.7) * ang(rd(-20), rd(-60), rd(-80)), 0.2)
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.2)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-5)), 0.2)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.2)
              lerpz(LH, "C0", LHC0 * cf(0.4, 0, -0.4) * ang(rd(-10), rd(70), rd(-5)), 0.2)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.2)
            end
            expa()
            for O = 1, 10 do
              swait()
              lerpz(RJ, "C0", RJC0 * cf(0, 0.3, 0) * ang(rd(0), rd(0), rd(60)), 0.001 + O * 0.01)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(-20)), 0.001 + O * 0.01)
              lerpz(RS, "C0", RSC0 * cf(0, 0.4, 0.2) * ang(rd(80), rd(-20), rd(80)), 0.001 + O * 0.01)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.001 + O * 0.01)
              lerpz(LS, "C0", LSC0 * cf(0, -0.2, -0.7) * ang(rd(-20), rd(-60), rd(-80)), 0.001 + O * 0.01)
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.001 + O * 0.01)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-5)), 0.001 + O * 0.01)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.001 + O * 0.01)
              lerpz(LH, "C0", LHC0 * cf(0.4, 0, -0.4) * ang(rd(-10), rd(70), rd(-5)), 0.001 + O * 0.01)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.001 + O * 0.01)
            end
            local whoooo = Instance.new("Sound")
            whoooo.Volume = 3
            whoooo.Pitch = 1.1
            whoooo.SoundId = "rbxassetid://201858024"
            whoooo.Parent = pt5
            whoooo:Play()
            game.Debris:AddItem(whoooo, 2)
            for O = 1, 1 do
              swait()
              hito(pt5, 70, 808282854, 0.75, hrp.CFrame.rightVector * -10000000 + Vector3.new(0, 50, 0), Vector3.new(0, rd2(-25, 25), rd2(-160, 160)))
              lerpz(RJ, "C0", RJC0 * cf(0.9, -0.7, 0) * ang(rd(0), rd(0), rd(120)), 0.1 + O * 0.05)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(-20)), 0.1 + O * 0.05)
              lerpz(RS, "C0", RSC0 * cf(0, 0.4, 0.2) * ang(rd(80), rd(20), rd(20)), 0.1 + O * 0.05)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + O * 0.05)
              lerpz(LS, "C0", LSC0 * cf(0, -0.2, -0.7) * ang(rd(-20), rd(-60), rd(-80)), 0.1 + O * 0.05)
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + O * 0.05)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-5)), 0.1 + O * 0.05)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + O * 0.05)
              lerpz(LH, "C0", LHC0 * cf(0.4, 0, -0.4) * ang(rd(-10), rd(70), rd(-5)), 0.1 + O * 0.05)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + O * 0.05)
            end
            for O = 1, 13 do
              swait()
              hmes.Scale = hmes.Scale:lerp(Vector3.new(2, 9, 2), 0.05 + O * 0.075)
              p1m.Scale = p1m.Scale:lerp(Vector3.new(2.5, 2.5, 2.5), 0.05 + O * 0.075)
              p1w.C0 = p1w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, 1, 0), 0.05 + O * 0.075)
              p3m.Scale = p3m.Scale:lerp(Vector3.new(2.5, 2.5, 2.5), 0.05 + O * 0.075)
              p3w.C0 = p3w.C0:lerp(ang(rd(0), rd(0), rd(0)) * cf(0, -1, 0), 0.05 + O * 0.075)
              p4m.Scale = p4m.Scale:lerp(Vector3.new(0.025, 0.025, 0.025), 0.05 + O * 0.075)
              p4w.C0 = p4w.C0:lerp(ang(rd(180), rd(0), rd(0)) * cf(0, -1.25, 0), 0.05 + O * 0.075)
              p5m.Scale = p5m.Scale:lerp(Vector3.new(21.5, 1, 1), 0.05 + O * 0.075)
              p5w.C0 = p5w.C0:lerp(ang(rd(0), rd(0), rd(90)) * cf(0, -4.025, 0), 0.05 + O * 0.075)
              lerpz(RJ, "C0", RJC0 * cf(1.1, -0.8, 0) * ang(rd(0), rd(0), rd(150)), 0.05 + O * 0.075)
              lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(-20)), 0.05 + O * 0.075)
              lerpz(RS, "C0", RSC0 * cf(0, 0.4, 0.2) * ang(rd(80), rd(30), rd(10)), 0.05 + O * 0.075)
              lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.05 + O * 0.075)
              lerpz(LS, "C0", LSC0 * cf(0, -0.2, -0.7) * ang(rd(20), rd(20), rd(-20)), 0.05 + O * 0.075)
              lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.05 + O * 0.075)
              lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-5)), 0.05 + O * 0.075)
              lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.05 + O * 0.075)
              lerpz(LH, "C0", LHC0 * cf(0.4, 0, -0.4) * ang(rd(-10), rd(70), rd(-5)), 0.05 + O * 0.075)
              lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.05 + O * 0.075)
            end
            if dipperhat then
              dipperhat.Handle.HatAttachment.Rotation = dipperrot
            end
            human.WalkSpeed = speed
            human:SetStateEnabled(3, true)
            activu = false
          end
          if keya == "q" then
            activu = true
            do
              local checkkey = true
              local keyingup = mouse.KeyUp:connect(function(xzx)
                if xzx == "q" then
                  checkkey = false
                end
              end)
              repeat
                for _ = 1, 2 do
                  swait()
                  lerpz(RJ, "C0", RJC0 * cf(0, 0.5, 0) * ang(rd(-20), rd(10), rd(-40)), 0.7)
                  lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(20), rd(0), rd(0)), 0.7)
                  lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(30), rd(-20), rd(80)), 0.7)
                  lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-20), rd(20), rd(30)), 0.7)
                  lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-30)), 0.7)
                  lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-110)), 0.7)
                  lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                end
                swingwoo:Play()
                for T = 1, 2 do
                  swait()
                  if T == 2 then
                    hito(pt5, 7, 30, 0.03, hrp.CFrame.lookVector * 0, Vector3.new(0, rd2(-2, 2), rd2(-10, 10)))
                  end
                  lerpz(RJ, "C0", RJC0 * cf(0, -0.5, 0) * ang(rd(60), rd(-10), rd(30)), 0.7)
                  lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(20), rd(40), rd(40)), 0.7)
                  lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-70), rd(20), rd(30)), 0.7)
                  lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(20), rd(-40), rd(80)), 0.7)
                  lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(60)), 0.7)
                  lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                end
                for _ = 1, 2 do
                  swait()
                  lerpz(RJ, "C0", RJC0 * cf(0, 0.5, 0) * ang(rd(-30), rd(20), rd(0)), 0.7)
                  lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(20), rd(0), rd(0)), 0.7)
                  lerpz(RS, "C0", RSC0 * cf(0, 0.5, 0) * ang(rd(60), rd(20), rd(179)), 0.7)
                  lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-40), rd(20), rd(30)), 0.7)
                  lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-30)), 0.7)
                  lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-30), rd(20), rd(35)), 0.7)
                  lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                end
                swingwoo:Play()
                for T = 1, 2 do
                  swait()
                  if T == 2 then
                    hito(pt5, 7, 30, 0.03, hrp.CFrame.lookVector * 0, Vector3.new(0, rd2(-2, 2), rd2(-10, 10)))
                  end
                  lerpz(RJ, "C0", RJC0 * cf(0, -0.5, 0) * ang(rd(40), rd(40), rd(0)), 0.7)
                  lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(20), rd(0), rd(0)), 0.7)
                  lerpz(RS, "C0", RSC0 * cf(0, 0.5, 0) * ang(rd(60), rd(20), rd(30)), 0.7)
                  lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-70), rd(20), rd(30)), 0.7)
                  lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-10), rd(10), rd(-30)), 0.7)
                  lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                  lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-30), rd(20), rd(-65)), 0.7)
                  lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.7)
                end
              until not checkkey
              keyingup:Disconnect()
              activu = false
            end
          end
          if keya == "f" then
            activu = true
            do
              local speed = human.WalkSpeed
              human.WalkSpeed = 2
              human:SetStateEnabled(3, false)
              local checkkey = true
              local chargecounter = 0
              local keyingup = mouse.KeyUp:connect(function(xzx)
                if xzx == "f" then
                  checkkey = false
                end
              end)
              local firederp
              for _ = 1, 8 do
                swait()
                hwel.C0 = hwel.C0:lerp(ang(rd(65), rd(0), rd(0)) * cf(0, 1, 0), 0.6)
                lerpz(RJ, "C0", RJC0 * cf(0.5, 0.5, 0) * ang(rd(0), rd(0), rd(-70)), 0.5)
                lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(60)), 0.5)
                lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(70), rd(-10), rd(80)), 0.5)
                lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
                lerpz(LS, "C0", LSC0 * cf(-0.3, -0.1, -1) * ang(rd(-10), rd(-70), rd(-75)), 0.5)
                lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(-20), rd(0)), 0.5)
                lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-5), rd(-10), rd(5)), 0.5)
                lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.5)
                lerpz(LH, "C0", LHC0 * cf(0.5, 0, -0.4) * ang(rd(0), rd(80), rd(-5)), 0.5)
                lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(0)), 0.5)
              end
              repeat
                swait()
                chargecounter = chargecounter + 1
                lerpz(RS, "C0", RSC0 * cf(rd2(-5, 5) / 100, rd2(-5, 5) / 100, rd2(-5, 5) / 100) * ang(rd(rd2(65, 75)), rd(rd2(-15, 5)), rd(rd2(75, 85))), 0.05 + chargecounter * 0.019)
                lerpz(LS, "C0", LSC0 * cf(-0.3, -0.1, -1) * ang(rd(rd2(-15, -5)), rd(rd2(-75, -65)), rd(rd2(-80, -70))), 0.05 + chargecounter * 0.019)
                lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(rd2(-25, -15)), rd(0)), 0.05 + chargecounter * 0.019)
                if chargecounter > 30 and firederp == nil then
					local colorKeyPoints={ColorSequenceKeypoint.new(0,Color3.new(1,1,1)),
						ColorSequenceKeypoint.new(1,Color3.new(1,1,1))
					}
					local sizeKeyPoints={NumberSequenceKeypoint.new(0,.25),
						NumberSequenceKeypoint.new(1,1),
						NumberSequenceKeypoint.new(1,0)
					}
					local opacityKeyPoints={NumberSequenceKeypoint.new(0,0);
						NumberSequenceKeypoint.new(.793,0);
					NumberSequenceKeypoint.new(1,1);
					}
					local runRing=Instance.new('ParticleEmitter',pt1)
					runRing.LightEmission=0
					runRing.Color=ColorSequence.new(colorKeyPoints)
					runRing.Size=NumberSequence.new(sizeKeyPoints)
					runRing.Texture='rbxassetid://0'
					runRing.LockedToPart = false
					runRing.Transparency=NumberSequence.new(opacityKeyPoints)
					runRing.Lifetime=NumberRange.new(1,2)
					runRing.Rate=100
					runRing.Rotation=NumberRange.new(0,360)
					runRing.RotSpeed=NumberRange.new(-20,20)
					runRing.Speed=NumberRange.new(4)
					runRing.VelocitySpread=10
					wait(.1)
					runRing.Enabled = false
                end
              until not checkkey or chargecounter > 50
              swingwoo:Play()
              sbchat("THE POWER OF CHEESEEEEE!!!!!!!!!",'[Bendy The Demon]')
              game.Chat:Chat(game.Players.LocalPlayer.Character.Head,"THE POWER OF CHEESEEEEE!!!!!!!!", "Red")
              for U = 1, 10 do
                swait()
                if U < 3 then
                  hito(pt5, 8, math.huge, 0.2, hrp.CFrame.lookVector * (math.huge + chargecounter * math.huge) + Vector3.new(0, 6 + 6 * (chargecounter / 5), 0), Vector3.new(0, rd2(-25, 25) * (chargecounter / 25), rd2(-80, 80) * (chargecounter / 25)))
                  if chargecounter > 30 then
                    tagexplode(pt5, 5, 1)
                  end
                end
                hwel.C0 = hwel.C0:lerp(ang(rd(135), rd(0), rd(0)) * cf(0, 1, 0), 0.6)
                lerpz(RJ, "C0", RJC0 * cf(0.5, -0.5, 0) * ang(rd(0), rd(0), rd(50)), 0.6)
                lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-5), rd(0), rd(-30)), 0.6)
                lerpz(RS, "C0", RSC0 * cf(0.75, 0.5, -0.5) * ang(rd(0), rd(60), rd(120)), 0.4)
                lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(100), rd(0)), 0.4)
                lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-10), rd(20), rd(-125)), 0.4)
                lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(-20), rd(0)), 0.4)
                lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-5), rd(-10), rd(5)), 0.6)
                lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.6)
                lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(-10), rd(-6)), 0.6)
                lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(5), rd(0), rd(0)), 0.6)
              end
              if firederp then
                firederp:Destroy()
              end
              swait(10)
              hwel.C0 = ang(rd(90), rd(0), rd(0)) * cf(0, 1, 0)
              keyingup:Disconnect()
              human.WalkSpeed = speed
              human:SetStateEnabled(3, true)
              activu = false
              HName.Text = "Bendy The Demon"
            end
          end
        end)
      end
    elseif batting == true then
      batting = false
      clibat:Disconnect()
      spec:Disconnect()
      hrp.sweae:Destroy()
      local batmod = chr:FindFirstChild("bmodel")
      batmod.hnd.Weld:Destroy()
      batmod.PrimaryPart = batmod.hnd
      batmod:SetPrimaryPartCFrame(rarm.CFrame * ang(rd(-90), rd(0), rd(0)) * cf(0, 0, -1))
      for _, A in pairs(batmod:GetChildren()) do
        if A.ClassName == "Part" then
          A.CanCollide = true
          A.Anchored = false
        end
      end
      batmod.Parent = workspace
      game.Debris:AddItem(batmod, 8)
    end
  end
  local movin = false
  local cliham, hamspec
  function ham()
    if batting == false then
      batting = true
      do
        local bmod = Instance.new("Model")
        bmod.Name = "bmodel"
        bmod.Parent = chr
        local makemotor = function(parent, p0, p1, c0, c1)
          local wel = Instance.new("Motor6D")
          wel.Part0 = p0
          wel.Part1 = p1
          wel.C0 = c0
          if c1 ~= nil then
            wel.C1 = c1
          end
          wel.Parent = parent
          return wel
        end
        local hnd = makepart("Really black", "hnd", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        hnd.Anchored = true
        local hmes = makemesh("Head", Vector3.new(5, 30, 5), nil, hnd)
        movin = true
        hnd.CFrame = hrp.CFrame
        coroutine.resume(coroutine.create(function()
          while hnd.Anchored == true do
            swait()
            if movin then
              hnd.CFrame = hnd.CFrame:lerp(hrp.CFrame * ang(rd(40), rd(0), rd(0)) * cf(0, 11, 0), 0.65)
            end
          end
        end))
        sbchat("CJ, DAT DAMN TRAIN IS BACK. USING DIS HAMMER TO BRAKE IT!",'[Bendy The Demon]')
        game.Chat:Chat(game.Players.LocalPlayer.Character.Head,"CJ, DAT DAMN TRAIN IS BACK. USING DIS HAMMER TO BRAKE IT!", "Red")
        local pt1 = makepart("Really black", "pt1", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p1m = makemesh("Head", Vector3.new(6, 5.5, 5.5), nil, pt1)
        local p1w = makemotor(pt1, pt1, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, 3, 0), nil)
        local pt2 = makepart("Really black", "pt2", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p2m = makemesh("Head", Vector3.new(6, 5.5, 5.5), nil, pt2)
        local p2w = makemotor(pt2, pt2, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, -3, 0), nil)
        local pt3 = makepart("Bright yellow", "pt3", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p3m = makemesh("Head", Vector3.new(6.5, 6.5, 6.5), nil, pt3)
        local p3w = makemotor(pt3, pt3, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, 3.75, 0), nil)
        local pt4 = makepart("Really black", "pt4", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p4m = makemesh("FileMesh", Vector3.new(1, 1, 1), "rbxassetid://0", pt4)
        p4m.TextureId = "rbxassetid://0"
        local p4w = makemotor(pt4, pt4, hnd, ang(rd(180), rd(180), rd(0)) * cf(0, 4.25, 0.25), nil)
        local pt5 = makepart("Bright blue", "pt5", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p5m = makemesh("Head", Vector3.new(5, 90, 4), nil, pt5)
        local p5w = makemotor(pt5, pt5, hnd, ang(rd(0), rd(0), rd(0)) * cf(0, -12, 0), nil)
        local pt6 = makepart("Bright blue", "pt6", 0, 0, "SmoothPlastic", bmod, hrp.CFrame)
        local p6m = makemesh("FileMesh", Vector3.new(0.16, 0.4, 0.16), "rbxassetid://862497341", pt6)
        p6m.TextureId = "rbxassetid://862497354"
        p6m.Scale = Vector3.new(0.5,0.50,0.5)
        local p6w = makemotor(pt6, pt6, hnd, ang(rd(180), rd(0), rd(0)) * cf(0, -16, 0), nil)
        local pt7 = makepart("Bright yellow", "pt7", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p7m = makemesh("Head", Vector3.new(75, 75, 75), nil, pt7)
        local p7w = makemotor(pt7, pt7, hnd, ang(rd(0), rd(90), rd(0)) * cf(0, -27, 0), nil)
        local pt8 = makepart("Bright yellow", "pt8", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p8m = makemesh("Head", Vector3.new(75, 75, 75), nil, pt8)
        local p8w = makemotor(pt8, pt8, hnd, ang(rd(0), rd(-90), rd(0)) * cf(0, -27, 0), nil)
        local hdec2 = Instance.new("Decal")
        local pt9 = makepart("Bright yellow", "pt9", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p9m = makemesh("FileMesh", Vector3.new(12, 11, 11), "rbxassetid://0", pt9)
        local p9w = makemotor(pt9, pt9, hnd, ang(rd(0), rd(90), rd(0)) * cf(0, -30, 0), nil)
        p9m.TextureId = "rbxassetid://0"
        local pt10 = makepart("Bright yellow", "pt10", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p10m = makemesh("Head", Vector3.new(60, 60, 60), nil, pt10)
        local p10w = makemotor(pt10, pt10, pt7, ang(rd(0), rd(0), rd(90)) * cf(11, 0, 0), nil)
        local hdec3 = Instance.new("Decal")
        local pt11 = makepart("Bright yellow", "pt11", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p11m = makemesh("Head", Vector3.new(60, 60, 60), nil, pt11)
        local p11w = makemotor(pt11, pt11, pt7, ang(rd(0), rd(180), rd(90)) * cf(11, 0, 0), nil)
        local pt12 = makepart("Bright yellow", "pt12", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p12m = makemesh("Head", Vector3.new(60, 60, 60), nil, pt12)
        local p12w = makemotor(pt12, pt12, pt7, ang(rd(0), rd(0), rd(-90)) * cf(-11, 0, 0), nil)
        local pt13 = makepart("Bright yellow", "pt13", 0, 1, "SmoothPlastic", bmod, hrp.CFrame)
        local p13m = makemesh("Head", Vector3.new(60, 60, 60), nil, pt13)
        local p13w = makemotor(pt13, pt13, pt7, ang(rd(0), rd(180), rd(-90)) * cf(-11, 0, 0), nil)
        cliham = tool.Activated:connect(function()
          if selected == false or activu == true or ragged == true then
            return
          end
          activu = true
          movin = false
          for B = 1, 20 do
            swait()
            lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(-5), rd(0), rd(0)), 0.4)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(8), rd(0), rd(0)), 0.4)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-15), rd(-5), rd(170)), 0.4)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.4)
            lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(0), rd(-10), rd(10)), 0.4)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.4)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-5), rd(-10), rd(-10)), 0.4)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.4)
            lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-5), rd(10), rd(10)), 0.4)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.4)
            hnd.CFrame = hnd.CFrame:lerp(rarm.CFrame * ang(rd(-110), rd(0), rd(0)) * cf(0, 0, -1), 0.1 + B * 0.045)
          end
          for B = 1, 30 do
            swait()
            lerpz(RJ, "C0", RJC0 * cf(0, 0.8, 0) * ang(rd(-25), rd(0), rd(-50)), 0.1 + B / 80)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-18), rd(0), rd(40)), 0.1 + B / 80)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-30), rd(-5), rd(160)), 0.1 + B / 80)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + B / 80)
            lerpz(LS, "C0", LSC0 * cf(-0.8, 0, -1) * ang(rd(-60), rd(-20), rd(-150)), 0.1 + B / 80)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + B / 80)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-15), rd(-20), rd(-10)), 0.1 + B / 80)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + B / 80)
            lerpz(LH, "C0", LHC0 * cf(0.5, 0, -0.4) * ang(rd(-5), rd(60), rd(-110)), 0.1 + B / 80)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.1 + B / 80)
            hnd.CFrame = hnd.CFrame:lerp(rarm.CFrame * ang(rd(-110), rd(0), rd(0)) * cf(0, 0, -1), 1)
          end
          for B = 1, 7 do
            swait()
            lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(40)), 0.015 + B / 15)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(9), rd(0), rd(-15)), 0.015 + B / 15)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(0), rd(-50), rd(100)), 0.015 + B / 15)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.015 + B / 15)
            lerpz(LS, "C0", LSC0 * cf(-0.8, 0, -1) * ang(rd(-60), rd(-25), rd(-90)), 0.015 + B / 15)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.015 + B / 15)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-15), rd(-20), rd(10)), 0.015 + B / 15)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.015 + B / 15)
            lerpz(LH, "C0", LHC0 * cf(0.1, 0, -0.1) * ang(rd(-5), rd(20), rd(-20)), 0.015 + B / 15)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.015 + B / 15)
            hnd.CFrame = hnd.CFrame:lerp(rarm.CFrame * ang(rd(-110), rd(0), rd(0)) * cf(0, 0, -1), 1)
          end
          for B = 1, 8 do
            swait()
            hito(pt6, 20, 808282854, 0.75, hrp.CFrame.rightVector * math.huge + Vector3.new(0, 50, 0), Vector3.new(0, rd2(-25, 25), rd2(-160, 160)))
            lerpz(RJ, "C0", RJC0 * cf(0, -0.8, 0) * ang(rd(70), rd(0), rd(40)), 0.38 + B * 0.1)
            lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(9), rd(0), rd(-15)), 0.38 + B * 0.1)
            lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(0), rd(-40), rd(100)), 0.38 + B * 0.1)
            lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.38 + B * 0.1)
            lerpz(LS, "C0", LSC0 * cf(-0.8, 0, -1) * ang(rd(-60), rd(-25), rd(-90)), 0.38 + B * 0.1)
            lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.38 + B * 0.1)
            lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-15), rd(-20), rd(60)), 0.38 + B * 0.1)
            lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.38 + B * 0.1)
            lerpz(LH, "C0", LHC0 * cf(0.1, 0, -0.1) * ang(rd(-5), rd(20), rd(70)), 0.38 + B * 0.1)
            lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.38 + B * 0.1)
            hnd.CFrame = hnd.CFrame:lerp(rarm.CFrame * ang(rd(-110), rd(0), rd(0)) * cf(0, 0, -1), 1)
            local exp = Instance.new("Explosion",plr.Character)
            exp.Position = pt6.Position
            exp.BlastRadius = 0
          end
          swait(15)
          movin = true
          sbchat("AW FAK. MY PEN1S IS BLOW UP NAW!",'[Bendy The Demon]')
          activu = false
        end)
      end
    elseif batting == true then
      batting = false
      cliham:Disconnect()
      local badevz = chr:FindFirstChild("bmodel")
      badevz.PrimaryPart = badevz.hnd
      for _, A in pairs(badevz:GetChildren()) do
        if A.ClassName == "Part" then
          A.CanCollide = true
          A.Anchored = false
        end
      end
      movin = false
      badevz.Parent = workspace
      badevz:SetPrimaryPartCFrame(hrp.CFrame * ang(rd(40), rd(0), rd(0)) * cf(0, -11, 0))
      game.Debris:AddItem(badevz, 8)
    end
  end
  game:GetService("ContentProvider"):Preload("rbxassetid://201858024")
  function lauf()
    if selected == false or activu == true then
      return
    end
    lauf1:Play()
  end
  function makenoob(cfrem, scalo, rags)
    nscale.Value = scalo
    local md = Instance.new("Model")
    md.Name = "Ink minion"
    md.Parent = workspace
    local hu = Instance.new("Humanoid")
    hu.RigType = "R6"
    hu.MaxHealth = 100 * scalo
    hu.Health = 100 * scalo
    hu.Parent = md
    local anm = Instance.new("Animator")
    anm.Parent = hu
    hu.PlatformStand = true
    local light = function(part)
      part.CustomPhysicalProperties = PhysicalProperties.new(0.35, 0.3, 0.5)
    end
    local hd = Instance.new("Part")
    hd.Name = "Head"
    hd.Size = Vector3.new(2 * nscale.Value, 1 * nscale.Value, 1 * nscale.Value)
    hd.TopSurface = "Smooth"
    hd.BottomSurface = "Inlet"
    hd.Locked = true
    hd.BrickColor = BrickColor.random()
    hd.CanCollide = true
    hd.Anchored = false
    light(hd)
    hd.Parent = md
    local hm = Instance.new("SpecialMesh")
    hm.MeshType = "Head"
    hm.Scale = Vector3.new(1.25, 1.25, 1.25)
    hm.Parent = hd
    local hf = Instance.new("Decal")
    hf.Texture = "rbxasset://textures/face.png"
    local gen = math.random(1, 40)
    if gen == 3 then
      hf.Texture = "rbxassetid://829370852"
    end
    if gen == 8 then
      hf.Texture = "rbxassetid://865030584"
    end
    if gen == 12 then
      hf.Texture = "rbxassetid://141795257"
    end
    if gen == 16 then
      hf.Texture = "rbxassetid://647052624"
    end
    if gen == 24 then
      hf.Texture = "rbxassetid://553786059"
    end
    if gen == 28 then
      hf.Texture = "rbxassetid://258268895"
    end
    if gen == 32 then
      hf.Texture = "rbxassetid://192267375"
    end
    if gen == 38 then
      hf.Texture = "rbxassetid://154195178"
      hf.Color3 = Color3.new(0, 0, 0)
    end
    hf.Face = "Front"
    hf.Parent = hd
    local hrpa = Instance.new("Part")
    hrpa.Name = "HumanoidRootPart"
    hrpa.TopSurface, hrpa.BottomSurface = 0, 0
    hrpa.Size = Vector3.new(2 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    hrpa.Transparency = 1
    hrpa.CanCollide = false
    hrpa.Locked = true
    light(hrpa)
    hrpa.Parent = md
    local tagbomb = Instance.new("BoolValue")
    tagbomb.Name = "tagbomb"
    tagbomb.Value = false
    tagbomb.Parent = hrpa
    local learm = Instance.new("Part")
    learm.Name = "Left Arm"
    learm.BrickColor = BrickColor.random()
    learm.CanCollide = false
    learm.Locked = true
    learm.Size = Vector3.new(1 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    light(learm)
    learm.Parent = md
    local riarm = Instance.new("Part")
    riarm.Name = "Right Arm"
    riarm.BrickColor = BrickColor.random()
    riarm.CanCollide = false
    riarm.Locked = true
    light(riarm)
    riarm.Size = Vector3.new(1 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    riarm.Parent = md
    local leleg = Instance.new("Part")
    leleg.Name = "Left Leg"
    leleg.BrickColor = BrickColor.random()
    leleg.CanCollide = false
    leleg.Locked = true
    light(leleg)
    leleg.BottomSurface = 0
    leleg.Size = Vector3.new(1 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    leleg.Parent = md
    local rileg = Instance.new("Part")
    rileg.Name = "Right Leg"
    rileg.BrickColor = BrickColor.random()
    rileg.CanCollide = false
    rileg.Locked = true
    light(rileg)
    rileg.BottomSurface = 0
    rileg.Size = Vector3.new(1 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    rileg.Parent = md
    local tor = Instance.new("Part")
    tor.Name = "Torso"
    tor.BrickColor = BrickColor.random()
    tor.Locked = true
    light(tor)
    tor.Size = Vector3.new(2 * nscale.Value, 2 * nscale.Value, 1 * nscale.Value)
    tor.LeftSurface, tor.RightSurface = "Weld", "Weld"
    tor.Parent = md
    md.PrimaryPart = hrpa
    md:SetPrimaryPartCFrame(cfrem)
    md:makeJoints()
    makejoint(hrpa, RootJointC0, RootJointC1, hrpa, tor, "RootJoint")
    makejoint(tor, NeckC0, NeckC1, tor, hd, "Neck")
    if rags == true then
      makegloo(tor, RightShoulderC0, RightShoulderC1, tor, riarm, "Right Shoulder")
      makegloo(tor, LeftShoulderC0, LeftShoulderC1, tor, learm, "Left Shoulder")
      makegloo(tor, RightHipC0, RightHipC1, tor, rileg, "Right Hip")
      makegloo(tor, LeftHipC0, LeftHipC1, tor, leleg, "Left Hip")
      maketouchy(riarm, riarm, CFrame.new(0, 0.5 * nscale.Value, 0))
      maketouchy(learm, learm, CFrame.new(0, 0.5 * nscale.Value, 0))
      maketouchy(leleg, leleg, CFrame.new(0, 0.5 * nscale.Value, 0))
      maketouchy(rileg, rileg, CFrame.new(0, 0.5 * nscale.Value, 0))
    elseif rags == false then
      makejoint(tor, RightShoulderC0, RightShoulderC1, tor, riarm, "Right Shoulder")
      makejoint(tor, LeftShoulderC0, LeftShoulderC1, tor, learm, "Left Shoulder")
      makejoint(tor, RightHipC0, RightHipC1, tor, rileg, "Right Hip")
      makejoint(tor, LeftHipC0, LeftHipC1, tor, leleg, "Left Hip")
      hu.PlatformStand = false
    end
    nscale.Value = 1
    hu.Touched:connect(function(tpart, uwot)
      if tagbomb.Value == true and tpart.Parent ~= md and tpart.Parent.Parent ~= md and tpart.Parent.Parent.Parent ~= md then
        tagbomb.Value = false
        hu.Health = 0
        local derp = Instance.new("Explosion")
        derp.BlastPressure = 200
        derp.BlastRadius = 8
        derp.DestroyJointRadiusPercent = 0
        derp.ExplosionType = 2
        derp.Visible = true
        derp.Position = uwot.Position - Vector3.new(0, 0.5, 0)
        derp.Parent = workspace
        game.Debris:AddItem(md, 8)
      end
    end)
    return md
  end
  function makecircle(cfrem, scalo)
    local mcir1 = Instance.new("Part")
    mcir1.Anchored = true
    mcir1.CanCollide = false
    mcir1.Size = Vector3.new(0.2, 0.2, 0.2)
    mcir1.Transparency = 1
    mcir1.CFrame = cfrem
    mcir1.Parent = modz
    game.Debris:AddItem(mcir1, 8)
    local d1 = Instance.new("Decal")
    d1.Texture = "rbxassetid://705615290"
    d1.Face = "Front"
    d1.Parent = mcir1
    local d2 = Instance.new("Decal")
    d2.Texture = "rbxassetid://0"
    d2.Face = "Back"
    d2.Parent = mcir1
    local bme = Instance.new("BlockMesh")
    bme.Parent = mcir1
    for _ = 1, 9 do
      swait()
      bme.Scale = bme.Scale:lerp(Vector3.new(35 * scalo, 35 * scalo, 0), 0.3)
    end
    coroutine.resume(coroutine.create(function()
      swait(15)
      for _ = 1, 12 do
        swait()
        d1.Transparency = d1.Transparency + 0.08
        d2.Transparency = d2.Transparency + 0.08
      end
      mcir1:Destroy()
    end))
    return mcir1
  end
  function spawnnoob(circlecf, noobcf, scalez, ragd)
    local aearae = makecircle(circlecf, scalez)
    local nananb
    if ragd then
      nananb = makenoob(aearae.CFrame * noobcf, scalez, true)
    elseif not ragd then
      nananb = makenoob(aearae.CFrame * noobcf, scalez, false)
    end
    return nananb
  end
  function tagexplode(partoz, magn, bombdelay)
    for _, guy in pairs(workspace:GetChildren()) do
      if guy:FindFirstChild("Humanoid") and guy:FindFirstChild("HumanoidRootPart") and guy.Name == "Skid" and guy.Name == "Dummy" and magn > (guy:FindFirstChild("HumanoidRootPart").Position - partoz.Position).magnitude then
        coroutine.resume(coroutine.create(function()
          swait(bombdelay * 0)
          guy:FindFirstChild("HumanoidRootPart").tagbomb.Value = true
        end))
      end
    end
  end
  function hito(partoz, magn, dmg, debtim, bodyfdire, bodyrot)
    for _, guy in pairs(workspace:GetChildren()) do
      if guy:FindFirstChild("Humanoid") and guy:FindFirstChild("HumanoidRootPart") and guy ~= chr and magn > (guy:FindFirstChild("HumanoidRootPart").Position - partoz.Position).magnitude and guy:FindFirstChild("HumanoidRootPart"):FindFirstChild("alabo") == nil then
        do
          local humz = guy:FindFirstChild("Humanoid")
          local horp = guy:FindFirstChild("HumanoidRootPart")
          humz:TakeDamage(dmg)
          humz:SetStateEnabled(16, true)
          delay(debtim, function()
            humz:SetStateEnabled(16, true)
          end)
          local db = Instance.new("StringValue")
          db.Name = "alabo"
          db.Parent = horp
          delay(debtim, function()
            db:Destroy()
          end)
          local b = Instance.new("Part")
          nooutline(b)
          b.Size = Vector3.new(0.2, 0.2, 0.2)
          b.Transparency = 0
          b.Anchored = true
          b.CanCollide = false
          b.Material = "Neon"
          b.BrickColor = BrickColor.new("Really black")
          b.Locked = true
          b.CFrame = horp.CFrame * CFrame.new(rd2(-1, 1), rd2(-2, 2), rd2(-1, 1))*CFrame.Angles(math.random(1412),math.random(423532),math.random(1312))
          b.Parent = modz
          local c = Instance.new("SpecialMesh")
          c.MeshType = "Sphere"
          c.Scale = Vector3.new(3.5, 3.5, 3.5)
          c.Parent = b
          game.Debris:AddItem(b, 1)
          if bodyfdire then
            local boopyve = Instance.new("BodyVelocity")
            boopyve.MaxForce = Vector3.new(9999999999999, 9999999999999, 9999999999999)
            boopyve.P = 9999999999
            boopyve.Velocity = bodyfdire
            boopyve.Parent = horp
            game.Debris:AddItem(boopyve, debtim)
          end
          if bodyrot then
            local boopyro = Instance.new("BodyAngularVelocity")
            boopyro.MaxTorque = Vector3.new(999999, 999999, 999999)
            boopyro.P = math.huge
            boopyro.AngularVelocity = bodyrot
            boopyro.Parent = horp
            game.Debris:AddItem(boopyro, debtim)
          end
          local bet = Instance.new("Sound")
          bet.Pitch = rd2(9, 11) / 10
          bet.Volume = rd2(12, 14) / 10
          bet.SoundId = "rbxassetid://201858024"
          bet.Parent = b
          bet:Play()
          coroutine.resume(coroutine.create(function()
            for _ = 1, 24 do
              swait()
              b.Transparency = b.Transparency + 0.08
              c.Scale = c.Scale + Vector3.new(.8 * dmg, .8 * dmg, .8 * dmg)
            end
          end))
        end
      end
    end
  end
  function cleannoobs()
    for _, nib in pairs(workspace:GetChildren()) do
      coroutine.resume(coroutine.create(function()
        if nib.Name == "Noob" then
          if nib:FindFirstChild("HumanoidRootPart") then
            local g = Instance.new("Part")
            g.CanCollide, g.Anchored = false, true
            g.Transparency = 1
            g.CFrame = nib:FindFirstChild("HumanoidRootPart").CFrame
            g.Parent = workspace
            game.Debris:AddItem(g, 3.5)
            local sou = Instance.new("Sound")
            sou.Pitch = 0
            sou.Volume = 3
            sou.SoundId = "rbxassetid://201858024"
            sou.Parent = g
            local pe = Instance.new("ParticleEmitter")
            pe.Acceleration = Vector3.new(0, 8, 0)
            pe.Lifetime = NumberRange.new(1, 1.5)
            pe.Rate = 0.005
            pe.RotSpeed = NumberRange.new(-30, 30)
            pe.Rotation = NumberRange.new(0, 360)
            pe.Size = NumberSequence.new({
              NumberSequenceKeypoint.new(0, 4.38, 0),
              NumberSequenceKeypoint.new(0.672, 4.14, 0),
              NumberSequenceKeypoint.new(1, 1.48, 0)
            })
            pe.Texture = "rbxassetid://0"
            pe.Transparency = NumberSequence.new({
              NumberSequenceKeypoint.new(0, 0, 0),
              NumberSequenceKeypoint.new(0.529, 0.3, 0),
              NumberSequenceKeypoint.new(1, 1, 1)
            })
            pe.ZOffset = 5
            pe.Enabled = true
            pe.VelocitySpread = 360
            pe.Parent = g
            swait(5)
            pe:Emit(6)
            sou:Play()
          end
          nib:Destroy()
        end
      end))
    end
  end
  function animo(yep)
    if yep == true then
      anim.Parent = human
      chr.Animate.Disabled = false
    elseif yep == false then
      chr.Animate.Disabled = true
      anim.Parent = nil
    end
  end
  mouse.KeyDown:connect(function(key)
    if key == "r" then
      test()
    end
    if key == "m" then
      lauf()
    end
    if key == "c"  then
      ham()
    end
    if key == "x" then
      bat()
    end
    if key == "l"  and selected == true then
      spawnnoob(hrp.CFrame * cf(5, 3, -1) * ang(rd(90), 0, 0), cf(0, 0, 0) * ang(rd(-90), 0, 0), 1, true)
    end
    if key == "h" and selected == true then
      spawnnoob(hrp.CFrame * cf(5, 60, -1) * ang(rd(90), 0, 0), cf(0, 0, 0) * ang(rd(-90), 0, 0), 10, true)
    end
    if key == "k" and selected == true then
      spawnnoob(hrp.CFrame * cf(5, 3, -1) * ang(rd(90), 0, 0), cf(0, 0, 0) * ang(rd(-90), 0, 0), 1, false)
    end
    if key == "p" then
      cleannoobs()
    end
    if key == "e" then
    	local so = Instance.new("Sound",plr.Character)
    	so.SoundId = "rbxassetid://852817448"
    	so.Volume = 10
    	so:Play()
    	game:GetService("Lighting").Ambient = Color3.new(255,0,0)
    	game:GetService("Lighting").Brightness = 0
    	game:GetService("Lighting").TimeOfDay = "00:00:00"
    	HName.Text = "YOU PICK THE WRONG HOUSE, FOOOOOOL!"
    	sbchat("YOU PICK THE WRONG HOUSE, FOOOOOOL!",'[Bendy The Demon]')
    	wait(2)
    	game.Players.LocalPlayer.PlayerGui.SB_DataTransfer.SB_CommandRemote.Value = "g/fl"
    	HName.Text = "Bendy The Demon"
    end
    if key == "z" then
      if selected == false or activu == true then
        return
      end
      if human.WalkSpeed == 25 then
        human.WalkSpeed = 100
        human.JumpPower = 125
      else
        human.WalkSpeed = 25
        human.JumpPower = 50
      end
    end
  end)
  tool.Equipped:connect(function()
    selected = true
  end)
  tool.Unequipped:connect(function()
    selected = false
  end)
  animo(false)
  human.WalkSpeed = 25
  sine = 0
  charge = 1
  cos = math.cos
  game:GetService("RunService").RenderStepped:connect(function()
    if ragged == false and activu == false then
      local checkfloor = Ray.new(hrp.Position, Vector3.new(0, -5, 0))
      local checkpart = workspace:FindPartOnRayWithIgnoreList(checkfloor, {chr}, false, false)
      local checkstate = human:GetState()
      if checkstate.Value == 13 then
        animpose = "Sitting"
      elseif hrp.Velocity.y > 1 and checkpart == nil then
        animpose = "Jumping"
      elseif hrp.Velocity.y < -1 and checkpart == nil then
        animpose = "Falling"
      elseif (hrp.Velocity * Vector3.new(1, 0, 1)).magnitude < 2 then
        animpose = "Idle"
      elseif (hrp.Velocity * Vector3.new(1, 0, 1)).magnitude < 40 then
        animpose = "Walking"
      elseif (hrp.Velocity * Vector3.new(1, 0, 1)).magnitude > 40 then
        animpose = "TooFast"
      end
      if animpose == "Idle" then
        sine = sine + charge
        lerpz(RJ, "C0", RJC0 * cf(0.05 * cos(sine / 40), 0, -0.05 - 0.05 * cos(sine / 20)) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(4 + 2 * cos(sine / 20)), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(10)), 0.3)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(100), rd(-40), rd(-32)), 0.3)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0.05 + 0.05 * cos(sine / 20), 0.05 * cos(sine / 40)) * ang(rd(-5), rd(-5), rd(1)), 0.3)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0.05 + 0.05 * cos(sine / 20), -0.05 * cos(sine / 40)) * ang(rd(-5), rd(5), rd(1)), 0.3)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
      if animpose == "Walking" then
        sine = sine + charge
        lerpz(RJ, "C0", RJC0 * cf(0, 0, 0 * cos(sine / 4)) * ang(rd(20), math.sin(hrp.RotVelocity.Y / 80), 0), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-2), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-20)), 0.6)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(100), rd(-40), rd(-32)), 0.6)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-1 - 1 * cos(sine / 60)), rd(-1 - 1 * cos(sine / 60)), rd(-60 * cos(sine / 8))), 0.6)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-1 - 1 * cos(sine / 60)), rd(1 - 1 * cos(sine / 60)), rd(-60 * cos(sine / 8))), 0.6)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
      if animpose == "Jumping" then
        lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(-5), rd(0), rd(0)), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-10), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, -0.5, 0.2) * ang(rd(-70), rd(-5), rd(-20)), 0.3)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, -0.5, 0.2) * ang(rd(-70), rd(5), rd(20)), 0.3)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-20), rd(-20), rd(-20)), 0.3)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-20), rd(20), rd(15)), 0.3)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
      if animpose == "Falling" then
        lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0.6) * ang(rd(-150), rd(-5), rd(-20)), 0.3)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0.6) * ang(rd(-150), rd(5), rd(20)), 0.3)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-15), rd(-15), rd(-20)), 0.3)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-15), rd(15), rd(15)), 0.3)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
      if animpose == "TooFast" then
        sine = sine + charge
        lerpz(RJ, "C0", RJC0 * cf(0, 0, 0.35 * cos(sine / 2)) * ang(rd(30), math.sin(hrp.RotVelocity.Y / 20), math.sin(hrp.RotVelocity.Y / 2)), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-15 - 5 * cos(sine / 2)), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-10), rd(-20), rd(-80)), 0.6)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(110), rd(-40), rd(-35)), 0.6)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-1 - 1 * cos(sine / 60)), rd(-1 - 1 * cos(sine / 60)), rd(-60 * cos(sine / 3))), 0.6)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-1 - 1 * cos(sine / 60)), rd(1 - 1 * cos(sine / 60)), rd(-60 * cos(sine / 3))), 0.6)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
      if animpose == "Sitting" then
        lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(90)), 0.3)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(-90)), 0.3)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(90)), 0.3)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
        lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(-90)), 0.3)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
      end
    end
  end)
  if plr.Character.Humanoid.PlatformStand == true then
  	plr.Character.Humanoid.PlatformStand = false
  end
  plr.Character.Humanoid.Died:connect(function()
  s:Stop()
  HName.TextColor3 = BrickColor.new("Hot white").Color
  HName.Text = "R.I.P"
  local f = Instance.new("Explosion",plr.Character.Torso)
  f.Position = plr.Character.Torso.Position
  f.BlastRadius = 0
  local m = Instance.new("Sound",Workspace)
  m.SoundId = "rbxassetid://319332735"
  m.Volume = 10
  m:Play()
  end)
--------------------------Gui---------------------------
makeframe = function(par, trans, pos, size, color)
  local frame = Instance.new("Frame", par)
  frame.BackgroundTransparency = trans
  frame.BorderSizePixel = 1
  frame.BorderColor3 = BrickColor.Black().Color
  frame.Position = pos
  frame.Size = size
  frame.BackgroundColor3 = BrickColor.new("Really black").Color
  frame.ZIndex = 5
  return frame
end

makelabel = function(par, text)
  local label = Instance.new("TextLabel", par)
  label.BackgroundTransparency = 1
  label.Size = ud(1, 0, 1, 0)
  label.Position = ud(0, 0, 0, 0)
  label.TextColor3 = c3(1,1,1)
  label.TextStrokeTransparency = 0
  label.FontSize = Enum.FontSize.Size24
  label.Font = Enum.Font.SciFi
  label.BorderSizePixel = 0
  label.TextScaled = true
  label.Text = text
end
----------------------------------------------
local scrn = Instance.new("ScreenGui", p.PlayerGui)
ud = UDim2.new
c3 = Color3.new

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.150,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[Q]:Automatic Attack (Hold)")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.190,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[E]:WRONG HAWSE DUD")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.230,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[R]:Ragdoll")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.270,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[Z]:Speed")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.310,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[C]:Big Smoke Hammer")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.350,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[K]:No Ragdoll Dummy")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.390,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[L]:Ragdoll Dummy")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.430,0), ud(0.19, 0, 0.03, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "[H]:Big Dummy")

Manabar = makeframe(scrn, 0.5, ud(0.8125,0,0.470,0), ud(0.19, 0, 0.17, 0), c3(0,0,0))
Manacover = makeframe(Manabar, 0.5, ud(0, 0, 0, 0), ud(1, 0, 1, 0), c3(0, 0, 0))
Manatext = makelabel(Manabar, "PUT DIS SH!T TO CJ'S FACE PLES!")
warn'<Script>[Anti Sent To Local]:Connect!'
warn'<Script>:Welcome!'
-----------------------------------------------------------------
end)

TextButton_3.Parent = scriptframe
TextButton_3.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_3.Position = UDim2.new(0, 0, 0, 200)
TextButton_3.Size = UDim2.new(0, 123, 0, 50)
TextButton_3.Font = Enum.Font.SourceSans
TextButton_3.Text = "Jonh Doe"
TextButton_3.TextColor3 = Color3.new(0, 1, 1)
TextButton_3.TextScaled = true
TextButton_3.TextSize = 14
TextButton_3.TextWrapped = true

TextButton_3.MouseButton1Down:connect(function()
------------
--John Doe--
------------
-----by-----
--CKbackup--
------------

--Player Stuff--
player = game:GetService("Players").LocalPlayer
chara = player.Character

ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].Name == "Torso" then
ch[i].roblox.Transparency = 1
elseif ch[i].Name == "Head" then
ch[i].face.Transparency = 1
ch[i].Transparency = 1
elseif ch[i].ClassName == "Accessory" or ch[i].ClassName == "Shirt" or ch[i].ClassName == "Pants" or ch[i].ClassName == "ShirtGraphic" then
ch[i]:Destroy()
end
end

chara["Left Arm"].BrickColor = BrickColor.new("Cool yellow")
chara["Right Arm"].BrickColor = BrickColor.new("Cool yellow")
chara["Left Leg"].BrickColor = BrickColor.new("Medium blue")
chara["Right Leg"].BrickColor = BrickColor.new("Medium blue")
chara.Torso.BrickColor = BrickColor.new("Bright yellow")

--Outfit--
New = function(Object, Parent, Name, Data)
	local Object = Instance.new(Object)
	for Index, Value in pairs(Data or {}) do
		Object[Index] = Value
	end
	Object.Parent = Parent
	Object.Name = Name
	return Object
end

function ScatterEff(part)
local eff1 = Instance.new("ParticleEmitter",part)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.9,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(1)
eff1.Speed = NumberRange.new(1)
eff1.Rate = 100
eff1.VelocitySpread = 10000
eff1.Texture = "rbxassetid://347504241"
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",part)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.9,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(1)
eff2.Speed = NumberRange.new(1)
eff2.Rate = 100
eff2.VelocitySpread = 10000
eff2.Texture = "rbxassetid://347504259"
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
end

function BurningEff(part)
local eff1 = Instance.new("ParticleEmitter",part)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(1)
eff1.Speed = NumberRange.new(0)
eff1.Rate = 100
eff1.Texture = "rbxassetid://347504241"
eff1.Acceleration = Vector3.new(0,10,0)
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",part)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(1)
eff2.Speed = NumberRange.new(0)
eff2.Rate = 100
eff2.Texture = "rbxassetid://347504259"
eff2.Acceleration = Vector3.new(0,10,0)
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
local eff3 = Instance.new("ParticleEmitter",part)
eff3.Size = NumberSequence.new(1)
eff3.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(1,1)})
eff3.LightEmission = 1
eff3.Lifetime = NumberRange.new(1)
eff3.Speed = NumberRange.new(0)
eff3.Rate = 100
eff3.Texture = "rbxasset://textures/particles/fire_main.dds"
eff3.Acceleration = Vector3.new(0,10,0)
eff3.Color = ColorSequence.new(Color3.new(1,0,0))
end

FakeHead = New("Model",chara,"FakeHead",{})
MainPart = New("Part",FakeHead,"MainPart",{FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(2, 1, 1),CFrame = CFrame.new(2.29537678, 7.81603718, 0.746068954, 0.00980896503, 0.00110200304, 0.999957919, -0.000536994543, 1.00000548, -0.00109680078, -0.99994874, -0.0005262224, 0.00980964955),CanCollide = false,TopSurface = Enum.SurfaceType.Smooth,})
Mesh = New("SpecialMesh",MainPart,"Mesh",{Scale = Vector3.new(1.25, 1.25, 1.25),})
face = New("Decal",MainPart,"face",{Texture = "rbxasset://textures/face.png",})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara.Head,C0 = CFrame.new(0, 0, 0, 0.00980896503, -0.000536994543, -0.99994874, 0.00110200304, 1.00000548, -0.0005262224, 0.999957919, -0.00109680078, 0.00980964955),C1 = CFrame.new(5.96046448e-008, -8.58306885e-006, 0, 0.00980896503, -0.000536994543, -0.99994874, 0.00110200304, 1.00000548, -0.0005262224, 0.999957919, -0.00109680078, 0.00980964955),})
FakeHead.MainPart.BrickColor = BrickColor.new("Cool yellow")
EyeFire = New("Part",FakeHead,"EyeFire",{BrickColor = BrickColor.new("Really red"),Material = Enum.Material.Neon,Size = Vector3.new(0.400000006, 0.200000003, 0.200000003),CFrame = CFrame.new(1.69668579, 8.11665249, 0.640022159, -0.00107900088, 0.999958038, -0.00980941113, -1.0000056, -0.00107390946, 0.000525554642, 0.000515007298, 0.00981007144, 0.999948859),CanCollide = false,Color = Color3.new(1, 0, 0),})
Mesh = New("CylinderMesh",EyeFire,"Mesh",{Offset = Vector3.new(0.0500000007, 0, -0.0399999991),Scale = Vector3.new(1, 0.150000006, 1),})
Weld = New("ManualWeld",EyeFire,"Weld",{Part0 = EyeFire,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0010790003, -0.999999344, 0.000515000196, 0.999951363, -0.0010738963, 0.00981000345, -0.00980944186, 0.000525560055, 0.99995178),C1 = CFrame.new(0.100008011, 0.300009251, -0.600027919, 0.00980899762, -0.000536999898, -0.99995178, 0.00110200245, 0.999999344, -0.000526215415, 0.999951363, -0.00109678751, 0.00980958249),})
Chest = New("Model",chara,"Chest",{})
MainPart = New("Part",Chest,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(2, 2, 1),CFrame = CFrame.new(2.2937007, 6.31611967, 0.746871948, 0.00980956201, 0.00110224239, 0.999954581, -0.000537135813, 1.00000238, -0.00109703222, -0.99995023, -0.000526354474, 0.00981019717),CanCollide = false,LeftSurface = Enum.SurfaceType.Weld,RightSurface = Enum.SurfaceType.Weld,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara.Torso,C0 = CFrame.new(0, 0, 0, 0.009809535, -0.000537137908, -0.99994725, 0.00110225554, 1.00000858, -0.000526368851, 0.999961257, -0.00109705783, 0.00981026888),C1 = CFrame.new(5.96046448e-008, -9.05990601e-006, -2.38418579e-007, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
CorruptedPart = New("Part",Chest,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.400000006, 0.800000072, 1),CFrame = CFrame.new(2.28977966, 7.11656427, 1.34486222, -0.00110228383, -0.00980954897, -0.9999578, -1.00000536, 0.000536905834, 0.00109708123, 0.000526248943, 0.99994868, -0.00981033035),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0011022957, -0.999999225, 0.000526249292, -0.00980958622, 0.000536918582, 0.99995172, -0.999951243, 0.0010970803, -0.00981026702),C1 = CFrame.new(-0.598430753, 0.800122261, 0.00106739998, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
CorruptedPart = New("Part",Chest,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.400000006, 0.400000066, 1),CFrame = CFrame.new(2.29174757, 6.71645212, 1.54485857, -0.00110228383, -0.00980954897, -0.9999578, -1.00000536, 0.000536905834, 0.00109708123, 0.000526248943, 0.99994868, -0.00981033035),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0011022957, -0.999999225, 0.000526249292, -0.00980958622, 0.000536918582, 0.99995172, -0.999951243, 0.0010970803, -0.00981026702),C1 = CFrame.new(-0.798183441, 0.399908543, 0.00543618202, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
LeftArm = New("Model",chara,"LeftArm",{})
MainPart = New("Part",LeftArm,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(1.90889204, 6.31596565, 3.24640989, -0.0484240092, -0.0324009918, 0.998301268, -0.00117100019, 0.999474883, 0.0323822871, -0.998826265, 0.000399069104, -0.0484365262),CanCollide = false,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Left Arm"],C0 = CFrame.new(0, 0, 0, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),C1 = CFrame.new(0, -8.10623169e-006, -2.38418579e-007, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(1.48370504, 6.50245714, 2.8663168, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(0.400017738, 0.200018406, -0.400015235, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.51924801, 6.60332775, 3.66543078, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.399997473, 0.300003052, -0.399972558, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
EffCorruptedPart = New("Part",LeftArm,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 1),CFrame = CFrame.new(1.92512023, 5.81624889, 3.24619365, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(1.52587891e-005, -0.49998045, 2.90870667e-005, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000072, 0.200000003),CFrame = CFrame.new(2.31463432, 6.72918367, 3.62673688, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.400012016, 0.400006294, 0.400012136, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(1.50631011, 6.40297413, 3.26581192, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(1.3589859e-005, 0.100014687, -0.400020242, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000036, 0.200000003),CFrame = CFrame.new(1.92179501, 6.51633835, 3.64602208, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.40000248, 0.200008869, 1.37090683e-005, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
BurningEff(EffCorruptedPart)
LeftLeg = New("Model",chara,"LeftLeg",{})
MainPart = New("Part",LeftLeg,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.2865479, 1.31659603, 1.24781799, 0.00980953407, 0.00110225566, 0.999961138, -0.000537137908, 1.00000858, -0.00109705783, -0.99994719, -0.000526368851, 0.00981026888),CanCollide = false,BottomSurface = Enum.SurfaceType.Smooth,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Left Leg"],C0 = CFrame.new(0, 0, 0, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),C1 = CFrame.new(0, -8.58306885e-006, -2.38418579e-007, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
EffCorruptedPart = New("Part",LeftLeg,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.200000048, 1),CFrame = CFrame.new(2.28007793, 0.400032878, 1.25993299, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.0116856098, -0.916567385, -0.00534534454, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.88013697, 0.800038397, 0.859943509, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(0.3841483, -0.516796231, -0.40962553, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000012, 0.200000003),CFrame = CFrame.new(2.69002914, 0.915953577, 0.851962805, 0.999971032, 0.0011022269, -0.00980960391, -0.00109704852, 1.00001776, 0.000537177373, 0.00981036108, -0.000526409131, 0.999942601),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999951303, -0.0010970087, 0.00981015898, 0.00110222446, 0.999999166, -0.000526388001, -0.00980970077, 0.00053719338, 0.99995172),C1 = CFrame.new(0.400011122, -0.399985313, 0.400013685, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000012, 0.200000003),CFrame = CFrame.new(1.88013721, 0.900040269, 1.65993917, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.415866137, -0.41721642, -0.40188694, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(1.88013721, 0.600035727, 1.25993288, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.0157161951, -0.717007458, -0.405481935, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.28007793, 0.700037479, 1.65993929, 1.00001967, -3.84054147e-007, 3.90969217e-006, 6.35045581e-007, 1.00001717, -5.60838998e-007, -6.19795173e-006, 9.32147486e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 6.5424797e-007, -6.48946025e-006, -3.64865258e-007, 0.999998629, 9.58411874e-007, 3.61912225e-006, -5.34497644e-007, 0.999998629),C1 = CFrame.new(-0.411835551, -0.616776347, -0.00175023079, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 1.20000005, 0.200000003),CFrame = CFrame.new(2.68018699, 1.10004401, 1.65993941, 1.00001967, -3.84054147e-007, 3.90969217e-006, 6.35045581e-007, 1.00001717, -5.60838998e-007, -6.19795173e-006, 9.32147486e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 6.5424797e-007, -6.48946025e-006, -3.64865258e-007, 0.999998629, 9.58411874e-007, 3.61912225e-006, -5.34497644e-007, 0.999998629),C1 = CFrame.new(-0.408125639, -0.216332912, 0.397896528, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(2.68596959, 0.816166699, 1.25195313, 0.999971032, 0.0011022269, -0.00980960391, -0.00109704852, 1.00001776, 0.000537177373, 0.00981036108, -0.000526409131, 0.999942601),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999951303, -0.0010970087, 0.00981015898, 0.00110222446, 0.999999166, -0.000526388001, -0.00980970077, 0.00053719338, 0.99995172),C1 = CFrame.new(5.20944595e-005, -0.499986172, 0.399987936, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
ScatterEff(EffCorruptedPart)
RightArm = New("Model",chara,"RightArm",{})
MainPart = New("Part",RightArm,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.011096, 6.31690788, -3.92582893, 0.00918400101, -0.262283146, 0.964947343, 0.259330034, 0.932596445, 0.251021653, -0.965745091, 0.247934431, 0.0765828639),CanCollide = false,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Right Arm"],C0 = CFrame.new(0, 0, 0, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),C1 = CFrame.new(-2.86102295e-006, -9.05990601e-006, -2.38418579e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
Hitbox = New("Part",RightArm,"Hitbox",{BrickColor = BrickColor.new("Really black"),Transparency = 1,Transparency = 1,Size = Vector3.new(1, 4, 1),CFrame = CFrame.new(22.2733669, 5.0842762, -22.1737366, -0.964945257, -0.262290984, 0.00919180829, -0.251027077, 0.93259424, 0.259333313, -0.0765930116, 0.247935042, -0.965744138),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Weld = New("ManualWeld",Hitbox,"Weld",{Part0 = Hitbox,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945257, -0.251027077, -0.0765930116, -0.262290984, 0.93259424, 0.247935042, 0.00919180829, 0.259333313, -0.965744138),C1 = CFrame.new(-1.52587891e-005, -1.00003147, -1.71661377e-005, 0.0091838371, 0.259330064, -0.965745151, -0.262283117, 0.932596445, 0.247934505, 0.964947283, 0.251021653, 0.0765827149),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.011096, 6.3169179, -3.92581391, -0.964945257, -0.262290984, 0.00919180829, -0.251027077, 0.93259424, 0.259333313, -0.0765930116, 0.247935042, -0.965744138),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945138, -0.251027018, -0.0765930042, -0.262290984, 0.932594121, 0.247935027, 0.00919180084, 0.259333313, -0.965744197),C1 = CFrame.new(-1.1920929e-005, 1.28746033e-005, 3.57627869e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.600000024, 0.400000036),CFrame = CFrame.new(2.14866924, 6.03215551, -4.72580194, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.699988842, -0.499982834, 7.62939453e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1.20000005, 0.600000024),CFrame = CFrame.new(2.63876629, 4.02682734, -4.32773018, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(-0.199987888, -2.39999342, 3.02791595e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 0.600000024),CFrame = CFrame.new(1.62134135, 7.81954479, -3.94021821, 0.964945078, -0.262291819, -0.00918725226, 0.251029015, 0.932593465, -0.259333432, 0.0765890032, 0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.964944899, 0.251028955, 0.0765889958, -0.262291819, 0.932593465, 0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.399995804, 1.5000124, -2.38418579e-007, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.600000024, 0.400000036),CFrame = CFrame.new(2.35483098, 5.18234444, -4.53787422, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.300010204, -1.29999256, 1.40666962e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 0.600000024),CFrame = CFrame.new(1.88730097, 6.99068737, -4.57445002, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.799996853, 0.50001812, 4.29153442e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.800000072, 0.600000024),CFrame = CFrame.new(2.37646794, 4.9594202, -4.07979012, -0.964945316, -0.262290984, 0.00918756705, -0.251028091, 0.932593942, 0.259333163, -0.0765890256, 0.247935995, -0.965744197),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945138, -0.251028031, -0.0765890107, -0.262290955, 0.932593882, 0.247935966, 0.0091875596, 0.259333193, -0.965744257),C1 = CFrame.new(-0.199994564, -1.39999104, 1.52587891e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
RightLeg = New("Model",chara,"RightLeg",{})
MainPart = New("Part",RightLeg,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.29641008, 1.31540966, 0.248092994, 0.00933599845, 0.00110999751, 0.999955773, -0.0030579993, 0.999994755, -0.00108149007, -0.99995178, -0.0030477671, 0.00933934376),CanCollide = false,BottomSurface = Enum.SurfaceType.Smooth,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Right Leg"],C0 = CFrame.new(0, 0, 0, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),C1 = CFrame.new(2.98023224e-008, -8.58306885e-006, 2.38418579e-007, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(2.70045996, 1.61376095, -0.149078026, 0.999955833, 0.00111049914, -0.0093326522, -0.00108199986, 0.999994755, 0.00305823679, 0.00933599938, -0.00304800388, 0.999951839),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955893, -0.00108199986, 0.00933599938, 0.00111049926, 0.999994755, -0.00304800388, -0.0093326522, 0.00305823679, 0.99995178),C1 = CFrame.new(0.400011688, 0.300008655, 0.400000095, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.90071809, 1.81462395, -0.157150015, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(0.400002658, 0.50000751, -0.399999142, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000036, 0.200000003),CFrame = CFrame.new(1.896873, 1.71584904, 0.243133992, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(4.14252281e-006, 0.400008917, -0.399998784, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000072, 0.200000003),CFrame = CFrame.new(1.89314091, 1.71706903, 0.643112063, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(-0.399993181, 0.400005698, -0.399996519, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
EffCorruptedPart = New("Part",RightLeg,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1.20000005, 1),CFrame = CFrame.new(2.29597116, 0.915416002, 0.249298006, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(1.41263008e-005, -0.399995744, 5.00679016e-006, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.300596, 1.71419013, -0.153122023, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(0.400015235, 0.400005817, 7.39097595e-006, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(2.69322205, 1.81620288, 0.650299072, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(-0.400013447, 0.500005245, 0.400009155, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.69684124, 1.71498096, 0.250625998, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(-1.63316727e-005, 0.400005937, 0.400005102, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
ScatterEff(EffCorruptedPart)

sa = RightArm:GetChildren()
for i = 1, #sa do
ScatterEff(sa[i])
end

local eff1 = Instance.new("ParticleEmitter",EyeFire)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(.5)
eff1.Speed = NumberRange.new(1)
eff1.EmissionDirection = "Front"
eff1.Rate = 100
eff1.Texture = "rbxassetid://347504241"
eff1.Acceleration = Vector3.new(0,10,0)
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",EyeFire)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(.5)
eff2.Speed = NumberRange.new(1)
eff2.EmissionDirection = "Front"
eff2.Rate = 100
eff2.Texture = "rbxassetid://347504259"
eff2.Acceleration = Vector3.new(0,10,0)
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
local eff3 = Instance.new("ParticleEmitter",EyeFire)
eff3.Size = NumberSequence.new(.1)
eff3.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(1,1)})
eff3.LightEmission = 1
eff3.Lifetime = NumberRange.new(.5)
eff3.Speed = NumberRange.new(1)
eff3.EmissionDirection = "Front"
eff3.Rate = 100
eff3.Texture = "rbxasset://textures/particles/fire_main.dds"
eff3.Acceleration = Vector3.new(0,10,0)
eff3.Color = ColorSequence.new(Color3.new(1,0,0))

--Sounds--
slashsnd = New("Sound",chara.Torso,"Slash",{SoundId = "rbxassetid://28144425",PlaybackSpeed = .7,Volume = 5})
hitsnd = New("Sound",chara.Torso,"Hit",{SoundId = "rbxassetid://429400881",PlaybackSpeed = .7,Volume = 5})
telesnd = New("Sound",chara.Torso,"Tele",{SoundId = "rbxassetid://2767090",PlaybackSpeed = .7,Volume = 5})
burnsnd = New("Sound",chara.Torso,"Burn",{SoundId = "rbxassetid://32791565",PlaybackSpeed = .7,Volume = 5})
music1 = New("Sound",chara.Torso,"Music1",{SoundId = "rbxassetid://151038517",PlaybackSpeed = .5,Volume = 10,Looped = true})
music2 = New("Sound",chara.Torso,"Music2",{SoundId = "rbxassetid://11984351",PlaybackSpeed = .2,Volume = 5,Looped = true})
deathmus = New("Sound",chara.Torso,"DeathMus",{SoundId = "rbxassetid://19094700",PlaybackSpeed = .5,Volume = 5,Looped = true})
deathex = New("Sound",chara.Torso,"DeathEx",{SoundId = "rbxassetid://11984351",PlaybackSpeed = 1,Volume = 5})
music1:Play()
music2:Play()

--Animations--
swinganim = chara.Humanoid:LoadAnimation(New("Animation",chara,"Swing",{AnimationId = "rbxassetid://186934658"}))

--Name Tag--
local naeeym = Instance.new("BillboardGui",chara)
naeeym.Size = UDim2.new(0,100,0,40)
naeeym.StudsOffset = Vector3.new(0,2,0)
naeeym.Adornee = chara.Head
local tecks = Instance.new("TextLabel",naeeym)
tecks.BackgroundTransparency = 1
tecks.BorderSizePixel = 0
tecks.Text = "John Doe"
tecks.Font = "Fantasy"
tecks.FontSize = "Size24"
tecks.TextStrokeTransparency = 0
tecks.TextStrokeColor3 = Color3.new(0,0,0)
tecks.TextColor3 = Color3.new(0,0,0)
tecks.Size = UDim2.new(1,0,0.5,0)

--Skybox--
skybox = Instance.new("Part",chara)
skybox.Size = Vector3.new(0,0,0)
skybox.Anchored = true
skybox.CanCollide = true
skyboxmesh = Instance.new("SpecialMesh",skybox)
skyboxmesh.MeshId = "http://www.roblox.com/asset/?id=1527559"
skyboxmesh.TextureId = "http://www.roblox.com/asset/?id=1529455"
skyboxmesh.VertexColor = Vector3.new(1,0,0)
skyboxmesh.Scale = Vector3.new(-3000,-1000,-3000)

--Soul Steal--
function SoulSteal(pos)
local soulst = coroutine.wrap(function()
local soul = Instance.new("Part",chara)
soul.Size = Vector3.new(0,0,0)
soul.CanCollide = false
soul.Anchored = false
soul.Position = pos
soul.CFrame = CFrame.new(pos.X,pos.Y,pos.Z)
soul.Transparency = 1
local ptc = Instance.new("ParticleEmitter",soul)
ptc.Texture = "http://www.roblox.com/asset/?id=413366101"
ptc.Size = NumberSequence.new(.5)
ptc.LockedToPart = true
ptc.Speed = NumberRange.new(0)
ptc.Lifetime = NumberRange.new(9999)
local bodpos = Instance.new("BodyPosition",soul)
bodpos.Position = pos
wait(2)
soul.Touched:connect(function(hit)
if hit.Parent == chara then
soul:Destroy()
end
end)
while soul do
wait(.1)
bodpos.Position = chara.Torso.Position
end
end)
soulst()
end

--Death of a Mortal--
function KillMortal(hitdude)
local torsy = nil
if hitdude:FindFirstChild("Torso")~=nil then
torsy = hitdude.Torso	
elseif hitdude:FindFirstChild("UpperTorso")~=nil then
torsy = hitdude.UpperTorso
end
local val = Instance.new("ObjectValue",hitdude)
val.Name = "HasBeenHit"
hitdude:BreakJoints()
hitdude.Humanoid:Destroy()
SoulSteal(torsy.Position)
local chi = hitdude:GetChildren()
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
local bodpos = Instance.new("BodyPosition",chi[i])
bodpos.Position = chi[i].Position + Vector3.new(math.random(-5,5),math.random(-5,5),math.random(-5,5))
ScatterEff(chi[i])
chi[i].BrickColor = BrickColor.new("Really black")
end
end
for i = 1, 4 do
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
chi[i].Transparency = chi[i].Transparency + .25
wait(.01)
end
end
end
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
chi[i]:Destroy()
end
end
end

--Arm Touch--
bladeactive = false
Hitbox.Touched:connect(function(hit)
if bladeactive == true then
if hit.Parent:FindFirstChild("Humanoid")~= nil and hit.Parent:FindFirstChild("HasBeenHit")== nil and hit.Parent ~= chara then
hitsnd:Play()
KillMortal(hit.Parent)
end
end
end)

--Teleport--
function Teleport(pos)
telesnd:Play()
local ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].ClassName == "Part" and ch[i].Name ~= "HumanoidRootPart" then
local trace = Instance.new("Part",game.Workspace)
trace.Size = ch[i].Size
trace.Material = "Neon"
trace.BrickColor = BrickColor.new("Really black")
trace.Transparency = .3
trace.CanCollide = false
trace.Anchored = true
trace.CFrame = ch[i].CFrame
if ch[i].Name == "Head" then
mehs = Instance.new("CylinderMesh",trace)
mehs.Scale = Vector3.new(1.25,1.25,1.25)
end
tracedisappear = coroutine.wrap(function()
wait(1)
for i = 1, 7 do
wait(.1)
trace.Transparency = trace.Transparency + .1
end
trace:Destroy()
end)
tracedisappear()
end
end
chara.Torso.CFrame = CFrame.new(pos.X,pos.Y,pos.Z)
end

--Grab--
function Grab(mouse)
local hit = mouse.Target
if hit ~= nil then
if hit.Parent:FindFirstChild("Humanoid")~=nil then
local torsy = nil
if hit.Parent:FindFirstChild("Torso")~=nil then
torsy = hit.Parent.Torso
elseif hit.Parent:FindFirstChild("UpperTorso")~=nil then
torsy = hit.Parent.UpperTorso
end
local bodpos = Instance.new("BodyPosition",torsy)
bodpos.Position = torsy.Position
wait(1)
burnsnd:Play()
hit.Parent.Humanoid.MaxHealth = 100
bodpos.Position = bodpos.Position + Vector3.new(0,4,0)
for i = 1, 10 do
wait(.1)
BurningEff(torsy)
hit.Parent.Humanoid.Health = hit.Parent.Humanoid.Health - 10
end
KillMortal(hit.Parent)
end
else end
end

--Button1Down--
dell = false
function onButton1Down()
if dell == false then
dell = true
swinganim:Play()
bladeactive = true
slashsnd:Play()
wait(.7)
bladeactive = false
dell = false
swinganim:Stop()
end
end

--KeyDowns--
function onKeyDown(key)
if key == "z" then
Teleport(Mouse.Hit.p + Vector3.new(0,2,0))
elseif key == "x" then
Grab(Mouse)
end
end

--Mouse Functions--
Mouse = player:GetMouse()
if Mouse then
Mouse.Button1Down:connect(onButton1Down)
Mouse.KeyDown:connect(onKeyDown)
end

--Death--
chara.Humanoid.Died:connect(function()
local pat = Instance.new("Part",game.Workspace)
pat.Transparency = 1
pat.Anchored = true
pat.CFrame = chara.Torso.CFrame
naeeym.Parent = pat
naeeym.Adornee = pat
skybox.Parent = game.Workspace
tecks.Text = "BAD CHOICE"
tecks.FontSize = "Size48"
tecks.TextColor3 = Color3.new(1,0,0)
music1:Stop()
music2:Stop()
deathmus.Parent = game.Workspace
deathex.Parent = game.Workspace
deathmus:Play()
deathex:Play()
game.Lighting.OutdoorAmbient = Color3.new(0,0,0)
game.Lighting.TimeOfDay = "00:00:00"
game.Lighting.FogColor = Color3.new(0,0,0)
game.Lighting.FogEnd = 1000
local ex = Instance.new("Explosion",game.Workspace)
ex.Position = chara.Torso.Position
ex.Visible = false
ex.BlastRadius = 999999999999999999999999
ex.BlastPressure = 9999999999999999999999999
end)

--Loop Function--
while true do
wait(.01)
chance = math.random(0,100)
if chance < 10 then
sel = math.random(1,3)
if sel == 1 then
tecks.Text = "NOHOPE"
elseif sel == 2 then
tecks.Text = "GIVEUP"
elseif sel == 3 then
tecks.Text = "BURNINHELL"
end
else tecks.Text = "John Doe"
end
if chara.Humanoid.Health > 0 then
chara.Humanoid.MaxHealth = math.huge
chara.Humanoid.Health = math.huge
game.Lighting.OutdoorAmbient = Color3.new(1,0,0)
game.Lighting.Ambient = Color3.new(1,0,0)
chara["Left Arm"].BrickColor = BrickColor.new("Cool yellow")
chara["Right Arm"].BrickColor = BrickColor.new("Cool yellow")
chara["Left Leg"].BrickColor = BrickColor.new("Medium blue")
chara["Right Leg"].BrickColor = BrickColor.new("Medium blue")
chara.Torso.BrickColor = BrickColor.new("Bright yellow")
chara["Left Arm"].Anchored = false
chara["Right Arm"].Anchored = false
chara["Left Leg"].Anchored = false
chara["Right Leg"].Anchored = false
chara.Torso.Anchored = false
ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].ClassName == "Accessory" or ch[i].ClassName == "Hat" then
ch[i]:Destroy()
end
end
tools = player.Backpack:GetChildren()
for i = 1, #tools do
if tools[i].ClassName == "HopperBin" then
tools[i]:Destroy()
end
end
skybox.CFrame = skybox.CFrame * CFrame.fromEulerAnglesXYZ(0,math.rad(1),0)
tecks.Position = UDim2.new(0,math.random(-3,3),0,math.random(-3,3))
local jtrace = Instance.new("Part",game.Workspace)
jtrace.Name = "JDTrace"
jtrace.Size = Vector3.new(10,0,10)
jtrace.Position = chara.Torso.Position
jtrace.CFrame = chara.Torso.CFrame - Vector3.new(0,3,0)
jtrace.Anchored = true
jtrace.CanCollide = false
jtrace.BrickColor = BrickColor.new("Really black")
jtrace.Material = "Granite"
BurningEff(jtrace)
game.Debris:AddItem(jtrace,1)
end
end
end)

TextButton_4.Parent = scriptframe
TextButton_4.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_4.Position = UDim2.new(0, 174, 0, 200)
TextButton_4.Size = UDim2.new(0, 123, 0, 50)
TextButton_4.Font = Enum.Font.SourceSans
TextButton_4.Text = "1x1x1x1"
TextButton_4.TextColor3 = Color3.new(0, 1, 1)
TextButton_4.TextScaled = true
TextButton_4.TextSize = 14
TextButton_4.TextWrapped = true

TextButton_4.MouseButton1Down:connect(function()
---------------------------------
--John Doe ---- (1x1x1x1 Edit)---
---------------------------------
---Script---------------Edited---
-----by-------------------by-----
--CKbackup----GlowingGlowstones--
---------------------------------

--Player Stuff--
player = game:GetService("Players").LocalPlayer
chara = player.Character

ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].Name == "Torso" then
ch[i].roblox.Transparency = 1
elseif ch[i].Name == "Head" then
ch[i].face.Transparency = 1
ch[i].Transparency = 1
elseif ch[i].ClassName == "Accessory" or ch[i].ClassName == "Shirt" or ch[i].ClassName == "Pants" or ch[i].ClassName == "ShirtGraphic" then
ch[i]:Destroy()
end
end

chara["Left Arm"].BrickColor = BrickColor.new("Really black")
chara["Right Arm"].BrickColor = BrickColor.new("Really black")
chara["Left Leg"].BrickColor = BrickColor.new("Really black")
chara["Right Leg"].BrickColor = BrickColor.new("Really black")
chara.Torso.BrickColor = BrickColor.new("Really black")

--Outfit--
New = function(Object, Parent, Name, Data)
	local Object = Instance.new(Object)
	for Index, Value in pairs(Data or {}) do
		Object[Index] = Value
	end
	Object.Parent = Parent
	Object.Name = Name
	return Object
end

function ScatterEff(part)
local eff1 = Instance.new("ParticleEmitter",part)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.9,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(1)
eff1.Speed = NumberRange.new(1)
eff1.Rate = 100
eff1.VelocitySpread = 10000
eff1.Texture = "rbxassetid://347504241"
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",part)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.9,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(1)
eff2.Speed = NumberRange.new(1)
eff2.Rate = 100
eff2.VelocitySpread = 10000
eff2.Texture = "rbxassetid://347504259"
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
end

function BurningEff(part)
local eff1 = Instance.new("ParticleEmitter",part)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(1)
eff1.Speed = NumberRange.new(0)
eff1.Rate = 100
eff1.Texture = "rbxassetid://347504241"
eff1.Acceleration = Vector3.new(0,10,0)
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",part)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(1)
eff2.Speed = NumberRange.new(0)
eff2.Rate = 100
eff2.Texture = "rbxassetid://347504259"
eff2.Acceleration = Vector3.new(0,10,0)
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
local eff3 = Instance.new("ParticleEmitter",part)
eff3.Size = NumberSequence.new(1)
eff3.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(1,1)})
eff3.LightEmission = 1
eff3.Lifetime = NumberRange.new(1)
eff3.Speed = NumberRange.new(0)
eff3.Rate = 100
eff3.Texture = "rbxasset://textures/particles/fire_main.dds"
eff3.Acceleration = Vector3.new(0,10,0)
eff3.Color = ColorSequence.new(Color3.new(1,0,0))
end

FakeHead = New("Model",chara,"FakeHead",{})
MainPart = New("Part",FakeHead,"MainPart",{FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(2, 1, 1),CFrame = CFrame.new(2.29537678, 7.81603718, 0.746068954, 0.00980896503, 0.00110200304, 0.999957919, -0.000536994543, 1.00000548, -0.00109680078, -0.99994874, -0.0005262224, 0.00980964955),CanCollide = false,TopSurface = Enum.SurfaceType.Smooth,})
Mesh = New("SpecialMesh",MainPart,"Mesh",{Scale = Vector3.new(1.25, 1.25, 1.25),})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara.Head,C0 = CFrame.new(0, 0, 0, 0.00980896503, -0.000536994543, -0.99994874, 0.00110200304, 1.00000548, -0.0005262224, 0.999957919, -0.00109680078, 0.00980964955),C1 = CFrame.new(5.96046448e-008, -8.58306885e-006, 0, 0.00980896503, -0.000536994543, -0.99994874, 0.00110200304, 1.00000548, -0.0005262224, 0.999957919, -0.00109680078, 0.00980964955),})
FakeHead.MainPart.BrickColor = BrickColor.new("Really black")
EyeFire = New("Part",FakeHead,"EyeFire",{BrickColor = BrickColor.new("Really red"),Material = Enum.Material.Neon,Size = Vector3.new(0.400000006, 0.200000003, 0.200000003),CFrame = CFrame.new(1.69668579, 8.11665249, 0.640022159, -0.00107900088, 0.999958038, -0.00980941113, -1.0000056, -0.00107390946, 0.000525554642, 0.000515007298, 0.00981007144, 0.999948859),CanCollide = false,Color = Color3.new(1, 0, 0),})
Mesh = New("CylinderMesh",EyeFire,"Mesh",{Offset = Vector3.new(0.0500000007, 0, -0.0399999991),Scale = Vector3.new(1, 0.150000006, 1),})
Weld = New("ManualWeld",EyeFire,"Weld",{Part0 = EyeFire,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0010790003, -0.999999344, 0.000515000196, 0.999951363, -0.0010738963, 0.00981000345, -0.00980944186, 0.000525560055, 0.99995178),C1 = CFrame.new(0.100008011, 0.300009251, -0.600027919, 0.00980899762, -0.000536999898, -0.99995178, 0.00110200245, 0.999999344, -0.000526215415, 0.999951363, -0.00109678751, 0.00980958249),})
Chest = New("Model",chara,"Chest",{})
MainPart = New("Part",Chest,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(2, 2, 1),CFrame = CFrame.new(2.2937007, 6.31611967, 0.746871948, 0.00980956201, 0.00110224239, 0.999954581, -0.000537135813, 1.00000238, -0.00109703222, -0.99995023, -0.000526354474, 0.00981019717),CanCollide = false,LeftSurface = Enum.SurfaceType.Weld,RightSurface = Enum.SurfaceType.Weld,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara.Torso,C0 = CFrame.new(0, 0, 0, 0.009809535, -0.000537137908, -0.99994725, 0.00110225554, 1.00000858, -0.000526368851, 0.999961257, -0.00109705783, 0.00981026888),C1 = CFrame.new(5.96046448e-008, -9.05990601e-006, -2.38418579e-007, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
CorruptedPart = New("Part",Chest,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.400000006, 0.800000072, 1),CFrame = CFrame.new(2.28977966, 7.11656427, 1.34486222, -0.00110228383, -0.00980954897, -0.9999578, -1.00000536, 0.000536905834, 0.00109708123, 0.000526248943, 0.99994868, -0.00981033035),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0011022957, -0.999999225, 0.000526249292, -0.00980958622, 0.000536918582, 0.99995172, -0.999951243, 0.0010970803, -0.00981026702),C1 = CFrame.new(-0.598430753, 0.800122261, 0.00106739998, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
CorruptedPart = New("Part",Chest,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.400000006, 0.400000066, 1),CFrame = CFrame.new(2.29174757, 6.71645212, 1.54485857, -0.00110228383, -0.00980954897, -0.9999578, -1.00000536, 0.000536905834, 0.00109708123, 0.000526248943, 0.99994868, -0.00981033035),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.0011022957, -0.999999225, 0.000526249292, -0.00980958622, 0.000536918582, 0.99995172, -0.999951243, 0.0010970803, -0.00981026702),C1 = CFrame.new(-0.798183441, 0.399908543, 0.00543618202, 0.00980956666, -0.000537143264, -0.99995023, 0.00110225484, 1.00000238, -0.000526361808, 0.999954581, -0.00109704456, 0.00981020182),})
LeftArm = New("Model",chara,"LeftArm",{})
MainPart = New("Part",LeftArm,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(1.90889204, 6.31596565, 3.24640989, -0.0484240092, -0.0324009918, 0.998301268, -0.00117100019, 0.999474883, 0.0323822871, -0.998826265, 0.000399069104, -0.0484365262),CanCollide = false,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Left Arm"],C0 = CFrame.new(0, 0, 0, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),C1 = CFrame.new(0, -8.10623169e-006, -2.38418579e-007, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(1.48370504, 6.50245714, 2.8663168, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(0.400017738, 0.200018406, -0.400015235, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.51924801, 6.60332775, 3.66543078, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.399997473, 0.300003052, -0.399972558, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
EffCorruptedPart = New("Part",LeftArm,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 1),CFrame = CFrame.new(1.92512023, 5.81624889, 3.24619365, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(1.52587891e-005, -0.49998045, 2.90870667e-005, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000072, 0.200000003),CFrame = CFrame.new(2.31463432, 6.72918367, 3.62673688, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.400012016, 0.400006294, 0.400012136, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(1.50631011, 6.40297413, 3.26581192, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(1.3589859e-005, 0.100014687, -0.400020242, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
CorruptedPart = New("Part",LeftArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000036, 0.200000003),CFrame = CFrame.new(1.92179501, 6.51633835, 3.64602208, -0.048417028, -0.0324150361, 0.998301387, -0.00116700074, 0.999474525, 0.03239654, -0.998826742, 0.000403525919, -0.0484294258),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.048417028, -0.00116700074, -0.998826623, -0.0324150361, 0.999474466, 0.000403525832, 0.998301208, 0.0323965363, -0.0484294109),C1 = CFrame.new(-0.40000248, 0.200008869, 1.37090683e-005, -0.0484240092, -0.00117100019, -0.998826265, -0.0324009918, 0.999474883, 0.000399069104, 0.998301268, 0.0323822871, -0.0484365262),})
BurningEff(EffCorruptedPart)
LeftLeg = New("Model",chara,"LeftLeg",{})
MainPart = New("Part",LeftLeg,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.2865479, 1.31659603, 1.24781799, 0.00980953407, 0.00110225566, 0.999961138, -0.000537137908, 1.00000858, -0.00109705783, -0.99994719, -0.000526368851, 0.00981026888),CanCollide = false,BottomSurface = Enum.SurfaceType.Smooth,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Left Leg"],C0 = CFrame.new(0, 0, 0, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),C1 = CFrame.new(0, -8.58306885e-006, -2.38418579e-007, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
EffCorruptedPart = New("Part",LeftLeg,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.200000048, 1),CFrame = CFrame.new(2.28007793, 0.400032878, 1.25993299, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.0116856098, -0.916567385, -0.00534534454, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.88013697, 0.800038397, 0.859943509, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(0.3841483, -0.516796231, -0.40962553, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000012, 0.200000003),CFrame = CFrame.new(2.69002914, 0.915953577, 0.851962805, 0.999971032, 0.0011022269, -0.00980960391, -0.00109704852, 1.00001776, 0.000537177373, 0.00981036108, -0.000526409131, 0.999942601),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999951303, -0.0010970087, 0.00981015898, 0.00110222446, 0.999999166, -0.000526388001, -0.00980970077, 0.00053719338, 0.99995172),C1 = CFrame.new(0.400011122, -0.399985313, 0.400013685, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000012, 0.200000003),CFrame = CFrame.new(1.88013721, 0.900040269, 1.65993917, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.415866137, -0.41721642, -0.40188694, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(1.88013721, 0.600035727, 1.25993288, 1.00001979, -3.03611159e-007, -5.47617674e-007, 5.67175448e-007, 1.00001717, -5.60779881e-007, -1.86450779e-006, 9.50574758e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 5.86369708e-007, -2.15602267e-006, -2.8440752e-007, 0.999998569, 9.76819592e-007, -8.39119252e-007, -5.34477465e-007, 0.999998569),C1 = CFrame.new(-0.0157161951, -0.717007458, -0.405481935, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.28007793, 0.700037479, 1.65993929, 1.00001967, -3.84054147e-007, 3.90969217e-006, 6.35045581e-007, 1.00001717, -5.60838998e-007, -6.19795173e-006, 9.32147486e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 6.5424797e-007, -6.48946025e-006, -3.64865258e-007, 0.999998629, 9.58411874e-007, 3.61912225e-006, -5.34497644e-007, 0.999998629),C1 = CFrame.new(-0.411835551, -0.616776347, -0.00175023079, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 1.20000005, 0.200000003),CFrame = CFrame.new(2.68018699, 1.10004401, 1.65993941, 1.00001967, -3.84054147e-007, 3.90969217e-006, 6.35045581e-007, 1.00001717, -5.60838998e-007, -6.19795173e-006, 9.32147486e-007, 0.99998951),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 1, 6.5424797e-007, -6.48946025e-006, -3.64865258e-007, 0.999998629, 9.58411874e-007, 3.61912225e-006, -5.34497644e-007, 0.999998629),C1 = CFrame.new(-0.408125639, -0.216332912, 0.397896528, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
CorruptedPart = New("Part",LeftLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(2.68596959, 0.816166699, 1.25195313, 0.999971032, 0.0011022269, -0.00980960391, -0.00109704852, 1.00001776, 0.000537177373, 0.00981036108, -0.000526409131, 0.999942601),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999951303, -0.0010970087, 0.00981015898, 0.00110222446, 0.999999166, -0.000526388001, -0.00980970077, 0.00053719338, 0.99995172),C1 = CFrame.new(5.20944595e-005, -0.499986172, 0.399987936, 0.00980953407, -0.000537137908, -0.99994719, 0.00110225566, 1.00000858, -0.000526368851, 0.999961138, -0.00109705783, 0.00981026888),})
ScatterEff(EffCorruptedPart)
RightArm = New("Model",chara,"RightArm",{})
MainPart = New("Part",RightArm,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.011096, 6.31690788, -3.92582893, 0.00918400101, -0.262283146, 0.964947343, 0.259330034, 0.932596445, 0.251021653, -0.965745091, 0.247934431, 0.0765828639),CanCollide = false,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Right Arm"],C0 = CFrame.new(0, 0, 0, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),C1 = CFrame.new(-2.86102295e-006, -9.05990601e-006, -2.38418579e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
Hitbox = New("Part",RightArm,"Hitbox",{BrickColor = BrickColor.new("Really black"),Transparency = 1,Transparency = 1,Size = Vector3.new(1, 4, 1),CFrame = CFrame.new(22.2733669, 5.0842762, -22.1737366, -0.964945257, -0.262290984, 0.00919180829, -0.251027077, 0.93259424, 0.259333313, -0.0765930116, 0.247935042, -0.965744138),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Weld = New("ManualWeld",Hitbox,"Weld",{Part0 = Hitbox,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945257, -0.251027077, -0.0765930116, -0.262290984, 0.93259424, 0.247935042, 0.00919180829, 0.259333313, -0.965744138),C1 = CFrame.new(-1.52587891e-005, -1.00003147, -1.71661377e-005, 0.0091838371, 0.259330064, -0.965745151, -0.262283117, 0.932596445, 0.247934505, 0.964947283, 0.251021653, 0.0765827149),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.011096, 6.3169179, -3.92581391, -0.964945257, -0.262290984, 0.00919180829, -0.251027077, 0.93259424, 0.259333313, -0.0765930116, 0.247935042, -0.965744138),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945138, -0.251027018, -0.0765930042, -0.262290984, 0.932594121, 0.247935027, 0.00919180084, 0.259333313, -0.965744197),C1 = CFrame.new(-1.1920929e-005, 1.28746033e-005, 3.57627869e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.600000024, 0.400000036),CFrame = CFrame.new(2.14866924, 6.03215551, -4.72580194, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.699988842, -0.499982834, 7.62939453e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1.20000005, 0.600000024),CFrame = CFrame.new(2.63876629, 4.02682734, -4.32773018, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(-0.199987888, -2.39999342, 3.02791595e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 0.600000024),CFrame = CFrame.new(1.62134135, 7.81954479, -3.94021821, 0.964945078, -0.262291819, -0.00918725226, 0.251029015, 0.932593465, -0.259333432, 0.0765890032, 0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.964944899, 0.251028955, 0.0765889958, -0.262291819, 0.932593465, 0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.399995804, 1.5000124, -2.38418579e-007, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.600000024, 0.400000036),CFrame = CFrame.new(2.35483098, 5.18234444, -4.53787422, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.300010204, -1.29999256, 1.40666962e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1, 0.600000024),CFrame = CFrame.new(1.88730097, 6.99068737, -4.57445002, -0.964945078, 0.262291819, -0.00918725226, -0.251029015, -0.932593465, -0.259333432, -0.0765890032, -0.247936144, 0.965744317),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("SpecialMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),MeshType = Enum.MeshType.Wedge,})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964944899, -0.251028955, -0.0765889958, 0.262291819, -0.932593465, -0.247936144, -0.00918724574, -0.259333432, 0.965744257),C1 = CFrame.new(0.799996853, 0.50001812, 4.29153442e-006, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
CorruptedPart = New("Part",RightArm,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 0.800000072, 0.600000024),CFrame = CFrame.new(2.37646794, 4.9594202, -4.07979012, -0.964945316, -0.262290984, 0.00918756705, -0.251028091, 0.932593942, 0.259333163, -0.0765890256, 0.247935995, -0.965744197),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, -0.964945138, -0.251028031, -0.0765890107, -0.262290955, 0.932593882, 0.247935966, 0.0091875596, 0.259333193, -0.965744257),C1 = CFrame.new(-0.199994564, -1.39999104, 1.52587891e-005, 0.00918400101, 0.259330034, -0.965745091, -0.262283146, 0.932596445, 0.247934431, 0.964947343, 0.251021653, 0.0765828639),})
RightLeg = New("Model",chara,"RightLeg",{})
MainPart = New("Part",RightLeg,"MainPart",{Transparency = 1,Transparency = 1,FormFactor = Enum.FormFactor.Symmetric,Size = Vector3.new(1, 2, 1),CFrame = CFrame.new(2.29641008, 1.31540966, 0.248092994, 0.00933599845, 0.00110999751, 0.999955773, -0.0030579993, 0.999994755, -0.00108149007, -0.99995178, -0.0030477671, 0.00933934376),CanCollide = false,BottomSurface = Enum.SurfaceType.Smooth,})
Weld = New("ManualWeld",MainPart,"Weld",{Part0 = MainPart,Part1 = chara["Right Leg"],C0 = CFrame.new(0, 0, 0, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),C1 = CFrame.new(2.98023224e-008, -8.58306885e-006, 2.38418579e-007, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.200000003, 0.200000003),CFrame = CFrame.new(2.70045996, 1.61376095, -0.149078026, 0.999955833, 0.00111049914, -0.0093326522, -0.00108199986, 0.999994755, 0.00305823679, 0.00933599938, -0.00304800388, 0.999951839),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955893, -0.00108199986, 0.00933599938, 0.00111049926, 0.999994755, -0.00304800388, -0.0093326522, 0.00305823679, 0.99995178),C1 = CFrame.new(0.400011688, 0.300008655, 0.400000095, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(1.90071809, 1.81462395, -0.157150015, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(0.400002658, 0.50000751, -0.399999142, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000036, 0.200000003),CFrame = CFrame.new(1.896873, 1.71584904, 0.243133992, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(4.14252281e-006, 0.400008917, -0.399998784, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.800000072, 0.200000003),CFrame = CFrame.new(1.89314091, 1.71706903, 0.643112063, 0.999955714, 0.00111050205, -0.0093366541, -0.00108199974, 0.999994755, 0.00305724167, 0.00933999754, -0.00304700364, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111050217, 0.999994755, -0.00304700388, -0.00933665317, 0.00305724121, 0.99995178),C1 = CFrame.new(-0.399993181, 0.400005698, -0.399996519, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
EffCorruptedPart = New("Part",RightLeg,"EffCorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(1, 1.20000005, 1),CFrame = CFrame.new(2.29597116, 0.915416002, 0.249298006, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",EffCorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",EffCorruptedPart,"Weld",{Part0 = EffCorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(1.41263008e-005, -0.399995744, 5.00679016e-006, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.300596, 1.71419013, -0.153122023, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(0.400015235, 0.400005817, 7.39097595e-006, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.600000024, 0.200000003),CFrame = CFrame.new(2.69322205, 1.81620288, 0.650299072, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(-0.400013447, 0.500005245, 0.400009155, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
CorruptedPart = New("Part",RightLeg,"CorruptedPart",{BrickColor = BrickColor.new("Really black"),Material = Enum.Material.Granite,Size = Vector3.new(0.200000003, 0.400000006, 0.200000003),CFrame = CFrame.new(2.69684124, 1.71498096, 0.250625998, 0.999955714, 0.00111051137, -0.00933665317, -0.00108199974, 0.999994755, 0.00305824191, 0.00933999754, -0.00304800365, 0.999951899),CanCollide = false,BackSurface = Enum.SurfaceType.SmoothNoOutlines,BottomSurface = Enum.SurfaceType.SmoothNoOutlines,FrontSurface = Enum.SurfaceType.SmoothNoOutlines,LeftSurface = Enum.SurfaceType.SmoothNoOutlines,RightSurface = Enum.SurfaceType.SmoothNoOutlines,TopSurface = Enum.SurfaceType.SmoothNoOutlines,Color = Color3.new(0.0666667, 0.0666667, 0.0666667),})
Mesh = New("BlockMesh",CorruptedPart,"Mesh",{Scale = Vector3.new(1.10000002, 1.10000002, 1.10000002),})
Weld = New("ManualWeld",CorruptedPart,"Weld",{Part0 = CorruptedPart,Part1 = MainPart,C0 = CFrame.new(0, 0, 0, 0.999955773, -0.00108199974, 0.00933999848, 0.00111051148, 0.999994755, -0.00304800388, -0.00933665223, 0.00305824145, 0.99995178),C1 = CFrame.new(-1.63316727e-005, 0.400005937, 0.400005102, 0.00933599845, -0.0030579993, -0.99995178, 0.00110999751, 0.999994755, -0.0030477671, 0.999955773, -0.00108149007, 0.00933934376),})
ScatterEff(EffCorruptedPart)

sa = RightArm:GetChildren()
for i = 1, #sa do
ScatterEff(sa[i])
end

local eff1 = Instance.new("ParticleEmitter",EyeFire)
eff1.Size = NumberSequence.new(.1)
eff1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff1.LightEmission = 1
eff1.Lifetime = NumberRange.new(.5)
eff1.Speed = NumberRange.new(1)
eff1.EmissionDirection = "Front"
eff1.Rate = 100
eff1.Texture = "rbxassetid://347504241"
eff1.Acceleration = Vector3.new(0,10,0)
eff1.Color = ColorSequence.new(Color3.new(1,0,0))
local eff2 = Instance.new("ParticleEmitter",EyeFire)
eff2.Size = NumberSequence.new(.1)
eff2.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(.2,0),NumberSequenceKeypoint.new(1,1)})
eff2.LightEmission = 1
eff2.Lifetime = NumberRange.new(.5)
eff2.Speed = NumberRange.new(1)
eff2.EmissionDirection = "Front"
eff2.Rate = 100
eff2.Texture = "rbxassetid://347504259"
eff2.Acceleration = Vector3.new(0,10,0)
eff2.Color = ColorSequence.new(Color3.new(1,0,0))
local eff3 = Instance.new("ParticleEmitter",EyeFire)
eff3.Size = NumberSequence.new(.1)
eff3.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0),NumberSequenceKeypoint.new(1,1)})
eff3.LightEmission = 1
eff3.Lifetime = NumberRange.new(.5)
eff3.Speed = NumberRange.new(1)
eff3.EmissionDirection = "Front"
eff3.Rate = 100
eff3.Texture = "rbxasset://textures/particles/fire_main.dds"
eff3.Acceleration = Vector3.new(0,10,0)
eff3.Color = ColorSequence.new(Color3.new(1,0,0))

--Sounds--
slashsnd = New("Sound",chara.Torso,"Slash",{SoundId = "rbxassetid://28144425",PlaybackSpeed = .7,Volume = 5})
hitsnd = New("Sound",chara.Torso,"Hit",{SoundId = "rbxassetid://429400881",PlaybackSpeed = .7,Volume = 5})
telesnd = New("Sound",chara.Torso,"Tele",{SoundId = "rbxassetid://2767090",PlaybackSpeed = .7,Volume = 5})
burnsnd = New("Sound",chara.Torso,"Burn",{SoundId = "rbxassetid://32791565",PlaybackSpeed = .7,Volume = 5})
music1 = New("Sound",chara.Torso,"Music1",{SoundId = "rbxassetid://692430417",PlaybackSpeed = .5,Volume = 10,Looped = true})
music2 = New("Sound",chara.Torso,"Music2",{SoundId = "rbxassetid://11984351",PlaybackSpeed = .2,Volume = 5,Looped = true})
deathmus = New("Sound",chara.Torso,"DeathMus",{SoundId = "rbxassetid://678930213",PlaybackSpeed = .5,Volume = 5,Looped = true})
deathex = New("Sound",chara.Torso,"DeathEx",{SoundId = "rbxassetid://11984351",PlaybackSpeed = 1,Volume = 5})
music1:Play()
music2:Play()

--Animations--
swinganim = chara.Humanoid:LoadAnimation(New("Animation",chara,"Swing",{AnimationId = "rbxassetid://186934658"}))

--Name Tag--
local naeeym = Instance.new("BillboardGui",chara)
naeeym.Size = UDim2.new(0,100,0,40)
naeeym.StudsOffset = Vector3.new(0,2,0)
naeeym.Adornee = chara.Head
local tecks = Instance.new("TextLabel",naeeym)
tecks.BackgroundTransparency = 1
tecks.BorderSizePixel = 0
tecks.Text = "1x1x1x1"
tecks.Font = "Fantasy"
tecks.FontSize = "Size24"
tecks.TextStrokeTransparency = 0
tecks.TextStrokeColor3 = Color3.new(0,0,0)
tecks.TextColor3 = Color3.new(0,0,0)
tecks.Size = UDim2.new(1,0,0.5,0)

--Skybox--
skybox = Instance.new("Part",chara)
skybox.Size = Vector3.new(0,0,0)
skybox.Anchored = true
skybox.CanCollide = true
skyboxmesh = Instance.new("SpecialMesh",skybox)
skyboxmesh.MeshId = "http://www.roblox.com/asset/?id=0"
skyboxmesh.TextureId = "http://www.roblox.com/asset/?id=0"
skyboxmesh.VertexColor = Vector3.new(0,0,0)
skyboxmesh.Scale = Vector3.new(-3000,-1000,-3000)

--Soul Steal--
function SoulSteal(pos)
local soulst = coroutine.wrap(function()
local soul = Instance.new("Part",chara)
soul.Size = Vector3.new(0,0,0)
soul.CanCollide = false
soul.Anchored = false
soul.Position = pos
soul.CFrame = CFrame.new(pos.X,pos.Y,pos.Z)
soul.Transparency = 1
local ptc = Instance.new("ParticleEmitter",soul)
ptc.Texture = "http://www.roblox.com/asset/?id=413366101"
ptc.Size = NumberSequence.new(.5)
ptc.LockedToPart = true
ptc.Speed = NumberRange.new(0)
ptc.Lifetime = NumberRange.new(9999)
local bodpos = Instance.new("BodyPosition",soul)
bodpos.Position = pos
wait(2)
soul.Touched:connect(function(hit)
if hit.Parent == chara then
soul:Destroy()
end
end)
while soul do
wait(.1)
bodpos.Position = chara.Torso.Position
end
end)
soulst()
end

--Death of a Mortal--
function KillMortal(hitdude)
local torsy = nil
if hitdude:FindFirstChild("Torso")~=nil then
torsy = hitdude.Torso	
elseif hitdude:FindFirstChild("UpperTorso")~=nil then
torsy = hitdude.UpperTorso
end
local val = Instance.new("ObjectValue",hitdude)
val.Name = "HasBeenHit"
hitdude:BreakJoints()
hitdude.Humanoid:Destroy()
SoulSteal(torsy.Position)
local chi = hitdude:GetChildren()
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
local bodpos = Instance.new("BodyPosition",chi[i])
bodpos.Position = chi[i].Position + Vector3.new(math.random(-5,5),math.random(-5,5),math.random(-5,5))
ScatterEff(chi[i])
chi[i].BrickColor = BrickColor.new("Really black")
end
end
for i = 1, 4 do
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
chi[i].Transparency = chi[i].Transparency + .25
wait(.01)
end
end
end
for i = 1, #chi do
if chi[i].ClassName == "Part" or chi[i].ClassName == "MeshPart" then
chi[i]:Destroy()
end
end
end

--Arm Touch--
bladeactive = false
Hitbox.Touched:connect(function(hit)
if bladeactive == true then
if hit.Parent:FindFirstChild("Humanoid")~= nil and hit.Parent:FindFirstChild("HasBeenHit")== nil and hit.Parent ~= chara then
hitsnd:Play()
KillMortal(hit.Parent)
end
end
end)

--Teleport--
function Teleport(pos)
telesnd:Play()
local ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].ClassName == "Part" and ch[i].Name ~= "HumanoidRootPart" then
local trace = Instance.new("Part",game.Workspace)
trace.Size = ch[i].Size
trace.Material = "Neon"
trace.BrickColor = BrickColor.new("Really black")
trace.Transparency = .3
trace.CanCollide = false
trace.Anchored = true
trace.CFrame = ch[i].CFrame
if ch[i].Name == "Head" then
mehs = Instance.new("CylinderMesh",trace)
mehs.Scale = Vector3.new(1.25,1.25,1.25)
end
tracedisappear = coroutine.wrap(function()
wait(1)
for i = 1, 7 do
wait(.1)
trace.Transparency = trace.Transparency + .1
end
trace:Destroy()
end)
tracedisappear()
end
end
chara.Torso.CFrame = CFrame.new(pos.X,pos.Y,pos.Z)
end

--Grab--
function Grab(mouse)
local hit = mouse.Target
if hit ~= nil then
if hit.Parent:FindFirstChild("Humanoid")~=nil then
local torsy = nil
if hit.Parent:FindFirstChild("Torso")~=nil then
torsy = hit.Parent.Torso
elseif hit.Parent:FindFirstChild("UpperTorso")~=nil then
torsy = hit.Parent.UpperTorso
end
local bodpos = Instance.new("BodyPosition",torsy)
bodpos.Position = torsy.Position
wait(1)
burnsnd:Play()
hit.Parent.Humanoid.MaxHealth = 100
bodpos.Position = bodpos.Position + Vector3.new(0,4,0)
for i = 1, 10 do
wait(.1)
BurningEff(torsy)
hit.Parent.Humanoid.Health = hit.Parent.Humanoid.Health - 10
end
KillMortal(hit.Parent)
end
else end
end

--Button1Down--
dell = false
function onButton1Down()
if dell == false then
dell = true
swinganim:Play()
bladeactive = true
slashsnd:Play()
wait(.7)
bladeactive = false
dell = false
swinganim:Stop()
end
end

--KeyDowns--
function onKeyDown(key)
if key == "z" then
Teleport(Mouse.Hit.p + Vector3.new(0,2,0))
elseif key == "x" then
Grab(Mouse)
end
end

--Mouse Functions--
Mouse = player:GetMouse()
if Mouse then
Mouse.Button1Down:connect(onButton1Down)
Mouse.KeyDown:connect(onKeyDown)
end

--Death--
chara.Humanoid.Died:connect(function()
local pat = Instance.new("Part",game.Workspace)
pat.Transparency = 1
pat.Anchored = true
pat.CFrame = chara.Torso.CFrame
naeeym.Parent = pat
naeeym.Adornee = pat
skybox.Parent = game.Workspace
tecks.Text = "BAD CHOICE"
tecks.FontSize = "Size48"
tecks.TextColor3 = Color3.new(1,0,0)
music1:Stop()
music2:Stop()
deathmus.Parent = game.Workspace
deathex.Parent = game.Workspace
deathmus:Play()
deathex:Play()
game.Lighting.OutdoorAmbient = Color3.new(0,0,0)
game.Lighting.TimeOfDay = "00:00:00"
game.Lighting.FogColor = Color3.new(0,0,0)
game.Lighting.FogEnd = 1000
local ex = Instance.new("Explosion",game.Workspace)
ex.Position = chara.Torso.Position
ex.Visible = false
ex.BlastRadius = 999999999999999999999999
ex.BlastPressure = 9999999999999999999999999
end)

--Loop Function--
while true do
wait(.01)
chance = math.random(0,100)
if chance < 10 then
sel = math.random(1,3)
if sel == 1 then
tecks.Text = "HACKED"
elseif sel == 2 then
tecks.Text = "GODIE"
elseif sel == 3 then
tecks.Text = "BURNINHELL"
end
else tecks.Text = "1x1x1x1"
end
if chara.Humanoid.Health > 0 then
chara.Humanoid.MaxHealth = math.huge
chara.Humanoid.Health = math.huge
game.Lighting.OutdoorAmbient = Color3.new(0,0,0)
game.Lighting.Ambient = Color3.new(0,0,0)
chara["Left Arm"].BrickColor = BrickColor.new("Really black")
chara["Right Arm"].BrickColor = BrickColor.new("Really black")
chara["Left Leg"].BrickColor = BrickColor.new("Really black")
chara["Right Leg"].BrickColor = BrickColor.new("Really black")
chara.Torso.BrickColor = BrickColor.new("Really black")
chara["Left Arm"].Anchored = false
chara["Right Arm"].Anchored = false
chara["Left Leg"].Anchored = false
chara["Right Leg"].Anchored = false
chara.Torso.Anchored = false
ch = chara:GetChildren()
for i = 1, #ch do
if ch[i].ClassName == "Accessory" or ch[i].ClassName == "Hat" then
ch[i]:Destroy()
end
end
tools = player.Backpack:GetChildren()
for i = 1, #tools do
if tools[i].ClassName == "HopperBin" then
tools[i]:Destroy()
end
end
skybox.CFrame = skybox.CFrame * CFrame.fromEulerAnglesXYZ(0,math.rad(1),0)
tecks.Position = UDim2.new(0,math.random(-3,3),0,math.random(-3,3))
local jtrace = Instance.new("Part",game.Workspace)
jtrace.Name = "JDTrace"
jtrace.Size = Vector3.new(10,0,10)
jtrace.Position = chara.Torso.Position
jtrace.CFrame = chara.Torso.CFrame - Vector3.new(0,3,0)
jtrace.Anchored = true
jtrace.CanCollide = false
jtrace.BrickColor = BrickColor.new("Really black")
jtrace.Material = "Granite"
BurningEff(jtrace)
game.Debris:AddItem(jtrace,1)
end
end
end)

TextButton_5.Parent = scriptframe
TextButton_5.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_5.Position = UDim2.new(0, 0, 0, 268)
TextButton_5.Size = UDim2.new(0, 123, 0, 50)
TextButton_5.Font = Enum.Font.SourceSans
TextButton_5.Text = "Scp Dark Demo"
TextButton_5.TextColor3 = Color3.new(0, 1, 1)
TextButton_5.TextScaled = true
TextButton_5.TextSize = 14
TextButton_5.TextWrapped = true

TextButton_5.MouseButton1Down:connect(function()
p = (game.Players.LocalPlayer.Name)
char = game.Players.LocalPlayer.Character


local player = game.Players.LocalPlayer
repeat wait() until player.Character.Humanoid
local humanoid = player.Character.Humanoid
local mouse = player:GetMouse()

for i,v in pairs(char:GetChildren()) do
   if v.ClassName == 'Hat' then
       v:Destroy()
   end
end

ScarySound1 = Instance.new("Sound")
ScarySound1.Parent = char.Torso
ScarySound1.SoundId = "rbxassetid://177113856"
ScarySound1.Volume = 1

ScarySound2 = Instance.new("Sound")
ScarySound2.Parent = char.Torso
ScarySound2.SoundId = "rbxassetid://234313800"
ScarySound2.Volume = 0.5
ScarySound2.Looped = true

ScarySound3 = Instance.new("Sound")
ScarySound3.Parent = char.Torso
ScarySound3.SoundId = "rbxassetid://254933693"
ScarySound3.Volume = 0.5
ScarySound3.Looped = true

Punch = Instance.new("Sound")
Punch.Parent = char.Torso
Punch.SoundId = "rbxassetid://261566877"
Punch.Volume = 1
Punch.Looped = false

hole = Instance.new("Sound")
hole.Parent = char.Torso
hole.SoundId = "rbxassetid://266364769"
hole.Volume = 1
hole.Looped = false

game.Players.LocalPlayer.Character.Sound:Destroy()

function Normal()
	ScarySound3:Play()
	char.Humanoid.WalkSpeed = 16
char.Head.face.Texture = "rbxassetid://443236276"
char["Left Leg"].Transparency = 0.5
char["Head"].Transparency = 0.5
char["Right Leg"].Transparency = 0.5
char["Torso"].Transparency = 0.5
char["Left Arm"].Transparency = 0.5
char["Right Arm"].Transparency = 0.5
end

function GoInvisible()
	ScarySound3:Stop()
ScarySound1:Stop()
	char.Humanoid.WalkSpeed = 120
	char.Head.face.Transparency = 1
	char["Left Leg"].Transparency = 0.5
char["Head"].Transparency = 0.5
char["Right Leg"].Transparency = 0.5
char["Torso"].Transparency = 0.5
char["Left Arm"].Transparency = 0.5
char["Right Arm"].Transparency = 0.5
wait(0.001)
char["Left Leg"].Transparency = 0.6
char["Head"].Transparency = 0.6
char["Right Leg"].Transparency = 0.6
char["Torso"].Transparency = 0.6
char["Left Arm"].Transparency = 0.6
char["Right Arm"].Transparency = 0.6
wait(0.001)
char["Left Leg"].Transparency = 0.7
char["Head"].Transparency = 0.7
char["Right Leg"].Transparency = 0.7
char["Torso"].Transparency = 0.7
char["Left Arm"].Transparency = 0.7
char["Right Arm"].Transparency = 0.7
wait(0.001)
char["Left Leg"].Transparency = 1
char["Head"].Transparency = 1
char["Right Leg"].Transparency = 1
char["Torso"].Transparency = 1
char["Left Arm"].Transparency = 1
char["Right Arm"].Transparency = 1
end

function GoVisible()
	ScarySound3:Play()
	char.Humanoid.WalkSpeed = 16
	ScarySound1:Play()
	char.Head.face.Transparency = 0
	char["Left Leg"].Transparency = 0.9
char["Head"].Transparency = 0.9
char["Right Leg"].Transparency = 9
char["Torso"].Transparency = 0.9
char["Left Arm"].Transparency = 0.9
char["Right Arm"].Transparency = 0.9
wait(0.001)
char["Left Leg"].Transparency = 0.7
char["Head"].Transparency = 0.7
char["Right Leg"].Transparency = 0.7
char["Torso"].Transparency = 0.7
char["Left Arm"].Transparency = 0.7
char["Right Arm"].Transparency = 0.7
wait(0.001)
char["Left Leg"].Transparency = 0.5
char["Head"].Transparency = 0.5
char["Right Leg"].Transparency = 0.5
char["Torso"].Transparency = 0.5
char["Left Arm"].Transparency = 0.5
char["Right Arm"].Transparency = 0.5

end

Normal()

local anim = Instance.new("Animation")
anim.AnimationId = "rbxassetid://191123156"

mouse.KeyDown:connect(function(key)
	if key == "z" then
		if char.Head.Transparency == 0.5 then
		GoInvisible()
		
		elseif char.Head.Transparency == 1 then
		GoVisible()
	end
end end)

mouse.KeyDown:connect(function(key)
	if key == "x" then
		if ScarySound2.IsPlaying == false then
			ScarySound2:Play()
		elseif ScarySound2.IsPlaying == true then
			ScarySound2:Stop()
			
			
	end
end end)

function onTouch(part)

local humanoid = part.Parent:findFirstChild("Humanoid")
local model = part.Parent
local torso = part.Parent:findFirstChild("Torso")
local head = part.Parent:findFirstChild("Head")
local leftleg = part.Parent:findFirstChild("Left Leg")
local rightleg = part.Parent:findFirstChild("Right Leg")
local leftarm = part.Parent:findFirstChild("Left Arm")
local rightarm = part.Parent:findFirstChild("Right Arm")


if (humanoid ~=nil) then

--humanoid.Health = 0

head.BrickColor = BrickColor.new("Really black")
torso.BrickColor = BrickColor.new("Really black")
leftleg.BrickColor = BrickColor.new("Really black")
rightleg.BrickColor = BrickColor.new("Really black")
rightarm.BrickColor = BrickColor.new("Really black")
leftarm.BrickColor = BrickColor.new("Really black")
humanoid.Sit = true
wait(0.5)
torso.Anchored = true
wait(3)

e=Instance.new('Part', model)
e.Size = Vector3.new(2.25,2.25,2.25)
e.Transparency = 1
e.Anchored = true
e.CFrame = CFrame.new(head.Position)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)
wait(0.1)
head.Mesh.Scale = head.Mesh.Scale + Vector3.new(0.01,0.01,0.01)


wait(2)
head:Destroy()
q=Instance.new('ParticleEmitter', e)
q.Size = NumberSequence.new(0.5)
q.Rate = 50
q.Transparency = NumberSequence.new(0.5)
q.Speed = NumberRange.new(7)
q.VelocitySpread = 100
q.Lifetime = NumberRange.new(1)
q.Texture = 'rbxassetid://122275188'

torso.Anchored = true
rightleg.Anchored = true
leftleg.Anchored = true
rightarm.Anchored = true
leftarm.Anchored = true
ded = Instance.new("Sound")
ded.Parent = torso
ded.SoundId = "rbxassetid://131060226"
ded.Volume = 1
ded.Looped = false
wait()
ded:Play()




end

end 



char.Torso.Touched:connect(onTouch)

mouse.KeyDown:connect(function(key)
	if key == "c" then
		local playAnim = humanoid:LoadAnimation(anim)

			Punch:Play()	
			playAnim:Play()
			
			
			
	end
end)

debounce = false

function onTouched(hit)
hole:Play()
hit.CanCollide=false
wait(.5)
hit.CanCollide = true
debounce = true

end
game.Players.LocalPlayer.Character.Torso.Touched:connect(onTouched)


while wait() do
	char["Left Leg"].BrickColor = BrickColor.new("Really black")
	char["Head"].BrickColor = BrickColor.new("Really black")
	char["Right Leg"].BrickColor = BrickColor.new("Really black")
	char["Torso"].BrickColor = BrickColor.new("Really black")
	char["Left Arm"].BrickColor = BrickColor.new("Really black")
	char["Right Arm"].BrickColor = BrickColor.new("Really black")
end
end)

TextButton_6.Parent = scriptframe
TextButton_6.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_6.Position = UDim2.new(0, 157, 0, 275)
TextButton_6.Size = UDim2.new(0, 123, 0, 50)
TextButton_6.Font = Enum.Font.SourceSans
TextButton_6.Text = "Mario Bomb"
TextButton_6.TextColor3 = Color3.new(0, 1, 1)
TextButton_6.TextScaled = true
TextButton_6.TextSize = 14
TextButton_6.TextWrapped = true

TextButton_6.MouseButton1Down:connect(function()
--[[qaeo baeo haeo]]--
wait(1 / 60)
Effects = { }
local Player = game.Players.localPlayer
local Character = Player.Character
local Humanoid = Character.Humanoid
local mouse = Player:GetMouse()
local m = Instance.new('Model', Character)
m.Name = "WeaponModel"
Character["Left Arm"]:remove()
Character["Right Arm"]:remove()
Character["Left Leg"]:remove()
Character["Right Leg"]:remove()
local Head = Character.Head
local Torso = Character.Torso
local cam = game.Workspace.CurrentCamera
local RootPart = Character.HumanoidRootPart
local RootJoint = RootPart.RootJoint
local equipped = false
local attack = false
local Anim = 'Idle'
local idle = 0
local attacktype = 1
local Torsovelocity = (RootPart.Velocity * Vector3.new(1, 0, 1)).magnitude 
local velocity = RootPart.Velocity.y
local sine = 0
local change = 1
local mana = 0
local it =Instance.new
vt=Vector3.new
local grabbed = false
local cf = CFrame.new
local mr = math.rad
local angles = CFrame.Angles
local ud = UDim2.new
local c3 = Color3.new
for i,v in pairs(Character:GetChildren()) do
	if v:IsA("Accessory") then
		v:Destroy()
	end
end
local NeckCF = cf(0, 1, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)
Humanoid.Animator:Destroy()
Character.Animate:Destroy()
Head.Transparency = 1
Torso.Transparency = 1
local RootCF = CFrame.fromEulerAnglesXYZ(-1.57, 0, 3.14)
local RHCF = CFrame.fromEulerAnglesXYZ(0, 1.6, 0)
local LHCF = CFrame.fromEulerAnglesXYZ(0, -1.6, 0)

Head.face:remove()
function clerp(a, b, t)
	return a:lerp(b, t)
end


local RbxUtility = LoadLibrary("RbxUtility")
local Create = RbxUtility.Create

function RemoveOutlines(part)
	part.TopSurface, part.BottomSurface, part.LeftSurface, part.RightSurface, part.FrontSurface, part.BackSurface = 10, 10, 10, 10, 10, 10
end
	
function CreatePart(Parent, Material, Reflectance, Transparency, BColor, Name, Size)
	local Part = Create("Part"){
		Parent = Parent,
		Reflectance = Reflectance,
		Transparency = Transparency,
		CanCollide = false,
		Locked = true,
		BrickColor = BrickColor.new(tostring(BColor)),
		Name = Name,
		Size = Size,
		Material = Material,
	}
	RemoveOutlines(Part)
	return Part
end
	
function CreateMesh(Mesh, Part, MeshType, MeshId, OffSet, Scale)
	local Msh = Create(Mesh){
		Parent = Part,
		Offset = OffSet,
		Scale = Scale,
	}
	if Mesh == "SpecialMesh" then
		Msh.MeshType = MeshType
		Msh.MeshId = MeshId
	end
	return Msh
end

--[[Credits to SazErenos for his Artificial Heartbeat]]--

ArtificialHB = Instance.new("BindableEvent", script)
ArtificialHB.Name = "Heartbeat"

script:WaitForChild("Heartbeat")

frame = 1 / 30
tf = 0
allowframeloss = false
tossremainder = false
lastframe = tick()
script.Heartbeat:Fire()

game:GetService("RunService").Heartbeat:connect(function(s, p)
	tf = tf + s
	if tf >= frame then
		if allowframeloss then
			script.Heartbeat:Fire()
			lastframe = tick()
		else
			for i = 1, math.floor(tf / frame) do
				script.Heartbeat:Fire()
			end
			lastframe = tick()
		end
		if tossremainder then
			tf = 0
		else
			tf = tf - frame * math.floor(tf / frame)
		end
	end
end)

function swait(num)
	if num == 0 or num == nil then
		ArtificialHB.Event:wait()
	else
		for i = 0, num do
			ArtificialHB.Event:wait()
		end
	end
end

	
function CreateWeld(Parent, Part0, Part1, C0, C1)
	local Weld = Create("Weld"){
		Parent = Parent,
		Part0 = Part0,
		Part1 = Part1,
		C0 = C0,
		C1 = C1,
	}
	return Weld
end

function rayCast(Position, Direction, Range, Ignore)
	return game:service("Workspace"):FindPartOnRay(Ray.new(Position, Direction.unit * (Range or 999.999)), Ignore) 
end 

function CreateSound(id, par, vol, pit) 
	coroutine.resume(coroutine.create(function()
		local sou = Instance.new("Sound", par or workspace)
		sou.Volume = vol
		sou.Pitch = pit or 1
		sou.SoundId = id
		swait() 
		sou:play() 
		game:GetService("Debris"):AddItem(sou, 6)
	end))
end


Handle=CreatePart(m,Enum.Material.Plastic,0.10000000149012,0,"Really black","Handle",Vector3.new(1, 1, 1))
HandleWeld=CreateWeld(m,Character["Torso"],Handle,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.0199661255, -0.0400784016, 0.15832901, 1, -5.67096185e-006, -2.38577304e-005, 5.6816225e-006, 0.999999344, 0.000446140766, 2.38577395e-005, -0.000446140766, 0.999999344))
Tock=CreatePart(m,Enum.Material.Plastic,0,0,"Medium stone grey","Tock",Vector3.new(1, 1, 1))
TockWeld=CreateWeld(m,Handle,Tock,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-3.81469727e-006, -0.699996948, 7.00950623e-005, 1, 2.04636308e-011, 7.80528353e-008, -7.29414751e-008, 1.35121719e-010, 0.999998868, -2.04636308e-011, -0.999998868, -1.35550668e-010))
CreateMesh("CylinderMesh",Tock,"","",Vector3.new(0, 0, 0),Vector3.new(0.150000006, 0.75, 1))
Tick=CreatePart(m,Enum.Material.Plastic,0,0,"Medium stone grey","Tick",Vector3.new(1, 1, 1))
TickWeld=CreateWeld(m,Tock,Tick,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.300003052, 0.200067759, 0, 7.80528353e-008, 0.999998868, -1.35550668e-010, 2.04636308e-011, 1.35121719e-010, -0.999998868, -1, 7.29414751e-008, 2.04636308e-011))
CreateMesh("SpecialMesh",Tick,Enum.MeshType.FileMesh,"http://www.roblox.com/asset/?id=3270017",Vector3.new(0, 0, 0),Vector3.new(0.400000006, 0.400000006, 1.20000005))
Tick=CreatePart(m,Enum.Material.Plastic,0,0,"Medium stone grey","Tick",Vector3.new(1, 1, 1))
TickWeld=CreateWeld(m,Tock,Tick,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.300003052, -0.199929476, -3.81469727e-006, 7.80528353e-008, 0.999998868, -1.35550668e-010, 2.04636308e-011, 1.35121719e-010, -0.999998868, -1, 7.29414751e-008, 2.04636308e-011))
CreateMesh("SpecialMesh",Tick,Enum.MeshType.FileMesh,"http://www.roblox.com/asset/?id=3270017",Vector3.new(0, 0, 0),Vector3.new(0.400000006, 0.400000006, 1.20000005))
CreateMesh("SpecialMesh",Handle,Enum.MeshType.Sphere,"",Vector3.new(0, 0, 0),Vector3.new(1.5, 1.5, 1.5))
Part=CreatePart(m,Enum.Material.Plastic,0,0,"Institutional white","Part",Vector3.new(0.540000021, 0.200000003, 0.460000038))
PartWeld=CreateWeld(m,Handle,Part,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.0200805664, -0.737700462, 0, -2.19000867e-007, -0.422617674, 0.906307518, -2.3091161e-007, 0.906307518, 0.422617704, -1, -1.16742285e-007, -2.98621671e-007))
CreateMesh("CylinderMesh",Part,"","",Vector3.new(0, 0, 0),Vector3.new(1, 1, 1))
LeftPeg=CreatePart(m,Enum.Material.Plastic,0,0,"Bright yellow","LeftPeg",Vector3.new(1, 0.560000002, 1))
LeftPegWeld=CreateWeld(m,Handle,LeftPeg,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.399997711, 0.779884815, 7.62939453e-006, 1, -4.36907612e-008, -4.11564542e-008, 4.372896e-008, 0.999999404, 1.54743116e-008, 4.62659955e-008, -1.53474389e-008, 0.999999404))
CreateMesh("SpecialMesh",LeftPeg,Enum.MeshType.Sphere,"",Vector3.new(0, 0, 0),Vector3.new(0.800000012, 0.75, 0.949999988))
Part=CreatePart(m,Enum.Material.Plastic,0.10000000149012,0,"Institutional white","Part",Vector3.new(0.200000003, 1.13999999, 0.590000033))
PartWeld=CreateWeld(m,Handle,Part,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.219978333, -0.00736188889, 0.492553711, 1, 5.67091502e-006, -1.42244971e-007, -5.44018985e-006, 0.965925276, 0.258818746, 1.60760464e-006, -0.258818775, 0.965925276))
CreateMesh("SpecialMesh",Part,Enum.MeshType.Sphere,"",Vector3.new(0, 0, 0),Vector3.new(1, 0.649999976, 1))
Part=CreatePart(m,Enum.Material.Plastic,0.10000000149012,0,"Institutional white","Part",Vector3.new(0.200000003, 1.13999999, 0.590000033))
PartWeld=CreateWeld(m,Handle,Part,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(0.189998627, -0.00735902786, 0.49256134, 1, 5.67091502e-006, -1.42244971e-007, -5.44018985e-006, 0.965925276, 0.258818746, 1.60760464e-006, -0.258818775, 0.965925276))
CreateMesh("SpecialMesh",Part,Enum.MeshType.Sphere,"",Vector3.new(0, 0, 0),Vector3.new(1, 0.649999976, 1))
Poot=CreatePart(m,Enum.Material.Plastic,0,0,"Mid gray","Part",Vector3.new(0.200000003, 0.219999999, 0.200000003))
PartWeld=CreateWeld(m,Handle,Poot,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(0.502023697, -1.00622749, 0, -9.02868123e-006, -0.81915164, 0.573576152, 2.20012589e-006, 0.573576152, 0.81915164, -1, 8.65777929e-006, -3.37895472e-006))
CreateMesh("CylinderMesh",Poot,"","",Vector3.new(0, 0, 0),Vector3.new(1, 1, 0.5))
Part=CreatePart(m,Enum.Material.Plastic,0,0,"Mid gray","Part",Vector3.new(0.200000003, 0.219999999, 0.200000003))
PartWeld=CreateWeld(m,Handle,Part,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(-0.0188560486, -0.944825172, 0, -1.92190091e-005, -0.422617674, 0.906307518, 1.27690937e-005, 0.906307518, 0.422617704, -1, 1.96949968e-005, -1.20244413e-005))
CreateMesh("CylinderMesh",Part,"","",Vector3.new(0, 0, 0),Vector3.new(1, 1, 0.5))
RightPeg=CreatePart(m,Enum.Material.Plastic,0,0,"Bright yellow","RightPeg",Vector3.new(1, 0.570000052, 1))
RightPegWeld=CreateWeld(m,Handle,RightPeg,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(0.400005341, 0.784877062, 1.14440918e-005, 1, -4.36907612e-008, -4.11564542e-008, 4.372896e-008, 0.999999404, 1.54743116e-008, 4.62659955e-008, -1.53474389e-008, 0.999999404))
CreateMesh("SpecialMesh",RightPeg,Enum.MeshType.Sphere,"",Vector3.new(0, 0, 0),Vector3.new(0.800000012, 0.75, 0.949999988))
Part=CreatePart(m,Enum.Material.Plastic,0,0,"Mid gray","Part",Vector3.new(0.200000003, 0.219999999, 0.200000003))
PartWeld=CreateWeld(m,Handle,Part,CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),CFrame.new(0.853747368, -0.98065567, 3.81469727e-006, -4.15784598e-008, -0.965925038, 0.258818835, 1.37861207e-008, 0.258818835, 0.965925038, -1, 4.36907612e-008, -2.55568011e-009))
CreateMesh("CylinderMesh",Part,"","",Vector3.new(0, 0, 0),Vector3.new(1, 1, 0.5))

function boom()
	attack = true
	d=Instance.new("Fire",Poot)
	d.Heat=0
	d.Size=2
	CreateSound("http://www.roblox.com/asset/?id=138931042",Torso,1,1)
	for i = 0, 1, 0.05 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Bright red")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.05 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Black")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.1 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Bright red")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.1 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Black")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
		for i = 0, 1, 0.2 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Bright red")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.2 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Black")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
		for i = 0, 1, 0.5 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Bright red")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.5 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Black")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
		for i = 0, 1, 0.5 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Bright red")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	for i = 0, 1, 0.5 do
		swait()
		if Torsovelocity > 2 then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		else
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
				Handle.BrickColor=BrickColor.new("Black")
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
	end
	CreateSound("http://www.roblox.com/asset/?id=282185588",Torso,1,1)
	gg=Instance.new("Explosion")
	gg.Parent=Torso
	gg.Position=Torso.Position
	attack = false
end

--[[Attacks]]--

mouse.Button1Down:connect(function()
	if attack == false and attacktype == 1 then
		boom()
	end
end)


Humanoid.WalkSpeed=10
--[[ Movement Detection ]]--
j=1
while true do
	swait()
	if j == 360 then
	j=1
	else
	j=j+5
	end
	Torsovelocity = (RootPart.Velocity * Vector3.new(1, 0, 1)).magnitude 
	velocity = RootPart.Velocity.y
	sine = sine + change
	local hit, pos = rayCast(RootPart.Position, (CFrame.new(RootPart.Position, RootPart.Position - Vector3.new(0, 1, 0))).lookVector, 4, Character)
	if equipped == true or equipped == false then
		if RootPart.Velocity.y > 1 and hit == nil then 
			Anim = "Jump"
			if attack == false then

				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
			end
		elseif RootPart.Velocity.y < -1 and hit == nil then 
			Anim = "Fall"
			if attack == false then

				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
			end
		elseif Torsovelocity < 1 and hit ~= nil then
			Anim = "Idle"
			if attack == false then
				change = 1
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
			end
		elseif Torsovelocity > 2 and hit ~= nil then
			Anim = "Walk"
			if attack == false then
				RightPegWeld.C0 = clerp(RightPegWeld.C0, CFrame.new(0,0, 0+.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				LeftPegWeld.C0 = clerp(LeftPegWeld.C0, CFrame.new(0,0, 0-.2* math.cos(sine / 3)) * angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				TockWeld.C0 = clerp(TockWeld.C0, CFrame.new(0,0, 0) * angles(math.rad(0), math.rad(0), math.rad(0+j)), .3)
			end
		end
	end
	if #Effects > 0 then
		for e = 1, #Effects do
			if Effects[e] ~= nil then
				local Thing = Effects[e]
				if Thing ~= nil then
					local Part = Thing[1]
					local Mode = Thing[2]
					local Delay = Thing[3]
					local IncX = Thing[4]
					local IncY = Thing[5]
					local IncZ = Thing[6]
					if Thing[1].Transparency <= 1 then
						if Thing[2] == "Block1" then
							Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Block2" then
							Thing[1].CFrame = Thing[1].CFrame
							Mesh = Thing[7]
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Cylinder" then
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Blood" then
							Mesh = Thing[7]
							Thing[1].CFrame = Thing[1].CFrame * Vector3.new(0, .5, 0)
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Elec" then
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[7], Thing[8], Thing[9])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Disappear" then
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Shatter" then
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
							Thing[4] = Thing[4] * CFrame.new(0, Thing[7], 0)
							Thing[1].CFrame = Thing[4] * CFrame.fromEulerAnglesXYZ(Thing[6], 0, 0)
							Thing[6] = Thing[6] + Thing[5]
						end
					else
						Part.Parent = nil
						table.remove(Effects, e)
					end
				end
			end
		end
	end
end
end)

TextButton_7.Parent = scriptframe
TextButton_7.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_7.Position = UDim2.new(0, 0, 0, 347)
TextButton_7.Size = UDim2.new(0, 123, 0, 50)
TextButton_7.Font = Enum.Font.SourceSans
TextButton_7.Text = "Asalt Rifle"
TextButton_7.TextColor3 = Color3.new(0, 1, 1)
TextButton_7.TextScaled = true
TextButton_7.TextSize = 14
TextButton_7.TextWrapped = true

TextButon_7.MouseButton1Down:connect(function()
Ply = game.Players.LocalPlayer
Char = Ply.Character
Tor = Char.Torso
He = Char.Head
Ne = Tor.Neck
Hu = Char.Humanoid
LA = Char["Left Arm"] 
LL = Char["Left Leg"] 
RA = Char["Right Arm"] 
RL = Char["Right Leg"]
LS = Tor["Left Shoulder"] 
RS = Tor["Right Shoulder"] 
LH = Tor["Left Hip"] 
RH = Tor["Right Hip"] 
Combo = 1
NeckCF = CFrame.new(0, 1, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)
RP = Char.HumanoidRootPart
RJ = RP.RootJoint
RootCF = CFrame.fromEulerAnglesXYZ(-1.57, 0, 3.14)
LHCF = CFrame.Angles(0, math.rad(-90), 0)
RHCF = CFrame.Angles(0, math.rad(90), 0)
attack = false
equipped = false
local Anim = "Idle"
Effects = { }
cam = workspace.CurrentCamera
local RbxUtility = LoadLibrary("RbxUtility")
local Create = RbxUtility.Create
local m = Create("Model"){
	Parent = Char,
	Name = "WeaponModel",
}

RS.Parent = nil 
LS.Parent = nil 

RW = Create("Weld"){
	Name = "Right Shoulder",
	Part0 = Tor ,
	C0 = CFrame.new(1.5, 0.5, 0),
	C1 = CFrame.new(0, 0.5, 0), 
	Part1 = RA ,
	Parent = Tor ,
}

LW = Create("Weld"){
	Name = "Left Shoulder",
	Part0 = Tor ,
	C0 = CFrame.new(-1.5, 0.5, 0),
	C1 = CFrame.new(0, 0.5, 0) ,
	Part1 = LA ,
	Parent = Tor ,
}
	
mouse = Ply:GetMouse()

function RemoveOutlines(part)
	part.TopSurface, part.BottomSurface, part.LeftSurface, part.RightSurface, part.FrontSurface, part.BackSurface = 10, 10, 10, 10, 10, 10
end
	
function CreatePart(FF, Par, Mat, Ref, Tra, BC, Nam, Siz)
	local Part = Create("Part"){
		formFactor = FF,
		Parent = Par,
		Reflectance = Ref,
		Transparency = Tra,
		CanCollide = false,
		Locked = true,
		BrickColor = BrickColor.new(tostring(BC)),
		Name = Nam,
		Size = Siz,
		Position = Tor.Position,
		Material = Mat,
	}
	RemoveOutlines(Part)
	return Part
end
	
function CreateMesh(Ms, Par, MType, MId, OS, Sca)
	local Msh = Create(Ms){
		Parent = Par,
		Offset = OS,
		Scale = Sca,
	}
	if Ms == "SpecialMesh" then
		Msh.MeshType = MType
		Msh.MeshId = MId
	end
end
	
function CreateWeld(Par, PartA, PartB, CA, CB)
	local Weld = Create("Weld"){
		Parent = Par,
		Part0 = PartA,
		Part1 = PartB,
		C0 = CA,
		C1 = CB,
	}
	return Weld
end
	
function CreateSound(id, par, vol, pit) 
	coroutine.resume(coroutine.create(function()
		local sou = Create("Sound"){
			Parent = par or workspace,
			Volume = vol,
			Pitch = pit or 1,
			SoundId = id,
		}
		wait() 
		sou:play() 
	end))
end
 
function clerp(a, b, t)
	return a:lerp(b, t)
end

function rayCast(Pos, Dir, Max, Ignore)
	return game:service("Workspace"):FindPartOnRay(Ray.new(Pos, Dir.unit * (Max or 999.999)), Ignore) 
end 

function Damage(hit, damage, cooldown, Color1, Color2, HSound, HPitch)
	for i, v in pairs(hit:GetChildren()) do 
		if v:IsA("Humanoid") and hit.Name ~= Char.Name then
			local find = v:FindFirstChild("Hitz")
			if not find then
				if v.Parent:findFirstChild("Head") then
					local BillG = Create("BillboardGui"){
						Parent = v.Parent.Head,
						Size = UDim2.new(1, 0, 1, 0),
						Adornee = v.Parent.Head,
						StudsOffset = Vector3.new(math.random(-3, 3), math.random(3, 5), math.random(-3, 3)),
					}
					local TL = Create("TextLabel"){
						Parent = BillG,
						Size = UDim2.new(3, 3, 3, 3),
						BackgroundTransparency = 1,
						Text = tostring(damage).."-",
						TextColor3 = Color1.Color,
						TextStrokeColor3 = Color2.Color,
						TextStrokeTransparency = 0,
						TextXAlignment = Enum.TextXAlignment.Center,
						TextYAlignment = Enum.TextYAlignment.Center,
						FontSize = Enum.FontSize.Size18,
						Font = "ArialBold",
					}
					coroutine.resume(coroutine.create(function()
						wait(1)
						for i = 0, 1, .1 do
							wait(.1)
							BillG.StudsOffset = BillG.StudsOffset + Vector3.new(0, .1, 0)
						end
						BillG:Destroy()
					end))
				end
				v.Health = v.Health - damage
				local bool = Create("BoolValue"){
					Parent = v,
					Name = 'Hitz',
				}
				if HSound ~= nil and HPitch ~= nil then
					CreateSound(HSound, hit, 1, HPitch) 
				end
				game:GetService("Debris"):AddItem(bool, cooldown)
			end
		end
	end
end

function MagnitudeDamage(Part, magni, mindam, maxdam, Color1, Color2, HitSound)
	for _, c in pairs(workspace:children()) do
		local hum = c:findFirstChild("Humanoid")
		if hum ~= nil then
			local head = c:findFirstChild("Torso")
			if head ~= nil then
				local targ = head.Position - Part.Position
				local mag = targ.magnitude
				if mag <= magni and c.Name ~= Ply.Name then 
					Damage(head.Parent, math.random(mindam, maxdam), 0, Color1, Color2, HitSound, 1)
				end
			end
		end
	end
end

Handle = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 1, "Navy blue", "Handle", Vector3.new(0.216133296, 0.432266444, 0.200000003))
Handleweld = CreateWeld(m, RA, Handle, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.03214836, -0.278110504, -0.0978469849, 0, 0.999999702, -2.98023224e-008, 0, -2.98023188e-008, -0.999999821, -1, 4.37113847e-008, -1.77635684e-015))
CreateMesh("BlockMesh", Handle, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 0.540333092))
FakeHandle = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 1, "Navy blue", "FakeHandle", Vector3.new(0.216133296, 0.432266444, 0.200000003))
FakeHandleweld = CreateWeld(m, Handle, FakeHandle, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0, 0, 0, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 4.37113812e-008, 4.73655636e-016, 1))
Barrel = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Smoky grey", "Barrel", Vector3.new(0.324199915, 0.200000003, 0.216133296))
Barrelweld = CreateWeld(m, FakeHandle, Barrel, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000385284424, 5.45991993, 0.648399353, 1.88395493e-016, 1.00281931e-024, -1, 0.999999642, 0, 4.37113812e-008, 0, -0.999999642, -4.73655636e-016))
CreateMesh("CylinderMesh", Barrel, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.567349613, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.324199826, 0.324199826, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.378201485, -0.162090302, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.216133282, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-1.03202057, 0.162498474, 0.864542007, 5.96045453e-008, 0.999996662, 2.34803412e-008, 4.76836078e-007, 6.32193187e-009, 0.999997854, 0.999997139, -2.98022425e-008, -4.3312528e-007))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.08066642, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.648406029, -0.594371796, -0.161685944, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.756466568, 0.200000003, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.8910985, -0.70243454, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.200000003, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.45885229, -0.832115173, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.75646615, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.40486634, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.810516357, -0.81047821, 0.162475586, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.216133282, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(2.37740993, -0.594367981, 0.162475586, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.200000003, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.0540370941, -0.162101746, 0, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 4.37113812e-008, 4.73655636e-016, 1))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.369587988, 0.358781129, 0.748901784))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.216133282, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(2.37741232, -0.702438354, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0.5, "Really black", "Part", Vector3.new(0.432266563, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000377655029, -1.56698084, -1.0320282, -4.17232428e-007, 6.32132613e-009, -0.999997616, -0.999997139, 2.98022425e-008, 2.99015426e-007, -8.70414851e-014, 0.999996722, -2.34809274e-008))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.432266563, 2.48553157, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000385284424, 3.51209116, 0.648399353, 1.78814986e-007, -6.32150376e-009, -1, 0.999999642, -5.96046341e-008, 2.22526424e-007, -5.96046341e-008, -0.999999642, 6.32149666e-009))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.216133282, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(2.37741327, -0.486289978, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.200000003, 0.756466269, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-1.45884228, 0.0540428162, 0.000385284424, 0.999999583, -4.47034729e-008, 4.37113776e-008, 4.47034729e-008, 0.999999583, 2.42770696e-015, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.324199975, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000377655029, -1.02661896, -0.162124634, 4.37113812e-008, 4.73655636e-016, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.218294606, 0.239907846, 1.02987504))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(2.485533, 0.216133222, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.02665424, -0.324203491, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(2.16133285, 0.200000003, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.18871307, -0.486282349, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.216133282, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000408172607, 1.19412231, 0.869961739, 4.17229757e-007, 6.32150021e-009, 0.999997854, 8.70414851e-014, -0.999996722, -2.34808173e-008, 0.999997079, 1.49012358e-008, -3.73518958e-007))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.324199975, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000377655029, -1.02661514, -0.378243446, 4.37113812e-008, 4.73655636e-016, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.229101285, 0.250714511, 2.71571469))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.324199975, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000385284424, -1.02661896, 1.56696892, -1.93715053e-007, 9.32587256e-015, -0.999999702, 0, 0.999999642, 4.73655636e-016, 0.999999404, 4.47034836e-008, -6.05967614e-008))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.218294606, 0.239907846, 1.02987504))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.200000003, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.0540370941, -0.162101746, 0, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 4.37113812e-008, 4.73655636e-016, 1))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.369587988, 0.369587809, 0.748901784))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.29679966, 0.200000003, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.864494324, -0.378234863, 0.000385284424, 0.999999583, -4.47034729e-008, 4.37113776e-008, 4.47034729e-008, 0.999999583, 2.42770696e-015, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.200000003, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.270159721, -0.832111359, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.75646615, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(1.08066642, 0.200000003, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.72902441, -0.594367981, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.324199975, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000385284424, -1.02661514, 1.35084629, -1.93715053e-007, 9.32587256e-015, -0.999999702, 0, 0.999999642, 4.73655636e-016, 0.999999404, 4.47034836e-008, -6.05967614e-008))
CreateMesh("SpecialMesh", Part, Enum.MeshType.FileMesh, "http://www.roblox.com/asset/?id=3270017", Vector3.new(0, 0, 0), Vector3.new(0.229101285, 0.250714511, 2.71571469))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.432266563, 0.648399651, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, 0.864570618, -1.03203201, 3.57626845e-007, 6.32133856e-009, 0.999997854, 0.999997139, -2.98022425e-008, -3.1391599e-007, -8.70414851e-014, 0.999996722, 2.34809345e-008))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.216133282, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(2.37740993, -0.594367981, -0.161708832, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.08066642, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.648406029, -0.594371796, 0.162475586, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.324199975, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.0540428162, -0.486282349, 0.162475586, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.864533126, 0.540332973, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.972568512, -0.0540428162, 0.000385284424, 0.999999583, -4.47034729e-008, 4.37113776e-008, 4.47034729e-008, 0.999999583, 2.42770696e-015, 0, -0, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.40486634, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.810501099, -0.810474396, -0.161685944, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0.5, "Really black", "Part", Vector3.new(0.432266563, 0.200000003, 0.216133296))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, 0.162106514, -1.0320282, 3.57626845e-007, 6.32133856e-009, 0.999997854, 0.999997139, -2.98022425e-008, -3.1391599e-007, -8.70414851e-014, 0.999996722, 2.34809345e-008))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.216134712, 0.216134697, 0.216134712))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000408172607, 0.864553452, -1.03203201, 3.57626561e-007, 6.59261232e-008, 1, 0.999999642, 0, -3.1391528e-007, 0, 0.999999642, -6.59261374e-008))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(1.40486634, 0.200000003, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.810516357, -0.70243454, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.324199975, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.0540428162, -0.486282349, -0.161685944, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.324199915, 0.756466269, 0.432266533))
Partweld = CreateWeld(m, FakeHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.000385284424, 5.1330142, 0.648399353, 0, 0, -1, 0.999999642, 0, 4.37113812e-008, 0, -0.999999642, -4.73655636e-016))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.432266563, 0.216133222, 0.864533186))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, -0.324199677, -0.972576141, 2.98023117e-008, 0, 0.999999702, 0, -0.999999642, -4.73655636e-016, 0.999999285, 1.49011701e-008, 1.3909041e-008))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Wedge", Vector3.new(0.200000003, 0.432266444, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.161708832, -0.648399353, -2.86102295e-005, 0, -0, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 1, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.432266563, 0.216133192, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, -0.108055115, -0.432257652, 2.98023117e-008, 0, 0.999999702, 0, -0.999999642, -4.73655636e-016, 0.999999285, 1.49011701e-008, 1.3909041e-008))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Wedge", Vector3.new(0.200000003, 0.200000003, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.162475586, -0.486286163, 0.32416153, 0, -0, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.540332973, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.200000003, 0.200000003, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.161708832, -0.810497284, 1.62095213, 1.49011559e-008, 0, -0.999999762, 0, 0.999999642, 4.73655636e-016, 0.999999404, 4.47034836e-008, 5.86125317e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.540332973, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Wedge", Vector3.new(0.200000003, 0.432266384, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.162475586, -0.648399353, -2.86102295e-005, 0, -0, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 1, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.200000003, 0.200000003, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.162475586, -0.810497284, 1.62095213, 1.49011559e-008, 0, -0.999999762, 0, 0.999999642, 4.73655636e-016, 0.999999404, 4.47034836e-008, 5.86125317e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.540332973, 1))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.432266563, 0.216133237, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, 0.324203491, 2.37740946, 1.06338617e-018, 5.01342412e-010, 0.999999404, 1.49011701e-008, -0.999999285, 5.01343078e-010, 0.999999285, 1.49011701e-008, 4.37113634e-008))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Wedge", Vector3.new(0.432266563, 0.216133222, 0.216133296))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.000385284424, 0.108070374, -0.108057022, 2.98023117e-008, 0, 0.999999702, 0, -0.999999642, -4.73655636e-016, 0.999999285, 1.49011701e-008, 1.3909041e-008))
Wedge = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Wedge", Vector3.new(0.200000003, 0.200000003, 0.216133267))
Wedgeweld = CreateWeld(m, FakeHandle, Wedge, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.161708832, -0.486286163, 0.32416153, 0, -0, 1, 0, 0.999999642, 4.73655636e-016, -0.999999642, 0, -4.37113812e-008))
CreateMesh("SpecialMesh", Wedge, Enum.MeshType.Wedge, "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 0.540332973, 1))
MagHandle = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "MagHandle", Vector3.new(0.432266504, 0.324199826, 0.216133296))
MagHandleweld = CreateWeld(m, FakeHandle, MagHandle, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.648423195, -0.0540428162, 0.000385284424, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 0, -0, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.200000003, 0.324199826, 0.216133296))
Partweld = CreateWeld(m, MagHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(-0.270163536, 0, 0, 0.999999642, 0, 0, 0, 0.999999642, -0, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.200000003, 0.324199826, 0.216133296))
Partweld = CreateWeld(m, MagHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.270174026, 0, 0, 0.999999642, 0, 0, 0, 0.999999642, -0, 0, -0, 1))
CreateMesh("BlockMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(0.540333211, 1, 1))
BoltHandle = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "BoltHandle", Vector3.new(0.216133282, 1.40486586, 0.216133267))
BoltHandleweld = CreateWeld(m, FakeHandle, BoltHandle, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.540328979, -0.486276627, -0.000385284424, -4.47034729e-008, -0.999999583, -2.42770696e-015, -0.999999642, 0, -4.37113812e-008, 0, 0, -0.99999994))
CreateMesh("CylinderMesh", BoltHandle, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.216133282, 0.216133252, 0.216133267))
Partweld = CreateWeld(m, BoltHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0, 0.70238018, 0, 0.999999523, 4.47034729e-008, 0, 4.47034729e-008, 0.999999642, 0, 0, 0, 0.999999881))
CreateMesh("SpecialMesh", Part, Enum.MeshType.Sphere, "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 1))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Really black", "Part", Vector3.new(0.324199915, 0.324199826, 0.200000003))
Partweld = CreateWeld(m, BoltHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.015832901, 0.146270752, 0.648381233, 0.707106292, 5.08757338e-008, 0.707106531, 0.707106411, -8.72889849e-009, -0.707106411, 8.94069458e-008, 0.999999404, -5.09424458e-009))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 1, 0.540333092))
Part = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 0, "Navy blue", "Part", Vector3.new(0.324199915, 0.200000003, 0.200000003))
Partweld = CreateWeld(m, BoltHandle, Part, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(0.0158443451, 0.362377167, 0.648385048, 0.707106292, 5.08757338e-008, 0.707106531, 0.707106411, -8.72889849e-009, -0.707106411, 8.94069458e-008, 0.999999404, -5.09424458e-009))
CreateMesh("CylinderMesh", Part, "", "", Vector3.new(0, 0, 0), Vector3.new(1, 0.540332973, 0.540333092))
ScopeZoom = CreatePart(Enum.FormFactor.Custom, m, Enum.Material.SmoothPlastic, 0, 1, "Bright violet", "ScopeZoom", Vector3.new(0.216133296, 0.200000003, 0.200000003))
ScopeZoomweld = CreateWeld(m, FakeHandle, ScopeZoom, CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1), CFrame.new(1.72752714, -1.03763962, 0, 0.999999642, 0, 4.37113812e-008, 0, 0.999999642, 4.73655636e-016, 4.37113812e-008, 4.73655636e-016, 1))

local PE1 = Create("ParticleEmitter"){
	Parent = Barrel,
	Color = ColorSequence.new(BrickColor.new("Dark stone grey").Color),
	Transparency = NumberSequence.new(0),
	Size = NumberSequence.new(.5),
	Texture = "rbxassetid://257430870",
	Lifetime = NumberRange.new(.1),
	Rate = 100,
	VelocitySpread = 180,
	Rotation = NumberRange.new(0),
	Speed = NumberRange.new(0),
	LightEmission = .6,
	LockedToPart = true,
	Enabled = false
}

local PE2 = PE1:Clone()
PE2.Size = NumberSequence.new(.7)
PE2.LightEmission = 1
PE2.Texture = "rbxassetid://87729590"

function CylinderEffect(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
	local prt = CreatePart(3, workspace, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new(0.2, 0.2, 0.2))
	prt.Anchored = true
	prt.CFrame = cframe
	local msh = CreateMesh("CylinderMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
	game:GetService("Debris"):AddItem(prt, 2)
	Effects[#Effects + 1] = {
		prt,
		"Cylinder",
		delay,
		x3,
		y3,
		z3
	}
end

local Ammo = 10
local Depleted = false

function Shoot(asd, spread1, spread2)
	local MainPos = asd.Position
	local MainPos2 = mouse.Hit.p
	local spread = Vector3.new((math.random(-spread1, 0) + math.random()) * spread2, (math.random(-spread1, 0) + math.random()) * spread2, (math.random(-spread1, 0) + math.random()) * spread2) * (asd.Position - mouse.Hit.p).magnitude / 100
	local MouseLook = CFrame.new((MainPos + MainPos2) / 2, MainPos2 + spread)
	num = 30
	Ammo = Ammo - 1
	print(Ammo)
	if Ammo == 0 then
		Depleted = true
	end
	coroutine.resume(coroutine.create(function(Spreaded) 
		repeat
			wait()
			local hit, pos = rayCast(MainPos, MouseLook.lookVector, 50, RP.Parent)
			local TheHit = mouse.Hit.p
			local mag = (MainPos - pos).magnitude 
			CylinderEffect(BrickColor.new("Dark stone grey"), CFrame.new((MainPos + pos) / 2, pos) * CFrame.Angles(1.57, 0, 0), 3, mag * 5, 3, .5, 1, .5, 0.2)
			MainPos = MainPos + (MouseLook.lookVector * 50)
			num = num - 1
			if hit ~= nil then
				num = 0
				local ref = CreatePart(3, workspace, "Neon", 0, 1, BrickColor.new("Dark stone grey"), "Reference", Vector3.new())
				ref.Anchored = true
				ref.CFrame = CFrame.new(pos)
				MagnitudeDamage(ref, 5, 999999999, 999999999, BrickColor.new("Dark stone grey"), BrickColor.new("Navy blue") , "rbxassetid://199149297")
				game:GetService("Debris"):AddItem(ref, 1) 
			end
		until num <= 0
	end))
end
local Aiming = false
gyro = Instance.new("BodyGyro")
gyro.Parent = nil
gyro.P = 1e7
gyro.D = 1e3
gyro.MaxTorque = Vector3.new(0,1e7,0)


local Crouching = false

function Fire()
	if Aiming == true then
		attack = true
		CreateSound("rbxassetid://132572951", Barrel, 1, .9)
		CreateSound("rbxassetid://130767489", Barrel, .7, 1.2)
		PE1.Enabled = true
		PE2.Enabled = true
		Shoot(Barrel, 0, 0)
		for i = 0, 1, 0.2 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(-10), math.rad(90)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(90), math.rad(-20), math.rad(-90)), .5)
			LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.7, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(140)), .5)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
		PE1.Enabled = false
		PE2.Enabled = false
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .3)
			LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.5, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
		Handleweld.Part0 = LA
		Handleweld.C0 = CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
		Handleweld.C1 = CFrame.new(-0.737663269, -0.281144857, 0.33117196, 0.00916702952, 0.939647615, 0.342020333, 0.999940991, -0.0106014106, 0.00232372736, 0.00580918044, 0.341978878, -0.939689875)
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .3)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
		CreateSound("rbxassetid://146740582", BoltHandle, .7, 1)
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(1, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .5)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
			BoltHandleweld.C0 = clerp(BoltHandleweld.C0, CFrame.new(.5, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
		end
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .5)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
			BoltHandleweld.C0 = clerp(BoltHandleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
		end
		for i = 0, 1, 0.3 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .4)
			RW.C0 = clerp(RW.C0, CFrame.new(.51, 0.51, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .4)
			LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.51, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .4)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
		end
		Handleweld.Part0 = RA
		Handleweld.C0 = CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
		Handleweld.C1 = CFrame.new(1.03214836, -0.278110504, -0.0978469849, 0, 0.999999702, -2.98023224e-008, 0, -2.98023188e-008, -0.999999821, -1, 4.37113847e-008, -1.77635684e-015)
		attack = false
	end
end

local Zoomed = false

function Reload()
	attack = true
	for i = 0, 1, 0.1 do
		wait()
		if Crouching == false and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		elseif Crouching == true and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		end
		Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(0), math.rad(0), math.rad(50)), .3)
		RW.C0 = clerp(RW.C0, CFrame.new(1, 0.5, -.5) * CFrame.Angles(math.rad(120), math.rad(0), math.rad(-50)), .3)
		LW.C0 = clerp(LW.C0, CFrame.new(-1.2, 0.5, -.5) * CFrame.Angles(math.rad(0), math.rad(60), math.rad(120)), .3)
		if Crouching == false and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
		elseif Crouching == true and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
		end
		FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
	end
	CreateSound("rbxassetid://131045401", FakeHandle, 1, 1)
	MagHandleweld.Part0 = LA
	MagHandleweld.C0 = CFrame.new(.5, -1, .6) * CFrame.Angles(1.5, 0, 1.5)
	for i = 0, 1, 0.08 do
		wait()
		if Crouching == false and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		elseif Crouching == true and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		end
		Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(5), math.rad(50)), .3)
		RW.C0 = clerp(RW.C0, CFrame.new(1, 0.5, -.5) * CFrame.Angles(math.rad(120), math.rad(0), math.rad(-50)), .3)
		LW.C0 = clerp(LW.C0, CFrame.new(-1.2, 0.5, -.3) * CFrame.Angles(math.rad(0), math.rad(90), math.rad(20)), .3)
		if Crouching == false and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
		elseif Crouching == true and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
		end
		FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
	end
	CreateSound("rbxassetid://131045429", FakeHandle, 1, 1)
	for i = 0, 1, 0.08 do
		wait()
		if Crouching == false and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		elseif Crouching == true and Aiming == true then 
			RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
		end
		Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(0), math.rad(0), math.rad(50)), .3)
		RW.C0 = clerp(RW.C0, CFrame.new(1, 0.5, -.5) * CFrame.Angles(math.rad(100), math.rad(0), math.rad(-50)), .5)
		LW.C0 = clerp(LW.C0, CFrame.new(-1.2, 0.5, -.3) * CFrame.Angles(math.rad(0), math.rad(60), math.rad(100)), .5)
		if Crouching == false and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
		elseif Crouching == true and Aiming == true then
			RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
		end
		FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
	end
	MagHandleweld.Part0 = FakeHandle
	MagHandleweld.C0 = CFrame.new(0, 0, 0) * CFrame.Angles(0, 0, 0)
	Ammo = 10
	print(Ammo)
	if Depleted == true then
		Depleted = false
		Handleweld.Part0 = LA
		Handleweld.C0 = CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
		Handleweld.C1 = CFrame.new(-0.737663269, -0.281144857, 0.33117196, 0.00916702952, 0.939647615, 0.342020333, 0.999940991, -0.0106014106, 0.00232372736, 0.00580918044, 0.341978878, -0.939689875)
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .3)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
		end
		CreateSound("rbxassetid://146740582", BoltHandle, .7, 1)
		for i = 0, 1, 0.1 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(1, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .5)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
			BoltHandleweld.C0 = clerp(BoltHandleweld.C0, CFrame.new(.5, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
		end
		for i = 0, 1, 0.3 do
			wait()
			if Crouching == false and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			elseif Crouching == true and Aiming == true then 
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
			end
			Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(80)), .3)
			RW.C0 = clerp(RW.C0, CFrame.new(.5, 0.5, -.6) * CFrame.Angles(math.rad(80), math.rad(-30), math.rad(-90)), .5)
			LW.C0 = clerp(LW.C0, CFrame.new(-1, 0.3, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(70)), .3)
			if Crouching == false and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
			elseif Crouching == true and Aiming == true then
				RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
			end
			FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
			BoltHandleweld.C0 = clerp(BoltHandleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
		end
	end
	Handleweld.Part0 = RA
	Handleweld.C0 = CFrame.new(0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
	Handleweld.C1 = CFrame.new(1.03214836, -0.278110504, -0.0978469849, 0, 0.999999702, -2.98023224e-008, 0, -2.98023188e-008, -0.999999821, -1, 4.37113847e-008, -1.77635684e-015)
	attack = false
end

mouse.Button1Down:connect(function()
	if attack == false and Depleted == false then
		Fire()
	end
end)

mouse.KeyDown:connect(function(k)
	k = k:lower()
	if k == "r" and attack == false then
		Reload()
	elseif k == "f" and Aiming == false then
		Aiming = true
	elseif k == "f" and Aiming == true then
		Aiming = false
	elseif k == "c" and Aiming == true and Crouching == false then
		Crouching = true
	elseif k == "c" and Aiming == true and Crouching == true then
		Crouching = false
	elseif k == "z" and Aiming == true and Zoomed == false then
		Zoomed = true
		CreateSound("rbxassetid://180144779", FakeHandle, 1, 1)
		for i = 0, 1, 0.2 do 
			wait()
			cam.FieldOfView = cam.FieldOfView - 5
		end
		Ply.CameraMode = "LockFirstPerson"
        --Ply.DevEnableMouseLock = false
		cam.FieldOfView = 10
		cam.CameraSubject = ScopeZoom
		mouse.Icon = "rbxassetid://18006519"
	elseif k == "z" and Aiming == true and Zoomed == true then
		Zoomed = false
		CreateSound("rbxassetid://190623951", FakeHandle, 1, 1)
		for i = 0, 1, 0.2 do 
			wait()
			cam.FieldOfView = cam.FieldOfView + 5
		end
		Ply.CameraMode = "Classic"
        --Ply.DevEnableMouseLock = true
		cam.FieldOfView = 80
		cam.CameraSubject = Hu
		mouse.Icon = ""
	end
end)


local sine = 0
local change = 1
local val = 0

while true do
	wait()
	sine = sine + change
	local torvel = (RP.Velocity * Vector3.new(1, 0, 1)).magnitude 
	local velderp = RP.Velocity.y
	hitfloor, posfloor = rayCast(RP.Position, (CFrame.new(RP.Position, RP.Position - Vector3.new(0, 1, 0))).lookVector, 4, Char)
	if equipped == true or equipped == false then
		if Aiming == true then
			if Crouching == false and Aiming == true then
				Hu.WalkSpeed = 10
			elseif Crouching == true and Aiming == true then
				Hu.WalkSpeed = 5
			end
			gyro.Parent = RP
			local gunpos = Vector3.new(mouse.Hit.p.x, He.Position.Y, mouse.Hit.p.z)
			offset = (Tor.Position.y - mouse.Hit.p.y) / 60
			local mag = (Tor.Position - mouse.Hit.p).magnitude / 80
			offset = offset / mag 
			gyro.CFrame = CFrame.new(Vector3.new(),(mouse.Hit.p -RP.CFrame.p).unit * 100)
		elseif Aiming == false then
			Hu.JumpPower = 50
			Hu.WalkSpeed = 16
			gyro.Parent = nil
		end
		if RP.Velocity.y > 1 and hitfloor == nil then 
			Anim = "Jump"
			if attack == false and Aiming == false then
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(-20), math.rad(0), math.rad(0)), .3)
				RW.C0 = clerp(RW.C0, CFrame.new(1.2, 0.4, -.2) * CFrame.Angles(math.rad(60), math.rad(0), math.rad(-40)), .3)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.5, -.4) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(60)), .3)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-4), math.rad(0), math.rad(-30)), .3)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-4), math.rad(0), math.rad(30)), .3)
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(0)), .3)
			elseif attack == false and Aiming == true then
				if Crouching == false and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				elseif Crouching == true and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				end
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .4)
				RW.C0 = clerp(RW.C0, CFrame.new(.51, 0.51, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .4)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.51, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .4)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				if Crouching == false and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				elseif Crouching == true and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
				end
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
			end
		elseif RP.Velocity.y < -1 and hitfloor == nil then 
			Anim = "Fall"
			if attack == false and Aiming == false then
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .3)
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(20), math.rad(0), math.rad(0)), .3)
				RW.C0 = clerp(RW.C0, CFrame.new(1.2, 0.4, -.2) * CFrame.Angles(math.rad(100), math.rad(0), math.rad(-40)), .3)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.5, -.4) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(100)), .3)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-4), math.rad(0), math.rad(30)), .3)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-4), math.rad(0), math.rad(-30)), .3)
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(0)), .3)
			elseif attack == false and Aiming == true then
				if Crouching == false and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				elseif Crouching == true and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				end
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .4)
				RW.C0 = clerp(RW.C0, CFrame.new(.51, 0.51, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .4)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.51, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .4)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				if Crouching == false and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				elseif Crouching == true and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
				end
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
			end
		elseif torvel < 1 and hitfloor ~= nil then
			Anim = "Idle"
			if attack == false and Aiming == false then
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(50)), .3)
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(-50)), .3)
				RW.C0 = clerp(RW.C0, CFrame.new(1.2, 0.4, 0) * CFrame.Angles(math.rad(70), math.rad(0), math.rad(-40)), .3)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.5, -.4) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(70)), .3)
				RH.C0 = clerp(RH.C0, CFrame.new(.9, -.5, .2) * RHCF * CFrame.Angles(math.rad(-5), math.rad(-50), math.rad(0)), .3)
				LH.C0 = clerp(LH.C0, CFrame.new(-.5, -1, -1) * LHCF * CFrame.Angles(math.rad(-5), math.rad(-50), math.rad(50)), .3)
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(70), math.rad(0)), .3)
			elseif attack == false and Aiming == true then
				if Crouching == false and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				elseif Crouching == true and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				end
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .4)
				RW.C0 = clerp(RW.C0, CFrame.new(.51, 0.51, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .4)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.51, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .4)
				if Crouching == false and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				elseif Crouching == true and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -.5, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
				end
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
			end
		elseif torvel > 2 and hitfloor ~= nil then
			Anim = "Walk"
			if attack == false and Aiming == false then
				RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(30), math.rad(0), math.rad(0)), .3)
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(-20), math.rad(0), math.rad(0)), .3)
				RW.C0 = clerp(RW.C0, CFrame.new(1.2, 0.4, -.2) * CFrame.Angles(math.rad(50), math.rad(0), math.rad(-40)), .3)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.5, -.4) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(50)), .3)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-3), math.rad(0), math.rad(0)), .3)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-3), math.rad(0), math.rad(0)), .3)
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(80), math.rad(0)), .3)
			elseif attack == false and Aiming == true then
				if Crouching == false and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				elseif Crouching == true and Aiming == true then 
					RJ.C0 = clerp(RJ.C0, RootCF * CFrame.new(0, 0, -.5) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(-90)), .4)
				end
				Ne.C0 = clerp(Ne.C0, NeckCF * CFrame.Angles(math.rad(5), math.rad(0), math.rad(90)), .4)
				RW.C0 = clerp(RW.C0, CFrame.new(.51, 0.51, -.6) * CFrame.Angles(math.rad(90), math.rad(0), math.rad(-90)), .4)
				LW.C0 = clerp(LW.C0, CFrame.new(-1.3, 0.51, 0) * CFrame.Angles(math.rad(0), math.rad(160), math.rad(90)), .4)
				RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				if Crouching == false and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -1, 0) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -1, 0) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
				elseif Crouching == true and Aiming == true then
					RH.C0 = clerp(RH.C0, CFrame.new(1, -.1, -.5) * RHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(0)), .4)
					LH.C0 = clerp(LH.C0, CFrame.new(-1, -.1, -.2) * LHCF * CFrame.Angles(math.rad(-5), math.rad(0), math.rad(50)), .4)
				end
				FakeHandleweld.C0 = clerp(Handleweld.C0, CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0)), .4)
			end
		end
		
	end
	if #Effects > 0 then
		for e = 1, #Effects do
			if Effects[e] ~= nil then
				local Thing = Effects[e]
				if Thing ~= nil then
					local Part = Thing[1]
					local Mode = Thing[2]
					local Delay = Thing[3]
					local IncX = Thing[4]
					local IncY = Thing[5]
					local IncZ = Thing[6]
					if Thing[1].Transparency <= 1 then
						if Thing[2] == "Block1" then
							Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Cylinder" then
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Blood" then
							Mesh = Thing[7]
							Thing[1].CFrame = Thing[1].CFrame * Vector3.new(0, .5, 0)
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Elec" then
							Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[7], Thing[8], Thing[9])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Disappear" then
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						end
					else
						Part.Parent = nil
						table.remove(Effects, e)
					end
				end
			end
		end
	end
end
end)

TextButton_8.Parent = scriptframe
TextButton_8.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
TextButton_8.Position = UDim2.new(0, 156, 0, 349)
TextButton_8.Size = UDim2.new(0, 123, 0, 50)
TextButton_8.Font = Enum.Font.SourceSans
TextButton_8.Text = "Pound"
TextButton_8.TextColor3 = Color3.new(0, 1, 1)
TextButton_8.TextScaled = true
TextButton_8.TextSize = 14
TextButton_8.TextWrapped = true

TextButton_8.MouseButton1Down:connect(function()
local plr = game.Players.LocalPlayer
local chr = plr.Character
local maus = plr:GetMouse()
local PGui=plr.PlayerGui
local lleg = chr["Left Leg"]
local rleg = chr["Right Leg"]
local larm = chr["Left Arm"]
local rarm = chr["Right Arm"]
local hed = chr.Head
local rutprt = chr.HumanoidRootPart
local torso = chr.Torso
local otheranims=false
local armmovement=false
local hitdb=false
local toss=false
local jamp=false
chr.Animate.Disabled=true
chr.Humanoid.WalkSpeed=10
local running=false
local tempignore={}

local weit=Instance.new('Part',hed)
weit.Shape='Ball'
weit.BrickColor=BrickColor.new('Black')
weit.Material='Neon'
weit.Size=Vector3.new(3,3,3)
weit.CanCollide=true
weit.Name='Weight'
weit.Friction=1
weit.Elasticity=0



local at1=Instance.new("Attachment",torso)
local at2=Instance.new("Attachment",weit)
local const=Instance.new("RopeConstraint",chr)
const.Attachment0=at2
const.Attachment1=at1
const.Visible=true
const.Restitution=0
const.Length=100

local pseudohead=hed:Clone()
for i,x in pairs(pseudohead:GetChildren()) do if not x.ClassName:find('Mesh') then x:Destroy() end end
pseudohead.Name='PseudoHead'
pseudohead.Parent=chr.Head
local pseudoweld=Instance.new('Weld',torso)
pseudoweld.Part0=hed
pseudoweld.Name='PseudoHedWld'
pseudoweld.Part1=pseudohead
hed.Transparency=1

--[[coroutine.resume(coroutine.create(function()
local rate=.05
local Hats={}
for i,x in pairs(chr:GetChildren()) do if x:IsA("Hat") then table.insert(Hats,x) x.Handle.Mesh.TextureId="http://www.roblox.com/asset?id=25701026"
end
end
local lam=Instance.new("SpecialMesh",larm)
lam.MeshId="http://www.roblox.com/asset?id=12221505"
lam.TextureId="http://www.roblox.com/asset?id=25701026"
local ram=Instance.new("SpecialMesh",rarm)
ram.MeshId="http://www.roblox.com/asset?id=12221505"
ram.TextureId="http://www.roblox.com/asset?id=25701026"
local rlm=Instance.new("SpecialMesh",rleg)
rlm.MeshId="http://www.roblox.com/asset?id=12221626"
rlm.TextureId="http://www.roblox.com/asset?id=25701026"
local llm=Instance.new("SpecialMesh",lleg)
llm.MeshId="http://www.roblox.com/asset?id=12221626"
llm.TextureId="http://www.roblox.com/asset?id=25701026"
local trm=Instance.new("SpecialMesh",torso)
trm.MeshId="http://www.roblox.com/asset?id=12221758"
trm.TextureId="http://www.roblox.com/asset?id=25701026"
local hem=Instance.new("SpecialMesh",hed)
hem.MeshId="rbxasset://fonts/head.mesh"
hem.TextureId="http://www.roblox.com/asset?id=25701026"
local hem2=Instance.new("SpecialMesh",pseudohead)
hem2.MeshId="rbxasset://fonts/head.mesh"
hem2.TextureId="http://www.roblox.com/asset?id=25701026"
local weitmesh=Instance.new("SpecialMesh",weit)
weitmesh.MeshId="http://www.roblox.com/asset/?id=1527559"
weitmesh.TextureId="http://www.roblox.com/asset?id=25701026"
local asd=Instance.new('PointLight',torso)
asd.Brightness=123
asd.Range=12
asd.Shadows=true

while wait'0' do
for a=0,1,rate do
lam.VertexColor=Vector3.new(a,0,-a+1)
ram.VertexColor=Vector3.new(a,0,-a+1)
rlm.VertexColor=Vector3.new(a,0,-a+1)
llm.VertexColor=Vector3.new(a,0,-a+1)
trm.VertexColor=Vector3.new(a,0,-a+1)
hem.VertexColor=Vector3.new(a,0,-a+1)
hem2.VertexColor=Vector3.new(a,0,-a+1)
weitmesh.VertexColor=Vector3.new(a,0,-a+1)
asd.Color=Color3.new(a,0,-a+1)
coroutine.wrap(function()
for x=1,#Hats do
Hats[x].Handle.Mesh.VertexColor=Vector3.new(a,0,-a+1)
end
end)()
wait''
end
for a=0,1,rate do
lam.VertexColor=Vector3.new(-a+1,a,0)
ram.VertexColor=Vector3.new(-a+1,a,0)
rlm.VertexColor=Vector3.new(-a+1,a,0)
llm.VertexColor=Vector3.new(-a+1,a,0)
trm.VertexColor=Vector3.new(-a+1,a,0)
hem.VertexColor=Vector3.new(-a+1,a,0)
hem2.VertexColor=Vector3.new(-a+1,a,0)
weitmesh.VertexColor=Vector3.new(-a+1,a,0)
asd.Color=Color3.new(-a+1,a,0)
coroutine.wrap(function()
for x=1,#Hats do
Hats[x].Handle.Mesh.VertexColor=Vector3.new(-a+1,a,0)
end
end)()
wait''
end
for a=0,1,rate do
lam.VertexColor=Vector3.new(0,-a+1,a)
ram.VertexColor=Vector3.new(0,-a+1,a)
rlm.VertexColor=Vector3.new(0,-a+1,a)
llm.VertexColor=Vector3.new(0,-a+1,a)
trm.VertexColor=Vector3.new(0,-a+1,a)
hem.VertexColor=Vector3.new(0,-a+1,a)
hem2.VertexColor=Vector3.new(0,-a+1,a)
weitmesh.VertexColor=Vector3.new(0,-a+1,a)
asd.Color=Color3.new(0,-a+1,a)
coroutine.wrap(function()
for x=1,#Hats do
Hats[x].Handle.Mesh.VertexColor=Vector3.new(0,-a+1,a)
end
end)()
wait''
end
end
end))]]


function Lerp(a, b, i)
local com1 = {a.X, a.Y, a.Z, a:toEulerAnglesXYZ()}
local com2 = {b.X, b.Y, b.Z, b:toEulerAnglesXYZ()}
local calx = com1[1] + (com2[1] - com1[1]) * i
local caly = com1[2] + (com2[2] - com1[2]) * i
local calz = com1[3] + (com2[3] - com1[3]) * i
local cala = com1[4] + (com2[4] - com1[4]) * i
local calb = com1[5] + (com2[5] - com1[5]) * i
local calc = com1[6] + (com2[6] - com1[6]) * i
return CFrame.new(calx, caly, calz) * CFrame.Angles(cala, calb, calc)
end

function TwnSingleNumber(s,f,m)
local wot=s+(f-s)*m
return wot
end

function TwnVector3(q,w,e)
local begin={q.x,q.y,q.z}
local ending={w.x,w.y,w.z}
local bgx=begin[1]+(ending[1]-begin[1])*e
local bgy=begin[2]+(ending[2]-begin[2])*e
local bgz=begin[3]+(ending[3]-begin[3])*e
return Vector3.new(bgx,bgy,bgz)
end

newWeld = function(wld, wp0, wp1, wc0x, wc0y, wc0z)
wld = Instance.new("Weld", wp1)
wld.Part0 = wp0
wld.Part1 = wp1
wld.C0 = CFrame.new(wc0x, wc0y, wc0z)
end

newWeld(law, torso, larm, -1.5, 0.5, 0)
newWeld(raw, torso, rarm, 1.5, 0.5, 0)
newWeld(llw, torso, lleg, -.5, -2, 0)
newWeld(rlw, torso, rleg, .5, -2, 0)
newWeld(hw, torso, hed, 0, 1.5, 0)
larm.Weld.C1 = CFrame.new(0, 0.5, 0)
rarm.Weld.C1 = CFrame.new(0, 0.5, 0)
rleg.Weld.C1=CFrame.new(0,.25,.05)*CFrame.Angles(math.rad(30),0,0)
lleg.Weld.C1=CFrame.new(0,.25,.05)*CFrame.Angles(math.rad(30),0,0)

local anim = "Idling"
local lastanim = "Idling"
local val = 0
local syne = 0
local num = 0
local runtime = 0


maus.KeyUp:connect(function(kei)
if string.byte(kei)==48 and not otheranims then
running=false
chr.Humanoid.WalkSpeed=10
end
end)

maus.KeyDown:connect(function(kei)
if string.byte(kei)==48 and not otheranims then
running=true
chr.Humanoid.WalkSpeed=18
end

chr.Humanoid.Changed:connect(function(ch)
if ch=='Jump' and not chr.Humanoid.Sit and not chr.Humanoid.PlatformStand then
local rei=Ray.new(torso.CFrame.p,((torso.CFrame*CFrame.new(0,-1,0)).p-torso.CFrame.p).unit*10)
local t,p=Workspace:FindPartOnRay(rei,chr)
if t then
chr.Humanoid.Jump=false
end
end
end)

if kei==' ' and not chr.Humanoid.Jump and not chr.Humanoid.Sit and not chr.Humanoid.PlatformStand and not jamp then
local rei=Ray.new(torso.CFrame.p,((rutprt.CFrame*CFrame.new(0,-1,0)).p-rutprt.CFrame.p).unit*3)
local t,p=Workspace:FindPartOnRay(rei,chr)
if t then
chr.Humanoid.PlatformStand=true
jamp=true
coroutine.wrap(function()
repeat wait()
chr.Torso.Velocity=Vector3.new(0,35,0)
until not chr.Humanoid.PlatformStand
end)()
wait(.1)
chr.Humanoid.PlatformStand=false
jamp=false
end
end
end)



local grunt=Instance.new('Sound',hed)
grunt.Name='Grunt'
grunt.Volume=1
grunt.Pitch=.9
grunt.Looped=false
grunt.SoundId="http://www.roblox.com/asset?id=143384769" 



local hut=Instance.new('Sound',weit)
hut.Name='Hit'
hut.Volume=1
hut.Looped=false
hut.Pitch=1
hut.SoundId="http://www.roblox.com/asset?id=146163534" 
local wtl=Instance.new('PointLight',weit)
wtl.Shadows=true
wtl.Brightness=123
wtl.Range=12
wtl.Color=weit.BrickColor.Color
wtl.Name='WeightLight'
local wgui=Instance.new('SurfaceGui',weit)
wgui.Face='Front'
wgui.Adornee=weit
wgui.CanvasSize=Vector2.new(100,100)
wgui.Name='WeightGui'
local tb=Instance.new('TextLabel',wgui)
tb.Size=UDim2.new(1,0,1,0)
tb.Text=[[LAWL'D]]
tb.TextColor3=Color3.new(1,1,1)
tb.BackgroundTransparency=1
local wtw=Instance.new('Weld',torso)
wtw.Name='WeightWeld'
wtw.Part0=torso
wtw.Part1=weit
wtw.C0=CFrame.new(0,.5,-1.8)*CFrame.Angles(math.rad(-20),0,0)
weit.Touched:connect(function(hit)
if hit and hit.CanCollide and hit.Parent and hit.Parent~=chr and hit.Parent.Parent~=chr and otheranims then
hum=hit.Parent:findFirstChild('Humanoid') and hit.Parent:findFirstChild('Torso') and hit.Parent.ClassName=='Model'
if hum and not hitdb then
local ex=Instance.new('Explosion',workspace)
ex.DestroyJointRadiusPercent=0
ex.BlastPressure=222222
ex.BlastRadius=18
hitdb=true
ex.Position=hit.Parent.Torso.Position
hit.Parent.Humanoid.Health=hit.Parent.Humanoid.Health-(101*(hit.Parent.Humanoid.MaxHealth/100))
table.insert(tempignore,hit.Parent)
hut:Play()
toss=false
hit.Parent.Humanoid.PlatformStand=true
coroutine.wrap(function()
repeat wait()
hit.Parent.Torso.Velocity=((hit.Parent.Torso.CFrame.p*Vector3.new(1,0,1))-(weit.CFrame.p*Vector3.new(1,0,1))).unit*100
weit.Velocity=((hit.Parent.Torso.CFrame.p*Vector3.new(1,0,1))-(weit.CFrame.p*Vector3.new(1,0,1))).unit*-10+Vector3.new(0,20,0)
until not hit.Parent.Humanoid.PlatformStand
end)()
wait(.2)
hit.Parent.Humanoid.PlatformStand=false
end
end
end)
maus.Button1Down:connect(function()
if not otheranims then
chr.Humanoid.WalkSpeed=0
otheranims=true
anim='PreThrow'
hitdb=false
coroutine.resume(coroutine.create(function()
for fgh,hgf in pairs(tempignore) do
table.remove(tempignore,hgf)
end
end))
wait(.3)
grunt:Play()
wait(.2)
anim='Throw'
const.Parent=nil
wtw.Parent=nil
wtw.Part0=nil
toss=true
weit.CFrame=rutprt.CFrame*CFrame.new(0,3,-3)
wait()
weit.Velocity=((rutprt.CFrame.p*Vector3.new(1,0,1))-(weit.CFrame.p*Vector3.new(1,0,1))).unit*-200+Vector3.new(0,12,0)
wait(.25)
const.Parent=chr
anim='Rest'
wait(1)
wtw.Parent=torso
wtw.Part0=torso
otheranims=false
chr.Humanoid.WalkSpeed=10
toss=false
end
end)

-----------------------------------------------------------------------------

game:service'RunService'.RenderStepped:connect(function()
chr.Humanoid.CameraOffset=(rutprt.CFrame:toObjectSpace(hed.CFrame)).p+Vector3.new(0,-1.25,0)
syne=syne+.95
if running and not otheranims then chr.Humanoid.WalkSpeed=18
elseif not running and not otheranims then chr.Humanoid.WalkSpeed=10
end
if not otheranims then
if (torso.Velocity*Vector3.new(1, 0, 1)).magnitude < 1 and torso.Velocity.y<1 and torso.Velocity.y>-1 then
anim="Idling"

elseif (rutprt.Velocity*Vector3.new(1, 0, 1)).magnitude > 1 and (rutprt.Velocity*Vector3.new(1, 0, 1)).magnitude < 12 and torso.Velocity.y<1 and torso.Velocity.y>-1 then
anim="Walking"

elseif (torso.Velocity*Vector3.new(1, 0, 1)).magnitude > 12 and torso.Velocity.y<1 and torso.Velocity.y>-1 then
anim="Sprinting"

elseif torso.Velocity.y>1 then
anim='Jumping'

elseif (torso.Velocity.y < -1) then
anim='Falling'
end
end

if anim=="Idling" then if not armmovement then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(-12.5)),.05)
end
wtw.C0=Lerp(wtw.C0,CFrame.new(0,.375,-1.7)*CFrame.Angles(math.rad(-20),0,0),.25)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(12.5)),.05)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,-1.3,.35)*CFrame.Angles(math.rad(-7),0,math.rad(-2.5)),.05)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,-1.3,.35)*CFrame.Angles(math.rad(-7),0,math.rad(2.5)),.05)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(30),0,math.cos(syne/30)/25),.05)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/40)/15-.5,0)*CFrame.Angles(math.rad(125),math.rad(180),0),.05)
end
if anim=="Walking" then if not armmovement then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(-12.5)),.05)
end
wtw.C0=Lerp(wtw.C0,CFrame.new(0,.375,-1.8)*CFrame.Angles(math.rad(-20),0,0),.25)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(12.5)),.05)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,(math.cos(syne/10))-1.3,(math.cos(syne/10))+.475)*CFrame.Angles((math.cos(syne/10))*-1,0,math.rad(-2.5)),.05)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,(math.cos(syne/10))*-1-1.3,(math.cos(syne/10))*-1+.475)*CFrame.Angles((math.cos(syne/10)),0,math.rad(2.5)),.05)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(30),math.cos(syne/10)/10*-1,math.cos(syne/10)/20),.05)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/6)/4-.5,0)*CFrame.Angles(math.rad(125),math.cos(syne/10)/10+math.rad(180),0),.05)
end

if anim=="Sprinting" then if not armmovement then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(-12.5)),.05)
end
wtw.C0=Lerp(wtw.C0,CFrame.new(0,.375,-1.8)*CFrame.Angles(math.rad(-20),0,0),.25)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(67),0,math.rad(12.5)),.05)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,(math.cos(syne/7))-1.3,(math.cos(syne/7))+.475)*CFrame.Angles((math.cos(syne/7))*-1,0,math.rad(-2.5)),.05)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,(math.cos(syne/7))*-1-1.3,(math.cos(syne/7))*-1+.475)*CFrame.Angles((math.cos(syne/7)),0,math.rad(2.5)),.05)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(30),math.cos(syne/7)/7*-1,math.cos(syne/7)/20),.05)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/6)/4-.5,0)*CFrame.Angles(math.rad(125),math.cos(syne/7)/7+math.rad(180),0),.05)
end

if anim=="Jumping" then if not armmovement then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.5,.525,0)*CFrame.Angles(math.rad(30),0,math.rad(30)),.15)
end
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.5,.525,0)*CFrame.Angles(math.rad(30),0,math.rad(-30)),.15)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.55,-1.85,1)*CFrame.Angles(0,0,math.rad(-2.5)),.05)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.55,-1.85,1)*CFrame.Angles(0,0,math.rad(2.5)),.05)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(0),0,0),.05)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/50)/20,.5)*CFrame.Angles(math.rad(75),math.rad(180),math.rad(0)),.05)
end

if anim=="Falling" then if not armmovement then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.425,.525,0)*CFrame.Angles(math.cos(syne/10)/5+math.rad(120),0,math.rad(22.5)),.15)
end
wtw.C0=Lerp(wtw.C0,CFrame.new(0,1.25,-2.25)*CFrame.Angles(math.cos(syne/20)/20,math.cos(syne/10)/30,0),.25)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.425,.525,0)*CFrame.Angles((math.cos(syne/10)/5)*-1+math.rad(120),0,math.rad(-22.5)),.15)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.725,-1.5,-.3)*CFrame.Angles(math.cos(syne/10)/5+math.rad(33),0,math.rad(-15)),.05)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.725,-1.5,-.3)*CFrame.Angles(math.cos(syne/10)/5*-1+math.rad(33),0,math.rad(15)),.05)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(30),0,0),.05)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,0,1)*CFrame.Angles(math.rad(125),math.rad(180),math.rad(0)),.05)
end

if anim=="PreThrow" then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.5,-.225)*CFrame.Angles(math.rad(105),0,math.rad(-12.5)),.1)
wtw.C0=Lerp(wtw.C0,CFrame.new(0,1,-2)*CFrame.Angles(math.rad(-10),0,0),.1)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(105),0,math.rad(12.5)),.1)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,-1.3,.3)*CFrame.Angles(math.rad(-10),0,math.rad(-2.5)),.1)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,-1.3,.3)*CFrame.Angles(math.rad(-10),0,math.rad(2.5)),.1)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(40),0,0),.1)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/40)/15-.5,0)*CFrame.Angles(math.rad(132.5),math.rad(180),0),.1)
end

if anim=="Throw" then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.6,-.225)*CFrame.Angles(math.rad(105),0,math.rad(-12.5)),.1)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(105),0,math.rad(12.5)),.1)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,-1.3,0)*CFrame.Angles(math.rad(40),0,math.rad(-2.5)),.1)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,-1.3,0)*CFrame.Angles(math.rad(40),0,math.rad(2.5)),.1)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(-5),0,0),.1)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/40)/15-.5,0)*CFrame.Angles(math.rad(75),math.rad(180),0),.1)
end

if anim=="Rest" then
rarm.Weld.C0=Lerp(rarm.Weld.C0,CFrame.new(1.35,.55,-.225)*CFrame.Angles(math.rad(35),0,math.rad(-12.5)),.1)
larm.Weld.C0=Lerp(larm.Weld.C0,CFrame.new(-1.35,.425,-.225)*CFrame.Angles(math.rad(35),0,math.rad(12.5)),.1)
lleg.Weld.C0=Lerp(lleg.Weld.C0,CFrame.new(-.525,-.85,-.25)*CFrame.Angles(math.rad(40),0,math.rad(-2.5)),.1)
rleg.Weld.C0=Lerp(rleg.Weld.C0,CFrame.new(.525,-.85,-.25)*CFrame.Angles(math.rad(40),0,math.rad(2.5)),.1)
hed.Weld.C0=Lerp(hed.Weld.C0,CFrame.new(0,1.5,0)*CFrame.Angles(math.rad(-5),0,0),.1)
rutprt.RootJoint.C0=Lerp(rutprt.RootJoint.C0,CFrame.new(0,math.cos(syne/40)/15-1,0)*CFrame.Angles(math.rad(75),math.rad(180),0),.1)
end

end)
end)
