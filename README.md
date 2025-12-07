# skybox-script
just past into localscript or script
-----------------------links
https://www.roblox.com/users/10091797115/profile
https://www.youtube.com/@Qwerkid
WARNING: copy RAW file!!!!!!!!!!
-----------------------script:



local button = script.Parent

button.MouseButton1Click:Connect(function()
	local skyId = "http://www.roblox.com/asset/?id=your images HERE"
	local Lighting = game:GetService("Lighting")

	game.Lighting.TimeOfDay = "14:30:00"	

	for _, v in ipairs(Lighting:GetChildren()) do
		if v:IsA("Sky") then v:Destroy() end
	end
	local sky = Instance.new("Sky")
	for _, face in ipairs({"Bk", "Dn", "Ft", "Lf", "Rt", "Up"}) do
		sky["Skybox" .. face] = skyId
	end
	sky.Parent = Lighting
end)

