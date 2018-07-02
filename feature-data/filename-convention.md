# Filename convention

Store numerical or categorical feature data derived from `sensor` or `event` files.

## Filename convention

```text
FeatureType.FEATUREID-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.feature.csv
```

Feature files could be in arbitrary length. But for on-the-fly computation, it is recommended to store features in **hourly** length to keep the file size reasonably small for fast I/O.

This often ships with source code that indicates the computation of the feature, the source code should be clear about FEATUREID and VERSIONCODE.

### FeatureType

1. Used to represent the name of the feature. If multiple features are combined into one file, becoming a feature set, then feature type should clearly state the name of the feature set.
2. CamelStyle, allowed characters: _alphabets_ and _digits_.
3. Required.

#### Examples

For single feature file: `Correlation`, `DominantFrequency`, `PhoneVariance`, `DominantWristActivityCount`.

For feature set file: `TimeDomainFeatures`, `DominantWristFeatures`.

### FEATUREID

1. Locally unique identifible for current feature set, flexible to include location, id, and any information.
2. UPPERCASE style, allowed characters: _alphabets_, _digits_ and _dash_.
3. Required.

#### Examples

For feature set: `DOMINANTWRIST`, `DOMINANTWRIST-PARTICIPANT1TO3` For single feature: `DOMIANTWRIST-CORRELATION`, `[IMEI]-CORRELATION`

### VERSIONCODE

1. It's possible feature gets updated, then use `VERSIONCODE` to indicate the difference.
2. Optional, if omit, use `NA` instead.
3. Allowed characters: _alphabets_ and _digits_.

### Timestamp

1. Timestamp has the same convention as that of sensor data. The time represents the first row of annotation.

