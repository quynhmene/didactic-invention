--
local function loadAndRunScript(url)
    print("LOADING SCRIPT FROM: " .. url)
    local success, result = pcall(function()
        return loadstring(game:HttpGet())()
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

-- Kiểm tra nếu trò chơi được hỗ trợ
local scriptName = gameScripts[myPlaceId]
if scriptName then
    -- Thay đổi URL script của bạn ở đây
    local yourScriptURL = "URL_MỚI_CỦA_BẠN"
  )
else
    -- Nếu trò chơi không được hỗ trợ
    game.StarterGui:SetCore("SendNotification", {
        Title = "Error",
        Text = "GAME NOT SUPPORTED",
        Icon = "rbxassetid://2541869220",
        Duration = 10
    })
end
