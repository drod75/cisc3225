## 1 Pokémon Visualizations (10 points)

For this section, download the Pokémon dataset from here: 
`https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/refs/heads/main/pokemon.csv`

If you like, you may experiment with different color schemes: 
see `https://matplotlib.org/stable/users/explain/colors/colormaps.html` for a listing of color maps available in 
Matplotlib. When plotting, you can indicate your chosen colors with the `cmap` argument. 
For example, if you want to use the "viridis" map, include `cmap="viridis"` into the plotting function.

### 1.1 Height across generations (10 points)

For this part, constrain the dataset to fire, water, and grass Pokémon (use the `type1` column).

1.  Produce a line plot of generation (x axis) and mean height per generation (y axis). 
Include a title and appropriate axis labels. Which generation has the tallest Pokemon? The shortest?

(see notebook)

2.  In Part 1, you should see a large spike in height at generation 3. 
Revise your previous plot so it shows lines for fire, grass, and water Pokémon separately. 
Include a legend in addition to an appropriate title and axis labels. 
Which type is responsible for the unusually tall Pokémon in generation 3?

It seems for generation 3 the pokemon with the skewed height from fire, grass, and water is water.

## 2 Statistical Tools (20 points)

For this section, use the camera dataset: 
`https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/refs/heads/main/cameras.csv`.

You may constrain your analysis to the following columns: 
`Release date`, `Max resolution`, `Effective pixels`, `Normal focus range`, `Weight (inc. batteries)`, and `Dimensions`.

For each statistical test you perform, give the null and alternative hypothesis. 
Use a significance level of 5% when evaluating p values, and indicate whether you are justified in rejecting the 
null hypothesis.

1.  Create a correlation matrix of the dataset. Find 1 interesting strong correlation and 1 interesting weak correlation. 
Briefly discuss what each correlation means. As part of your discussion, indicate whether each correlation is significant.

2.  How much does max resolution increase each year? By how much?

3.  Split the dataset in two: one for cameras released on or after 2004, and one for cameras released before 2004. 
Is the mean camera weight different across these time periods? Is it significant?

4.  Using the before/after 2004 split, create a contingency table showing how many cameras were released for each brand 
(rows) in each time period (columns). Are there significant differences in brand distribution before and after 2004? 
Which brands released a very different number of cameras than expected?
