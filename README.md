# Surfs-Up
This Repository contains an Analysis on A SQLite Weather Database By Utilizing Flask, Pandas, Python, and SQLAlchemy. 


Overview:

The Purpose for this Analysis is to Investigate Trends Pertaining to Temperatures In Oahu Hawaii For The Months of June And December (In Order To Determine if The Ice Cream Shop Business and The Surf Shop Business will be Viable Year Round) By Utilizing Flask, Python, Pandas, And SQLAlchemy. The Data For Performing The Analysis For Both Deliverables In This Module Challenge Is From The Hawaii SQLite Database. The Analysis For Deliverable 1 was based on Obtaining Summary Statistics Pertaining to Temperatures In Oahu Hawaii For The Month of June. The Analysis For Deliverable 2 was based on Obtaining Summary Statistics Pertaining to Temperatures In Oahu Hawaii For The Month of December. 


Results:

Deliverable 1:

• The Table Below That Was Generated Displays Summary Statistics Pertaining to Temperatures In Oahu Hawaii For The Month of June.

![Module 9 Challenge Deliverable 1](https://user-images.githubusercontent.com/80506578/188492207-c22e58c7-06b2-4fc1-b381-e4d5b90b550b.png)


Deliverable 2: 

• The Table Below That Was Generated Displays Summary Statistics Pertaining to Temperatures In Oahu Hawaii For The Month of December. 

![Module 9 Challenge Deliverable 2](https://user-images.githubusercontent.com/80506578/188492326-a6433f32-a1ef-4e17-ae0a-9ee654e30c3c.png)


• The Range Of Temperatures For Oahu Hawaii In The Month Of June Is From 64 Degrees Fahrenheit To 85 Degrees Fahrenheit. The Range Of Temperatures For Oahu Hawaii In The Month Of December Is From 56 Degrees Fahrenheit To 83 Degrees Fahrenheit.

• The Average Temperature In Oahu Hawaii For The Month Of June Is 75 Degrees Fahrenheit. The Average Temperature In Oahu Hawaii For The Month Of December Is 71 Degrees Fahrenheit. 

• The Standard Deviation Of Temperatures In Oahu Hawaii For The Month Of June Is 3.26 And The Standard Deviation Of Temperatures In Oahu Hawaii For The Month Of December Is 3.75 (Based On The Summary Statistics Tables Pertaining To Temperatures In Oahu Hawaii For Both Months). 



Summary:

• The Temperatures In Oahu Hawaii For The Month Of June Appear To Be Slightly Greater Than The Temperatures In Oahu Hawaii For The Month Of December (Even Though They Remain Quite Close To Each Other For Both Months). I Believe That It'll Be Viable For The Ice Cream Shop Business and The Surf Shop Business In Oahu Hawaii To Operate Year Round.

• I Would Perform The Following Queries Below To Acquire More Weather Data For Oahu Hawaii During The Month Of June And During The Month Of December:


Queries For Determining The Total Precipitation Levels In Oahu Hawaii For The Months Of June And December:

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()


Queries For Determining The Amount Of Precipitation At The Most Active Station In Oahu Hawaii For The Months Of June And December:

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 12).all()




