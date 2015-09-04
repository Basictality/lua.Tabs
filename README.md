r65 = game.Players.LocalPlayer.Character

z=Instance.new("Part",r65)
z.Transparency = 0.6
z.FormFactor = "Custom"
z.Size = Vector3.new(15,12,0)
z.TopSurface = "Smooth"
z.BottomSurface = "Smooth"
z.Color = Color3.new(0,0,0)

--tab
z2=Instance.new("Part",z)
z2.Transparency = 0.6
z2.FormFactor = "Custom"
z2.Size = Vector3.new(15,10,0)
z2.TopSurface = "Smooth"
z2.BottomSurface = "Smooth"
z2.Color = Color3.new(0,0,0)

z23=Instance.new("SelectionBox",z)
z23.Adornee=z2
z23.Transparency=0.5
z23.Color=BrickColor.new('Teal');



x=Instance.new("SelectionBox",z)
x.Adornee=z
x.Transparency=0.5
x.Color=BrickColor.new('Really black');

b=Instance.new("SurfaceGui",z)
b.Face = "Back"

h=Instance.new("ImageLabel",b)
h.Image = "rbxassetid://88092458"
h.BackgroundTransparency = 1
h:TweenPosition(UDim2.new(0, 0,0, 0),"In",style,interval,false)
h:TweenSize(UDim2.new(0, 800,0, 590),"In",style,interval,false)
----------------------------------
bb=Instance.new("ImageButton",h)
bb.Image = "rbxassetid://63822717"
bb.BackgroundTransparency = 1
bb:TweenPosition(UDim2.new(0, 20,0, 40),"In",style,interval,false)
bb:TweenSize(UDim2.new(0, 100,0, 100),"In",style,interval,false)

sw=Instance.new("TextLabel",b)
sw.Text = "Settings"
sw.FontSize = "Size14"
sw.BackgroundTransparency = 1
sw:TweenPosition(UDim2.new(0, 40,0, 60),"In",style,interval,false)
sw:TweenSize(UDim2.new(0, 50,0, 50),"In",style,interval,false)
------------

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



brick = r65.Head
orbittingbrick = z23
orbittingbrick.Anchored = true
orbittingbrick.CanCollide = true
distancefrombrick = 5

while true do 
for i = 0,360 do
wait()
orbittingbrick.CFrame = brick.CFrame * CFrame.new(5,4,-distancefrombrick)
end
end


