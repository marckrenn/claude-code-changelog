
   - Exception: the MSVC toolchain (`cl`, `nmake`, `msbuild`) is only on PATH inside a Visual Studio developer shell, so it may be installed even if not listed. Environment changes do NOT persist between commands, so initialize and build in ONE command: `cmd /c '"C:\Program Files\Microsoft Visual Studio\<year>\<edition>\VC\Auxiliary\Build\vcvarsall.bat" x64 && <build command>'`
