# Imputer

Cleans up missing and NaN values from data. 

2 primary methods are used:
1. Fit
2. Transform

What imputer does is that it populates missing data with either the mean or mode.
Fit is the method that is called to calculate the mean and mode.

Transform populates the polluted dataset with the specified values. 


For String data, it appears that one needs to fill in the values oneself. A bit of python fu should do the trick
