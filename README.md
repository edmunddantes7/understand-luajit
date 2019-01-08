# understand-luajit
Well to some extent


## Stack
In a python JIT like pypy, there'll be a common value holder union like python_value, but lua JIT does 
not have such a value, they fear that if they start to use C unions for holding any kind of value that lua
can take which being a dynamic language will take even a kitchen sink, they'll not be able to collect garbage
using lua garbage collector as it will not know what kind of value does that c variable hold, and may even
think of an important value as garbage and collect and remove it!
<br/>
have a link: https://www.lua.org/pil/24.2.html
