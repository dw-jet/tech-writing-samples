# Weather API

Weather data object returned in JSON or XML.

## Description

Represents the weather conditions for one day.

<details open>
	<summary>JSON results</summary>

## Sample JSON

```JSON
{
  "date": "2021-09-01",
  "description": "sunny",
  "maxTemp": 22,
  "minTemp": 20,
  "windSpeed": 12,
  "danger": false
}
```
</details>

<details>
<summary>XML results</summary>

## XML Example

```XML
<?xml version="1.0" encoding="UTF-8"?>
<dailyForecast>
   <date>2021-09-01</date>
   <description>sunny</description>
   <maxTemp>22</maxTemp>
   <minTemp>20</minTemp>
   <windSpeed>12</windSpeed>
   <danger>false</danger>
</dailyForecast>
```
</details>

## Elements

| Element         | Description                      | Type    | Notes                                                                        |
|:----------------|:---------------------------------|:--------|:-----------------------------------------------------------------------------|
| **date**        | Forecast date                    | string  | Formatted as: YYYY-MM-DD                                                     |
| **description** | Text description of the weather  | string  | Valid values: "sunny", "overcast", "partly cloudy", "raining", and "snowing" |
| **maxTemp**     | High temperature for the day     | number  | In degrees Celsius                                                           |
| **minTemp**     | Low temperature for the day      | number  | In degrees Celsius                                                           |
| **windSpeed**   | The wind speed                   | number  | In kilometers per hour                                                       |
| **danger**      | True if conditions are dangerous | boolean |                                                                              |