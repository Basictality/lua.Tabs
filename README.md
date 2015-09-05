r65 = game.Players.LocalPlayer.Character

z=Instance.new("Part",r65)
z.Transparency = 0.6
z.FormFactor = "Custom"
z.Size = Vector3.new(15,12,0)
z.TopSurface = "Smooth"
z.BottomSurface = "Smooth"
z.Color = Color3.new(0,0,0)

z2=Instance.new("Part",z)
z2.Transparency = 0.6
z2.FormFactor = "Custom"
z2.Size = Vector3.new(15,10,0)
z2.TopSurface = "Smooth"
z2.BottomSurface = "Smooth"
z2.Color = Color3.new(0,0,0)

z23=Instance.new("SelectionBox",z2)
z23.Adornee=z2
z23.Transparency=0.5
z23.Color=BrickColor.new('Teal');

x=Instance.new("SelectionBox",z)
x.Adornee=z
x.Transparency=0.5
x.Color=BrickColor.new('Really black');

we2=Instance.new("Weld",z2)
we2.Part0=z
we2.Part1=z2
we2.C0=CFrame.new(10,0,0)


brick = game.Players.LocalPlayer.Character.Head
orbittingbrick = z
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 5

while true do 
for i = 0,360 do
wait()
orbittingbrick.CFrame = brick.CFrame * CFrame.new(0,4,-distancefrombrick)
end
end
