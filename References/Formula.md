
| Function     | Description                                                                            | Category | Output Type | Inputs                                                             |
| ------------ | -------------------------------------------------------------------------------------- | -------- | ----------- | ------------------------------------------------------------------ |
| prop         | Get the value of a property                                                            | Property | any         | property: (text)                                                   |
| slice        | Get a part of a text                                                                   | String   | text        | text: (text)<br>start: (number)<br>end: (number)                   |
| if           | If condition is true return the first argument else return the second                  | Logic    | any         | condition: (boolean)<br>ifTrue: (any)<br>ifFalse: (any)            |
| ifs          | If the first condition is true return the first argument else check the next condition | Logic    | any         | condition: (boolean)<br>ifTrue: (any)<br>...: ()<br>ifFalse: (any) |
| empty        | Check if a list is empty                                                               | String   | boolean     | value: (any)                                                       |
| length       | Get the length of a list                                                               | List     | number      | list: (any-multi)                                                  |
| values       | Get the number of values in a list                                                     | List     | number      | list: (any-multi)                                                  |
| uniques      | Get the number of unique values in a list                                              | List     | number      | list: (any-list)                                                   |
| substring    | Get a substring of a string                                                            | String   | text        | string: (text)<br>start: (number)<br>end: (number)                 |
| startsWith   | Check if a string starts with another string                                           | String   | boolean     | string: (text)<br>substring: (text)                                |
| contains     | Check if a string contains another string                                              | String   | boolean     | string: (text)<br>substring: (text)                                |
| test         | Test a string with a regex                                                             | String   | boolean     | string: (text)<br>regex: (text)                                    |
| match        | Match a string with a regex                                                            | String   | boolean     | string: (text)<br>regex: (text)                                    |
| replace      | Replace a string with another string                                                   | String   | text        | string: (text)<br>search: (text)<br>replace: (text)                |
| replaceAll   | Replace all occurences of a string with another string                                 | String   | text        | string: (text)<br>search: (text)<br>replace: (text)                |
| lower        | Convert a string to lowercase                                                          | String   | text        | string: (text)                                                     |
| upper        | Convert a string to uppercase                                                          | String   | text        | string: (text)                                                     |
| repeat       | Repeat a string                                                                        | String   | text        | string: (text)<br>times: (number)                                  |
| format       | Format a value to string                                                               | String   | text        | value: (any)                                                       |
| toNumber     | Convert a value to a number                                                            | Number   | number      | value: (any)                                                       |
| now          | Get the current date                                                                   | Date     | date        |                                                                    |
| minute       | Get the minutes of a date                                                              | Date     | number      | date: (date)                                                       |
| hour         | Get the hours of a date                                                                | Date     | number      | date: (date)                                                       |
| day          | Get the day of a date                                                                  | Date     | number      | date: (date)                                                       |
| date         | Get the date of a date                                                                 | Date     | number      | date: (date)                                                       |
| week         | Get the week of a date                                                                 | Date     | number      | date: (date)                                                       |
| month        | Get the month of a date                                                                | Date     | number      | date: (date)                                                       |
| year         | Get the year of a date                                                                 | Date     | number      | date: (date)                                                       |
| pad          | Pad a number with text                                                                 | String   | text        | number: (number)<br>length: (number)<br>text: (text)               |
| range        | Get the difference between the largest and smallest from a list of numbers             | List     | number      | numbers: (number-multi)                                            |
| latest       | Get the latest date of a list of dates                                                 | Date     | date        | dates: (date-multi)                                                |
| earliest     | Get the earliest date of a list of dates                                               | Date     | date        | dates: (date-multi)                                                |
| dateRange    | Get the date range of a list of dates                                                  | Date     | number      | dates: (date-multi)<br>type: (text)                                |
| dateAdd      | Add an amount to a date                                                                | Date     | date        | date: (date)<br>amount: (number)<br>type: (text)                   |
| dateSubtract | Subtract an amount from a date                                                         | Date     | undefined   | date: (date)<br>amount: (number)<br>type: (text)                   |
| dateBetween  | Get the difference between two dates                                                   | Date     | number      | date1: (date)<br>date2: (date)<br>type: (text)                     |
| spaceItems   | Get the items inside of a path                                                         | Path     | link-multi  | path: (text)                                                       |
| spaces       | Get the spaces the path is inside of                                                   | Path     | link-multi  | path: (text)                                                       |
| timeStamp    | Get the timestamp of a date                                                            | Date     | number      | date: (date)                                                       |
| at           | Get an element at a specific index                                                     | List     | any         | list: (any-list)<br>index: (number)                                |
| first        | Get the first element of a list                                                        | List     | any         | list: (any-multi)                                                  |
| last         | Get the last element of a list                                                         | List     | any         | list: (any-multi)                                                  |
| concat       | Concatenate two lists                                                                  | List     | any-multi   | list 1: (any-multi)<br>list 2: (any-multi)                         |
| sort         | Sort a list                                                                            | List     | any-multi   | list: (any-multi)                                                  |
| reverse      | Reverse a list                                                                         | List     | any-multi   | list: (any-multi)                                                  |
| join         | Turn a list into text separator                                                        | List     | text        | list: (text-multi)<br>separator: (text)                            |
| includes     | Check if a list includes a value                                                       | List     | boolean     | list: (any-multi)<br>value: (any)                                  |
| split        | Split text into a list using a separator                                               | String   | text-multi  | string: (text)<br>separator: (text)                                |
| formatDate   | Format a date into text                                                                | Date     | text        | date: (date)<br>format: (text)                                     |
| parseDate    | Transform date from text                                                               | Date     | date        | date: (text)                                                       |
| find         | Find an element in a list                                                              | List     | any         | list: (any-multi)<br>condition: (boolean)                          |
| findIndex    | Find the index of an element in a list                                                 | List     | number      | list: (any-multi)<br>condition: (boolean)                          |
| filter       | Filter a list based on a condition                                                     | List     | any-multi   | list: (any-multi)<br>condition: (boolean)                          |
| map          | Change all the values in a list based on a formula                                     | List     | any-multi   | list: (any-multi)<br>formula: (any)                                |
| some         | Check if some elements in a list are true                                              | List     | boolean     | list: (any-multi)<br>condition: (boolean)                          |
| every        | Check if every element in a list is true                                               | List     | boolean     | list: (any-multi)<br>condition: (boolean)                          |
| flat         | Flatten a list of lists into a single list                                             | List     | any-multi   | list: (any-multi)                                                  |
| path         | Get the path object of a path                                                          | Path     | link        | path: (text)                                                       |
| let          | Define a variable to use in a formula                                                  | Variable | any         | variable: (text)<br>value: (any)<br>formula: (any)                 |
| lets         | Define multiple variables to use in a formula                                          | Variable | any         | variable: (text)<br>value: (any)<br>...: ()<br>formula: (any)      |
