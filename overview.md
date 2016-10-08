# Directory overview

```
- root
  - [Participant ID]
    - MasterSynced
    - OriginalRaw
    - Derived
      - [SetName]
  - DerivedCrossParticipants
    - [SetName]
```

## Participant ID

1. Numerical or String

2. Globally Unique

3. Used as directory name


### [Participant ID]/MasterSynced

1. Synchronized **sensor**, **feature**, **event**, **annotation **files, stored in mhealth specification.

2. Files are divided **hourly**, in folder `MasterSynced/YYYY/MM/DD/`


### [Participant ID]/OriginalRaw

1. Original files stored in manufacturer's format.
2. Arbitrary directory structure.

### [Participant ID]/Derived

1. Store data files derived or merged from files in `MasterSynced` folder. Such as **feature** files, **class** files, **model** files, ema summary files.

2. `SetName` is used to specify the time character of a set of derived files. Popular names could be `AllTime`,`LabSession`,`Weekend`, `February` or `Morning` or the combination between them.

## DerivedCrossParticipants

1. 