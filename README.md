--
local function loadAndRunScript(https://github.com/quynhmene/didactic-invention/blob/main/README.md)
    print("LOADING SCRIPT FROM: " .. https://github.com/quynhmene/didactic-invention/blob/main/README.md)
    local success, result = pcall(function()
        return loadstring(game:HttpGet(https://github.com/quynhmene/didactic-invention/blob/main/README.md))()
    end)
    if not success then
        print("ERROR LOADING SCRIPT: " .. result)
        game.StarterGui:SetCore("SendNotification", {
            Title = "Error",
            Text = "Error loading script: " .. result,
            Icon = "rbxassetid://2541869220",
            Duration = 10
        })
    end
end


local gameScripts = {
    [914010731] = "_RoGhoul",
    [537413528] = "_BuildBoatForTreasure",
    [13808990310] = "_TLS",
    [3237168] = "_OPL"
}


local myPlaceId = game.PlaceId


local scriptName = gameScripts[myPlaceId]
if scriptName then

    local yourScriptURL = "https://github.com/quynhmene/didactic-invention/blob/main/README.md"
  )
else
    
    game.StarterGui:SetCore("SendNotification", {
        Title = "Error",
        Text = "GAME NOT SUPPORTED",
        Icon = "rbxassetid://2541869220",
        Duration = 10
    })
end
