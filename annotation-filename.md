# `annotation`

Store **formatted** annotations from a predefined or user defined annotation set.

## Filename convention

```
AnnotationSet.ANNOTATIONSETID-ANNOTATORID-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.annotation.csv
```

Annotation files are divided into **hourly** files.

{% method %}

### AnnotationSet

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

{% method %}



### Timestamp



1. Timestamp has the same convention as that of sensor data. The time represents the first row of event.



2. Because it's a daily file, normally there will only be one file for a day.



3. In case time zone is changed during the day, there will be multiple files for one day.



{% common %}



#### Examples



If time zone changes from M0500 to M0300 at 10am on a day, and an event happens at 12pm in M0500 time zone, then the new file would have timestamp `YYYY-MM-DD-14-00-00-000-M0300` in the filename.







{% endmethod %}








