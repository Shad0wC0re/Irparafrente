local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Função para fazer o personagem andar para frente continuamente
local function moveForward()
    while true do
        humanoid:Move(Vector3.new(0, 0, -1), true) -- Move o personagem para frente
        wait(0.1) -- Pequena espera para evitar sobrecarga no script
    end
end

-- Chama a função para começar a andar
moveForward()
