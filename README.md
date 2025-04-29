# @Svalbaz's JellyFin Organiser

![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-blue?logo=powershell&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Welcome to **@Svalbaz's JellyFin Organiser**! This repository contains a collection of PowerShell scripts designed to help you organise and manage your media library for use with **JellyFin** and similar media servers. The scripts automate common tasks such as sanitising episode names, removing unnecessary metadata, organising folders, and ensuring your media library is well-structured.

These were all created after I moved my years-old collection from my PC to my HomeLab and had some catastrophic issues due to the sheer chaos of how I stored the Movies/TV shows (e.g. mixed folders, stupid file names like `Deadpool.2016.xVID.H264.[InsertName].1080p.[XdumbRIP].mkv`, etc.)

---

## 🎯 Scripts

The project includes the following scripts to help manage your TV shows and movies:

### 1. [[Overall_VideoScanReporter.ps1](https://github.com/Svalbaz/Overall_VideoScanReporter)](https://github.com/Svalbaz/JellyFin_Overall_VideoScanReporter)
- **Target**: TV & Movies  
- **Purpose**: Scans all folders in `$rootTV` and `$rootMovies` for video files using `ffmpeg` to generate a codec/quality report.  
- **Why**: Identify oversized 4K rips and optimise storage.  
- **Note**: Requires ffmpeg in your system PATH.

### 2. [TV_EpisodeNameSanitiser.ps1](https://github.com/Svalbaz/TV_EpisodeNameSanitiser)
- **Target**: TV  
- **Purpose**: Renames episode files to a standard format like `Show Name (Year) - SXXEXX.ext`.  
- **Why**: Improves metadata scraping accuracy in JellyFin.  
- **Safe Mode**: Only previews by default with `-WhatIf`.

### 3. [TV_TrickplayRemove.ps1](https://github.com/Svalbaz/TV_TrickplayRemove)
- **Target**: TV  
- **Purpose**: Removes leftover `.trickplay` folders.  
- **Why**: Cleans up old data before rescanning libraries.  
- **Safe Mode**: Previews with `-WhatIf` enabled.

### 4. [TV_SeasonNumberer.ps1](https://github.com/Svalbaz/TV_SeasonNumberer)
- **Target**: TV  
- **Purpose**: Pads single-digit season folders to `Season 01`, `Season 02`, etc.  
- **Why**: Aligns with JellyFin’s preferred format for season folders.  
- **Safe Mode**: Previews renaming with `-WhatIf`.

### 5. [Overall_MetaDataRemover.ps1](https://github.com/Svalbaz/Overall_MetaDataRemover)
- **Target**: TV & Movies  
- **Purpose**: Deletes `.nfo`, `.jpg`, `.png`, `.xml` files across media folders.  
- **Why**: Clears old or inconsistent metadata files for a clean rescan.  
- **Safe Mode**: Preview only unless `-WhatIf` is removed.

### 6. [Movie_CollectionSorter.ps1](https://github.com/Svalbaz/Movie_CollectionSorter)
- **Target**: Movies  
- **Purpose**: Detects collection folders (e.g., trilogies) without years and renames them to a proper format.  
- **Why**: Better folder structure, especially for collections.  
- **Safe Mode**: Uses `-WhatIf` to simulate renames.

---

## ▶️ Usage

To use these scripts:

1. Download the `.ps1` files to your machine.  
2. Open in PowerShell ISE or your preferred terminal.  
3. Update the **Config/Variables** section for your system.  
4. Run with `-WhatIf` first to test.

> All scripts follow this structure:  
> **1. Comment block**  
> **2. Config/variables**  
> **3. Script logic**  
>  
> Just tweak the config, and you're good to go.

---

## 🚧 Project Management

Check out the full GitHub Kanban board for script planning and tasks:  
🔗 [@Svalbaz's JellyFin Organiser – GitHub Project](https://github.com/users/Svalbaz/projects/2)

---

## 🤝 Contribution

Feel free to fork or contribute improvements, bug fixes, or feature enhancements via pull requests.

---

## 📜 License

Licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🙏 Thanks

Thanks for checking out **@Svalbaz's JellyFin Organiser**!  
If this helps clean up your chaotic library — mission accomplished.  
Feel free to raise issues, suggest improvements, or just star the repo.  
Happy organising! 📺🎬
