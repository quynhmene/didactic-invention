-- Hàm để tải và chạy script từ URL
local function loadAndRunScript(url)
    print("LOADING SCRIPT FROM: " .. url)
    local success, result = pcall(function()
        return loadstring(game:HttpGet(url))()
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

-- Danh sách các trò chơi và script tương ứng
local gameScripts = {
    [914010731] = "_RoGhoul",
    [537413528] = "_BuildBoatForTreasure",
    [13808990310] = "_TLS",
    [3237168] = "_OPL"
}

-- Lấy PlaceId của trò chơi
local myPlaceId = game.PlaceId

-- Kiểm tra nếu trò chơi được hỗ trợ
local scriptName = gameScripts[myPlaceId]
if scriptName then
    -- Thay đổi URL script của bạn ở đây
    local yourScriptURL = "URL_MỚI_CỦA_BẠN"
    
    -- Hiển thị thông báo
    game.StarterGui:SetCore("SendNotification", {
        Title = "Note",
        Text = "WAIT FEW SECONDS TO LOAD",
        Icon = "rbxassetid://2541869220",
        Duration = 10
    })
    wait(1) -- Chờ một lát trước khi tải script
    -- Tải và chạy script của bạn
    loadAndRunScript(yourScriptURL)
else
    -- Nếu trò chơi không được hỗ trợ
    game.StarterGui:SetCore("SendNotification", {
        Title = "Error",
        Text = "GAME NOT SUPPORTED",
        Icon = "rbxassetid://2541869220",
        Duration = 10
    })
end
