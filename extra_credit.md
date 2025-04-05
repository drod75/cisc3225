Extra Credit
10 points
Due March 19, 2025 at 11:00 AM

1 Exploratory Analysis: Pokemon (5 points)
The dataset for this assignment contains data about Pokemon:
https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/refs/heads/main/pokemon.csv
Using the exoplanet or wine exploratory analysis notebook as a model, perform an exploratory analysis

of the Pokemon dataset. In your analysis, address the following points:
1. What columns does the dataset contain? What are they, what do they mean, and what kind of values
do they contain? What is their type?
     0   attack          800 non-null    int64  
    1   base_happiness  800 non-null    int64  
    2   cap_rate        800 non-null    int64  
    3   defense         800 non-null    int64  
    4   exp_growth      800 non-null    int64  
    5   height          780 non-null    float64
    6   hp              800 non-null    int64  
    7   name            800 non-null    object 
    8   pokedex_number  800 non-null    int64  
    9   speed           800 non-null    int64  
    10  type_1          800 non-null    object 
    11  type_2          416 non-null    object 
    12  weight          780 non-null    float64
    13  generation      800 non-null    int64  
    14  is_legendary    800 non-null    int64  
dtypes: float64(2), int64(10), object(3)
(a) For any column you believe contains a categorical value (i.e., a specific set of discrete values
intended to be interpreted as categories), show which values the column contains and how many
instances of each there are.
    There are three categorical columns aka name, type_1, and type_2, name is the name and the types are the types for the pokemon, 
    pokemon have to have at least on type and each type they have must be distinct, so they can only have fire and not fire fire. This is what
    type 1 and 2 is.
(b) For any column you believe contains a continuous value (i.e., real numbers that are not constrained
to a specific set of values), produce a summary of their values with describe(). Do not include
categorical columns in this analysis.

2. Does the dataset contain any missing values? Which columns and how many?
(a) Of the columns with missing values, do you believe any could be the result of an oversight or
unavailable data? Which ones?
    Yes there are missing values, in height and type 2, type 2 makes sense since a second type is not mandatory, height meanwhile is very common so missing height values must be an error or weird case.
(b) Of the columns with missing values, do you believe any could communicate useful information?
In other words, does a NaN mean something about the Pokemon it is associated with?
    For type if there are actual missing type 2 it would be very useful because types have weaknesses and resistances, and mutli type pokemon have the two ladder options shared and in some cases cancel each other out. For height it could contain useful info for people looking to average any of the stats by height, so yes either column could have useful data.
3. Pick 5 continuous numeric columns and visualize them with either histograms or box plots. Pick one
that looks interesting and describe what you see.
(a) Describe the range that the majority of values in the column. Give an upper and lower boundary.
     For speed the lower boundry lies between about 5 and the upper boundry is a bit under 150, the majority of points lie between just under 50 around 80
(b) Are there any outliers? Roughly how many are there (i.e., a lot or a few?), and how extreme are
they?
    There are outlier values and there seems to be just a few, the majority of them are at around 150 while 1 is some were near 160 and one is all the way above 175.
4. Look for correlations between the continuous numeric columns. Identify one moderate to strong cor-
relation and discuss the relationship between the two columns.
    One moderate to strong correlation is weight and height, this make sense as beings of a ceratin height typically have a certain weight, or that more pounds and weight are to put to taller pokemon to make them seem fit or normally sized compared to their height.


2 Grouping (2 points)
Use the Pokemon dataset to answer the following questions:

1. Which type(s) in the Type 1 column contain the heaviest Pokemon? The lightest?
    It seems that typically steel types have the heaviest pokemon, with ground at a good second, this is because metal is culturally heavier and in pokemon steel pokemon can be very heavy, this can apply to ground pokemon to but steel pokemon contain very heavy examples like aagron, steelix, and metagross
2. On average, which generation is easiest to catch? The higher the capture rate, the easier the Pokemon
is to catch.
    It seems that the generation with the higher capture rate on average and most occuring is generation, generation 3 had a mean leading by 6 points and a median leading by a whopping 15.


3 Hierarchical Indexing (3 points)
Make the Type 1 and Type 2 columns a hierarchical index on the Pokemon dataset. Then show how to
retrieve the following queries using IndexSlice objects. If possible, complete the query in a single .loc/.iloc
operation.

1. The average weight of water (Type 1) Pokemon.
    weight 	68.524418
2. The average weight of water (Type 1) bug (type2) Pokemon.
    weight 	43
3. The average weight of bug (Type 2) Pokemon shorter than 1m.
                weight
    type_1 	type_2 	
    poison 	bug 	12.0
