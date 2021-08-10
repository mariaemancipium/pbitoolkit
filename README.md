# pbitoolkit
Various DAX and other tools for PowerBI

**Sparklines:** 
this is from https://gist.github.com/deldersveld/62523ca8350ac97797131560cb317677

You need to replace the value for "All_Cases[dateindex]" on lines 9 and 10 with corresponding date column for your data. Note that this works best if you convert it to an index:
So instead of raw date values like 1/12/2020, 1/13/2020, 1/14/2020, convert them to something like: 1,2,3 or 20200112, 20200113, 20200114... I think the former is preferable but the latter should work as well.

Use the same index column to replace "All_Cases[dateindex]" on line 14

On lines 9, 10, and 15, replace "[G_% Patients_AQ]" with your column that has your Y values.

On line 17, replace [dateindex] with the column name containing your date index.

If you want to change the line color, adjust the hexadecimal reference on line 4.
