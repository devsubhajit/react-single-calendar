# React Single Calendar

## **Description:** 
**react-single-calendar** is a very useful and easy to use date picker, no external dependency is needed for this. You can chagne theme of it's color, by simply editing css variables.

### **How to install?**
```
npm i react-single-calendar
```
### **Link with material icons**
Copy and paset this material icons cdn link on head tag.
```
<link href="https://fonts.googleapis.com/icon?family=Material+Icons"
      rel="stylesheet">
```

### **Implementation**
```
import React, {useState} from 'react';
import SingleCalendar from 'react-single-calendar';


const App = () => {
    let [date, filterDate] = useState('');
    return (
        ....
        <SingleCalendar selectedDate={filterDate} />
    )
}
export default App;
```
In this **date** useState you will get the **selectedDate**, **selectedDate** is the props for **SingleCalendar** component. It will return this **filterDate** method, you can use your own method.

**react-single-calendar** returns a string value like **March 21, 2019**, you can use Date.parse() method to convert it as a date.

*Single Calendar doesn't come with any pre-defined button, so you can open or close this component on a freedom of your own button click function*


## **Getting Date Range **
For getting date range, add a on for **< SingleCalendar />**, named as **range={true}**, by default **range** is false.

*When using* **range**, *this* **filterDate** *method returns an array of to strings*

```
import React, {useState} from 'react';
import SingleCalendar from 'react-single-calendar';


const App = () => {
    let [date, filterDate] = useState('');
    return (
        ....
        <SingleCalendar selectedDate={filterDate} range={true} />
    )
}
export default App;
```
In this example it the **date** variable will return:

Example: **['March 21, 2019', 'August 10, 2019']**

Again you can use **Date.parse()** method, to gate a date value, or you can use this strings in your way.

## **Theming:** 
On your css/ scss add this variables.
You can customize your theme color and width, height through this css variables.
```
:root {
  --weekend: rgba(0, 0, 0, 0);
  --date-light: #f8f9fa;
  --date-primary: #5644c1;
  --date-success: #37d37d;
  --date-primaryLight: #eceaf5;
  --date-primaryTitle: #dbd8f0;
  --date-hover: #262769;
  --date-highlight: #f83854;
  --date-disabled:#c2c1cc;
  --date-width: 260px;
  --date-height: 280px;
```
These fields are added, for the range:

1. date-rangebg: is for highlighting dates between two selected dates
2. date-rangetext: changing color of text in range area
3. date-rangeDateBg: two main dates which will indicate "from" and "to" dates
```
  --date-rangebg:#8072d0;
  --date-rangetext:#f8f9fa;
  --date-rangeDateBg:#5644c1;
}
```
## **Implementation Video**
Here is the demo video link:
https://www.youtube.com/watch?v=61hOnfyPL7U&t=27s

## **Using Date Range Video**
How to use date range:
https://www.youtube.com/watch?v=61hOnfyPL7U&t=27s

## **Raise an Issue**
If you are facing any issue regarding installation and usage, raise your issue in **Git repo**. 
```
https://github.com/devsubhajit/react-single-calendar/issues
```
