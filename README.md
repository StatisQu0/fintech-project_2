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

Along with the comments from each user there is a binary rating system.  Essentially a digital "thumbs up" or "thumbs down" rating.  We are identifying with the "thumbs up" rating and calling it a "positive" rating.  That is captured in the data sets that are pulled from [STEAM?].

[QRISTIAN AND RICHARD - MATERIALS FOUND BELOW ARE LEFT OVER FROM PRIOR CHALLENGES/PROJECTS - I USE THEM ONLY AS OUTLINES AND THEN FILL IN]


# Instructions
        *There was no material change in the 4 iterations that I performed*

# Evaluate a New Machine Learning Classifier

Create an Evaluation Report
As mentioned throughout this README files, the differrences were not dramatic.  I was already late and actually spent Monday - Wednesday tweaking the model and making sure it was being done correctly and applying the LogisticRegression along side.  

1. If time were not an issue:

    A. I would have built the quasi-Monte Carlo simulator to solve for the peak values for the long and the short SMA.  

    B. I would then have selected several alternate methods of classifying the data in order to optimize the findings, as buided by the backtesting.  

Shown below are the results of the 4 differing iterations:

# Iteration 1 - Original Short and Long SMA

![Original Data](images/Original_ShortSMA_LongSMA%20-%20first%20before%20all.png)

![Original Classification Report](/images/Original_shortSma)

![Original Chart]()

![Original variables with LogisticRegression]()

# Iteration 2

# Iteration 3

# Iteration 4



---

## Technologies
This program was built entirely in tandem with the prepared questions in a Jupyter Notebook using Python and the associated libraries noted above.  It was also built using Windows 10 on a Dell Laptop PC.  


---

## Installation Guide

[LEFT OVER FROM PRIOR PROJECTS/CHALLENGES]

### *This is how the libraries are imported into the program.  These import statements reside at the top of the code and are executed first.*

Written in python and utiizing the following libraries:

    import pandas as pd
    import numpy as np
    from pathlib import Path
    import hvplot.pandas
    import matplotlib.pyplot as plt
    from sklearn import svm
    from sklearn.preprocessing import StandardScaler
    from pandas.tseries.offsets import DateOffset
    from sklearn.metrics import classification_report 

pandas: https://pandas.pydata.org/

numpy: https://numpy.org/

Path (from pathlib): https://docs.python.org/3/library/pathlib.html

hvplot: https://hvplot.holoviz.org/user_guide/Introduction.html

matplotlib.pyplot: https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.html

sklearn: https://scikit-learn.org/

StandardScaler from sklearn.preprocessing: http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html

DateOffset from pandas.tseries.offsets: https://pandas.pydata.org/docs/reference/api/pandas.tseries.offsets.DateOffset.html

classification_report from sklearn.metrics: http://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html



## Contributors

All of the work was performed by Qristian Walker, Richard Kell and Christopher Todd Garner

---

## License

You may use this code as you see fit as long as any copy and paste is done so with proper sourcing of materials back to this repository.                                      
