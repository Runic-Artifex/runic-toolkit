# RunicToolkit.Hosting.WebUi

Serve a validated static frontend and scope its root session through framework-neutral browser contracts.

```bash
dotnet add package RunicToolkit.Hosting.WebUi --prerelease
```

Requires .NET 10. Use it to author a browser-host adapter; choose `RunicToolkit.Hosting.CsWebUi.App` when you want the supplied native app composition.

```csharp
var manifest = new FrontendAssetManifestBuilder().BuildFromDirectory("wwwroot", "index.html");
var assets = new DirectoryFrontendAssetProvider("wwwroot", manifest);
```

This is not an ASP.NET Core host and does not discover a native runtime. Pair the assets with a concrete browser adapter and root-session factory. See the [public API](https://github.com/Runic-Artifex/runic-toolkit/blob/main/src/RunicToolkit.Hosting.WebUi/PUBLIC-API.md), [examples](https://github.com/Runic-Artifex/runic-toolkit-examples), and [issues](https://github.com/Runic-Artifex/runic-toolkit/issues). Preview package; [MIT licensed](https://github.com/Runic-Artifex/runic-toolkit/blob/main/LICENSE).
