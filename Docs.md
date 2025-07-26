---raw link---
local lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/YoshiroScripts/MAITRE-UI-LIBRARY/refs/heads/main/SIMILAR-TO-ELERIUM.py"))()

---Adding A Tab---
local mainTab = win:AddTab("Main")

---Adding A Switch/Toggle
tab:AddSwitch("Switch Text", function(state)
    print("Switch is now", state)
end)

switch:Set(true) -- Programmatically set state
---Adding A Button---
tab:AddButton("Button Text", function()
    print("Button pressed!")
end)

---Adding A TextBox/Placeholder---
tab:AddTextBox("Placeholder", function(text)
    print("Input:", text)
end, {clear = true}) -- clears box after submit

---Adding A Slider---
tab:AddSlider("Slider Name", function(value)
    print("Slider value:", value)
end, {min = 0, max = 100, readonly = false})
slider:Set(50) -- Set slider position

---Adding A DropDown---
tab:AddDropdown("Dropdown Name", function(selected)
    print("Selected:", selected)
end)

---Adding A ColorPicker---
local colorPicker, colorPickerObject = tab:AddColorPicker(function(color)
    print("Color picked:", color)
end)
colorPicker:Set(Color3.fromRGB(255, 0, 0))

---Adding A KeyBind---
tab:AddKeybind("Keybind Name", function(key)
    print("Pressed:", key)
end, {standard = Enum.KeyCode.RightShift}) -- default key
keybind:SetKeybind(Enum.KeyCode.K)

---Adding A Folder---
local folder = tab:AddFolder("Settings")

Folders are like tabs, you can add controls inside:
