# Survival
New Game in Development
.
init = function()
  player_x = 0
  player_y = 0
  cooldown = 0
  boost = 10
  
end

update = function()

  speed = 2


  // Normal movement
  if keyboard.D then player_x += speed end
  if keyboard.A then player_x -= speed end
  if keyboard.W then player_y += speed end
  if keyboard.S then player_y -= speed end

if keyboard.A and keyboard.SPACE then
  player_x -= boost
  end
  
  if keyboard.D and keyboard.SPACE then
    player_x += boost
  end
  
  if keyboard.W and keyboard.SPACE then
  player_y += boost
  end
  
  if keyboard.S and keyboard.SPACE then
  player_y -= boost
  end
  
  
end


draw = function()
  screen.clear()
 
  
   screen.fillRect(0,0,screen.width,screen.height,"rgb(92,147,65)")
   screen.drawSprite("entity",player_x,player_y,40,40)
   screen.drawSprite("sun",70,70,80,80)
end
