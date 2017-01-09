# Pico-8 Space Invaders

## Lesson 1

Type this code into the editor:

```lua
SPR(1, 64, 64)
```

Now press ESC to get to the console, and run the program

```
> RUN
```

![][screenshot1]

[screenshot1]: PICO-8_1.png "Screenshot 1"

```lua
function _draw()
  cls()
  foreach(stars, draw_sprite)
  draw_sprite(ship)
  foreach(aliens, draw_sprite)
  foreach(missiles, draw_sprite)
  draw_score()
end
```
```lua
FUNCTION _DRAW()
  CLS()
  FOREACH(STARS, DRAW_SPRITE)
  DRAW_SPRITE(SHIP)
  FOREACH(ALIENS, DRAW_SPRITE)
  FOREACH(MISSILES, DRAW_SPRITE)
  DRAW_SCORE()
END
```
```lua
function update_ship(s)
  if btn(0) then
    s.x = ship.x - 1
  end
  if btn(1) then
  	 s.x = ship.x + 1
  end
  if btn(2) then
    s.y = ship.y - 1
  end
  if btn(3) then
  	 s.y = s.y + 1
  end
end
```

```lua
FUNCTION UPDATE_SHIP(S)
  IF BTN(0) THEN
    S.X = SHIP.X - 1
  END
  IF BTN(1) THEN
  	 S.X = SHIP.X + 1
  END
  IF BTN(2) THEN
    S.Y = SHIP.Y - 1
  END
  IF BTN(3) THEN
  	 S.Y = S.Y + 1
  END
END
```