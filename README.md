# BunnyLoader.ModSdk

C# Mod 的 NuGet SDK，提供 API 编译引用和 `.bl` 源码打包。需要 .NET 10 SDK。

```xml
<PackageReference Include="BunnyLoader.ModSdk" Version="0.3.0" PrivateAssets="all" />
```

项目根目录放置 `manifest.json` 和 `<id>.cs`，执行 `dotnet build`，产物位于 `artifacts/`。包发布到 NuGet 源后，C# IDE 可自动还原引用。

## 构建

```powershell
dotnet pack BunnyLoader.ModSdk/BunnyLoader.ModSdk.csproj -c Release -o artifacts/nupkg -p:BunnyLoaderApiPath="C:/path/to/BunnyLoader.dll"
```

API DLL 仅在制作包时提供，不提交到此仓库。

## 授权

本仓库的 SDK 源码采用 [MIT](LICENSE)。外部 `BunnyLoader.dll` 及其包含的 Terraria、ReLogic、XNA 等内容不在这份授权范围内。本仓库不提供这些二进制文件，也不授予其分发权；含外部 API 的 NuGet 包须先确认相应分发授权。当前未为完整二进制 NuGet 包声明 MIT 许可证。
