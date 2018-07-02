# Filename convention

Store **formatted** annotations from a predefined or user defined annotation set.

## Filename convention

```text
AnnotationSet.ANNOTATIONSETID-ANNOTATORID-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.annotation.csv
```

Annotation files are divided into **hourly** files.

### AnnotationSet

1. Used to represent the name of the annotation set.
2. CamelStyle, allowed characters: _alphabets_ and _digits_.
3. There should be a file named [`AnnotationSet.ANNOTATIONSETID-VERSIONCODE.ontology.csv`](filename-convention.md) associated with the dataset.
4. Required.

#### Examples

`SpadesLab`, `SpadesTwoDays`, `SpadesThreeMonths`, `UserDefined`, `CrowdSourcing`

### ANNOTATIONSETID

1. Locally unique identifier for the annotation set.
2. Globally unique identifier for the annotation set when combining with ANNOTATORID and VERSIONCODE.
3. UPPERCASE style, allowed characters: _alphabets_ and _digits_.
4. Required.

### ANNOTATORID

1. local identifier for event types.
2. UPPERCASE style, allowed characters: _alphabets_.
3. Required.
4. If it's user's own annotation, the ANNOTATORID should be the same as PARTICIPANT ID.

### VERSIONCODE

1. It's possible annotation set gets updated, then use `VERSIONCODE` to indicate the difference.
2. Optional, if omit, use `NA` instead.
3. Allowed characters: _alphabets_ and _digits_.

### Timestamp

1. Timestamp has the same convention as that of sensor data. The time represents the first row of annotation.

