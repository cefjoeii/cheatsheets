---
title: ExifTool
---

### Date
This can be used for **Date Taken** (DateTimeOriginal), **Date Created** (CreateDate), **Date Modified** (ModifyDate), or all the three (AllDates).

```
# Set exact date and time for all files in the current directory
  exiftool "-DateTimeOriginal=YYYY:MM:DD HH:MM:SS" ./
  exiftool "-CreateDate=YYYY:MM:DD HH:MM:SS" ./
  exiftool "-ModifyDate=YYYY:MM:DD HH:MM:SS" ./
  exiftool "-AllDates=YYYY:MM:DD HH:MM:SS" ./

# Set exact date and time for a single file
  exiftool "-DateTimeOriginal=YYYY:MM:DD HH:MM:SS" filename.jpg
  ...

# Shift date and time for a single file
  exiftool "-DateTimeOriginal+=YYYY:MM:DD HH:MM:SS" filename.jpg
  exiftool "-DateTimeOriginal-=YYYY:MM:DD HH:MM:SS" filename.jpg
  ...

# Print formatted date and time for all jpg files in the current directory.
  exiftool -d "%r %a, %B %e, %Y" -DateTimeOriginal -S -s *.jpg
  ...
```
