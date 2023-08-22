# Instructions
- Insert into qb-smallresource/clien/consumables.lua Line 50
  `
RegisterNetEvent('consumables:client:UseVest', function()
    -- if GetPedArmour(PlayerPedId()) == 100 then QBCore.Functions.Notify(Lang:t('consumables.armor_full'), 'error') return end
    local ped = PlayerPedId()
    local PlayerData = QBCore.Functions.GetPlayerData()   
    TriggerEvent('animations:client:EmoteCommandStart', {"adjusttie"})
    QBCore.Functions.Progressbar("use_vest", Lang:t('Attaching Traffic Vest...'), 5000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
        disableMouse = false,
        disableCombat = true,
    }, {}, {}, {}, function() -- Done
        if not Config.DisableVestDrawable then
            if PlayerData.charinfo.gender == 0 then
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 0)
                if GetPedDrawableVariation(ped, 9) == 7 then
                    SetPedComponentVariation(ped, 9, 19, GetPedTextureVariation(ped, 9), 10)
                else
                    SetPedComponentVariation(ped, 9, 10, 0, 0) -- Blue
                end
            else
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 0)
                SetPedComponentVariation(ped, 9, 30, 0, 2)
            end
        end
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items["vest1"], "remove")
        TriggerEvent('animations:client:EmoteCommandStart', {"c"})
        TriggerServerEvent("consumables:server:useVest")
        -- SetPedArmour(ped, 100)
    end)
end)

RegisterNetEvent('consumables:client:UseVest2', function()
    -- if GetPedArmour(PlayerPedId()) == 100 then QBCore.Functions.Notify(Lang:t('consumables.armor_full'), 'error') return end
    local ped = PlayerPedId()
    local PlayerData = QBCore.Functions.GetPlayerData()   
    TriggerEvent('animations:client:EmoteCommandStart', {"adjusttie"})
    QBCore.Functions.Progressbar("use_lspd_vest", Lang:t('Attaching LSPD Traffic Vest...'), 5000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
        disableMouse = false,
        disableCombat = true,
    }, {}, {}, {}, function() -- Done
        if not Config.DisableVestDrawable then
            if PlayerData.charinfo.gender == 0 then
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 1)
                if GetPedDrawableVariation(ped, 9) == 7 then
                    SetPedComponentVariation(ped, 9, 19, GetPedTextureVariation(ped, 9), 10)
                else
                    SetPedComponentVariation(ped, 9, 10, 1, 1) -- Blue
                end
            else
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 1)
                SetPedComponentVariation(ped, 9, 30, 1, 2)
            end
        end
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items["vest2"], "remove")
        TriggerEvent('animations:client:EmoteCommandStart', {"c"})
        TriggerServerEvent("consumables:server:useVest")
        -- SetPedArmour(ped, 100)
    end)
end)

RegisterNetEvent('consumables:client:UseVest3', function()
    -- if GetPedArmour(PlayerPedId()) == 100 then QBCore.Functions.Notify(Lang:t('consumables.armor_full'), 'error') return end
    local ped = PlayerPedId()
    local PlayerData = QBCore.Functions.GetPlayerData()   
    TriggerEvent('animations:client:EmoteCommandStart', {"adjusttie"})
    QBCore.Functions.Progressbar("use_sast_vest", Lang:t('Attaching SAST Traffic Vest...'), 5000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
        disableMouse = false,
        disableCombat = true,
    }, {}, {}, {}, function() -- Done
        if not Config.DisableVestDrawable then
            if PlayerData.charinfo.gender == 0 then
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 2)
                if GetPedDrawableVariation(ped, 9) == 7 then
                    SetPedComponentVariation(ped, 9, 19, GetPedTextureVariation(ped, 9), 10)
                else
                    SetPedComponentVariation(ped, 9, 10, 2, 2) -- Blue
                end
            else
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 2)
                SetPedComponentVariation(ped, 9, 30, 2, 2)
            end
        end
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items["vest3"], "remove")
        TriggerEvent('animations:client:EmoteCommandStart', {"c"})
        TriggerServerEvent("consumables:server:useVest")
        -- SetPedArmour(ped, 100)
    end)
end)

RegisterNetEvent('consumables:client:UseVest4', function()
    -- if GetPedArmour(PlayerPedId()) == 100 then QBCore.Functions.Notify(Lang:t('consumables.armor_full'), 'error') return end
    local ped = PlayerPedId()
    local PlayerData = QBCore.Functions.GetPlayerData()   
    TriggerEvent('animations:client:EmoteCommandStart', {"adjusttie"})
    QBCore.Functions.Progressbar("use_traffic_vest", Lang:t('Attaching Traffic Vest...'), 5000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
        disableMouse = false,
        disableCombat = true,
    }, {}, {}, {}, function() -- Done
        if not Config.DisableVestDrawable then
            if PlayerData.charinfo.gender == 0 then
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 3)
                if GetPedDrawableVariation(ped, 9) == 7 then
                    SetPedComponentVariation(ped, 9, 19, GetPedTextureVariation(ped, 9), 10)
                else
                    SetPedComponentVariation(ped, 9, 10, 3, 3) -- Blue
                end
            else
                currentVest = GetPedDrawableVariation(ped, 10)
                currentVestTexture = GetPedTextureVariation(ped, 3)
                SetPedComponentVariation(ped, 9, 30, 3, 2)
            end
        end
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items["vest4"], "remove")
        TriggerEvent('animations:client:EmoteCommandStart', {"c"})
        TriggerServerEvent("consumables:server:useVest")
        -- SetPedArmour(ped, 100)
    end)
end)
`
