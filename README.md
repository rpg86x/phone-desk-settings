# Phone Desk Settings

Windows settings utility for Phone Desk I, II, III and the two iPad profiles. Configure model, case color, scale and enabled devices. The current existing local build is imported without changes under `A/source` and `A/windows`.

Download ZIP, extract and open `A/windows/Phone Desk Settings.exe`. Requires Windows and .NET Framework 4.x. The executable is unsigned.

Settings writes `phone-desk-settings.xml` beside itself. Personal settings and backups are excluded from Git. Place the Settings executable beside your Phone Desk executables so they share the same settings file. The launch button requires the corresponding device executables there; enable only devices that you have downloaded. This repository does not bundle device applications.

Available devices: [Phone Desk I](https://github.com/rpg86x/phone-desk-i), [Phone Desk II](https://github.com/rpg86x/phone-desk-ii). Other device applications are not included here.

Build from the repository root with PowerShell:

```powershell
& C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe /nologo /target:winexe '/out:A\windows\Phone Desk Settings.exe' /reference:System.Windows.Forms.dll /reference:System.Drawing.dll 'A\source\PhoneDeskSettingsV2.cs' 'A\source\PhoneDeskConfig.cs'
```

The existing build has no reliable numeric release metadata. Git Sync records its version as `current`. Publication of this exact existing build was requested by the owner. The original installed Phone Desk suite remains unchanged.
