# XP3

XP3 is a set of code built primarily to run on Crestron 3-Series and 4-Series processors using Simpl#. The major components of it will also run on .NET Standard on any supported platform. It was built to be used in place of traditional crosspoints, but work across different programs and processors, and allow new advanced features.

## Discovery
XP3 uses multicast to discover all avaliable crosspoints on the network automatically. The multicast address used is 239.64.0.1

## Console
To use the console, add the `ICDConsole SPlus Handler` module, and feed the output of the `User Program Commands` symbol into the module. While running, the cosole can be accessed by typing `ucmd "icd ?"` into the processor's console.

## SystemId
All modules have a "SystemId" parameter. Different SystemIds won't interact with each other at all. If using independent systems all on the same network (multicast domain), use different SystemIds to prevent the crosspoints from unintentianl interactions.