# Configuration

Open ```init.lua``` file and edit lines 12 and 13 with the name of your first and second monitor. You can get the name openning MacOS display settings.

```
12		local main_monitor = "Color LCD"
13		local second_monitor = "IPS236"
```

# Shortcuts

	cmd + alt + right key
	cmd + alt + left key
	cmd + alt + up key
	cmd + alt + down key
	ctrl + cmd + alt + right key
	ctrl + cmd + alt + left key
	ctrl + cmd + alt + up key
	ctrl + cmd + alt + down key
	cmd + alt + c
	ctrl + cmd + alt + c
	cmd + alt + f
	ctrl + cmd + alt + f

	ctrl + cmd + alt + r (reloads init.lua file)
	ctrl + cmd + alt + 1 (moves focused window to second_monitor)
	ctrl + cmd + alt + 2 (moves focused window to main_monitor)
	ctrl + cmd + alt + 3 (applies all layouts)
	ctrl + cmd + alt + 4 (applies only one layout (focused one))

	ctrl + cmd + alt + p (closes all applications defined by closeAll variable at line 120)
	ctrl + cmd + alt + o (open all applications defined by openAll variable at line 128)
 	ctrl + cmd + alt + h (hints for all opened windows, CapLetter to switch focus)

# Layouts:

You can configure the variable "layouts" (line 32) according your monitor configuration.

### The syntax is:

```
  {
    name = "App name" ou { "App name", "App name" }
    func = function(index, win)
      COMMANDS
    end
  },
```

### Example

```
  {
    name = {"Mail", "Calendar"},
    func = function(index, win)
      win:moveToScreen(hs.screen.get("Color LCD"))
      win:maximize()
    end
  },
```
