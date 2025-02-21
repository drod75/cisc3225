## Dataset Questions

1. The csv file unlike its namesake uses the pipe character aka | as its separator, it most likely uses this because the file uses commas in its values for the text column, as sentences usually use commas to separate words.
2. The file contains three columns, an id column and two text columns, the columns are objects and the id is to the file is most likely used to log text.
3. Despite looking the exact same the datafame has one major difference, the numbers in text are written as norms in text_norm. This may have been done to create a column of only words and symbols for the intended purpose of the dataset.
4. LJ001-0001|Printing, in the only sense with which we are at present concerned, differs from most if not from all the arts and crafts represented in the Exhibition|Printing, in the only sense with which we are at present concerned, differs from most if not from all the arts and crafts represented in the Exhibition
5. LJ001-0002|in being comparatively modern.|in being comparatively modern.

## DataFrame Practice

1. When fetching the rows at index and position 2 the both are different, for the first case we get 6 and 2 but fot the second case we get 3 and 99, this is because loc uses the index while iloc uses relative the position. Loc can technically return another row if we change the index while iloc will return the same thing unless a row is deleted or added.
2. When fetching the value at the second position and first column you get 3, you can do this in one operation by either using iloc[2,0].
3. When fetching the min for each column you get -4 and 1, for the min of each row you get 1,1,3,-4,9,5 and for the min of the whole dataframe you get -4.
4. The amount of values in a less than 10 is 5.
5. We get 5 rows where the value in column ’a’ is less than 10.
6. We get 4 rows where the value in column ’b’ is less than the mean of column ’b’.
7. We get 2 rows where the value in column ’b’ is less than the mean of column ’a’.
8. The column where the sum is an odd number is b

## Cameras

1. The average cost of cameras is 454.94093264248704
2. For the brand and model name of the most expensive camera we get Canon as the brand and three models, the Canon EOS-1ds, the Canon EOS-1ds Mark 2 and the Canon EOS-1ds Mark 3.
3. For the cameras below the average there are 812 while for above the average there are 153 so the cameras below the average are more common.
4. 
   - The features such as Max resolution, Low resolution, Effective pixels, Zoom tele (T), Storage included, Weight (inc. batteries), Dimensions, Price are better for the cameras after 2002.
   - Zoom wide while better back than is only better by about 1 point, the others differ by at least 4 points, so to be technical they all don't stay the same on average but some are very close to the same.
   - It seems that the dataframe with cameras after 2002 have worse features on average than before on the following, Zoom Wide, Normal focus Range, Macro Focus Range.r
5. When finding the average for the columns in the cameras now and then dataframes i excluded the columns that were not integers because a type error would be sent back, so im not sure what the answer would be here since pandas does not filter out any columns by either finding the mean after the condition or not.
6. The cameras that provide the most pixels per dollar are:
   - Kodak DCS SLR/c
   - Kodak DCS 14n
   - Kodak DCS SLR/n
   - Kodak Z1275
   - Olympus FE-300
   - Ricoh Caplio R7
   - Ricoh Caplio GX8
   - Samsung S830
   - Samsung L830
   - Nikon Coolpix P1
7. Using the .info() method we find out there are 965 non null values per column, and it has 965 entries meaning there are no null values.
8. In order to find out if the dataframe actually has any null values represented in another way I decided to find the amount of zeroes in the dataframe, and they are:
   - Max resolution 1 
   - Low resolution 51 
   - Effective pixels 26 
   - Zoom wide (W) 80 
   - Zoom tele (T) 80
   - Normal focus range 127 
   - Macro focus range 113 
   - Storage included 113 
   - Weight (inc. batteries) 13 
   - Dimensions 7 
   - Price 0 
   - Brand 0

   While there is no proof any of these are null values zeroes for some of these columns needs more context, if there are null values this messes with the previous answers as there is now way to accurately calculate the average without metadata to describe the data in depth.

## Pandas Questions

1. So in pandas we have series and dataframes, in numpy we have arrays and this is the backbone of each, a pandas series is like an array but with an interesting twist, besides the option of labeling each row there are no columns only the row of data. A dataframe is like a table with rows and columns, as a result its shape can be like 4,5 while a series is 4,. This is important because a series is more useful for an array of values with possible labels, which is what pandas does sometimes.
2. In a series accessing by an index is liking a list, you get the value at that index, a dataframe does something similar but retrieves an entire row, or like an entire list at that index.
3. for series iloc is good to access an element at an index, while loc is good to access an element by a label.
4. for dataframe iloc is good to access a row at a position, while loc is good to access a row by an index
5. A series is like a dictionary because each row can have an index, while each element can be a list the object is still x rows by 1, its like a list and one dimensional array because its by definition a single line of data like the formers.
6. A dataframe is like a dictionary because while a dictionary uses keys dataframes uses positions, its like a two dimensional list because it has rows and columns that can vary in size.
