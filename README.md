# SideServer for Windows

In order to compile SideServer on VS 2019/2022, follow these steps

**Dev Environment**
You need all of the below to build SideServer
- `Desktop development with C++` set of tools in VS Installer
- `MSBuild support for LLVM (clang-cl) toolset` in VS Installer
- `Test Adapter for Boost.Test` in VS Installer
- Bootstrapped and Integrated  [VCPKG](https://github.com/microsoft/vcpkg) package manager setup.
- Installer projects plugin that matches your VS version - [VS2017/2019](https://marketplace.visualstudio.com/items?itemName=VisualStudioClient.MicrosoftVisualStudio2017InstallerProjects), [VS2022](https://marketplace.visualstudio.com/items?itemName=VisualStudioClient.MicrosoftVisualStudio2022InstallerProjects).

**Build Instructions**
1. clone the repository **recursively** (or run `git submodule update --init --recursive` after pull).
2. In the `Dependencies\libimobiledevice-vs` folder, run the `./get-source` script to download the source repos
3. If using VS2022, in the `AltServer` and `AltSign` projects, change the MSVC toolset to `v143`.
4. Compile (x86 only - the project won't work in x64).

### To Do

- [x] Add pairing file support (commented out, some module error)
- [x] Rebrand AltServer to SideServer
- [ ] Add release channels and correct IPA links
- [ ] Testing with users
