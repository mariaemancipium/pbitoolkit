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



**Distance Calculator:**
I am indebited to a plethora of online sources explaining how to use the great circles formula, especially but not limited to Phil Seamark's Post here: https://dax.tips/2017/05/13/dynamic-distances-in-power-bi

Basically, since Lattitue and Longitude are descriptions of relative location on a sphere, it is possible to caculate distance using trigonometry.

Replace "Treatments by Zip'[Hsp Lat]" on line 2 with a reference to a column containing the latitude of your first point. Yes, it has to be repeated twice.

Replace "Treatments by Zip'[Hsp Lon]" on line 3 with a reference to a column containing the longitude of your first point. Yes, it has to be repeated twice.

Replace "Treatments by Zip'[Patient Lat]' on line 9 with a reference to a column containing the latitude of your second point. Yes, it has to be repeated twice.

Replace "Treatments by Zip'[Patient Lon]' on line 9 with a reference to a column containing the longitude of your second point. Yes, it has to be repeated twice.

Replace 'Treatments by Zip' on line 8 with the table containing all of these points.
