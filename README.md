## Installation

Just drop it in and require!

## Usage

This library mirrors the functionality of Lua's coroutine library.

```lua
local ucoroutine = require 'ucoroutine'

local cr = ucoroutine.create(function()
  print("hello")
end)
ucoroutine.resume(cr)
```

## Error Messages



## Documentation


```lua 
cr = ucoroutine.create(f)
```
```lua
f = ucoroutine.wrap(f)
```
```lua
results... = ucoroutine.resume(cr, ...)
```
