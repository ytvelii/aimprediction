- // INFORMACION:
-- silent aim que "predice" el movimiento del jugador
-- aimlock que manipula la camara asi apuntas al jugador
-- solo funciona en synapse X o sirhurt (posiblemente krnl pero no probe)
-- presiona la tecla1 para lockear a alguien
-- presiona la tecla2 para deslockear a alguien
-- presiona la tecla3 para desactivar/activar el lock
-- // CREDITOS:
-- hecho por cute_misael en roblox/mariee#1051 (550687407020965888) en discord
-- gracias a 2a60/Horbyss por la idea
-- // CREDITOS ADICIONALES: 
-- doxxeados_asesinos (mininos asesinos)
-- 4PEDOFILO (4drizzy)
-- 26Skid (tfw cuando alguien que no muchos conocen hace audios mas fuertes que los tuyos y le decis que usa metodos de otras personas y usas metodos de otros kek)
-- Skidable19 (tfw cuando intentas cookie loggear)
-- por ultimo gracias a pedos on top (best on top) y R (lleno de virgos)
-- // NOTAS:
-- fuck UserInputService all my homies use GetMouse
-- esta Open Source si al menos lo usas dame creditos peteeee
]]

-- // servicios
local DAHOODPLAYERS = game:GetService("Players")
local thisaudiowasmadebytueniSEXdrip = game:GetService("StarterGui")
local FIVE_NIGHTS_AT_FREDDYS_IS_GOING_TO_BE_REAL_IN_60_SECONDS = game:GetService("RunService")

-- // objetos
local THISAUDIOWASMADEBYDRIZZY = DAHOODPLAYERS.LocalPlayer
local mordida_del_87 = THISAUDIOWASMADEBYDRIZZY:GetMouse()
local camara_de_la_porno = workspace:FindFirstChildOfClass("Camera") -- por si los devs de da hood intentan parchearlo cambiando el nombre de la camara :]

-- // variables
local TECLAS_PARA_BUSCAR_PORNOGRAFIA = techware_aimlock.teclas
local doxxeados_asesinos = getrawmetatable(game)
local dahood = doxxeados_asesinos.__namecall
local drizzy_groomer = {
  ["activado"] = true,
  ["victima_de_grooming"] = nil,
}

-- // evita ejecutar el script si ya se ejecuto antes o el juego no es da hood
if not techware_aimlock["configuracion general"]["sos down"] then 
	thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
	    Title="[Reverb X]",
	    Text = "the script refuses to execute because you have the value of \ "sos down \" in false"
	})
    return
end 

if game.PlaceId ~= 2788229376 or TECHWARESILENTAIM_LOADED then
	thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
	    Title="[Reverb X]",
	    Text = "THE GAME IS NOT DA HOOD / THE SCRIPT WAS ALREADY RUNNING BEFORE"
	})
    return
end

if techware_aimlock["configuracion general"]["modo metametodos"] and techware_aimlock["configuracion general"]["modo manipulacion de camara"] then
    thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
	    Title="[Reverb X]",
	    Text = "you have both methods activated silly \ navigate only one and run again."
	})
    return
end

getgenv().TECHWARESILENTAIM_LOADED = true

-- // creditos (si de verdad eliminas/editas esto para poner tus creditos, sos la persona mas triste del mundo)
if techware_aimlock["configuracion general"]["modo metametodos"] then
	thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
		Title="[Reverb X]",
		Text = "AIMLOCK ON \ MODE: METATABLES POSITION SPOOFING \ MADE BY VELII"
	})
elseif techware_aimlock["configuracion general"]["modo manipulacion de camara"] then 
	thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
		Title="[Reverb X]",
		Text = "AIMLOCK ON \ MODE: CAMERA HANDLING \ MADE BY VELII"
	})
end 

wait(1.5)

thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
    Title="[Reverb X]",
    Text = "PRESS THE KEY "..TECLAS_PARA_BUSCAR_PORNOGRAFIA.tecla3 .." TO ACTIVATE AIMLOCK"
})
thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
    Title="[Reverb X]",
    Text = "PRESS THE KEY ".. KEYS_FIND_PORNOGRAPHY.key2 .." TO LOCK"
})
thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
    Title="[Reverb X]",
    Text = "PRESS THE KEY ".. KEYS_BOOK_PORNOGRAPHY.key1 .." TO LOCK SOMEONE \ n (put the mouse over the person you want to lock)"
})

