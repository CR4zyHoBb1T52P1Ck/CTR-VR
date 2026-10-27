# Build the CTR VR v0.2.2 source package

Extract the complete `ctr-vr-v0.2.2-source.zip` to a new short writable path.
The source root contains `Build-Source.ps1`, `SOURCE-REVISION.json`, `vr-mod/`
and the already patched `turbocharged/` tree. Do not apply launcher.patch again.
The pinned OpenVR headers/library/DLL and vendored SDL sources are included.
Retail disc data is not needed for building or CPU tests.

Prerequisites: Windows, Visual Studio 2022 or 2026 with the Desktop C++ workload,
Windows SDK, CMake 3.20+, and the .NET Framework C# compiler. A Python 3 runtime
is needed only for the additional offline tooling tests. Git/network access is
not needed for this extracted-source build.

From PowerShell in the extracted source root:

```powershell
.\Build-Source.ps1 -Generator 'Visual Studio 18 2026'
# Or use 'Visual Studio 17 2022' with that installed toolchain.
```

The script configures a Win32 Release build and runs native CPU tests, then
builds/tests the launcher. It does not launch a VR session or edit GPU settings.
Outputs: `build/Release/CTR-VR.exe` and
`vr-mod/.work/launcher-build/CTR VR Launcher.exe`. These are build outputs, not a
staged installation. Runtime inputs/defaults/licenses must be packaged together;
do not copy only an executable into a known working installation.

For launcher-only verification from the source root:

```powershell
.\vr-mod\scripts\Build-DesktopLauncher.ps1 -UiOnly
```

The source archive's reviewed changelog and SOURCE-REVISION.json supply the
launcher snapshot without a `.git` directory. In a regular Git checkout, the
reviewed release changelog is used with the checkout's snapshot revision. Missing/mismatched source snapshot metadata refuses
the source launcher build rather than silently reporting another revision.

Native source builds may have different hashes because build paths/toolchains
and generated upstream Git/time banners differ. Matching source is supplied;
byte-for-byte reproducibility is not claimed. The public Windows ZIP retains
the explicitly pinned game executable in `vr-mod/release/Release.json`.
