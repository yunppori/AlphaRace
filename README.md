# AlphaRace

**Turn AiM SmartyCam video and RaceStudio telemetry into a lap video with synchronized driving analysis.**

AlphaRace is a Windows desktop application that combines an MP4 racing video with an exported CSV telemetry session. It selects the best lap, aligns video and logger data, and creates a motorsport video with a telemetry HUD and corner-by-corner review pages.

> **Beta software (v1.0.3).** Data formats and available channels vary between logging systems and sessions. Corner boundaries, sector estimates, and driving feedback may be incomplete or inaccurate. Review the results before relying on them for driving decisions.

## Download

Open the [Releases](../../releases) page and select one of the **Assets**:

| Download | Recommended for |
| --- | --- |
| `AlphaRace_Setup_1.0.3_Win64.exe` | Most users: Windows installer |
| `AlphaRace_Portable_1.0.3_Win64.zip` | Users who prefer a portable application |

**Do not use GitHub's automatically generated "Source code (zip)" as a Windows installer.** It is a snapshot of this repository, not the packaged application.

## Requirements

- Windows 64-bit (tested on Windows PCs by the developer).
- An AiM SmartyCam MP4 video and the corresponding RaceStudio telemetry export in CSV format.
- Sufficient free disk space for high-quality video rendering and temporary files.
- **No separate Python, FFmpeg, or FFprobe installation is required.** These are bundled in the release packages.

## Quick start

1. Download the installer and run it, **or** extract the entire Portable ZIP to a local folder.
2. Open **AlphaRace** using its red-and-white AR icon (`AR.exe` for the Portable edition).
3. Add the MP4 and CSV files from the same driving session.
4. Check the detected best lap and synchronization, then select **Generate Video**.
5. Use **Open Output Folder** to view the rendered MP4 (normally in `Videos\\AlphaRace`).

For the Portable edition, keep `AR.exe` and the bundled `_internal` folder together. Do not run `AR.exe` from inside the ZIP archive.

## Features

- Best-lap video extraction and telemetry alignment
- Brake, throttle, steering, yaw and additional telemetry visualization when the respective channels are available
- Corner-focused feedback and sector review pages
- AlphaRace master-style HUD and AR steering graphic
- Optional session-weather lookup when online data and suitable session metadata are available

## Privacy and connectivity

Video processing happens on the user's computer. The optional weather feature may query Open-Meteo with approximate GPS coordinates and the session date/time; if no suitable information or internet connection is available, weather details may be omitted. Please do not upload private session videos or telemetry to public issue reports without checking their contents.

## Known limitations

- Not every CSV export or video overlay layout is guaranteed to be supported.
- Automatic lap/video synchronization and corner/sector mapping need verification for each track/session.
- Individual feedback is an automated assessment, **not a certified race engineer or safety assessment**.
- The beta is intended for track review, not real-time driving assistance.

## Support and bug reports

Use the repository's **Issues** tab. Please include the AlphaRace version, Windows version, track, logger/export format, and what happened. Attach a screenshot or relevant error log. Do not publicly attach original video or CSV files containing personal information unless you intend to share them.

## Third-party software

AlphaRace redistributes FFmpeg / FFprobe and Python-based dependencies. FFmpeg licensing depends on the **exact binaries bundled**. See the third-party notices and corresponding-source materials linked from the release. This repository description does not change any third-party licenses.

Developed by Yun G.H.
