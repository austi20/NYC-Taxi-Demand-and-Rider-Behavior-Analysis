# NYC-Taxi-Demand-and-Rider-Behavior-Analysis

Data analysis and predictive modeling project using 2023 NYC Yellow Taxi trip data to study rider behavior, taxi demand, trip duration, fare prediction, and tipping patterns.

## CMSE 202 Group 4 Project

## Members:
- Rafin Ahon
- Rashik Alahi
- Gunnar Austin
- Connor Curtis
- Emily Evans

## Main Research Question
### How do rider behavior patterns across time, location, and trip characteristics- shape taxi demand, trip duration, fares, and tipping outcomes in New York City?

---

## Team Members and Assigned Subtopics

Each team member was responsible for writing the code and analysis for their assigned subtopic. Below is the breakdown:

### 1. Connor Curtis
**Subtopic:** Investigating New York Taxi Traffic via Network Graphing/Modeling  

**Description of Code and Contributions:**  

<u>My Contributions:</u>

I found, filtered and downloaded the data set for our group to use. Additionally, I loaded the main data set into our workspace (taxi.csv) and performed some cleaning by altering some columns into a more usable form, deleting unnecessary columns, and shortening the data due to it having millions of rows. Additionally, I set up a workspace for each group member to use within the notebook in order to help us stay organized. 

Being responsible for sub-topic #1, I am also responsible for all of the code within that section pertaining to network graphing which includes finding and downloading the secondary data set (taxi_zones.csv). Thus, I am also responsible for the portions of the presentation and the written report pertaining to my subtopic, as well as some of the introduction and conclusion in those sections.

Outside of our notebook and the code itself, I helped come up with the different sub-topics that each group member could take on in order to gain insights on our main question. I also constantly communicated with group members trying to set up schedules and checkpoints in order for a more cohesive and smooth group experience. Finally I helped create the basic layout for this README file as well as our presentation and report.

<u>How to run code:</u>

1. Open the Project.ipynb notebook in Jupyter Notebook or JupyterLab.
2. Run each cell from top to bottom.
3. There are no custom functions. All visualizations are generated directly from the cells as written.


---

### 2. Rafin Ahon
**Subtopic:** Time-of-Day / Day-of-Week Demand Analysis  

**Description of Code and Contributions:**  
For this part of the project, I analyzed the second question. I intended to explore how taxi demand changes across different hours and days to understand rider behavior patterns. My work focused on transforming timestamp data into usable time-based features and generating visualizations that reveal clear daily and weekly trends. My specific contributions include:

- Created time-based variables by converting raw pickup and dropoff timestamps into hour, day, and weekday columns to make temporal patterns easier to analyze.

- Generated multiple visualizations- including hourly demand trends, weekday vs. weekend comparisons, daily trip totals, and a full heatmap showing hour-by-hour activity across the week.

- Organized and documented all analysis in the updated Project.ipynb file, with exported graphs used directly in the final presentation.
  
My code uses pandas to clean and transform the timestamp column into hour, day, and weekday features, numpy for basic numeric calculations, and matplotlib to generate the four visualizations for my section. The analysis relies on grouping the data with groupby() to measure trip counts across different time intervals. These steps allowed our group to clearly see how rider activity fluctuates throughout the day and across the week, providing a strong foundation for understanding temporal demand patterns.

Instructions on running my code: 
After the dataset is loaded in Part 1, my section runs by continuing through the remaining cells in the notebook. These cells create the time-based features (hour, day, weekday), compute the trip counts, and produce all visualizations for hourly trends, weekday vs. weekend patterns, daily totals, and the hour-by-weekday heatmap. All figures appear directly in the notebook and are also saved to the project folder automatically, with no extra setup required.

---

### 3. Chowdhury Rashik E Alahi
**Subtopic:** Tip likelihood logistic regression  

**Description of Code and Contributions:**  
For my part of the project, I focused on two modeling questions: predicting taxi fare amounts and analyzing the likelihood that a passenger leaves a tip. My work centered on preparing the relevant numerical features, running regression models, and generating the visualizations used in our final presentation. My specific contributions include:

- Cleaned and converted key variables such as trip distance, fare amount, passenger count, and tip amount into usable numeric formats, while removing invalid or extreme values.

- Built a multiple linear regression model to estimate fare amounts and created the “Fare vs Trip Distance” regression scatterplot to illustrate the model’s relationship between distance and pricing.

- Developed a logistic regression model to predict whether a passenger tips, including generating the binary tip variable, sampling the dataset for efficient training, and producing the final ROC curve used in the presentation.

- Documented all steps clearly in the Project.ipynb file and simplified code blocks for readability, ensuring that visualizations and outputs are easy for the entire team to interpret and reference.

My analysis uses pandas for cleaning and preparing the dataset, numpy for numeric handling, seaborn and matplotlib for all visualizations, and scikit-learn for both regression models. This workflow allowed us to explore how well trip-level features can explain fare pricing and tipping behavior, ultimately revealing that distance is highly predictable while tipping remains much harder to model.

**Instructions on running my code:**
Once the main dataset is loaded and cleaned in Part 1, my sections can be executed by running the subsequent cells in order. The fare prediction section automatically generates the distance–fare regression plot, while the tipping analysis produces the logistic regression output and the ROC curve. All figures render directly in the notebook and do not require any additional setup.

---

### 4. [Member Name]
**Subtopic:** [Subtopic #4 title]  

**Description of Code and Contributions:**  
[Describe code and contributions in this space]

---

### 5. Gunnar Austin  
**Subtopic:** Linear Regression Modeling of New York Taxi Trip Durations  

**Description of Code and Contributions:**  

<u>My Contributions:</u>

I oversaw the creation of the regression framework that evaluates how different trip-related variables affect taxi ride duration in New York City. My work also involved preparing the dataset, which included converting data to numeric formats, eliminating erroneous or missing entries, and filtering out trips with extreme or implausible values. I structured the input variables for modeling and carried out the SKLearn regression procedure, which included dividing the data into training and testing subsets and computing the model’s R² value, intercept, and feature coefficients.

Additionally, I created a secondary filtered dataset to remove extreme outliers that could distort visual interpretation. I computed median values for each predictor variable in order to isolate the effect of one variable at a time. I then generated a complete set of regression visualizations, with each plot comparing observed trip durations against the model-predicted regression line for a single feature while holding all other variables constant. This produced clear, interpretable graphics that form the basis for the analysis in my section of the report.

Outside of the code itself, I contributed to discussions about the structure of the report and how each subtopic fits into the larger research question. I also communicated regularly with group members to coordinate code integration and ensure that updates were properly merged into the main branch.

<u>How to run code:</u>

1. Open the Project Group 4 .ipynb notebook in Jupyter Notebook or JupyterLab.  
2. Run each cell sequentially from top to bottom.  
3. All outputs, graphs, and regression lines are generated directly from the executed cells; no additional files or manual steps are required.
