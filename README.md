# Preservia.tech
Hack the North 2023 Project developed by Theodore, Helen, Alex, Freddy

More details are available on Devpost: https://devpost.com/software/expierly
## How to run
1. Install the requirements
2. Init the database with `flask db init`
3. Then prep the database with `flask db migrate` and `flask db upgrade`
4. Run the flask server with `python app.py`

## How to connect phone to computer to demo it from the phone
1. Set the phone as a hotspot
2. Connect the computer to the phone's hotspot
3. Make sure that in app.py, the host is set to 0.0.0.0
4. Take the secondary ip in the print when the server starts
5. On the phone, go to the ip address of the computer and the port 8000 like the print says
6. Proffit.

## Inspiration
As young adults, we're navigating the new waves of independence and university life, juggling numerous responsibilities and a busy schedule. Amidst the hustle, we often struggle to keep track of everything, including our groceries. It's all too common for food to get pushed to the back of the fridge, only to be rediscovered when it's too late and has gone bad. That’s how we came up with preservia - a personal grocery smart assistant designed to help you save money, reduce food waste, and enjoy fresher meals.

## What it does
Catalogue food conveniently: preservia.tech allows grocery shoppers to keep track of their purchased food, ensuring less goes to waste. Users take photos of their receipts and the app will identify the food items bought, estimate reasonable expiry timeframes, and catalogue them within a user-friendly virtual inventory. Users also have the option of directly photographing their grocery items and the app will add them to the database as well, or even manually enter items.

Inventory: The user interface offers intuitive control, allowing users to delete items from the inventory at their will once items are used. Users can also request the application to reevaluate expiry dates if they suspect any mistakes in the AI predictions.

Recipes: Additionally, users can select food items in their grocery inventory and prompt the application to suggest a recipe based on selected ingredients.

## How we built it
Preservia.tech is built around leveraging Large Language Models (Cohere) as flexible databases and answer engines, here to give nuanced answers about expiration, for even the most specific food! This allows us to enter any possible food item, and the AI systems will do their best to understand and classify them. The predictive power of Preservia.tech will only expand as LLMs grow.

OpenAI’s GPT-4 was also used as a flexible system to accurately decipher cryptic and generally unstandardized receipts, a task probably impossible without such models. GPT-4 is also the engine generating recipes.

We employed Google’s MediaPipe for food item classification, and converted images to text with API Ninjas to read the receipts.

Our app is primarily built on a Python backend for computation, with Flask to handle the web app, and mySQL as a database to track items. The web pages are written in HTML with some CSS and JavaScript.

We can connect it to a smartphone through a local network to take pictures more easily.

Challenges we ran into
Working with cutting edge APIs and AI was a brand-new challenge for the entire team, so we had to navigate different types of models and documentations, overcoming integration hell to eventually arrive at a successful project. We also found prompt engineering hard, especially trying to get the most accurate results possible.

It was all of our first times working with Flask, so there was a learning curve there. Deploying our app to online services like Replit or Azure also posed a major challenge.


