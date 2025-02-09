## Vectorized Matrix Addition Written Questions

  1. (2 points) Besides the speed difference, can you think of any other reasons to prefer NumPy’s adddition
  ufunc over your handwritten matrix addition function?  
  
- I would prefer numpys function simply because I can chain it with the numerous other methods numpy has, cutting down time in general and allowing for an easier work flow.
    
2. (3 points) np.add() checks the dimensions of arrays to ensure it is possible to add them together. If
  you wanted to check that your 2-dimensional lists are the same size, how would you have to modify
  your program and what would you have to check? As part of your answer, give an error condition that
  could occur with 2-dimensional lists but not with NumPy arrays.
 
- An error condition is that lists can have any datatypes as elements, so the entire 2d list would need to be checked to make sure it is the right data type else a type error could occur, besides that another
  error that could occur is if we weren't able to assume that the 2d lists were the same size out of bounds error could occur when trying to check both at once, in total having to do it manually creates the need  
  to handel tons of errors manually.



## Broadcasting (10 points)
  1. Problem 1
- Since matrix a is a (3,3) and b is a (3,1), the fris step is that b is transformed from a shape of 3 to a shape of (3,1), now the second step is that rule two is applied and b is turned from a (3,1) to a (3,3) aka its padded, then what happens is that the two matrixis are now equal length so the operation is done and we have our result.

  2. Problem 2
- Since a is 2,2,2 and b is 2 the first step is that b is padded so b becomes 2,1,2 as in where the array has two arrays each having one b, then step two kicks in so that dimension that is one aka one b in the arrays in the array is expanded now making an array of two arrays of two b's. Now that they are equal dimensions we have our array.

  3. Problem 3
- For this one we have a which is 3 and b which is 3,1 now since a is three columns side it is expanded to being 1,3 techinally, now we have a 1,3 and b 3,1 so each of the dimensions that are 1 in both are streteched meaning a is now 3,3 and b is now 3,3 as well, this means they are ready so we can begin to add them to a matrix we get that is 3,3.

  4. Problem 4
- a is 2,2,2 and b is 4 for step one we set b to 4 the problem here is that neither dimension is comaptible so the result does not work resulting in an error.

  5. Problem 5
- First a is 2,1,1,1 and b is 2, so b is expanded to 2,1,1,2 since b had two elements orginally, now step 2 is that a is padded and not b, meaning a is now 2,1,1,2, as a result we get our result.



## Answerering Questions with Numpy
  1. How many watts were generated all year?
- 218010.26201750195

2. What were the most watts generated in the morning, afternoon, and evening? The least?
- [446.40434207 450.23976606 247.01509894] for the most
  [166.23303073   0.           0.        ] for the least

3. What is the average number of watts generated on January afternoons (i.e, afternoons for the first 31
  days)?
- 213.90079970179

 4. How many days did the system generate fewer than 500 watts total (in the morning, afternoon, and
  evening)?
- 85 days of the year occur when the total watt a day is less than 500.

 5. What is the average number of watts generated in the morning, afternoon, and evening all year? Based
on what you find, which direction do you believe the solar panels are facing?
- [300.38834891, 198.39523217,  98.50480801] I believe that the solarpanels are facing towards the morning and slowly go away to the oppisite dirrection which is why the wat t   average goes down
