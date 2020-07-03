# Recipe-Week-Planer

This app is a recipe week planer. A user can fill his week with recipes and the app
calculates what ingredients the user has to buy for the whole week.

## Functionalities
- Users can create (edit and delete) recipes
- Users can browse recipes
- Users can add recipes to the week schedule
- The app calculates how many ingredients to buy for a week

## Database

### User
-  username: String
-  password hash: String
-  has_one weekplan: Array with day objects (e.g. [{ monday: [recipe1], [recipe2], [recipe3], tuesday: [recipe4]...}])
-  has_many recipes

### Recipe
-  title: String
-  ingredients: Array with ingredient objects (e.g. [{ sugar: 3teaspoons }, { water: 4l }])
-  description: String
-  belongs_to user

### Weekplan
-  weekplan: Array with day objects (e.g. [{mondy: [recipe1], ...}])
-  belongs_to user
