---
description: The data collection sessions information
---

# Sessions.csv

## Format

<table>
  <thead>
    <tr>
      <th style="text-align:left">START_TIME</th>
      <th style="text-align:left">STOP_TIME</th>
      <th style="text-align:left">SESSION_NAME</th>
      <th style="text-align:left">SUPERVISOR_EMAIL</th>
      <th style="text-align:left">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>timestamp(<code>str</code>)</p>
        <p>YYYY-mm-dd HH:MM:SS</p>
      </td>
      <td style="text-align:left">
        <p>timestamp(<code>str</code>)</p>
        <p>YYYY-mm-dd HH:MM:SS</p>
      </td>
      <td style="text-align:left">
        <p>name (<code>str</code>)</p>
        <p>SPADES_LAB</p>
      </td>
      <td style="text-align:left">
        <p>email (<code>str</code>)</p>
        <p>Contact email of the session supervisor</p>
      </td>
      <td style="text-align:left">
        <p>text (<code>str</code>)</p>
        <p>Brief description of the session</p>
      </td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
For the concatenated file, the first column should be `SUBJECT_ID`.
{% endhint %}

