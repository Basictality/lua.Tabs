z=Instance.new("Part",workspace)
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

y=Instance.new("ScrollingFrame",b)
y.Size = UDim2.new(0,850,0,550)
y.BackgroundColor3 = Color3.new(0,0,0)

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



brick = game.Players.LocalPlayer.Character.Head
orbittingbrick = z
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 10

while true do 
for i = 0,360 do
wait()
orbittingbrick.CFrame = brick.CFrame * CFrame.new(-1,5,-distancefrombrick)
end
end
