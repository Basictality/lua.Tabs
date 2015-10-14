plyr = game.Players.LocalPlayer.Character
orbp1 = Instance.new("Part",workspace)
torso = orbp1
orbp1.Size = Vector3.new(1,1,1)
orbp1.Name = "orbp1"
orbp1.Locked = true
orbp1.Color = Color3.new(255,255,255)
orbp1.CanCollide = true
orbp1.Shape = "Ball"
orbp1.Material = "Neon"
orbp1.Transparency=0.3

orbittingbrick = orbp1
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 4.5


while true do 
for i = 0,360.43434 do
pa=Instance.new("Part",orbp1)
pa.FormFactor = "Custom"
pa.Material = "Neon"
pa.Transparency=0.5
pa.Size = Vector3.new(0.3,0.3,0.3)
pa.BrickColor = BrickColor.new'Really black'
pa.CFrame = orbp1.CFrame * CFrame.new(0.5,0,0) * CFrame.Angles(math.random(),math.random(),math.random())
pa.Anchored = true
pa.CanCollide = false
game.Debris:AddItem(pa,1.5)
wait()
orbittingbrick.CFrame = CFrame.new(plyr.Torso.Position) * CFrame.Angles(0.5,math.rad(i),0) * CFrame.new(0,0,-distancefrombrick)
end
end
