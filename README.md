<h1 align="center">Food.com Recipe Recommender</h1>
<h3 align="center">SOEN 471 - Big Data Analytics Project</h3>

## Table of Contents

- [Dataset Description](#dataset-description)
- [Research Question (1)](#research-question-1)
- [Research Question (2)](#research-question-2)
- [Model Classes](#model-classes)
- [Algorithm (1)](#algorithm-1)
- [Algorithm (2)](#algorithm-2)
- [Team Members](#team-members)




## Abstract

[ABSTRACT HERE]

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
[RESEARCH QUESTION 1 HERE]

## Research question (2):
[RESEARCH QUESTION 2 HERE]

## Model classes
[MODEL CLASSES HERE]

## Algorithm (1)
[ALGORITHM 1 HERE]

## Algorithm (2)
[ALGORITHM 2 HERE]
    
---
 
## Team Members

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
