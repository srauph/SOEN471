<h1 align="center">Food.com Recipe Recommender</h1>
<h3 align="center">SOEN 471 - Big Data Analytics Project</h3>

## Abstract

This project proposes a food recommender system that utilizes user preferences and dietary restrictions to suggest meals that are both personalized and healthy. The dataset used includes more than 230K recipes and 1M reviews that were uploaded to Food.com over the course of 18 years (formerly GeniusKitchen). Using this data, the system applies a recommendation algorithm to suggest meals that meet the user's dietary restrictions, health goals, and taste preferences. Additionally, the system provides nutritional information for each recommended meal and offers the option to filter meals by specific macro and micronutrient requirements. The proposed system aims to assist users in making informed food choices and to encourage healthier eating habits.

## Table of Contents

- [Dataset Description](#dataset-description)
- [Research Question (1)](#research-question-1)
- [Research Question (2)](#research-question-2)
- [Model Classes](#model-classes)
- [Algorithm (1)](#algorithm-1)
- [Algorithm (2)](#algorithm-2)
- [Team Members](#team-members)

## Dataset Description

The dataset can be found [here](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions).  

### Dataset Statistics

| Feature | Counts |
| ----------- | ----------- |
| Recipes | 230K+ |
| Interactions | 1M+ |

### Metadata
- Ratings and Reviews. 
- Recipe Name, Description, Ingredients, and Directions. 
- Recipe Categories (Tags). 
- Recipe Nutrition Information. 

The two .csv files of particular interest for this project are `RAW_interactions.csv` and `RAW_recipes.csv`. Here the `RAW_interactions.csv` file contains metadata relating to users, their ratings for particular recipes and any reviews they may have left. The other dataset, `RAW_recipes.csv` contains information about particular recipes. Dataset features are well described using their column names. Moreover, the feature types are standard python feature types including (but not limited to) integers, strings and lists. See below for an example tuple from the datasets.

<h3 align="center">RAW_interactions.csv</h3>

```python
{
  "user_id": 38094,
  "recipe_id": 40893,
  "date": "2003-02-17",
  "rating": 4,
  "review": "Great with a salad. Cooked on top of stove for..."
}
```

<h3 align="center">RAW_recipes.csv</h3>

```python
{
  "name": "arriba baked winter squash mexican style",
  "id": 137739,
  "minutes": 55,
  "contributor_id": 47892,
  "submitted": "2005-09-16",
  "tags": ['60-minutes-or-less', 'time-to-make', ... , ],
  "nutrition": [51.5,0,13,0,2,0,4],
  "n_steps": 11,
  "steps": ['depending on size of squash , cut into half or fourths', 'remove seeds', ... , ],
  "description": "autumn is my favorite time of year to cook! this recipe ... ",
  "ingredients": ['winter squash', 'mexican seasoning', 'mixed spice', ... , ],
  "n_ingredients": 7
}
```

## Research question (1): 
How can the recommender system take into account the availability of ingredients in a user's pantry when recommending recipes?

## Research question (2):
How can the recommender system personalize recipe recommendations based on the user's preferences (i.e calories)?

## Model classes

 - Recommender Engine + KNN
    - To answer the first research question, we can make use of ingredient information from recommended recipes and transform it into a vectorized format. The model would then compare the user's pantry inventory to the recommended recipe's ingredients vector using similarity measures such as cosine similarity or Jaccard similarity. Recipes that have a higher similarity score would be recommended to the user.

- Collaborative Filtering
    - Collaborative filtering could be used to identify users with similar preferences in terms of calorie intake, and recommend recipes that have been positively rated by those users. Additionally, collaborative filtering can be enhanced by incorporating additional user and recipe features, such as dietary restrictions, cooking time, ingredients, and cuisine type, to provide even more personalized recommendations. 


## Algorithm (1)
Content based recommender engine + KNN (to filter out recipes that do not match the users pantry of ingredients). The KNN method will make use of one hot encoding to check similarity between vectors. For example, in a scenario where the only ingredients for a recipe are ``[apple, banana, pear]`` and the pantry of a user has ``[apple, pear]`` and all the ingredients in existance are ``[kiwi, apple, banana, pear]``- the similarity between ``[0,1,1,1]`` and ``[0,1,0,1]`` will be compared.

## Algorithm (2)
Collaborative Filtering Recommender System (to match users with similar dietry preferences to each other). This perhaps could be done by looking metadata of each recipe. For instance nutrition facts of a recipe.

 ---
 
<h2 align="center">Team Members</h2>

<div align="center">
  <table>
    <tr>
      <td align="center"><a href="https://github.com/Zafirmk"><img src="https://avatars.githubusercontent.com/u/42074951?v=4" width="100px;" alt=""/><br /><sub><b>Zafir Khalid</b></sub></a></td>
      <td align="center"><a href="https://github.com/srauph"><img src="https://avatars.githubusercontent.com/u/47877347?v=4" width="100px;" alt=""/><br /><sub><b>Shuaib Rauph</b></sub></a></td>
    </tr>
    <tr>
      <td align="center"><a href="https://github.com/MarwaKhalid"><img src="https://avatars.githubusercontent.com/u/71287263?v=4" width="100px;" alt=""/><br /><sub><b>Marwa Khalid</b></sub></a></td>
      <td align="center"><a href="https://github.com/lailaalhalabi"><img src="https://avatars.githubusercontent.com/u/70773705?v=4" width="100px;" alt=""/><br /><sub><b>Laila Alhalabi</b></sub></a></td>
    </tr>
  </table>
</div>
