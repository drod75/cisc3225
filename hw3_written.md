1 Planets (12 points)
    Access the following dataset for this assignment:
    https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/planets.csv.
    It is from a dataset about exoplanets, or planets discovered outside of our solar system. Answer the
    following questions. Where applicable, query Pandas using bitwise logical operators (&, |, ∼).
    
    
    1. How many exoplanets are missing an orbital period? Missing a mass? Missing a distance?
        Missing orbital is: 43
        Missing mass is: 522
        Missing distance is: 227
        Missing year is: 0
        Missing method is: 0
        Missing number is: 0

    2. How many exoplanets are missing both orbital period and mass?
        43

    3. How many exoplanets are missing orbital period, mass, and distance?
        11

    4. Produce a DataFrame containing all exoplanets with missing mass. Which discovery method found
    the most exoplanets with missing mass?
        Transit

    5. Did the discovery method from Question 4 find any exoplanets with a known mass?
        Yes

    6. Given the evidence you just found, do you think it is possible to determine exoplanet mass using the
    discovery method from Question 5? Do some independent research on this discovery method to confirm
    your hypothesis. Include links to references you find.
        No, the transit method is used to find the radius but not the mass.

        'Transiting planets are highly prized in exoplanet science because we find out so much more about them. When we discover a new planetary system by measuring its reflex motion (radial velocity), there's always some missing information. This technique can't measure the inclination of the planet's orbit relative to us, and this leads to an uncertainty over the planet's true mass.'

        -https://lco.global/spacebook/exoplanets/transit-method/#:~:text=Like%20the%20radial%20velocity%20method%2C%20this%20method,frequently%20so%20they%20are%20easier%20to%20detect.&text=This%20technique%20can%27t%20measure%20the%20inclination%20of,an%20uncertainty%20over%20the%20planet%27s%20true%20mass.


2 College (16 points)
    The following datasets contain enrollment data from a fictional college for the Fall 2015/Spring 2016 academic
    year:

    * https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/college/students.csv:
    A listing of students and their ID.

    * https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/college/clubs.csv:
    A listing of clubs that students belong to.

    * https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/college/courses.csv:
    A listing of course numbers and names (scraped from the Brooklyn College website)

    * https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/college/f15.csv:
    Enrollment data from Fall 2015.

    * https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/college/s16.csv:
    Enrollment data from Spring 2016.

    Using a combination of Pandas features, including concatenation, merging, and grouping, answer the
    following questions. Avoid using loops.


    1. Use merging to produce a DataFrame showing which students belong to which clubs.
    2. In Question 1, did you perform a one-to-one, many-to-one, or many-to-many merge? Why?
        many to one because in the students df there are no duplicates, while in the clubs dataframe there are, so by performing many to one we keep the duplicates in clubs and associate each with a student name, this is because students have no reason not to be part of multiple clubs
    3. Are there any students who are not in any clubs? If so, how many? Show their names and student ID.
                id	name
        8	3822320	Jon
        9	9548347	Jennifer
        10	5131111	Leah
        11	2227757	Grace
        12	1802931	Troy


    4. Use merging to produce a DataFrame showing the names of courses that students enrolled in.
            student_id	course	grade	points_earned	max_points	course_name	student_name
        0	1015901	1597	a	4	4	New Media and Business	Scott
        1	1015901	1215	a	4	4	Intro to Programming in Python	Scott
        2	1015901	2210	a	4	4	Discrete Structure	Scott
        3	1015901	1590	b	3	4	Management Information Systems	Scott
        4	1017158	1001	a	4	4	Computing &Quantitative Reason	Ernest

    5. In Question 4, did you perform a one-to-one, many-to-one, or many-to-many merge? Why?
        I performed many to one, students has no duplicate ids but courses does, so many to one attributes the many duplicates in courses with the name of the student in ids, same for courses
    6. For the whole F15/S16 academic year, what is the name of the course that is probably the hardest?
    Which is probably the easiest? Ignore withdrawals when determining the answer.
        Based on the pass to fail ratio, Management Information Systems	is the easiest and Intro to Computer Applications is the hardest

    7. Did any students not enroll in any course during the whole F15/S16 academic year? Who?
        Yes	
                id	name
        420	9224256	Ron


    8. Over the whole F15/S16 academic year, what career was most common among students taking 1215?
        gamedev          19
        research         15
        finance          15
        consulting       13
        robotics         13
        security         12
        graphics         12
        publishing       11
        hardware         11
        startup          10
        ecommerce         7
        education         7
        manufacturing     6
        self-employed     6
        logistics         5

3 Concatenation (8 points)
    For this section, you do not need to write code. Refer to the following DataFrames:
    df1:


    1. Show the result if we concatenate df1, df2 with axis=0.
        pd.concat([df1, df2], axis=0)
    2. Show the result if we concatenate df1, df2 with axis=1.
        df_c2 = pd.concat([df1, df2], axis=1)
    3. Assume df2 has columns ‘c’, ‘d’ instead of ‘a’, ‘b’. Show the result if we concatenate df1, df2 with axis=0.
        pd.concat([df1, df2], axis=0)
    4. Assume df2 has columns ‘c’, ‘d’ instead of ‘a’, ‘b’. Show the result if we concatenate df1, df2 with axis=1.
        pd.concat([df1, df2], axis=1)

4 Merging (14 points)
    For this section, you do not need to write code. Refer to the following DataFrames:
    books:


    1. What type (one-to-one, many-to-one, many-to-many) is the merge across books and genres? Why?
        One to one, as there is is no duplicate values many to one or the reverse is not needed, one to one is just fine
    2. What type (one-to-one, many-to-many, many-to-many) is the merge across genres and favorites? Why?
        Many to One as we have people with lots of favorites on the left side aka genre and no duplicates on the right so many to one would provide all of the rows on the left with a row on the right, thus not reducing the favorites on the left side.
    3. What type (one-to-one, many-to-many, many-to-many) is the merge across genres and read? Why?
        Many to one becuase while there is no duplicate genre there are duplicate reads to provding the many reads with a genre name that coresponds would be the best option.
    4. Show the result of performing a merge across genres (left) and favorites (right) for each of the following
    merges:
        (a) Left
        pd.merge(genres_df, favorites_df, how='left', on='genre')
        Left merging provides everything on the left with a match so in this cases all the genres in genre_df are given the matches they have in favorites_Df and in this case they are all either fullfilled or not.
        (b) Right
        pd.merge(genres_df, favorites_df, how='right', on='genre')
        Right merging provided everything on the right with the match they have in genres or simply has none, so its similat to the left result but instead of name having none isbn has nan because we weren't provided with all the isbns possible or names for the last question.
        (c) Inner
        pd.merge(genres_df, favorites_df, how='inner', on='genre')
        Inner merging provides everything with a match so we got no none nan values, this is useful for making sure we see the actual matching rows and nothing else.
        (d) Outer
        pd.merge(genres_df, favorites_df, how='outer', on='genre')
        Outer merge just shows you everything which can be useful to gain a view on the entier merged data.
