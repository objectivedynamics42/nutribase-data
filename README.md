# Overview
This repo holds the files that provide the data for the _NutriBase_ application.
All data is stored in a pair of [json](https://www.w3schools.com/js/js_json_syntax.asp) files. 

The data comprises two fundamental types:
* Tag
* Food
# Tag
A _Tag_ is a term that can be applied to one or more foods, opening  up the possibility of _NutriBase_ being able to display flexible groupings of foods. You can add as many tags as you require. 

Here is an example of a tag that could be used to group items such as _bread_,_cakes_ and _muffins_:
```
    {
      "Name":"Bakery"
    },

```
Tag files have the following naming convention:
```
    tags.<version>.json
```
The current tag file is:
```
    tags.v1.0.json
```

# Food
* Name - the name of the food item e.g. Apple, Bran or Sunflower Seeds
* Tags - a comma separated array of terms that can be used to group foods to which the tag is applied 
* kCalPer100g - this property defines the calorific value of a quantity of the food. By default this is for 100g but you can override the meaning of the value using the kCalUnit property. See below
* kCalUnit - this enables you to provide a custom caption for the kCal amount

Here is an example that uses a non-default value for _kCalUnit_:
```
    {
      "Name":"Bread - Wholemeal",
      "kCalPer100g":"121",
	  "kCalUnit":"Calories per round:",
      "Tags":["Bakery"]
    },
```


Food files have the following naming convention:
```
    foods.<version>.json
```
The current tag file is:
```
    foods.v1.0.json
```


