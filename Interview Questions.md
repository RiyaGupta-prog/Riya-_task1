1. What are the different types of missing data?
There are three main types:
MCAR (Missing Completely at Random): The missing data isn't related to anything in your dataset—it's just randomly missing.
MAR (Missing at Random): The missingness is related to something else in your data, but not the actual missing value.
MNAR (Missing Not at Random): This one's tricky—the missing value is missing because of its own value. So there's some bias involved.

2. How do you handle categorical variables?
A few common techniques:
Label encoding turns categories into numbers—good for binary or ordered categories.
One-hot encoding makes new columns for each category—great for non-ordered stuff like cities or colors.
There’s also ordinal encoding for when the categories have a natural order (like "small", "medium", "large").
For some advanced stuff, target encoding replaces categories with the mean of the target variable.

3. What’s the difference between normalization and standardization?
Both are ways to scale your data:
Normalization squishes everything into a 0–1 range—great when you know your min and max.
Standardization centers your data around 0 with a standard deviation of 1—useful when you don’t know the range or when your data has outliers.

4. How do you detect outliers?
Boxplots are my go-to for a quick visual.
You can also use z-scores or the IQR method to spot numbers that are way off.
For more advanced cases, models like Isolation Forest or DBSCAN help find outliers based on patterns in the data.

5. Why is preprocessing important in machine learning?
Because models are picky! Preprocessing helps clean up messy data, makes features easier to compare, and ensures the model doesn't learn the wrong thing. Honestly, a good model with bad data is like trying to build a house on sand.

6. One-hot encoding vs label encoding—what’s the difference?
Label encoding gives each category a number. It's fast, but risky if the model thinks those numbers have meaning.
One-hot encoding avoids that by turning each category into its own column with 1s and 0s. It’s safer for unordered categories but can create a lot of new columns.

7. How do you handle data imbalance?
If one class massively outweighs the others:
You can resample—either oversample the minority class or undersample the majority.
Use techniques like SMOTE to generate synthetic samples.
Or tweak model settings to weight the classes differently.
Some algorithms also have built-in ways to handle imbalance, like Balanced Random Forest.

8. Can preprocessing affect model accuracy?
Oh, definitely. Good preprocessing can boost your model's performance big time. But if you skip steps—or do them wrong—you might confuse the model or bury important signals in noise. It’s like prepping ingredients before cooking: if you don’t chop the veggies right, the dish won’t turn out well.