<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recipe Generator</title>
    <link rel="stylesheet" href="/static/style.css">
</head>
<body>
    <header>
        <h1>Recipe Generator</h1>
    </header>

    <div class="container">
        <section class="form-section">
            <h2>Enter Your Preferences</h2>
            <form id="recipeForm" action="/generate_recipe" method="post">
                <div class="form-group">
                    <label for="ingredients">Ingredients (separated by commas):</label><br>
                    <textarea id="ingredients" name="ingredients" rows="4" cols="50" required></textarea>
                </div>

                <div class="form-group">
                    <label for="mealType">Meal Type:</label>
                    <select id="mealType" name="mealType" required>
                        <option value="breakfast">Breakfast</option>
                        <option value="lunch">Lunch</option>
                        <option value="dinner">Dinner</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>Diet Type:</label><br>
                    <input type="radio" id="veg" name="dietType" value="vegetarian" required>
                    <label for="veg">Vegetarian</label>
                    <input type="radio" id="nonVeg" name="dietType" value="non-vegetarian" required>
                    <label for="nonVeg">Non-Vegetarian</label>
                </div>

                <button type="submit">Generate Recipe</button>
            </form>
        </section>
    </div>

    <!-- Placeholder for displaying recipe details -->
    <div class="recipe-details">
        <h2>Recipe Details</h2>
        <p><strong>Procedure:</strong> <!-- Procedure will be displayed here --></p>
        <p><strong>Calorie Intake:</strong> <!-- Calorie intake will be displayed here --></p>
        <p><strong>Cooking Time:</strong> <!-- Cooking time will be displayed here --></p>
        <p><strong>Nutritional Facts:</strong> <!-- Nutritional facts will be displayed here --></p>
        <p><strong>Historical Facts:</strong> <!-- Historical facts will be displayed here --></p>
    </div>
</body>
</html>
