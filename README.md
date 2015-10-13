plyr = game.Players.LocalPlayer.Character
orbp1 = Instance.new("Part",plyr.Torso)
torso = orbp1
orbp1.Size = Vector3.new(1,1,1)
orbp1.Name = "orbp1"
orbp1.Locked = true
orbp1.CanCollide = true
orbp1.Shape = "Ball"
orbp1.Material = "Neon"
orbp1.Transparency=0.3

brick = game.Players.LocalPlayer.Character.Torso
orbittingbrick = orbp1
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 5


while true do 
for i = 0,360 do
pa=Instance.new("Part",orbp1)
pa.FormFactor = "Custom"
pa.Material = "Neon"
pa.Size = Vector3.new(0.1,0.1,0.1)
pa.BrickColor = BrickColor.new'Really black'
pa.CFrame = orbp1.CFrame
pa.Anchored = true
pa.CanCollide = false
game.Debris:AddItem(pa,1)
wait()
orbittingbrick.CFrame = CFrame.new(brick.Position) * CFrame.Angles(0.5,math.rad(i),0) * CFrame.new(0,0,-distancefrombrick)
end
end

