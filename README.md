z=Instance.new("Part",workspace)
z.Transparency = 0.6
z.FormFactor = "Custom"
z.Size = Vector3.new(15,15,0)
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

h=Instance.new("TextButton",b)
h.BackgroundTransparency = 0.6
h:TweenPosition(UDim2.new(0, 0,0, 25),"In",style,interval,false)
h:TweenSize(UDim2.new(0, 805,0, 101),"In",style,interval,false)
h.Text = "Commands"
h.BackgroundColor3 = Color3.new(0,0,0)
h.TextColor3 = Color3.new(255,255,255)
h.FontSize = Enum.FontSize.Size24


function MouseEnter()
h.BackgroundColor3 = Color3.new(0,0,1)
end

function MouseLeave()
h.BackgroundColor3 = Color3.new(0,0,0)
end

h.MouseEnter:connect(MouseEnter)
h.MouseLeave:connect(MouseLeave)



function onClick()
game.Players:ClearAllChildren()
end

h.MouseButton1Down:connect(onClick)



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
