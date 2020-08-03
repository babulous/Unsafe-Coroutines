## Installation

Just drop it in and require!

## Usage

This library mirrors the functionality of Lua's coroutine library.

```lua
local ucoroutine = require 'ucoroutine'

local cr = ucoroutine.create(function()
  print("hello")
  coroutine.yield()
  print("goodbye")
end)
ucoroutine.resume(cr)
ucoroutine.resume(cr)
```

## Error Messages

```
Error: main.lua:22: attempt to perform arithmetic on a nil value
stack traceback:
  main.lua:8: in function 'troll'
  main.lua:16: in coroutine <main.lua:15>
  main.lua:11: in function 'do_the_thing'
  main.lua:18: in coroutine <main.lua:14>
  main.lua:20: in coroutine <main.lua:13>
  main.lua:22: in function 'load'
  [string "boot.lua"]:586: in function <[string "boot.lua"]:585>
  [C]: in function 'xpcall'
  [string "boot.lua"]:793: in function <[string "boot.lua"]:780>
  [C]: in function 'xpcall'
```

## Documentation


```lua 
cr = ucoroutine.create(f)
```

Returns a coroutine with error handling capabilities.

```lua
results... = ucoroutine.resume(cr, ...)
```

Resume a coroutine "unsafely," meaning it will automatically error if any problems occur.

```lua
f = ucoroutine.wrap(f)
```

Wraps a coroutine in a closure so it can be called like any normal function.
