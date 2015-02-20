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
y.Size = UDim2.new(0,650,0,600)
y.BackgroundColor3 = Color3.new(0,0,0)


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
