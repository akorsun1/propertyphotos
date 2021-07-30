## Helping to pick the best cover photo for real estate listings

### Project Motivation

The world we live in today is a digital one and searching for a home is no different. The typical buyer searches for properties online by checking websites with available images of a house. Most of the websites(zillow, trulia, realtor.com and others) are structured in a way that potential buyer sees a cover image first before other photos of a listed house and that is why it is extremely important to select that picture wisely. Many sellers (homeowners, real estate agents, brokers...),however, do not pay enough attention to the quality of a listing photos of a houses so, the goal of my project is to help sellers to pick the best cover photos of their houses to sell them faster.

### Dataset

I have been considering 2 options to collect the relevant data for my project:

1. Extract data from websites.

2. Use existing datasets.

I could not extract enough data from the websites because of their security measures so I decided to search for existing datasets. I found two good datasets on Kaggle and Github:

Github - https://github.com/emanhamed/Houses-dataset.git

Kaggle - https://www.kaggle.com/ted8080/house-prices-and-images-socal

After analyzing both of them, I have decided to continue with Github dataset. Even though it contains smaller number of pictures (2,136) compare to one from Kaggle (15,000), I chose Github dataset because it has 4 images for each house ( bedroom, bathroom, kitchen and a frontal image of the house) which is exactly what I need for my project because not only the front image of a house can be the best option to present a house(the dataset from Kaggle contains mostly front images of houses).

### Modeling

For this project I used ImageDataGenerators and Pandas DataFrames to load my dataset then I augmented my images to improve prediction results; next, I plotted augmentations. Also, I adapted EfficientNet to a regression. In my modeling section I built 3 models (Simple Dense Model, Simple CNN and Adapted EfficientNet) and compared their results.

### Results

Based on validation error results, AdaptedEfficientNet has the lowest validation score (240934572092) so I managed to beat a benchmark (289255608280) and visualize predicted price and true price ( you can find visualization in notebook).

## Future work

1. Gather more data

2. Arrange pictures in order (from the most "expensive" to the "cheapest")

3. Find some general patterns which can make a picture look better.


