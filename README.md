god = game:service'Players'.localPlayer -- who's chat the commands respond to
function onChatted(msg)

if msg == "add;tab" then

z=Instance.new("Part",game:service'Players'.localPlayer.Character)
z.Transparency = 0.5
z.FormFactor = "Custom"
z.Size = Vector3.new(15,15,0)
z.TopSurface = "Smooth"
z.BottomSurface = "Smooth"
z.Color = Color3.new(0,0,0)

x=Instance.new("SelectionBox",z)
x.Adornee=z
x.Transparency=0.5
x.Color=BrickColor.new('Really black');

b=Instance.new("SurfaceGui",z)
b.Face = "Back"
q=Instance.new("TextLabel",b)
q.Text = "Welcome "
q:TweenSize(UDim2.new(0, 800,0, 300),"In",style,interval,false)
q:TweenPosition(UDim2.new(0,0,0,1),"In",style,interval,false)
q.FontSize = Enum.FontSize.Size48
q.BackgroundColor3 = Color3.new(255,255,255)


m=Instance.new("TextButton",b)
m.Text = "Play"
m:TweenSize(UDim2.new(0, 800,0, 300),"In",style,interval,false)
m:TweenPosition(UDim2.new(0,0,0,300),"In",style,interval,false)
m.FontSize = Enum.FontSize.Size48
m.BackgroundColor3 = Color3.new(255,255,255)

function onClick()
Sound = 145763936
O = Instance.new("Sound",workspace)
O.SoundId = ("http://www.roblox.com/asset/?id="..Sound)
O.Pitch = 1
O.Volume = 1
O.Looped = true 
O:Play()
m.TextColor3 = Color3.new(0,1,0)


end

m.MouseButton1Down:connect(onClick)



while true do 
for i = 0,360 do
wait()
orbittingbrick.CFrame = brick.CFrame * CFrame.new(-1,5,-distancefrombrick)
end
end

end 
end 
god.Chatted:connect(onChatted) 
