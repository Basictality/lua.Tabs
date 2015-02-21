z=Instance.new("Part",workspace)
z.Transparency = 0.6
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

h=Instance.new("TextLabel",b)
h.BackgroundTransparency = 0.6
h.Size = UDim2.new(0,800,0,50)
h.Text = "Commands:"
h.BackgroundColor3 = Color3.new(0,0,0)
h.TextColor3 = Color3.new(255,255,255)
h.FontSize = Enum.FontSize.Size24



brick = game.Players.LocalPlayer.Character.Head
orbittingbrick = z
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 5

while true do 
for i = 0,360 do
wait()
orbittingbrick.CFrame = CFrame.new(brick.Position) * CFrame.new(0,5,-distancefrombrick)
end
end
