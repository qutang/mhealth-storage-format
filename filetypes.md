# File types

These file types will appear as suffix in a filename, for example,

    xxx.xxxxxx.2016-01-01-08-00-00-000-M0500.sensor.csv
    xxx.xxxxxx.2016-01-01-09-00-00-110-P0400.log.csv

## File types to store raw information

### `sensor` file

> Store raw numerical or categorical sensor data in high or low sampling frequency.

> User can add their own `sensor type` to define new `senosr` data file format.

### `event` file

> Store **formatted** event information happens at a time point, such as EMA prompt questions and responses.

### `annotation` file

> Store annotation information by user or by annotator. Annotation set may be from user definition or predefined annotation set.

### `log` file

> Store **formatted** debug log information for devices.

### `note` file

> Store **unformatted** user or researcher's note about experiment.

## File types for data analysis

### `feature` file

> Store numerical or categorical feature data derived from `sensor` or `event` files.

### `class` file

> Store class labels used for machine learning tasks derived from `annotation`, `event` or `note` files.

### `model` file

> Store model definition including hyper parameters and trained structure.

### `stat` file

> Store summary or statistics information derived from any other files.