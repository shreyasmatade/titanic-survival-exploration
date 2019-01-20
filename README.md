## Project: Titanic Survival Exploration

### Install

This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 2.7 installer and not the Python 3.x installer.

### Code

`titanic_survival_exploration.ipynb` - Model implementation and predictions.
`visuals.py` - Data visualisation and plots

### Run

In a terminal or command window, navigate to the top-level project directory `titanic_survival_exploration/` (that contains this README) and run one of the following commands:

```bash
jupyter notebook titanic_survival_exploration.ipynb
```
or
```bash
ipython notebook titanic_survival_exploration.ipynb
```

This will open the Jupyter Notebook software and project file in your web browser.

### Data

The dataset used in this project is included as `titanic_data.csv`. This dataset is provided by Udacity and contains the following attributes:

**Features**
- `pclass` : Passenger Class (1 = 1st; 2 = 2nd; 3 = 3rd)
- `name` : Name
- `sex` : Sex
- `age` : Age
- `sibsp` : Number of Siblings/Spouses Aboard
- `parch` : Number of Parents/Children Aboard
- `ticket` : Ticket Number
- `fare` : Passenger Fare
- `cabin` : Cabin
- `embarked` : Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

**Target Variable**
- `survival` : Survival (0 = No; 1 = Yes)

### Problem Statement

` Given the Titanic passanger data mentioned above, predict whether person survives or not `

### Implementation Details :

#### Custom Algorithm:  
Prediction_1 to Prediction_3 implements naive algorithms for servival prediction. By exploring features in the data I have formed different If else condition to predict whether person servives or not. 

#### Logistic Regression Model:
**Data Preparation :**
Features like 'Ticket', 'Cabin', 'PassangerId' are to specific and hold not good information about the servival of the person so I have droped these columns from final data.
Features like 'Pclass', 'Sex' , 'Embarked' are categorical variables, so it is important to convert them to seperate feature for betterment of model. I have used on hot encoding here.
Data is split in 80/20, Training / testing respectively
I have used sklearn LogisticRegression to train the model and predict.

#### Decision Tree Model: 
 Data preparation is same as used in above model. This model gives higher score of **93.27 %**.
