## binPatchAMD

Kernel binary patches to support AMD CPU on macOS

### Supported AMD CPUs

| Family | Codename  | Example                           |
| ------ | --------- | --------------------------------- |
| 15h    | Bulldozer | FX Series                         |
| 16h    | Jaguar    | A Series (including AM4 A-Series) |
| 17h    | Zen       | Ryzen, Threadripper, Athlon 2xxGE |

### Supported macOS

- High Sierra (10.13.x)
- Mojave (10.14.x)
- Catalina (10.15.x)

### Supported bootloaders

- [Opencore](https://github.com/acidanthera/OpenCorePkg) (Recommended)
- [Clover](https://github.com/CloverHackyColor/CloverBootloader)

### Notes

- Patches for beta macOS versions can be found [here](https://github.com/naveenkrdy/binPatchAMD/tree/beta)

- Due to lack of required x86 instruction sets (SYSENTER / SYSEXIT) on AMD processors there is no 32-bit support and since macos Catalina (10.15.x), apple has anyway moved away from 32 bit completely. But if anyone still intrested in implementing 32-bit Opcode emulator through a kext for AMD on prior macOS versions, they can look [here](https://www.insanelymac.com/forum/topic/337075-new-opemu-supporting-fully-till-sse41/) and [here](https://www.insanelymac.com/forum/topic/329704-opcode-emulator-opemu-plug-in-project/).

- Apple Hypervisor framework of macOS doesn't support AMD CPU, so any app that likely needs it will not work (eg. VMware Fusion, Parallels Desktop, Docker for mac). As an alternative use virtualbox.

### Credits

- [Apple](https://opensource.apple.com/) for opensource xnu
- [AlGrey](https://github.com/AlGreyy) for idea and creating the patches.
- [naveenkrdy](https://github.com/XLNCs) for maintaining patches to various macOS versions.
- Sinetek, Andy Vandijck, spakk, Bronya, Tora Chi Yo, Shaneee and many others for sharing their AMD/XNU kernel knowledge.