-- // funciones utiles
function esautista(minino_asesino)
    if DAHOODPLAYERS:GetPlayerFromCharacter(minino_asesino) then
        return true
    else
        return false
    end
end

function matar_y_violar_su_cuerpo_putrefacto_como_haria_kiIIuli(victima)
    return DAHOODPLAYERS:GetPlayerFromCharacter(victima)
end

function groomear(pedofilo,victima,genitales,esmujer,esmenor)
	if pedofilo == "Drizzy" and victima and esmujer and esmenor then
        if techware_aimlock["configuracion general"].predice_movimientos then
            return victima.Character[genitales].Position + victima.Character.UpperTorso.Velocity * techware_aimlock["configuracion general"].pornografia
        else
            return victima.Character[genitales].Position
        end
    end
end

function espedofilo(jugadorDeDH,fdmg)
	if jugadorDeDH == "Drizzy" then
		if tostring(fdmg) == "MainEvent" then
			return true
		end
	end
end

function suicidio(mongolico)
	local feo = mongolico.Character
    feo.Humanoid.Died:Connect(function()
		drizzy_groomer.activado = false
        THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic
        thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
            Title="[Reverb X]",
            Text = "you've died, the aimlock was deactivated."
        })
    end)
    feo.BodyEffects["K.O"].Changed:Connect(function()
        if feo.BodyEffects["K.O"].Value == true then
            drizzy_groomer.activado = false
            THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic
            thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
                Title="[Reverb X]",
                Text = "You have been shot, the aimlock was deactivated."
            })
        end
    end)
end

function muerte(mongolico)
    local feo = mongolico.Character
	if feo:FindFirstChild("BodyEffects") and feo.BodyEffects:FindFirstChild("K.O") then
		hong_kong = feo.BodyEffects["K.O"].Changed:Connect(function()
			if feo.BodyEffects["K.O"].Value == true and drizzy_pedofilo["victima_de_grooming"] == mongolico then
				drizzy_groomer.activado = false
				drizzy_groomer.victima_de_grooming = nil
				THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic
				thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
					Title="[Reverb X]",
					Text = "They threw the one you had locked, the aimlock was deactivated."
				})
			end
			hong_kong:Disconnect() -- no queremos lag en el cliente
		end)
	end
	china = feo.Humanoid.Died:Connect(function()
		if drizzy_pedofilo["victima_de_grooming"] == mongolico then
			drizzy_groomer.activado = false
			drizzy_groomer.victima_de_grooming = nil
			THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic
			thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
				Title="[Reverb X]",
				Text = "Locked player died player unlocked."
			})
		end
		china:Disconnect() -- no queremos lag en el cliente
	end)
end

function ir_a_hong_kong(ubicacion_geografica)
	-- esto antes era un Tween, pero decidi cambiarlo a esto de abajo
	-- ya que habian muchos bugs con eso
	-- :]
    camara_de_la_porno.CoordinateFrame = ubicacion_geografica
end

-- // desactivar el aimlock al morir
suicidio(THISAUDIOWASMADEBYDRIZZY)

THISAUDIOWASMADEBYDRIZZY.CharacterAdded:Connect(function(asjfkg)
	repeat wait() until asjfkg:FindFirstChild("Humanoid")
	repeat wait() until asjfkg:FindFirstChild("BodyEffects")
	wait(0.2)
    suicidio(THISAUDIOWASMADEBYDRIZZY)
end)

-- // por si el maricon que estabas lockeando se va
DAHOODPLAYERS.PlayerRemoving:Connect(function(pelotudo)
    if pelotudo == drizzy_groomer["victima_de_grooming"] then
        drizzy_groomer["victima_de_grooming"] = nil
        drizzy_groomer.activado = false
        thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
            Title="[Reverb X]",
            Text = "Created By Velii"
        })
    end
end)

