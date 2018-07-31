# fortnite-wine
## Collection of my wine patches for fortnite, including a fixed crash and anticheat work.

## psapi-fix:  
Fixes an issue where the game tries to call functions inside the physical dll, which is only supposed to work on older versions of the dll.


# Unreleased patches:

## Update:
These patches are complete, but the code quality is low so I am abstaining from releasing them right now

## register-callbacks-definition-fix:  
Currently the ObRegisterCallbacks function definition is incorrect in wine

## register-callbacks-implementation:  
A basic implementation of ObRegisterCallbacks which satisfies all the parameters that battleye uses.

## dispatcher object / KMUTEX / KEVENT implementation (KeWaitForSingleObject only):

Emulates windows dispatcher objects via thread wakeup events, which allows mutexes and events to work

# In-Progress patches

## PsSet(LoadImage/CreateThread)NotifyRoutine-implementation

notifies the driver in these cases, less complex than the ObRegisterCallbacks as the caller does not need to wait for a response

# Future patches

# RtlCreateUserProcess-implementation

Once battleye loads like it did in April, it will use this function to start the fortnite executable, however the process creation code is currently in kernel32, not ntdll, this patch will move code around to fix that.
