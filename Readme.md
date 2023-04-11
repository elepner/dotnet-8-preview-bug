# How to reproduce the bug

1. Publish the project in release mode ``dotnet publish -o ./output``
1. Navigate to the output folder ``cd ./output/wwwroot``
1. Serve static content using some static server e.g. [http-server](https://www.npmjs.com/package/http-server) ``http-sever``
1. Go to http://localhost:8080 and open the browser console ![screenshot](screenshot.png)
Stacktrace from the error:
```
Error: [MONO] * Assertion at /__w/1/s/src/mono/mono/mini/aot-runtime.c:2443, condition `<disabled>' not met

    at se (:8080/_framework/dotnet.8.0.0-preview.2.23128.3.eix09tz9ug.js:3:14137)
    at ie (:8080/_framework/dotnet.8.0.0-preview.2.23128.3.eix09tz9ug.js:3:14427)
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
    at wasm://wasm/022a4626
ie @ dotnet.8.0.0-preview.2.23128.3.eix09tz9ug.js:3
blazor.webassembly.js:1 MONO_WASM: mono_wasm_load_runtime () failed: {"name":"ExitStatus","message":"Program terminated with exit(1)","status":1}
Ct @ blazor.webassembly.js:1
blazor.webassembly.js:1 MONO_WASM: Error in mono_wasm_before_user_runtime_initialized: {"name":"ExitStatus","message":"Program terminated with exit(1)","status":1}
Ct @ blazor.webassembly.js:1
blazor.webassembly.js:1 MONO_WASM: onRuntimeInitializedAsync() failed: {"name":"ExitStatus","message":"Program terminated with exit(1)","status":1}
Ct @ blazor.webassembly.js:1
blazor.webassembly.js:1 Error: Failed to start platform. Reason: [object Object]
    at Qt (blazor.webassembly.js:1:59902)
```
