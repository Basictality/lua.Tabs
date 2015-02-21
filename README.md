screngui=Instance.new("ScreenGui",game.Players.LocalPlayer.PlayerGui)
tie=Instance.new("TextBox",screngui)
tie:TweenSize(UDim2.new(0, 500,0, 50),"In",style,interval,false)
tie.BackgroundColor3 = Color3.new(0,0,0)
tie.TextColor3 = Color3.new(255,255,255)
tie.BackgroundTransparency = 0.3
tie:TweenPosition(UDim2.new(0, 300,0, 0),"In",style,interval,false)
tie.FontSize = Enum.FontSize.Size24



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

h=Instance.new("TextButton",b)
h.BackgroundTransparency = 0.6
h:TweenSize(UDim2.new(0, 800,0, 100),"In",style,interval,false)
h.Text = "Commands"
h.BackgroundColor3 = Color3.new(0,0,0)
h.TextColor3 = Color3.new(255,255,255)
h.FontSize = Enum.FontSize.Size24



function onClick()
h:TweenPosition(UDim2.new(0, 0,0, 0),"In",style,interval,false)
h:TweenSize(UDim2.new(0, 0,0, 0),"In",style,interval,false)
bt=Instance.new("ScrollingFrame",b)
bt:TweenSize(UDim2.new(0, 800,0, 700),"In",style,interval,false)
bt.BackgroundTransparency = 0.5
bt.Background.Color = Color3.new(0,0,0)
bt.Positon
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
