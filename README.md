# FINTECH PROJECT 2 - RICE UNIVERSITY FINTECH BOOT CAMP ![RICE](./Todd's%20project%20folder/images/Rice_logo_name.png)

# Project 2 - Video Game Recommendation Bot - *VGR BOT*

This program is designed around the web site https://store.steampowered.com/ that is self described simply as:

    Steam is the ultimate destination for playing, discussing, and creating games.


At the time this author was evaluating elements and attributes of Steam, this was displayed on the initial splash page of the web site:

![Steam](./Todd's%20project%20folder/images/Steam_splash_page.png)

Steam has a deep user base from which to draw data that we will evaluate and are to be utilized in tandem with new data sets pulled from www.kaggle.com and includes valuable datasets that evaluate the User based ratings found with each game.  Kaggle.com details in one of their "Steam" related data sets called "Steam-200k.csv", and describes the file in the following way:

    About this file: Steam is the world's most popular PC Gaming hub. With a massive collection that includes everything from AAA blockbusters to small indie titles, great discovery tools can be super valuable for Steam. How can we make them better?

    This dataset is a list of user behaviors, with columns: user-id, game-title, behavior-name, value. The behaviors included are 'purchase' and 'play'. The value indicates the degree to which the behavior was performed - in the case of 'purchase' the value is always 1, and in the case of 'play' the value represents the number of hours the user has played the game.

This is just one of many datasets found via Kaggle that evaluate the metrics of the Steam web site.  

Along with the comments from each user there is a binary rating system.  Essentially a digital "thumbs up" or "thumbs down" rating.  We are identifying with the "thumbs up" rating and calling it a "positive" rating.  That is captured in the data sets that are pulled from http://store.steampowered.com.

# Goal of the VGR BOT

Our Group 1 - Project 2 is playing the role of independent developers utilizing state-of-the-art machine learning techniques to sell our VGR BOT to Steam (and others) by doing the following:

    1. Use already existing data within Steam to grow sales.

    2. Build in a Video Game Recommendation BOT to reside within Steam.

    3. The BOT will evaluate user data and the warehouse of titles to recommend probably choices for the user to purchase or play (and then purchase) on Steam.

    4. The BOT will resemble the features found on numerous web sites like Amazon that say, "Customers who bought these items also liked/searched for these items."  

    5. The BOT will show the recommended videos to the user as Steam sees fit, but we recommend using the recommendation BOT when: 
        A. The User logs onto Steam but has not selected their title
        B. After a user selects a title.
        C. When a user completes or shuts down a game prior to exit.  

    6. This provides numerous ways to promote various games to users including new video game titles and high margin legacy video game titles.  

    7. Our sales team believes we can assist in increasing profits at Steam by 30% to 50% by just mining their existing user base and using the VGR BOT.

# Methodology

We will be using Collaborative Filtering to base our VGR BOT upon.  As quoted from "Real Python" (https://realpython.com/build-recommendation-engine-collaborative-filtering/)  

    "Collaborative Filtering is the most common technique used when it comes to building intelligent recommender systems that can learn to give better recommendations as more information about users is collected.

    Most websites like Amazon, YouTube, and Netflix use collaborative filtering as a part of their sophisticated recommendation systems. You can use this technique to build recommenders that give suggestions to a user on the basis of the likes and dislikes of similar users."

All of the graphics below were taken from the web site on realpython.com cited above:

We feel like this is a smart choice for making our VGR BOT.  It is unsupervised learning and the premise is that we do the following:

    1. Matrix Factorization - This is basic matrix multiplication.  
        A. If you have User History and ratings, you can show it as one matrix.  
![User_matrix]("../Todd's project folder/images/matrix_User.png")

        B. This User matrix is then multiplied by the feature matrix.  

![Feature_matrix]("../Todd's project folder/images/Feature_matrix.png")

        C. The result is a matrix that defines User ratings and options for recommendation related to features.  

![Resultant_matrix]("../Todd's project folder/images/result_matrix.png")


# Cleaning and Preparing the Data

There is extraneous data and columns that need to be removed and the code below shows how that's done and the resultant dataframe.  

![Data_cleaning]("../Todd's project folder/images/cleaning_data.png")

# Preparing the training and testing sets.  

The program shows how the data is further prepared and configured into training and testing data sets and the resultant arrays, as shown below.

![training_testing]("../Todd's project folder/images/training_testing.png")

# Employ Tensorflow

At this point in the program, the data is further segregated for analysis.  Certain biases are applied to take into account the different user behaviors and certain game attributes.  

From there, the training and testing are performed iteratively until a reasonable precision is achieved.  

At that point in the process, the recommendation engine is in place and ready to be deployed.  When the program is deployed, it iteratively checks each user's history of purchased software, hours played, genre, etc.  Given the user's data, the VGR BOT makes specific recommendations for specific users.  Sample output is show below.  

![final_recommendations]("../Todd's project folder/images/final_recommendations.png")



---

## Installation Guide


### *This is how the libraries are imported into the program.  These import statements reside at the top of the code and are executed first.*

Written in python and utiizing the following libraries:

    import numpy as np # linear algebra
    import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
    import os
    !pip install tensorflow==1.14
    import random
    from collections import Counter
    from sklearn.metrics import roc_curve, auc, average_precision_score
    import tensorflow as tf
    tf.__version__

    
numpy: https://numpy.org/

pandas: https://pandas.pydata.org/

os: https://docs.python.org/3/library/os.html

!pip install tensorflow == 1.14:  https://www.tensorflow.org/install/pip

random: https://docs.python.org/3/library/random.html

from collections import Counter: https://docs.python.org/3/library/collections.html

from sklearn.metrics import roc_curve, auc, average_precision_score: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.auc.html

tensorflow: https://www.tensorflow.org/resources/learn-ml?gclid=CjwKCAjwiJqWBhBdEiwAtESPaDqYjiqoHJ3p3fpsSI0VGqSX4KSfFhYJYiQRjo7cpn5K0rNoEsZYQBoCcgAQAvD_BwE



## Contributors

All of the work was performed by Qristian Walker, Richard Kell and Christopher Todd Garner

Qristian Walker is solely responsible for the code. 
Richard Kell is solely responsible for the PowerPoint presentation materials.
Christopher Todd Garner is solely responsible for this README.md.

Much of the work shown here in this README.md is based upon the very helpful link in kaggle.com:  https://www.kaggle.com/code/jwyang91/steam-game-recommender

---

## License

You may use this code as you see fit as long as any copy and paste is done so with proper sourcing of materials back to this repository.                                      
