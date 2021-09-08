# Lua
## Properties

### private:
##### lua_State * L

##### [[Pcall(int args, int rets)]] :
calls a Lua function and throws an [[Exception]] if an error occours.

### public:
##### [[Exception(string exString)]] :
returns an exception object that can be thrown by your program.
the exString argument sets the return for the [[What()]] function.

##### [[What()]] :
Returns a constant char pointer that describes what exception has occoured.