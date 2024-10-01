---
  layout: post
---

Updates 2024/04/29

I am a frequent user of WSL 2 (Windows Subsystem for Linux 2) on Windows. 

Recently I find out that my laptop has become very slow. The task manager shows that the Memory usage is 99%, and the process of Wmmem takes up to 50% RAM. The reason behind this is that WSL uses a lot of memory to store cached files.

An immediate solution is to terminate WSL 2 on the machine. To turn off Vmmem, simply go into Powershell or CMD or whatever terminal you like to use under admin rights, enter the command `wsl --shutdown`. This will terminate WSL. Then, you can always restart a WSL terminal.

A long term solution is to set a limit on the RAM of WSL 2. To do this, go into Powershell under admin rights (e.g. right click on the Powershell icon and choose 'Run as an Admin'), then input ```notepad "$env:USERPROFILE/.wslconfig"```. If you are told that such file doesn't exist, just click 'Creating a new file'. In this notepad UI, set the values you want for CPU core and memory of WSL:

```
# Settings apply across all Linux distros running on WSL 2
[wsl2]

# Limits VM memory to use no more than 4 GB, this can be set as whole numbers using GB or MB
memory=4GB

[experimental]
autoMemoryReclaim=gradual
```

Then it is done! Try it if you are using WSL.

# Reference

1. https://github.com/microsoft/WSL/issues/4166
2. https://superuser.com/questions/1559170/how-can-i-reduce-the-consumption-of-the-vmmem-process

