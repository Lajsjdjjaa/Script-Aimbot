local aimbot = false
local aimFov = 90 -- Valor padrão de FOV
local espLine = false
local espSkeleton = false
local espLife = false

-- Função para ativar/desativar o Aimbot
function toggleAimbot()
    aimbot = not aimbot
    print("Aimbot ativado: " .. tostring(aimbot))
end

-- Função para alterar o FOV do Aimbot
function setAimFov(fov)
    if fov >= 1 and fov <= 360 then
        aimFov = fov
        print("FOV do Aimbot definido para: " .. tostring(aimFov))
    else
        print("Valor de FOV inválido. O valor deve estar entre 1 e 360.")
    end
end

-- Função para ativar/desativar o ESP Line
function toggleEspLine()
    espLine = not espLine
    print("ESP Line ativado: " .. tostring(espLine))
end

-- Função para ativar/desativar o ESP Skeleton
function toggleEspSkeleton()
    espSkeleton = not espSkeleton
    print("ESP Skeleton ativado: " .. tostring(espSkeleton))
end

-- Função para ativar/desativar o ESP Life
function toggleEspLife()
    espLife = not espLife
    print("ESP Life ativado: " .. tostring(espLife))
end

-- Menu de opções
print("Interface de Script para Roblox")
print("Escolha uma opção:")
print("1 - Ativar/Desativar Aimbot")
print("2 - Definir FOV do Aimbot (de 1 a 360)")
print("3 - Ativar/Desativar ESP Line")
print("4 - Ativar/Desativar ESP Skeleton")
print("5 - Ativar/Desativar ESP Life")

-- Loop principal
while true do
    local option = tonumber(read())
    
    if option == 1 then
        toggleAimbot()
    elseif option == 2 then
        print("Informe o valor do FOV:")
        local fov = tonumber(read())
        setAimFov(fov)
    elseif option == 3 then
        toggleEspLine()
    elseif option == 4 then
        toggleEspSkeleton()
    elseif option == 5 then
        toggleEspLife()
    else
        print("Opção inválida. Escolha novamente.")
    end
    
    print("\nEscolha uma opção:")
    print("1 - Ativar/Desativar Aimbot")
    print("2 - Definir FOV do Aimbot (de 1 a 360)")
    print("3 - Ativar/Desativar ESP Line")
    print("4 - Ativar/Desativar ESP Skeleton")
    print("5 - Ativar/Desativar ESP Life")
end
