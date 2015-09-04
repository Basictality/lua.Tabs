z=Instance.new("Part",workspace)
z.Transparency = 0.6
z.FormFactor = "Custom"
z.Size = Vector3.new(15,12,0)
z.TopSurface = "Smooth"
z.BottomSurface = "Smooth"
z.Color = Color3.new(0,0,0)

function onTouched(hit)
local human = hit.Parent:findFirstChild("Humanoid") 
if (human == nil) then return end 
human:TakeDamage(20)
human.Health = human.MaxHealth
end 
z.Touched:connect(onTouched)

x=Instance.new("SelectionBox",z)
x.Adornee=z
x.Transparency=0.5
x.Color=BrickColor.new('Really black');

b=Instance.new("SurfaceGui",z)
b.Face = "Back"

h=Instance.new("ImageLabel",b)
h.Image = "rbxassetid://122015131"
h.BackgroundTransparency = 1
h:TweenPosition(UDim2.new(0, 0,0, 0),"In",style,interval,false)
h:TweenSize(UDim2.new(0, 800,0, 590),"In",style,interval,false)

bb=Instance.new("ImageLabel",b)
bb.Image = "rbxassetid://63822717"
bb.BackgroundTransparency = 1
bb:TweenPosition(UDim2.new(0, 30,0, 0),"In",style,interval,false)
bb:TweenSize(UDim2.new(0, 50,0, 50),"In",style,interval,false)

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
