local MessageSender = require(game.Players.LocalPlayer.PlayerScripts:WaitForChild("ChatScript"):WaitForChild("ChatMain"):WaitForChild("MessageSender"))
MessageSender:RegisterSayMessageFunction(game:GetService("ReplicatedStorage"):WaitForChild("DefaultChatSystemChatEvents"):WaitForChild("SayMessageRequest"))

MessageSender:SendMessage("", "All")
local LoadingTime = tick();
local Commands, Prefix = {}, "?"
getgenv().Notify = function(title, text, icon, time)
	game:GetService("StarterGui"):SetCore("SendNotification",{
		Title = title;
		Text = text;
		Icon = "";
		Duration = time;
	}) 
end

getgenv().SearchPlayers = function(Name)
	local Inserted = {}
	for _, p in pairs(game:GetService("Players"):GetPlayers()) do 
		if string.lower(string.sub(p.Name, 1, string.len(Name))) == string.lower(Name) then 
			table.insert(Inserted, p);return p
		end
	end
end

getgenv().GetInit = function(CName)
	for _, v in next, Commands do 
		if v.Name == CName or table.find(v.Aliases, CName) then 
			return v.Function 
		end 
	end
end

getgenv().RunCommand = function(Cmd)
	Cmd = string.lower(Cmd)
	pcall(function()
		if Cmd:sub(1, #Prefix) == Prefix then 
			local Args = string.split(Cmd:sub(#Prefix + 1), " ")
			local CmdName = GetInit(table.remove(Args, 1))
			if CmdName and Args then
				return CmdName(Args)
			end
		end
	end)
end

local ScreenGui = Instance.new("ScreenGui")
local Cmdbar = Instance.new("TextBox")
local UIGradient = Instance.new("UIGradient")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.ResetOnSpawn = false

Cmdbar.Name = "Cmdbar"
Cmdbar.Parent = ScreenGui
Cmdbar.BackgroundColor3 = Color3.fromRGB(116, 0, 211)
Cmdbar.Position = UDim2.new(-0.000620263279, 0, 0.3856107, 0)
Cmdbar.Size = UDim2.new(0, 940, 0, 64)
Cmdbar.Visible = false
Cmdbar.Font = Enum.Font.SourceSans
Cmdbar.Text = ""
Cmdbar.TextColor3 = Color3.fromRGB(0, 0, 0)
Cmdbar.TextSize = 14.000

UIGradient.Parent = Cmdbar

local Uis = game:GetService("UserInputService")
Uis.InputBegan:Connect(function(Key, Typing)
	if Typing then return end
	if Key.KeyCode == Enum.KeyCode.Semicolon then
		Cmdbar.Visible = true
		Cmdbar.Text = ""
		wait()
		Cmdbar:CaptureFocus()
		--Cmdbar:TweenSize(UDim2.new(0, 419, 0, 20), "Out", "Quad", 0.1, true)
	end
end)
Cmdbar.FocusLost:Connect(function(Foc)
	if Foc == true then
		--Cmdbar:TweenSize(UDim2.new(0, 0, 0, 20), "Out", "Quad", 0.1, true)
		wait()
		Cmdbar.Visible = false
		game:GetService("Players"):Chat(Prefix..Cmdbar.Text)
	end
end)
Uis.InputEnded:Connect(function(Key)
	if Key.KeyCode.Name == "LeftAlt" then
		Cmdbar.Visible = false
	end
end)

-- [[ locals ]] -- 
local Players, RService, RStorage, VUser, SGui, TPService = game:GetService("Players"), game:GetService("RunService"), game:GetService("ReplicatedStorage"), game:GetService("VirtualUser"), game:GetService("StarterGui"), game:GetService("TeleportService")
local Client, Mouse, Camera, CF, INew, Vec3, Vec2, UD2, UD = Players.LocalPlayer, Players.LocalPlayer:GetMouse(), workspace.CurrentCamera, CFrame.new, Instance.new, Vector3.new, Vector2.new, UDim2.new, UDim.new;
local Noclip, Blink, Esp, Flying, Noseats = false, false, false, false, false;
local Aimbot, Viewing, Camlock = false, false, false;
local AimbotTarget, ViewTarget, CamlockTarget, EspTarget = nil, nil, nil, nil;
local Flyspeed, Aimvelocity, Blinkspeed = 5, 10, 2;
local AimPart, CamPart = "Torso", "Torso";
local StreetsID, PrisonID = 455366377, 4669040;
local AFK, AFKMessage = false, "AFK !"

-- [[ functions ]] -- 
local AimPartTable = {
	["torso"] = "Torso";
	["head"] = "Head";
}
local KeysTable = {
	["W"] = false;["A"] = false;
	["S"] = false;["D"] = false;
	["LeftControl"] = false;["LeftShift"] = false;
}

local function ChatSpy()
	local ChatSpyFrame = Client.PlayerGui.Chat.Frame
	ChatSpyFrame.ChatChannelParentFrame.Visible = true
	ChatSpyFrame.ChatBarParentFrame.Position = ChatSpyFrame.ChatChannelParentFrame.Position + UD2(UD(), ChatSpyFrame.ChatChannelParentFrame.Size.Y)
end
ChatSpy()

local function ConfirmCallbacks()
	wait()
	SGui:SetCore("ResetButtonCallback", true)
end
ConfirmCallbacks()

getgenv().ResetCharacter = function()
	if Client and Client.Character and Client.Character:FindFirstChild("Humanoid") then 
		Client.Character.Humanoid:ChangeState(15)
	end
end

getgenv().EspPlayer = function(Dude)
	local bgui = Instance.new("BillboardGui", Dude.Character.Head)
	local tlabel = Instance.new("TextLabel", bgui)

	bgui.Name = "ESP"
	bgui.Adornee = part
	bgui.AlwaysOnTop = true
	bgui.ExtentsOffset = Vector3.new(0, 3, 0)
	bgui.Size = UDim2.new(0, 5, 0, 5)
	bgui.ResetOnSpawn = false

	tlabel.Name = "espTarget"
	tlabel.BackgroundColor3 = Color3.new(170, 0, 0)
	tlabel.BackgroundTransparency = 1
	tlabel.BorderSizePixel = 0
	tlabel.Position = UDim2.new(0, 0, 0, -30)
	tlabel.Size = UDim2.new(1, 0, 7, 0)
	tlabel.Visible = true
	tlabel.ZIndex = 10
	tlabel.Font = "ArialBold"
	tlabel.FontSize = "Size18"
	RService.RenderStepped:Connect(function()
		if Dude and Dude.Character and Dude.Character:FindFirstChildOfClass("Humanoid") then 
			tlabel.Text = Dude.Name.." ["..math.floor(Dude.Character.Humanoid.Health).."/"..math.floor(Dude.Character.Humanoid.MaxHealth).."]".." ["..math.floor(Dude:DistanceFromCharacter(Client.Character.Head.Position)).."]"
		end
	end)
	tlabel.TextColor = BrickColor.new("Red") 
	tlabel.TextStrokeTransparency = 0.5
end

getgenv().togglefly = function()
	Flying = not Flying
	Notify("covax", "Flying: "..tostring(Flying), "", 3)
	local T = Client.Character:FindFirstChild("HumanoidRootPart") or Client.Character:FindFirstChild("Torso")
	local BV, BG = INew("BodyVelocity", T), INew("BodyGyro", T)
	BV.Velocity = Vec3(0, 0.1, 0);BV.MaxForce = Vec3(math.huge, math.huge, math.huge)
	BG.CFrame = T.CFrame;BG.P = 9e9;BG.MaxTorque = Vec3(9e9, 9e9, 9e9)
	local FlyPart = INew("Part", workspace)
	FlyPart.Anchored = true;FlyPart.Size = Vec3(6, 1, 6);FlyPart.Transparency = 1 

	while Flying == true and Client and Client.Character and Client.Character:FindFirstChild("Humanoid") and Client.Character.Humanoid.Health ~= 0 and RService.Heartbeat:Wait() and T do 
		local Front, Back, Left, Right = 0, 0, 0, 0
		if KeysTable["W"] == true then 
			Front = Flyspeed 
		elseif not KeysTable["W"] == true then
			Front = 0 
		end
		if KeysTable["A"] == true then 
			Right = -Flyspeed
		elseif not KeysTable["A"] == true then 
			Right = 0 
		end
		if KeysTable["S"] == true then 
			Back = -Flyspeed 
		elseif not KeysTable["S"] == true then 
			Back = 0
		end
		if KeysTable["D"] == true then 
			Left = Flyspeed
		elseif not KeysTable["D"] == true then 
			Left = 0
		end
		if tonumber(Front + Back) ~= 0 or tonumber(Left + Right) ~= 0 then 
			BV.Velocity = ((Camera.CoordinateFrame.lookVector * (Front + Back)) + ((Camera.CoordinateFrame * CF(Left + Right, (Front + Back) * 0.2, 0).p) - Camera.CoordinateFrame.p)) * 50
		else 
			BV.Velocity = Vec3(0, 0.1, 0)
		end
		BG.CFrame = Camera.CoordinateFrame
	end
	FlyPart:Destroy();BG:Remove();BV:Remove()
end

Uis.InputBegan:Connect(function(Key)
	if not (Uis:GetFocusedTextBox()) then
		if Key.KeyCode == Enum.KeyCode.W then 
			KeysTable["W"] = true 
		end 
		if Key.KeyCode == Enum.KeyCode.A then 
			KeysTable["A"] = true 
		end
		if Key.KeyCode == Enum.KeyCode.S then 
			KeysTable["S"] = true 
		end
		if Key.KeyCode == Enum.KeyCode.D then 
			KeysTable["D"] = true 
		end
		if Key.KeyCode == Enum.KeyCode.F then 
			if FirstFly == true then 
				Notify("covax", "You can now fly, like a bird.", "", 3)
				FirstFly = false 
			end
			togglefly()
		end
		if Key.KeyCode == Enum.KeyCode.X then 
			Noclip = not Noclip 
			Notify("covax", "Noclip: "..tostring(Noclip), "", 3)
		end
		if Key.KeyCode == Enum.KeyCode.LeftShift then
			KeysTable["LeftShift"] = true
			while Blink == true and KeysTable["LeftShift"] == true and Client and Client.Character and RService.Heartbeat:Wait() do
				local ClientRF = Client.Character:FindFirstChild("HumanoidRootPart") or Client.Character:FindFirstChild("Torso")
				local Hum = Client.Character:FindFirstChild("Humanoid")
				ClientRF.CFrame = ClientRF.CFrame + Vec3(Hum.MoveDirection.X * Blinkspeed, Hum.MoveDirection.Y * Blinkspeed, Hum.MoveDirection.Z * Blinkspeed)
			end 
		end
	end
end)
Uis.InputEnded:Connect(function(Key --[[Typing]])
	if not (Uis:GetFocusedTextBox()) then
		if Key.KeyCode == Enum.KeyCode.W then 
			KeysTable["W"] = false 
		end
		if Key.KeyCode == Enum.KeyCode.A then 
			KeysTable["A"] = false 
		end
		if Key.KeyCode == Enum.KeyCode.S then 
			KeysTable["S"] = false 
		end
		if Key.KeyCode == Enum.KeyCode.D then 
			KeysTable["D"] = false
		end
		if Key.KeyCode == Enum.KeyCode.LeftShift then
			KeysTable["LeftShift"] = false
		end
	end
end)

-- [[ Bypass ]] --
local rm = getrawmetatable(game) or debug.getrawmetatable(game) or getmetatable(game)
if setreadonly then setreadonly(rm, false) else make_writeable(rm, true) end
local caller, cscript = checkcaller or is_protosmasher_caller, getcallingscript or get_calling_script;
local rindex, nindex, ncall, closure = rm.__index, rm.__newindex, rm.__namecall, newcclosure or read_me;

rm.__newindex = closure(function(self, Meme, Val)
	if caller() then return nindex(self, Meme, Val) end 
	if game.PlaceId ~= (StreetsID) then 
		if Meme == "WalkSpeed" then 
			return 16
		end
		if Meme == "JumpPower" then 
			return 37.5 
		end
		if Meme == "HipHeight" then 
			return 0 
		end
		if Meme == "Health" then 
			return 100 
		end
	end
	if self:IsDescendantOf(Client.Character) and self.Name == "HumanoidRootPart" or self.Name == "Torso" then 
		if Meme == "CFrame" or Meme == "Position" or Meme == "Anchored" then 
			return nil 
		end
	end
	return nindex(self, Meme, Val) 
end)
rm.__namecall = closure(function(self, ...)
	local Args, Method = {...}, getnamecallmethod() or get_namecall_method();
	if Method == "BreakJoints" then 
		return wait(9e9)
	end
	if game.PlaceId ~= (StreetsID) then
		if Method == "FireServer" and not self.Name == "SayMessageRequest" then
			if tostring(self.Parent) == "ReplicatedStorage" or self.Name == "lIII" then 
				return wait(9e9) 
			end
			if Args[1] == "hey" then 
				return wait(9e9) 
			end
		end
		if Method == "FireServer" and self.Name == "Fire" and AimbotTarget ~= nil and Aimbot == true  then
			return ncall(self, AimbotTarget.Character[AimPart].CFrame + AimbotTarget.Character[AimPart].Velocity/Aimvelocity)
		end
	end
	if game.PlaceId == (StreetsID) then
		if Method == "FireServer" and Args[1] == "WalkSpeed" or Args[1] == "JumpPower" or Args[1] == "HipHeight" then 
			return nil 
		end
		if Method == "FireServer" and self.Name == "Input" then 
			if Args[1] == "bv" or Args[1] == "hb" or Args[1] == "ws" then 
				return wait(9e9)
			end
		end
		if Method == "FireServer" and self.Name == "Input" and AimbotTarget ~= nil and Aimbot == true then 
			Args[2].mousehit = AimbotTarget.Character[AimPart].CFrame + AimbotTarget.Character[AimPart].Velocity/Aimvelocity 
			Args[2].velo = math.huge
			return ncall(self, unpack(Args))
		end
	end
	return ncall(self, unpack(Args))
end)
if setreadonly then setreadonly(rm, true) else make_writeable(rm, false) end

-- [[ CharacterAdded/Died ]] --
Client.Character.Humanoid.Died:Connect(function()
	if Flying then togglefly() end
end)
Client.CharacterAdded:Connect(function()
	repeat wait() until Client.Character:FindFirstChild("Humanoid")
	Client.Character.Humanoid.Died:Connect(function()
		if Flying then togglefly() end
	end)
end)

-- [[ Commands ]] --
Commands["Play a Song"] = {
	["Aliases"] = {"pl", "play", "playsong", "ps", "song"};
	["Function"] = function(Args)
		if Args[1] then 
			local Radio = Client.Backpack:FindFirstChild("BoomBox")
			if Radio then 
				Radio.Parent = Client.Character
				Radio.RemoteEvent:FireServer("play", tonumber(Args[1]))
			end
			Notify("covax", "Audio: "..tonumber(Args[1]), "", 3)
		end
	end
}
Commands["Go AFK"] = {
	["Aliases"] = {"afk", "brb"};
	["Function"] = function(Args)
		AFK = not AFK
		if (not AFK) then return end
		spawn(function()
			while AFK do
				wait(0.5)
				game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer(AFKMessage, "All")
			end
		end)
	end
}
Commands["Sets your Flyspeed"] = {
	["Aliases"] = {"flyspeed", "fs"};
	["Function"] = function(Args)
		if Args[1] then 
			Flyspeed = tonumber(Args[1])
			Notify("covax", "Flyspeed: "..tonumber(Flyspeed), "", 3)
		end
	end
}
Commands["Toggles Fly"] = {
	["Aliases"] = {"fly", "togglefly"};
	["Function"] = function(Args)
		togglefly()
	end
}
Commands["Sets your Chat Command Prefix"] = {
	["Aliases"] = {"prefix", "pfix"};
	["Function"] = function(Args)
		if Args[1] then 
			Prefix = Args[1]
		end
		Notify("covax", "Prefix: "..tostring(Prefix), "", 3)
	end
}
Commands["Sets your FieldOfView"] = {
	["Aliases"] = {"fieldofview", "fov"};
	["Function"] = function(Args)
		if Args[1] then 
			Camera.FieldOfView = tonumber(Args[1])
		end
		Notify("covax", "FieldOfView: "..tonumber(Args[1]), "", 3)
	end
}
Commands["Toggles Blink"] = {
	["Aliases"] = {"blink", "blinkspd"};
	["Function"] = function(Args)
		Blink = not Blink 
		Notify("covax", "Blink: "..tostring(Blink), "", 3)
	end
}
Commands["Esp a Player"] = {
	["Aliases"] = {"esp", "find"};
	["Function"] = function(Args)
		if Args[1] then
			EspTarget = SearchPlayers(Args[1])
			if EspTarget then
				EspPlayer(EspTarget)
			end
		end
		Notify("covax", "Esp Target: "..tostring(EspTarget), "", 3)
	end
}
Commands["UnEsp Esp'd Player"] = {
	["Aliases"] = {"unesp", "unfind"};
	["Function"] = function(Args)
		if Args[1] then 
			local UnEspPlayer;UnEspPlayer = SearchPlayers(Args[1])
			if UnEspPlayer then 
				for _, v in next, UnEspPlayer.Character:GetDescendants() do 
					if v:IsA("BillboardGui") or v:IsA("TextLabel") then 
						v:Destroy() --[[if staircase(s) go brrrRRR]]
					end
				end
			end
		end
	end
}
Commands["Rejoins Current Game"] = {
	["Aliases"] = {"rejoin"};
	["Function"] = function()
		TPService:Teleport(game.PlaceId, Client)
	end
}
Commands["Resets Your Character"] = {
	["Aliases"] = {"r", "reset", "re", "res"};
	["Function"] = function()
		ResetCharacter()
	end
}
Commands["Sets Camlock Target"] = {
	["Aliases"] = {"camlock", "cam", "cl", "cml"};
	["Function"] = function(Args)
		if Args[1] then 
			CamlockTarget = SearchPlayers(Args[1]);Camlock = true
		end
		Notify("covax", "Camlock Target: "..tostring(CamlockTarget), "", 3)
	end
}
Commands["UnCamlocks Camlocked Target"] = {
	["Aliases"] = {"uncamlock", "uncam", "uncl", "uncml"};
	["Function"] = function()
		CamlockTarget = nil;Camlock = false 
		Notify("covax", "Camlock: "..tostring(Camlock), "", 3)
	end
}
Commands["Sets Aimbot Target"] = {
	["Aliases"] = {"aim", "s", "aimbot", "shoot"};
	["Function"] = function(Args)
		if Args[1] then 
			AimbotTarget = SearchPlayers(Args[1]);Aimbot = true
		end
		Notify("covax", "Aimbot Target: "..tostring(AimbotTarget), "", 3)
	end
}
Commands["UnAimbots Aimbotted Target"] = {
	["Aliases"] = {"unaim", "uns", "unaimbot", "unshoot"};
	["Function"] = function()
		AimbotTarget = nil;Aimbot = false
		Notify("covax", "Aimbot: "..tostring(Aimbot), "", 3)
	end
}
Commands["View a Player"] = {
	["Aliases"] = {"view"};
	["Function"] = function(Args)
		if Args[1] then 
			ViewTarget = SearchPlayers(Args[1]);Viewing = true 
		end
		Notify("covax", "View Target: "..tostring(ViewTarget), "", 3)
	end
}
Commands["UnView Viewed Target"] = {
	["Aliases"] = {"unview"};
	["Function"] = function()
		ViewTarget = nil;Viewing = false
		Camera.CameraSubject = Client.Character
		Notify("covax", "Viewing: "..tostring(Viewing), "", 3)
	end
}
Commands["Sets Aimvelocity"] = {
	["Aliases"] = {"aimvelocity"};
	["Function"] = function(Args)
		if Args[1] then 
			Aimvelocity = tonumber(Args[1])
		end
		Notify("covax", "Aimvelocity: "..tonumber(Args[1]), "", 3)
	end
}
Commands["Toggles Noclip"] = {
	["Aliases"] = {"noclip", "nc", "nclip"};
	["Function"] = function()
		Noclip = not Noclip 
		Notify("covax", "Noclip: "..tostring(Noclip), "", 3)
	end
}
Commands["Sets Blinkspeed"] = {
	["Aliases"] = {"bs", "blinkspeed"};
	["Function"] = function(Args)
		if Args[1] then 
			Blinkspeed = tonumber(Args[1])
		end
		Notify("covax", "Blinkspeed: "..tonumber(Args[1]), "", 3)
	end
}
Commands["Sets Aimbot Part"] = {
	["Aliases"] = {"aimpart"};
	["Function"] = function(Args)
		AimPart = Args[1]
		if AimPartTable[Args[1]] then 
			AimPart = AimPartTable[Args[1]] 
		end
		Notify("covax", "AimPart: "..tostring(AimPart), "", 3)
	end
}
Commands["Removes Chairs"] = {
	["Aliases"] = {"removechair", "rc"};
	["Function"] = function()
		for _, v in next, workspace:GetChildren() do 
			if v:IsA("Seat") then 
				v:Destroy()
			end
		end
	end
}


RService.Stepped:Connect(function()
	if Camlock == true and CamlockTarget and CamlockTarget.Character and CamlockTarget.Character:FindFirstChild(CamPart) then 
		Camera.CoordinateFrame = CF(Camera.CoordinateFrame.p, CF(CamlockTarget.Character[CamPart].Position).p)
	end
	if Noclip == true then 
		for i = 1, #Client.Character:GetChildren() do
			local CG = Client.Character:GetChildren()[i]
			if CG:IsA("BasePart") then 
				CG.CanCollide = false 
			end
		end
		pcall(function()
			if Client and Client.Backpack then 
				Client.Backpack:FindFirstChild("Glock").Barrel.CanCollide = false 
			else
				Client.Character:FindFirstChild("Glock").Barrel.CanCollide = false
			end
		end)
	end
	if Viewing == true and ViewTarget ~= nil then 
		Camera.CameraSubject = ViewTarget.Character
	end
	if Flying and Client.Character then
		if Client.Character and Client.Character:FindFirstChild("Humanoid") then
			RService.Heartbeat:Wait()
			Client.Character.Humanoid.PlatformStand = false;Client.Character.Humanoid.Sit = false
			Client.Character.Humanoid:ChangeState(Enum.HumanoidStateType.Running)
		end
	end
	if Client.Character:FindFirstChild("FlyPart") then
		Client.Character:FindFirstChild("FlyPart").CFrame = Client.Character.HumanoidRootPart.CFrame * CF(0, -3.5, 0)
	end
end)

print([[

got the source for a dick pic :smirk:
=======

-------
Toggles = Turns On and Off
Alt = Other names for the Command
-------

Keybinds:

F - Toggles Fly 
X - Toggles Noclip
; - Toggles Command Bar
=======

(Names can be Shortened/Not-Capitalized)
Commands:

[1]: pl <id here>, Plays that song in your Radio (Alt: play, playsong, ps, song)
[2]: afk, Toggles Anti-Afk (Alt: brb)
[3]: flyspeed <number here>, Sets your FlySpeed (Alt: fs)
[4]: fly, Toggles Fly (Alt: togglefly)
[5]: prefix <letter or whatever here>, Sets your Chat Command Prefix (Alt: pfix)
[6]: fieldofview <number here>, Sets your FieldOfView (Alt: fov, f)
[7]: blink, Toggles Blink (Alt: blinkspd)
[8]: esp <name here>, Sets ESP Target 
[9]: unesp <name here>, UnEsp's ESP'd Target 
[10]: rejoin, Rejoins the Current Game 
[11]: r, Resets your Character (Alt: reset, re, res)
[12]: camlock <name here>, Sets Camlock Target (Alt: cam, cl, cml)
[13]: uncamlock, UnCamlocks Camlocked Target (Alt: uncam, uncl, uncml)
[14]: aimbot <name here>, Sets Aimbot Target (Alt: s, aim, shoot) (Press LeftClick/Mouse1 to Aimbot them)
[15]: unaimbot, UnAimbots Aimbot Target (Alt: uns, unaim, unshoot)
[16]: view <name here>, Sets View Target 
[17]: unview, UnViews Viewed Target 
[18]: aimvelocity <number here>, Sets Aimvelocity 
[19]: noclip, Toggles Noclip 
[20]: blinkspeed <number here>, Sets Blinkspeed (Alt: bs)
[21]: aimpart <torso or head>, Sets the Part in which Aimbot shoots at
[22]: removechair, Removes Chairs in the workspace (Alt: rc)

]])

Client.Chatted:Connect(RunCommand)
Notify("covax", "Took "..string.format("%.3f", tick() - LoadingTime).." f9 for cmds", "" , 3)
-- credits to unknown X
local ScreenGui = Instance.new("ScreenGui")
local TextLabel = Instance.new("TextLabel")
local Frame = Instance.new("Frame")
local HealthInfo = Instance.new("TextLabel")
local WalkSpeedtxt = Instance.new("TextLabel")
local WsInfo = Instance.new("TextLabel")
local Healthtxt = Instance.new("TextLabel")
local StanInfo = Instance.new("TextLabel")
local StanTxt = Instance.new("TextLabel")
local ToolsInfo = Instance.new("TextLabel")
local Toolstxt = Instance.new("TextLabel")
local lp = game:GetService("Players").LocalPlayer
local p = game:GetService("Players")
local hum = lp.Character.Humanoid
local info = true or false
info = true
local m = lp:GetMouse()
ScreenGui.Parent = game.CoreGui
TextLabel.Parent = ScreenGui
TextLabel.BackgroundColor3 = Color3.new(0.278431, 0.278431, 0.278431)
TextLabel.BorderColor3 = Color3.new(0.129412, 0.129412, 0.129412)
TextLabel.Position = UDim2.new(0, 0, 0.537848592, 0)
TextLabel.Size = UDim2.new(0, 160, 0, 12)
TextLabel.Font = Enum.Font.Code
TextLabel.Text = "Player Info"
TextLabel.TextColor3 = Color3.new(1, 1, 1)
TextLabel.TextSize = 14
Frame.Parent = TextLabel
Frame.BackgroundColor3 = Color3.new(0, 0, 0)
Frame.BackgroundTransparency = 0.40000000596046
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0, 0, 1, 0)
Frame.Size = UDim2.new(0, 160, 0, 100)
HealthInfo.Name = "HealthInfo"
HealthInfo.Parent = Frame
HealthInfo.BackgroundColor3 = Color3.new(1, 1, 1)
HealthInfo.BackgroundTransparency = 1
HealthInfo.Position = UDim2.new(-0.000946760178, 0, 0.0700000077, 0)
HealthInfo.Size = UDim2.new(0, 47, 0, 21)
HealthInfo.Font = Enum.Font.Code
HealthInfo.Text = "Health:"
HealthInfo.TextColor3 = Color3.new(1, 1, 1)
HealthInfo.TextSize = 14
WalkSpeedtxt.Name = "WalkSpeedtxt"
WalkSpeedtxt.Parent = Frame
WalkSpeedtxt.BackgroundColor3 = Color3.new(1, 1, 1)
WalkSpeedtxt.BackgroundTransparency = 1
WalkSpeedtxt.Position = UDim2.new(0.455303222, 0, 0.279999971, 0)
WalkSpeedtxt.Size = UDim2.new(0, 30, 0, 21)
WalkSpeedtxt.Font = Enum.Font.Code
WalkSpeedtxt.Text = ""
WalkSpeedtxt.TextColor3 = Color3.new(255, 0, 0)
WalkSpeedtxt.TextSize = 14
WsInfo.Name = "WsInfo"
WsInfo.Parent = Frame
WsInfo.BackgroundColor3 = Color3.new(1, 1, 1)
WsInfo.BackgroundTransparency = 1
WsInfo.Position = UDim2.new(0.0740532428, 0, 0.279999971, 0)
WsInfo.Size = UDim2.new(0, 47, 0, 21)
WsInfo.Font = Enum.Font.Code
WsInfo.Text = "WalkSpeed:"
WsInfo.TextColor3 = Color3.new(1, 1, 1)
WsInfo.TextSize = 14
Healthtxt.Name = "Healthtxt"
Healthtxt.Parent = Frame
Healthtxt.BackgroundColor3 = Color3.new(1, 1, 1)
Healthtxt.BackgroundTransparency = 1
Healthtxt.Position = UDim2.new(0.505303204, 0, 0.0700000003, 0)
Healthtxt.Size = UDim2.new(0, 40, 0, 21)
Healthtxt.Font = Enum.Font.Code
Healthtxt.Text = ""
Healthtxt.TextColor3 = Color3.new(255, 0, 0)
Healthtxt.TextSize = 12
StanInfo.Name = "StanInfo"
StanInfo.Parent = Frame
StanInfo.BackgroundColor3 = Color3.new(1, 1, 1)
StanInfo.BackgroundTransparency = 1
StanInfo.Position = UDim2.new(-0.000946760178, 0, 0.49000001, 0)
StanInfo.Size = UDim2.new(0, 59, 0, 21)
StanInfo.Font = Enum.Font.Code
StanInfo.Text = "Stamina:"
StanInfo.TextColor3 = Color3.new(1, 1, 1)
StanInfo.TextSize = 14
StanTxt.Name = "StanTxt"
StanTxt.Parent = Frame
StanTxt.BackgroundColor3 = Color3.new(1, 1, 1)
StanTxt.BackgroundTransparency = 1
StanTxt.Position = UDim2.new(0.62405324, 0, 0.48999995, 0)
StanTxt.Size = UDim2.new(0, 30, 0, 21)
StanTxt.Font = Enum.Font.Code
StanTxt.Text = ""
StanTxt.TextColor3 = Color3.new(255, 0, 0)
StanTxt.TextSize = 14
ToolsInfo.Name = "ToolsInfo"
ToolsInfo.Parent = Frame
ToolsInfo.BackgroundColor3 = Color3.new(1, 1, 1)
ToolsInfo.BackgroundTransparency = 1
ToolsInfo.Position = UDim2.new(-0.0134467632, 0, 0.699999988, 0)
ToolsInfo.Size = UDim2.new(0, 103,0, 21)
ToolsInfo.Font = Enum.Font.Code
ToolsInfo.Text = "Equipped Tool:"
ToolsInfo.TextColor3 = Color3.new(1, 1, 1)
ToolsInfo.TextSize = 14
Toolstxt.Name = "Toolstxt"
Toolstxt.Parent = Frame
Toolstxt.BackgroundColor3 = Color3.new(1, 1, 1)
Toolstxt.BackgroundTransparency = 1
Toolstxt.Position = UDim2.new(0.687, 0,0.7, 0)
Toolstxt.Size = UDim2.new(0, 30, 0, 21)
Toolstxt.Font = Enum.Font.Code
Toolstxt.Text = ""
Toolstxt.TextColor3 = Color3.new(255, 0, 0)
Toolstxt.TextSize = 14
if info == true and not info == false then
	m.Button1Down:connect(function()
	if m.Target or m.Target.Parent then
		local plr = p:GetPlayerFromCharacter(m.Target.Parent)
		local name = plr.Name
		if plr ~= nil then
			local tools = plr.Backpack
			TextLabel.Text = "Info("..name..")"
			repeat
				wait()
				if TextLabel.Text == "Info("..name..")" then
					TextLabel.Text = "Info("..name..")"
				else
					plr = nil
				end
				Healthtxt.Text = plr.Character.Humanoid.Health
				WalkSpeedtxt.Text = plr.Character.Humanoid.WalkSpeed
				StanTxt.Text = plr.Backpack.ServerTraits.Stann.Value
				for _,x in pairs(plr.Character:GetChildren()) do
					if x:IsA("Tool") then
						Toolstxt.Text = x.Name
					else
						Toolstxt.Text = ""
					end
				end
			until info == false 
		end
	end
	end)
end
-- end of that script lol

-- zoom inf 
game.Players.LocalPlayer.CameraMaxZoomDistance = math.huge
-- end of zoom inf



-- walkshoot 
if game.PlaceId == 4669040 or 455366377 then
local mt = getrawmetatable(game)
local backup
backup = hookfunction(mt.__newindex, newcclosure(function(self, key, value)
if key == "WalkSpeed" and value < 16 then
value = 16
end
return backup(self, key, value)
end))
end
--end of walkshoot
-- credits to citizen or some shit
