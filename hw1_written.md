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

## Answerering Questions with Numpy
  1. How many watts were generated all year?
-

  2. What were the most watts generated in the morning, afternoon, and evening? The least?
-

  3. What is the average number of watts generated on January afternoons (i.e, afternoons for the first 31
  days)?
-

  4. How many days did the system generate fewer than 500 watts total (in the morning, afternoon, and
  evening)?
-

  5. What is the average number of watts generated in the morning, afternoon, and evening all year? Based
  on what you find, which direction do you believe the solar panels are facing?
-
