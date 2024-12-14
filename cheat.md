while wait(0.5) do
	for i, pidors in ipairs(workspace:GetDescendants()) do
		if pidors:FindFirstChild("Humanoid") then
			 if not pidors:FindFirstChild("EspBox") then
			 	if pidors ~= game.Players.LocalPlayer.Character then
					local esp = Instance.new("BoxHandleAdornment",pidors)
					esp.Adornee = pidors
					esp.ZIndex = 0
					esp.Size = Vector3.new(5, 5, 0)
					esp.Transparency = 0.65
					esp.Name = "EspBox"
					esp.AlwaysOnTop = true
					esp.Color3 = Color3.fromRGB(255,48,48)
				end
			end
		end
	end
end
