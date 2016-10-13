# `feature`

Store numerical or categorical feature data derived from `sensor` or `event` files.

## Filename convention

```
FeatureType.FEATUREID_VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.feature.csv
```

Feature files could be in arbitrary length. But for on-the-fly computation, it is recommended to store features in **hourly** length to keep the file size reasonably small for fast I/O.

{% method %}

### FeatureType
1. Used to represent the name of the annotation set.
2. CamelStyle, allowed characters: *alphabets* and *digits*.
3. There should be a file named [`AnnotationSet.ANNOTATIONSETID-VERSIONCODE.ontology.csv`](#) associated with the dataset.

4. Required.



{% common %}

#### Examples

`SpadesLab`, `SpadesTwoDays`, `SpadesThreeMonths`, `UserDefined`, `CrowdSourcing`



{% endmethod %}



### ANNOTATIONSETID



1. Locally unique identifier for the annotation set.

2. Globally unique identifier for the annotation set when combining with ANNOTATORID and VERSIONCODE.

3. UPPERCASE style, allowed characters: *alphabets* and *digits*.

4. Required.



### ANNOTATORID



1. local identifier for event types.

2. UPPERCASE style, allowed characters: *alphabets*.

3. Required.

4. If it's user's own annotation, the ANNOTATORID should be the same as PARTICIPANT ID.



### VERSIONCODE



1. It's possible annotation set gets updated, then use `VERSIONCODE` to indicate the difference.

2. Optional, if omit, use `NA` instead.

3. Allowed characters: *alphabets* and *digits*.



### Timestamp



1. Timestamp has the same convention as that of sensor data. The time represents the first row of annotation.


