-- // conexion
mordida_del_87.KeyDown:Connect(function(AMONGUS)
    if AMONGUS:lower() == TECLAS_PARA_BUSCAR_PORNOGRAFIA.tecla1:lower() then
        local genital = mordida_del_87.Target
        if genital then
            local victima_de_grooming = genital.Parent
            if victima_de_grooming:IsA("Accessory") then
                victima_de_grooming = victima_de_grooming.Parent
            elseif victima_de_grooming.Name == "SpecialParts" then
                victima_de_grooming = victima_de_grooming.Parent.Parent
            end
            if victima_de_grooming:FindFirstChild("Humanoid") and esautista(victima_de_grooming) then
                drizzy_groomer.victima_de_grooming = matar_y_violar_su_cuerpo_putrefacto_como_haria_kiIIuli(victima_de_grooming)
                thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
                    Title = "[Reverb X]",
                    Text = "aimlock activated on: "..victima_de_grooming.Name
                })
                if victima_de_grooming:FindFirstChild("BodyEffects") and victima_de_grooming.BodyEffects:FindFirstChild("K.O") then 
					if victima_de_grooming.BodyEffects["K.O"].Value == false then
						muerte(matar_y_violar_su_cuerpo_putrefacto_como_haria_kiIIuli(victima_de_grooming))
					end
                end
           end
        end
    elseif AMONGUS:lower() == TECLAS_PARA_BUSCAR_PORNOGRAFIA.tecla2:lower() then
        if drizzy_groomer.victima_de_grooming then
            local anterior_victima = drizzy_groomer.victima_de_grooming
            drizzy_groomer.victima_de_grooming = nil
            thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
                Title = "[Reverb X]",
                Text = "aimlock disabled on: "..anterior_victima.Name
            })
	    wait(0.3)
	    THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic 
        end
    elseif AMONGUS:lower() == TECLAS_PARA_BUSCAR_PORNOGRAFIA.tecla3:lower() then
        if drizzy_groomer.activado == true then
            drizzy_groomer.activado = false
            thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
                Title = "[Reverb X]",
                Text = "aimlock activity (false)"
            })
            wait(0.3)
            THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.Classic 
        else
            drizzy_groomer.activado = true
            thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
                Title = "[Reverb X]",
                Text = "aimlock activity (true)"
            })
        end
    end
end)

if techware_aimlock["configuracion general"]["modo metametodos"] then
    -- // momento metamethods
    setreadonly(doxxeados_asesinos,false)
    doxxeados_asesinos.__namecall = newcclosure(function(self,...) 
        local metodos_de_audios_de_dripin = {...}
        local creacion_de_audios_loud = getnamecallmethod()
        if creacion_de_audios_loud == "FireServer" and espedofilo("Drizzy",self) and metodos_de_audios_de_dripin[1] == "UpdateMousePos" and drizzy_groomer.activado and drizzy_groomer["victima_de_grooming"] then 
            metodos_de_audios_de_dripin[2] = groomear("Drizzy",drizzy_groomer["victima_de_grooming"],techware_aimlock["configuracion general"].lockear_a or "Head",true,true)
        end
        return dahood(self,unpack(metodos_de_audios_de_dripin))
    end)
    setreadonly(doxxeados_asesinos,true)
elseif techware_aimlock["configuracion general"]["modo manipulacion de camara"] then
	-- // BindToRenderStep es mas rapido que usar solo RenderStepped
FIVE_NIGHTS_AT_FREDDYS_IS_GOING_TO_BE_REAL_IN_60_SECONDS:BindToRenderStep("HONG KONG",Enum.RenderPriority.First.Value,function()
	local nombre_del_genital = techware_aimlock["configuracion general"].lockear_a
        if drizzy_groomer.activado and drizzy_groomer["victima_de_grooming"] then
		-- esta mierda se ve asi ya que queria que se vea mas organizado :]
            	THISAUDIOWASMADEBYDRIZZY.CameraMode = Enum.CameraMode.LockFirstPerson
            	ir_a_hong_kong(
			CFrame.new(
				camara_de_la_porno.CoordinateFrame.p, 
				CFrame.new(drizzy_groomer["victima_de_grooming"].Character[nombre_del_genital].Position - Vector3.new(0,techware_aimlock["configuracion general"].Y,0)).p 
			)
		)
        end
end)
else
    thisaudiowasmadebytueniSEXdrip:SetCore("SendNotification",{
        Title="[Reverb X]",
        Text = "Press E aiming at someone"
    })
    return
end
