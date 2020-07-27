function Blow(Hit)
    if not Hit or not Hit.Parent or not CheckIfAlive() or not ToolEquipped then
        return
    end
    local RightArm = Character:FindFirstChild("Right Arm") or Character:FindFirstChild("RightHand")
    if not RightArm then
        return
    end
    local RightGrip = RightArm:FindFirstChild("RightGrip")
    if not RightGrip or (RightGrip.Part0 ~= Handle and RightGrip.Part1 ~= Handle) then
        return
    end
    local character = Hit.Parent
    if character == Character then
        return
    end
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    if not humanoid or humanoid.Health == 0 then
        return
    end
    local player = Players:GetPlayerFromCharacter(character)
    if player and (player == Player or IsTeamMate(Player, player)) then
        return
    end
    UntagHumanoid(humanoid)
    TagHumanoid(humanoid, Player)
        if humanoid.Name ~= "Humanoid" then
    humanoid:TakeDamage(Damage)
        end    
end
