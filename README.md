# VenyxUI
Reupload of the Venyx UI Library for Roblox

Plus Documentation!!!! (im wasting my time)

## Booting The Library
```lua
local library = loadstring(game:Httpget("https://raw.githubusercontent.com/Stratxgy/VenyxUI/refs/heads/main/Venyx.lua"))()
local venyx = library.new("Venyx", 5013109572)
```
## Theme (This is the default)
```lua
-- themes
local themes = {
Background = Color3.fromRGB(24, 24, 24),
Glow = Color3.fromRGB(0, 0, 0),
Accent = Color3.fromRGB(10, 10, 10),
LightContrast = Color3.fromRGB(20, 20, 20),
DarkContrast = Color3.fromRGB(14, 14, 14),  
TextColor = Color3.fromRGB(255, 255, 255)
}
```

## Does something, just put it at the end
```lua
venyx:SelectPage(venyx.pages[1], true)
```

## Create a Page (Tab)
```lua
local page = venyx:addPage("Test", 5012544693)
```

## Create a Section
```lua
-- If you want another just add the next number at local section(num here)
-- Here's an example of 2
local section1 = page:addSection("Section 1")
local section2 = page:addSection("Section 2")
```

## Create a Toggle 
```lua
section1:addToggle("Toggle", nil, function(value)
print("This is what the toggle executes!")
end)
```

## Create a Button 
```lua
section1:addButton("Button", function()
print("This is what the button executes!")
end)
```

## Make a second page
```lua
local theme = venyx:addPage("Theme", 5012544693)
local colors = theme:addSection("Colors")

for theme, color in pairs(themes) do -- all in one theme changer
colors:addColorPicker(theme, color, function(color3)
venyx:setTheme(theme, color3)
end)
end
```

## Create a Textbox (who uses this?)
```lua
section1:addTextbox("Notification", "Default", function(value, focusLost)
print("Input", value)
```

## Notify the User
```lua
venyx:Notify("Example")
end
end)
```

## Create a Keybind
```lua
section1:addKeybind("Toggle Keybind", Enum.KeyCode.One, function()
print("This is where what happens when its activated - Usually leave it with print keybind activated")
venyx:toggle()
end, function()
print("This is where what happens when its completed -- put something you want to change the keybind of")
end)
```

## Add a Color Picker
```lua
section1:addColorPicker("ColorPicker", Color3.fromRGB(50, 50, 50))
```

## Add a Color Picker
```lua
section1:addSlider("Slider", 0, -100, 100, function(value)
print("Dragged, now im gonna print the value", value)
end)
```
