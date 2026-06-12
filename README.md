# calmlib
## this is a ui library, completely open source, feel free to do whatever you want with it, credits would be cool but you aren't required
p.s. its 'K' to toggle window

# Full example:
```lua
local CalmLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/IcantAffordSynapse/calmlib/refs/heads/main/src.lua"))()

local window = CalmLib:win("Any title here")

local section1 = window:tab("Tab 1", "rbxassetid://109121102062195") -- {name, icon}
local section2 = window:tab("Tab 2", "rbxassetid://128509752758345") -- {name, icon}

section1:label("this is a label")

section1:button("this is a button", function()
    print("and it works")
end)

section1:toggle("this is a toggle", false, function(bool) -- {name, default value, callback}
    print(bool)
end)

section2:textbox("this is a textbox", "", function(str) -- {name, default value, callback}
    print("and we said: " .. str)
end)

section2:slider("this is a slider", 1, 1000, 50, function(num) -- {name, min, max, default value, callback}
    print(num)
end)
```
