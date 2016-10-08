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


## MasterSynced

1. Synchronized **sensor**, **feature**, **event**, **annotation **files, stored in mhealth specification.

2. Files are divided **hourly**, in folder `MasterSynced/YYYY/MM/DD/`


## OriginalRaw

1. Original files stored in manufacturer's format.
2. Arbitrary directory structure.

## Derived

1. Store data files derived from files in `MasterSynced` folder. Such as **feature** files, **class** files, **model** files, ema summary files.

