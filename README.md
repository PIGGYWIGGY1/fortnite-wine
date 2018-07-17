# fortnite-wine
## Collection of my wine patches for fortnite, including a fixed crash and anticheat work.

## psapi-fix:  
Fixes an issue where the game tries to call functions inside the physical dll, which is only supposed to work on older versions of the dll.


# Upcoming Patches (soon):

## register-callbacks-definition-fix:  
Currently the ObRegisterCallbacks function definition is incorrect in wine

## register-callbacks-implementation:  
A basic implementation of ObRegisterCallbacks which satisfies all the parameters that battleye uses.


After I finish these two patches, I will implement mutexes and maybe events in ntoskrnl.
