---
layout: page-fullwidth
title: "Programming Interviews! - Week 1 - Possible Solutions"
teaser: "I'm a TA for a Data Structures class. Every Friday, I give my class a few programming interview questions I've received in the past."
header:
    image_fullwidth: "code.jpg"
image:
    homepage: code.jpg
categories:
    - design
comments: true
show_meta: false
---
I wrote the following answers below. I was allowed to pick whatever programming language I wanted, and I picked Javascript. These may not be completely accurate, and I would love any feedback! 


1) What is the current day number given the function below:

{% highlight JavaScript %}
function dayNumber(int month, int day, int year)
{


    //I populated the last few months with junk data for testing/lazy purposes.
    int monthArray[] = {31, 28, 31, 30, 31, 30, 30,30,30,30,30,30};


    //This is to check if we have good data. We dont want someone submitting 2/30/15.
    if( m < 0 && m > 13 &&  month[m] > 0 && d < month[m]){
       
        //this account for leap year by changing the 2nd data in the month array
        if( year % 4)
            monthArray[1] = 29;
            
            
        //adds the number of days in the month at each space in data to a temp variable
        int tempMonth;  
        for( i = 0, i < month, i++)
        {
            tempMonth += monthArray[i];
        
        }
        

        //adds the days to the temp month 
        days = tempMonth + day;
        
        //if its January, subtract the days. 
        if (month == 1)
        {
            days -= monthArray[0];
        }
         
        return days;

	}
}
{% endhighlight %}

Looking back on this one, it might have been easier to just break out if int month = 0;





2) Calculate the angle between the two handles of the clock. The angle must less than  180 degrees. 

{% highlight JavaScript %}
function angleBetween(int hour, int minute)
{
	int hourDegrees;
   	int minuteDegrees;

   	//The hour hand moves 30 degrees every hour, and .5 degrees every minute that passes.
    hourDegrees = (hour * 30) + (minute * .5);

    //The minute hand moves 6 degrees for every  minute that passes by
    minuteDegrees = (minute * 6);
    
    //The two calculations make what each individual angle would be, but we want the angle between the two, so we subtract them.
    //The result might be negative if the time is something like 6:04.
    int angle = Math.abs(mintuteDegrees - hourDegrees);
    

    //This rejects any answer bigger than 180, and makes it into a number we would like. 
    if(angle > 180)
        angle = 360 - angle;
    

    return angle;
}
{% endhighlight %}