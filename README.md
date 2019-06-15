# Sketchfab-dl
Downloader for 3d model from [Sketchfab](https://sketchfab.com/) in .NET

## Options
```csharp
  -u, --url=URL              // The URL input.
  -s, --source=NAME          // The source NAME file.
  -t, --textures             // Download texture files.
  -e, --export               // Export the file to .obj (blender is required).
  -c, --clear                // Clear the workplace (export option is required).
  -b, --background           // Call the processing export in background (export option is required).
  -h, --help                 // Show this message and exit
```

## Usage
- Downloads just the raw files of the model from url
```bash
  Sketchfab-dl.exe -c -u {sketchfab 3d model url}
```

- Downloads the raw files of the model and texture files from siurce file
```bash
  Sketchfab-dl.exe -ct -u {sketchfab 3d model url}
```

- Downloads the raw files of the model and exports it in `.obj` file by [blender 2.49b](https://www.blender.org/) (with python script)
```bash
  Sketchfab-dl.exe -ec -u {sketchfab 3d model url}
  
  Sketchfab-dl.exe -ec -s "path\source.txt"
```

## Building Code
[.NET Standard 2.0](https://github.com/dotnet/standard/blob/master/docs/versions.md) and .NET Framework 4.6

## Dependencies
* [CloudFlareUtilities](https://www.nuget.org/packages/CloudFlareUtilities/)
* [HtmlAgilityPack](https://www.nuget.org/packages/HtmlAgilityPack)
* [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json)
* [NDesk.Options](https://www.nuget.org/packages/NDesk.Options)
