# Lua
## Properties

### private:
##### lua_State \* L
the current state of the lua virtual machine.

##### [[Pcall(int args, int rets)]] :
calls a Lua function and throws an [[Exception]] if an error occours.

### public:

##### std::map<std::string, int (\*)(lua_State \* L) functs
pointers to all c functions that have been added to this Lua virtual machine.

##### [[TableValue]] :
A struct that can represent a lua variable.

##### [[Table]] :
A type definition of  a map using string [[TableValue]] pairs.

##### [[LuaTableBuilder]] :
a class that can be used to build lua tables that can be sent to the lua virtual machine.

##### [[static Table lua_gettable(lua_State pointer L)|static Table lua_gettable(lua_State \* L)]] :
returns the table stored on the first position of the lua stack.

##### [[ClassTable]] :
a parent class that provides virtual functions to convert a classes functions and properties to and from a [[Table]].

##### [[PrintTable(lua_State pointer L)|PrintTable(lua_State \* L)]] :
Prints the table stored on the first position of the lua stack to the console.

##### [[lua_pushtable(lua_State pointer LUA, Table val)|lua_pushtable(lua_State \* LUA, Table val)]] :
pushes a [[Table]] onto the lua stack.