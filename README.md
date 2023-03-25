# VideoGamesDataAnalysis_Using_Python

It is a brief analysis on the Video Games dataset taken from Kaggle website.

![Video Games Data](https://user-images.githubusercontent.com/72240938/227703334-97b290a1-6ee3-4756-a125-3e2184d9e812.jpg)


### Tool Used: Pycharm

Here, I asked several questions with respect to the dataset and on that basis and then answered them using Python.
First of all, I loaded the libraries required for analysis and the dataset as shown below:

![image](https://user-images.githubusercontent.com/72240938/227702893-c3e3b877-1124-498b-8ed5-e581ca2b23ef.png)


1. Remove all the records with null values in any of the columns.

## Code:

df.dropna()

## Output:

The above command removes all the records containing null values in the records present in the table.

2. Find the count of different genres in the table.

## Code:

![image](https://user-images.githubusercontent.com/72240938/227703041-7d881b8b-5d22-4b32-ae62-ffaf89601ec4.png)

## Output:

![image](https://user-images.githubusercontent.com/72240938/227703056-b7b52e49-f6a6-464d-85aa-13ad64f4a882.png)



3. Find the Total North America Sales overall.

## Code:

Total_NA_Sales_Sum = df['NA_Sales'].sum()
print(Total_NA_Sales_Sum)

## Output:

![image](https://user-images.githubusercontent.com/72240938/227703093-ee6be7d4-0077-43c8-a609-bcd0a59a3af6.png)


4. Find the Global Sales for all Genres respectively and their distribution overall and find the genre which has no outliers.

## Code:
sns.boxplot(x='Genre', y= 'Global_Sales', data=df)
plt.show()


## Output:

![image](https://user-images.githubusercontent.com/72240938/227703140-f8d37f48-af82-42bc-950b-942e38594eed.png)

"Strategy" Genre has no outliers and Platform has the maximum Global sales among the genres.


5. Find the year in which maximum and minimum videos were released.

## Code:
year_of_release_count = df['Year_of_Release'].value_counts()
print(year_of_release_count)


## Output:

2008 has the most number of videos released i.e. 1427 whereas 2020 has the least number of videos released i.e. 1.


6. Compare Global Sales Vs North America, Japanese and Europe Sales in the dataset and find which country sales among the three countries are the most correlated with Global Sales.

## Code:

sns.lmplot(x='NA_Sales', y='Global_Sales', data=df )
sns.lmplot(x='JP_Sales', y='Global_Sales', data=df )
sns.lmplot(x='EU_Sales', y='Global_Sales', data=df )
plt.show()


## Output:

![image](https://user-images.githubusercontent.com/72240938/227703241-a56e1ec5-476d-4ebf-838e-6a879ec7b376.png)

![image](https://user-images.githubusercontent.com/72240938/227703250-b02d8a03-ec57-432e-bc12-bd86aa926087.png)

![image](https://user-images.githubusercontent.com/72240938/227703262-d17fed2e-ae37-41c2-9ff8-8dd389f5fe73.png)


According to the three plots, Global Sales are most correlated with North America Sales and have the least number of outliers among the three plots.



