## Helping to pick the best cover photo for real estate listings

### Project Motivation

The world we live in today is a digital one and searching for a home is no different. The typical buyer searches for properties online by checking websites with images of a house. Most of the websites(zillow, trulia, realtor.com and others) are structured in a way that potential buyer sees a cover image first before other photos of a listed house and that is why it is extremely important to select that picture wisely. Many sellers (homeowners, real estate agents, brokers...),however, do not pay enough attention to the quality of a listing photos of a houses so, the goal of my project is to help sellers to pick the best cover photos of their houses to make them look more attractive for the home buyers.


### Dataset
I have considering 2 options to collect the relevant data for my project:

1. Extract data from websites.

2.Use existing datasets.

I could not extract enough data from the websites because of their security measures so, I decided to search for existing datasets. I found two good datasets on Kaggle and Github:

Github - https://github.com/emanhamed/Houses-dataset.git

Kaggle - https://www.kaggle.com/ted8080/house-prices-and-images-socal

After analyzing both of them, I have decided to continue with Github dataset. Even though it contains smaller number of pictures (2,136) compare to one from Kaggle (15,000), I chose Github dataset because, unlike the other one, it has 4 images for each house ( bedroom, bathroom, kitchen and a frontal image of the house) which is exactly what I need for my project because not only the front image of a house can be the most attractive part of a listed property.


### Modeling

The goal of this project is to help sellers to present their listed properties in the best possible way by choosing a cover photo which will attract buyers' attention. To achieve my goal I have been using dataset which contains 4 pictures for each house together with prices of that house. During data preprocessing stage I defined a constant baseline which I had to beat. To increase number of pictures and improve prediction results I used augmentation technique but first I used EfficientNet model architecture to scale all dimensions of depth/width/resolution. In the result models training (3 models) I could compare their results(MSE) and picked the best one(Adapted EfficientNet) which beat a baseline. Also, in the notebook you can find images of a houses with true and predicted prices linked to them.


## Future work

1. Gather more data

2. Arrange pictures in order (from the most "expensive" to the "cheapest")

3. Find some general patterns which can make a picture look better.


