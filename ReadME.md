# Frida HWID Manipulation

Frida HWID Manipulation is a  frida based HWID manipulation tool. Manipulates Win32 functions by hooking them.

### Hooked  win32 functions
- GetVolumeInformationW
- GetAdaptersInfo 
- GetCurrentHwProfileW
- RegGetValueW

### GetVolumeInformation
Retrieves the serial of all the partitions on the computer.

### GetAdaptersInfo
Retrieves the information of all adapters on the computer (Mac adress, Guid, name etc.)

### GetCurrentHwProfile
Retrieves the current user HW Profile Guid

### RegGetValue
Retrieves the any value from regedit. If the key is in the list below, it will be manipulated similarly to the structure of that key.
> - SusClientId => Guid
> - ProductId => 4x5 Key ( xxxxx-xxxxx-xxxxx-xxxxx ) 
> - InstallDate => timestamp
> - MachineGuid => Guid



### Usage
install frida-tools
> pip install frida-tools

 start cmd from project folder
> frida-trace <process_name> -O opt