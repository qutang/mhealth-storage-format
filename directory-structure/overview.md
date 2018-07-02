---
description: >-
  Description of the directory structure of a typical mhealth storage compatible
  dataset
---

# Overview of directory structure

```text
- root
 - [Participant ID 1]
     - MasterSynced
     - OriginalRaw
     - Derived
         - location_mapping.csv
         - subject.csv
         - sessions.csv
         - [SetName]
 - [Participant ID 2]
     - MasterSynced
     - OriginalRaw
     - Derived
         - location_mapping.csv
         - subject.csv
         - sessions.csv
         - [SetName]
 - DerivedCrossParticipants
     - location_mapping.csv
     - sessions.csv
     - subjects.csv
     - [SetName]
```

## Participant ID

1. Allowed characters: _alphabets_ and _digits_.
2. Globally Unique.
3. Used as directory name.

### MasterSynced

1. Synchronized **sensor**, **feature**, **event**, **annotation** files, stored in mhealth storage format.
2. Files are divided **hourly**, in folder `MasterSynced/YYYY/MM/DD/HH/`

### OriginalRaw

1. Original files stored in manufacturer's format.
2. Arbitrary directory structure.
3. Recommended to divide sub directories by the type of sensor or data.

### Derived

1. Store data files derived or merged from files in `MasterSynced` folder. Such as **feature** files, **class** files, **model** files, ema summary files.
2. `SetName` is used to specify any common properties of a set of derived files. Popular names could be `AllTime`,`LabSession`,`Weekend`, `FebruaryMorning` or the combination between them.

## DerivedCrossParticipants

1. Store data files derived and merged from files in each participant's `MasterSynced` or `Derived` folders.
2. `SetName` is used to specify the time or participant characte of a set of derived files. For example, `AllTimeMale`, `LabSessionAdults` and so on.

