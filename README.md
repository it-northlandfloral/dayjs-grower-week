# DayJS Grower Week Plugin
Custom DayJS plugin that handles floral grower weeks
- Weeks run from Sunday to Saturday
- Week Year is determined by the Thursday

## Examples:
| Date              | Grower Week |  Grower Year |
|-------------------|:-----------:|-------------:|
| January 1, 2022   |  52         | 2021         |
| December 31, 2024 |  1          | 2025         |
| December 31, 2026 |  53         | 2026         |


## Installation
```bash
npm install 
```

## Usage

### Get Grower Week
```javascript
// returns the current grower week
dayjs('2023-01-25').growerWeek() // 4
```

### Set Grower Week
```javascript
// sets the grower week
dayjs('2023-01-25').growerWeek(52) // dayjs object 2023-12-27
```

### Get Start of Grower Week
```javascript
// get the start of the grower week
dayjs('2023-01-25').startOf('growerWeek') // dayjs object 2023-01-22 0:00:00
```

### Get End of Grower Week
```javascript
// get the end of the grower week
dayjs('2023-01-25').endOf('growerWeek') // dayjs object 2023-01-28 23:59:59
```

### Get Number of Grower Weeks in a year 
```javascript
// requires isLeapYear plugin
//returns the current grower week year
dayjs('2023-01-25').growerWeekYear() // 52
```

### Format Grower Week
- ```gw``` = Grower Week
- ```gww``` = Grower Week (2 Digit)
- ```gy``` = Grower Year

```javascript
// formats the grower week
dayjs('2023-01-25').format('gw') // 4
dayjs('2023-01-25').format('gy') // 2023
```