# Faster-File-Copy

Decompressed files capture and delivery and memory mapping for Skyrim (SE/AE) and Fallout 4. Hooks the engine's file reads so decompressed payloads are captured once and served through memory-mapped I/O instead of repeated decompression.

> Fork of [1001Bits/Faster-File-Copy](https://github.com/1001Bits/Faster-File-Copy).

## Layout

| Path | Contents |
| --- | --- |
| `src/` | SKSE plugin source (`BSAMemoryMap`, decomp cache, hooks, mmap streams) |
| `Fallout4/` | Fallout 4 (F4SE) variant |
| `CMakeLists.txt`, `vcpkg.json` | CMake + vcpkg build (project name `BSAMemoryMap`) |

## Building

Requirements: Visual Studio 2022 (C++ workload), CMake 3.23+, vcpkg (`VCPKG_ROOT` set).

```powershell
cmake -S . -B build -DCMAKE_TOOLCHAIN_FILE="$env:VCPKG_ROOT/scripts/buildsystems/vcpkg.cmake"
cmake --build build --config Release
```

## License

No license file is present yet; all rights reserved by the respective authors until one is added.
