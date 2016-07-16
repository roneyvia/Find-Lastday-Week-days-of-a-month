```javascript
//note: month is 0 based, just like Dates in js
getWeeksInMonth(1, 2016);


function getWeeksInMonth(month, year){
   var weeks=[],
       firstDate=new Date(year, month, 1),
       lastDate=new Date(year, month+1, 0), 
       numDays= lastDate.getDate();
   alert(lastDate);
   var start=1;
   var end=7-firstDate.getDay();
   while(start<=numDays){
       weeks.push({start:start,end:end});
       start = end + 1;
       end = end + 7;
       if(end>numDays)
           end=numDays;    
   }   
   alert(JSON.stringify(weeks));
    return weeks;
}  
```
