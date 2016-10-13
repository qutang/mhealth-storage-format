# `feature`

Store numerical or categorical feature data derived from `sensor` or `event` files.

## Filename convention

```
FeatureType.FEATUREID_VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.feature.csv
```

Feature files could be in arbitrary length. But for on-the-fly computation, it is recommended to store features in **hourly** length to keep the file size reasonably small for fast I/O.

{% method %}

### FeatureType

1. Used to represent the name of the feature.
2. CamelStyle, allowed characters: *alphabets* and *digits*.
3. Required.

{% common %}

#### Examples

`Correlation`, `DominantFrequency`, `Variance`, `ActivityCount`

{% endmethod %}

### FEATUREID

1. Locally unique identifier for among all features.
2. Globally unique identifier when combining with VERSIONCODE.
3. UPPERCASE style, allowed characters: *alphabets* and *digits*.
4. Required.

### VERSIONCODE

1. It's possible feature gets updated, then use `VERSIONCODE` to indicate the difference.
2. Optional, if omit, use `NA` instead.
3. Allowed characters: *alphabets* and *digits*.

### Timestamp

1. Timestamp has the same convention as that of sensor data. The time represents the first row of annotation.


















