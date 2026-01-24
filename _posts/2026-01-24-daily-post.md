---
layout: single
title: "Machine Learning"
date: 2023-12-27 09:00:00 +0600
categories: [NLO]
tags: [physics]
description: "My Daily thoughts"
---



 **Artificial Intelligence (AI)** is a broad area of computer science where the goal is to enable computers and machines to **simulate human behavior** and perform human-like tasks.

 **Machine Learning (ML)** is a specific subdomain of computer science and a **subset of AI** that focuses on creating algorithms that allow a computer to learn from data to solve problems or make predictions. While traditional programming involves a human telling a computer exactly what to do—known as explicit programming—ML allows the computer to **learn without being explicitly programmed** for every scenario.

**Data Science (DS)** is a field that focuses on **finding patterns and drawing insights** from data. While these fields are distinct, they overlap significantly; for instance, Data Science and AI both frequently utilize Machine Learning to achieve their objectives.

---

 **Three primary types of machine learning**:

 **1. Supervised Learning**
Supervised learning utilizes **labeled inputs**, meaning every piece of data fed into the model has a corresponding output label. The model uses these labels to learn how to predict the output for new, unseen inputs. This type of learning is further divided into two main tasks:
*   **Classification:** The goal is to predict **discrete classes** or categories. This can be **binary classification** (choosing between two categories, such as "spam" vs. "not spam") or **multi-class classification** (choosing between more than two, such as identifying if an image is a cat, dog, or lizard).
*   **Regression:** This task involves predicting **continuous numerical values** instead of discrete categories. Examples include predicting the future price of a house or the temperature for the following day.

 **2. Unsupervised Learning**
Unsupervised learning uses **unlabeled data** to identify hidden patterns or structures within the information. Since there are no "correct" answers or labels provided, the computer finds commonalities on its own. Common applications include:
*   **Clustering:** Grouping data points into "clusters" based on shared characteristics (e.g., K-Means Clustering).
*   **Dimensionality Reduction:** Reducing a large number of features into a smaller, more manageable set while retaining the most important information (e.g., Principal Component Analysis or PCA).

 **3. Reinforcement Learning**
In reinforcement learning, an **agent** learns how to behave in an interactive environment based on a system of **rewards and penalties**. Similar to training a dog, the agent receives "rewards" for positive actions to encourage the computer to continue those behaviors in the future.

---

### Features

Based on the sources, a **feature** is an attribute or property of a data point that is passed into a machine learning model to help it predict a target label. In a dataset, each column typically represents a different feature, while each row represents a single sample or example. These features provide the "evidence" or information the model uses to solve a specific problem or make predictions.

The sources describe features in several ways:

### **Structure of Features**
*   **Feature Vector:** This is the collection of all individual features for a single sample.
*   **Features Matrix (X):** This is the entire set of features for all samples in a dataset, often represented by the letter **X**.

### **Types of Features**
Features are generally categorized into two main types:
*   **Qualitative (Categorical):** These represent categories or groups and are divided into **Nominal** data (no inherent order, like nationality) and **Ordinal** data (inherent order, like age groups or ratings).
*   **Quantitative (Numerical):** These are numerical values that can be **Discrete** (integers, like a count of items) or **Continuous** (any real number, like temperature or length).

### **Preparation for the Model**
Because computers understand numbers better than letters, features often require preprocessing before being fed into a model. For example, nominal qualitative features are often converted using **one-hot encoding**, and quantitative features may be **scaled** relative to their mean and standard deviation to ensure their different scales do not negatively affect the model's results.

---

**One-hot encoding** is a method used to convert **qualitative features**—specifically **nominal data**—into a numerical format that a computer can understand. Because computers are highly efficient at processing numbers but struggle with human concepts like language or categories, this technique is essential for feeding categorical information into a machine learning model.

### **Key Characteristics of One-Hot Encoding**
*   **Target Data Type:** It is specifically used for **nominal data**, which are categories that have **no inherent order**. Examples include nationalities (e.g., US, France, Japan) or gender.
*   **The Logic:** For every possible category in a dataset, a new column is essentially created. If an input matches a specific category, it is assigned a **1**; if it does not match, it is assigned a **0**.
*   **Contrast with Ordinal Data:** Unlike **ordinal data** (like ratings from "bad" to "great" or age groups), which can be mapped to a simple numerical scale like 1 to 5 because they have a natural ranking, nominal data requires one-hot encoding because one category is not "higher" or "closer" to another in a mathematical sense.

### **Example of One-Hot Encoding**
If you have a dataset with four different countries, the encoding would look like this:

| Category | One-Hot Representation |
| :--- | :--- |
| **US** | `1, 0, 0, 0` |
| **India** | `0, 1, 0, 0` |
| **Canada** | `0, 0, 1, 0` |
| **France** | `0, 0, 0, 1` |

In this format, each item is represented by a vector where only one "bit" is "hot" (set to 1), while the rest are "cold" (set to 0). This allows the model to treat each category as distinct without incorrectly assuming a mathematical relationship or order between them.


---

In supervised learning, the two primary tasks are **classification** and **regression**. The fundamental difference lies in the type of output the model is designed to predict.

### **Classification**
Classification is the process of predicting **discrete classes** or categories for a given input. The model uses features to assign a specific label to a sample.

*   **Binary Classification:** This involves predicting between only **two categories**. Examples include determining if an email is "spam" or "not spam," or identifying if a particle is a "gamma" or a "hadron".
*   **Multi-class Classification:** This involves predicting one label from **more than two categories**. Examples include identifying an image as a cat, dog, or lizard, or classifying different species of plants.
*   **Mechanism:** Models like **K-Nearest Neighbors (KNN)** or **Support Vector Machines (SVM)** are often used to find boundaries (hyperplanes) that best divide these different classes.

### **Regression**
Regression is used when the goal is to predict **continuous numerical values** rather than categories. Instead of picking a label, the model predicts a number on a scale that is as close to the true value as possible.

*   **Continuous Outputs:** Regression is used for values that do not fit into discrete classes, such as the **price of a house**, the **temperature**, or the future price of a cryptocurrency.
*   **Linear Regression:** This is a common form of regression where the model fits a **line of best fit** to the data using the equation $y = b_0 + b_1x$.
*   **Residuals and Errors:** The model's performance is measured by **residuals**, which are the distances between the actual data points and the model's predicted line. The objective is to find a line that minimizes these residuals across the entire dataset.

### **Key Summary of Differences**
| Feature | Classification | Regression |
| :--- | :--- | :--- |
| **Output Type** | Discrete classes/labels | Continuous numerical values |
| **Goal** | Discriminate between groups | Find a value on a scale/line of best fit |
| **Examples** | Spam detection, image labeling | Predicting house prices, temperature |

---

In machine learning, **training** is the iterative process of "tinkering" with a model to reduce the difference between its predictions and the actual truth. This process involves feeding data into a model, measuring its performance, and making mathematical adjustments to improve accuracy.

According to the sources, the following steps and concepts are essential to training a model:

### **1. Data Splitting**
You should never use your entire dataset for training, as this prevents you from knowing if the model can generalize to new, unseen information. Instead, the data is divided into three distinct sets:
*   **Training Set:** Usually about 60–80% of the data, this is the only portion fed into the model to teach it patterns.
*   **Validation Set:** Used during or after training as a "reality check" to ensure the model can handle unseen data. Crucially, the loss from the validation set is **never fed back into the model**; the feedback loop remains open to provide an unbiased assessment.
*   **Testing Set:** A final, separate chunk of data used to report the model's ultimate performance after training is complete.

### **2. The Feedback Loop: Loss and Optimization**
Training relies on a feedback loop centered on the concept of **Loss**—the numerical quantity representing the difference between a prediction and the true label. 
*   **Loss Functions:** Formulas like **L1 loss** (absolute difference) or **L2 loss** (squared difference) quantify how "wrong" the model is.
*   **Backpropagation:** In complex models like neural networks, the loss is "fed back" into the model to determine how much each internal weight contributed to the error.
*   **Gradient Descent:** This mathematical technique allows the model to "follow the slope" of a loss curve downward to find the point where the error is at its minimum.

### **3. Controlling the Training Process**
Several "hyperparameters" are used to manage how a model learns:
*   **Learning Rate (Alpha):** This determines the size of the "step" the model takes when adjusting its weights. If the rate is too high, the model might "diverge" or miss the optimal solution; if too low, it will take a very long time to converge.
*   **Epochs:** These represent full training cycles where the entire training dataset is passed through the model once.
*   **Batch Size:** This refers to the number of training examples utilized in one iteration.
*   **Dropout:** A technique used during training to prevent **overfitting** by randomly "turning off" certain nodes in a neural network, forcing the model to become more robust.

### **4. Hyperparameter Tuning**
To find the best version of a model, you may perform a **Grid Search**. This involves searching through various combinations of nodes, learning rates, and batch sizes to identify which specific parameters result in the lowest validation loss. In libraries like **TensorFlow**, this is implemented using the `.fit()` command, which handles the iterations and keeps a history of the loss and accuracy across every epoch.

---

**Loss** is a numerical quantity that represents the **difference between a model's prediction and the actual true label**. It acts as a measure of how "wrong" a model is; for instance, a model with a high loss is performing poorly because its predictions are far from the truth, while a **smaller loss indicates the model is performing better**. A **loss function** is the specific **mathematical formula** used to calculate these numbers and provide a consistent way to evaluate a model's error.

The sources describe several common loss functions used for different machine learning tasks:

### **1. L1 Loss**
*   **Definition:** L1 loss calculates the **absolute value of the difference** between the real output label and the predicted value. 
*   **Purpose:** It measures the total distance of all points from the truth. In this function, the loss increases linearly as the prediction moves further away from the actual value.
*   **Characteristic:** While useful, it is **not totally differentiable everywhere**, which can make certain mathematical optimizations more difficult compared to other functions.

### **2. L2 Loss**
*   **Definition:** This is a **quadratic formula** that squares the difference between the prediction and the truth.
*   **Purpose:** Because it is quadratic, its primary purpose is to **punish large errors and outliers** much more heavily than small ones.
*   **Characteristic:** Unlike L1 loss, L2 is **differentiable**, making it highly valuable for training methods like **backpropagation** and gradient descent, which rely on calculus to adjust model weights.

### **3. Binary Cross Entropy Loss**
*   **Definition:** This loss function is specifically utilized for **binary classification** tasks.
*   **Purpose:** It is used to measure the performance of models predicting between two distinct categories (e.g., 0 or 1). It is the standard choice when using **neural networks with a sigmoid activation function** in the final layer, as it helps the model project predictions into discrete classes.

### **Which One is Better?**
The sources indicate that **no single loss function is universally "better"** because the choice depends entirely on the specific problem you are trying to solve and the nature of your data. 
*   **L2** is often preferred for regression when you want to heavily penalize large errors, and its differentiability is a major advantage for complex models. 
*   **Binary Cross Entropy** is the superior choice for **binary classification** problems.
*   Ultimately, the "better" model and loss function are determined through **experimentation**, such as a grid search, where you toggle hyperparameters and observe which settings yield the **lowest validation loss** for your specific dataset.

---


**Accuracy** is a metric used to evaluate the performance of a machine learning model by determining **how many predictions it gets right compared to the total number of predictions made**. It is a common measure of performance for classification tasks, such as identifying different types of images or particles.

### **How Accuracy is Calculated**
To find the accuracy, you divide the number of correct predictions by the total number of samples. For example, if you feed a model four pictures and it predicts three of them correctly and one incorrectly, the accuracy of that model is **three-quarters, or 75%**. 

### **Context in Model Evaluation**
*   **Performance Comparison:** In practical examples like K-Nearest Neighbors (KNN), an accuracy of **82%** indicates that for every 100 new points the model evaluates, it correctly identifies the class for 82 of them.
*   **Limitations:** While accuracy provides a general overview of performance, it is often viewed alongside other metrics like **precision**, **recall**, and the **F1-score**. This is particularly important when dealing with **unbalanced datasets**, where one class appears much more frequently than another.
*   **Tracking during Training:** When building neural networks with tools like TensorFlow, accuracy is often tacked onto the model's metrics during compilation so that researchers can monitor its improvement over multiple training cycles (epochs) alongside the reduction of **loss**.


----

## Code

```
cols = ["fLength", "fWidth", "fSize", "fConc", "fConc1", "fAsym", "fM3Long", "fM3Trans", "fAlpha", "fDist", "class"]
df = pd.read_csv("magic04.data", names=cols)
df.head()
```

These lines of code are part of the initial data loading and preprocessing phase for the Magic Gamma Telescope dataset. The purpose of each line is as follows:

### **1. `cols = ["fLength", "fWidth", ..., "class"]`**
The purpose of this line is to **manually define the column headers** for the dataset. The instructor observed that when the raw data file was first opened, it did not contain any descriptive labels or headers. By creating this list, she is taking the **attribute names** from the dataset's documentation (such as length, width, and asymmetry) so they can be applied to the data in the next step. 

The last item in this list, `"class"`, represents the **target label** (identifying a particle as either a gamma or a hadron), while the other ten items are the **features** used to train the model.

### **2. `df = pd.read_csv("magic04.data", names=cols)`**
This line performs two primary functions:
*   **Data Conversion:** The `pd.read_csv` function takes the downloaded CSV file (comma-separated values) and turns it into a **Pandas DataFrame object**, which is a structured format the computer can manipulate.
*   **Label Assignment:** By passing the `names=cols` parameter, the function **assigns the labels** defined in the previous list to the columns of the dataset. This ensures that each piece of data is correctly categorized under the appropriate feature or target header.

### **3. `df.head()`**
The purpose of this line is to **inspect the resulting DataFrame**. Calling the `.head()` method returns only the **first five entries** of the dataset. This acts as a visual "reality check" to ensure the data was loaded correctly and that the column labels from the `cols` list were applied to the data as intended.

----

#
```
 df["class"] = (df["class"] == "g").astype(int)
```


The purpose of the line `df["class"] = (df["class"] == "g").astype(int)` is to **convert qualitative text labels into numerical values** that a computer can process,. 

In the specific dataset used in the sources (the Magic Gamma Telescope dataset), the "class" column originally contains letters: **"g"** for gammas and **"h"** for hadrons. Because machine learning models and computers are "really good at understanding numbers" rather than letters, the data must be transformed before training begins,,.

### **How the Code Works**
1.  **Comparison (`df["class"] == "g"`)**: This part of the code checks every entry in the "class" column. If the value is "g", it evaluates to **True**; if the value is not "g" (in this case, "h"), it evaluates to **False**.
2.  **Conversion (`.astype(int)`)**: This converts those Boolean values (True/False) into integers. 
    *   **True** becomes **1** (representing gamma).
    *   **False** becomes **0** (representing hadron).

### **The Result**
By running this line, the entire "class" column is transformed from strings of text into a sequence of **zeros and ones**. This numerical format is essential for the computer to understand the target labels and use them for **classification** tasks,.

---
## 
```
for label in cols[:-1]:
  plt.hist(df[df["class"]==1][label], color='blue', label='gamma', alpha=0.7, density=True)
  plt.hist(df[df["class"]==0][label], color='red', label='hadron', alpha=0.7, density=True)
  plt.title(label)
  plt.ylabel("Probability")
  plt.xlabel(label)
  plt.legend()
  plt.show()
  ```

The provided Python code block is used to **visualize the relationship between various features and the target classes** (gammas and hadrons) by plotting overlapping histograms. 

Here is a breakdown of what each part of the code does:

### **1. Iterating Through Features**
*   **`for label in cols[:-1]:`** This line sets up a loop that iterates through every attribute in the `cols` list except for the very last one. In this dataset, the last column is the "class" (the target label), while the previous ten columns are the **features** (like `fLength` or `fWidth`) that the model uses to make predictions.

### **2. Selecting and Plotting Data**
*   **`plt.hist(df[df["class"]==1][label], ...)`**: This identifies all rows where the particle is a **gamma** (represented by the number 1) and isolates the data for the current feature (`label`) to plot it in blue.
*   **`plt.hist(df[df["class"]==0][label], ...)`**: This identifies all rows where the particle is a **hadron** (represented by the number 0) and plots that same feature in red.
*   **`alpha=0.7`**: This sets the **transparency** of the histograms. By making the colors slightly see-through, it allows the user to see where the two distributions overlap.
*   **`density=True`**: This **normalizes the distributions**. Because there are significantly more gamma samples (~7,000) than hadron samples (~4,000) in the dataset, the blue histogram would naturally look much larger than the red one. Normalizing them ensures they are on the same scale (probability) for an accurate visual comparison.

### **3. Labeling and Displaying the Plots**
*   **`plt.title(label)`**: Sets the name of the feature currently being plotted as the title.
*   **`plt.ylabel("Probability")`**: Labels the y-axis as "Probability" because the data has been normalized by the `density` parameter.
*   **`plt.xlabel(label)`**: Labels the x-axis with the name of the specific feature.
*   **`plt.legend()`**: Adds a key to the plot so the viewer knows that blue represents gammas and red represents hadrons.
*   **`plt.show()`**: Commands the computer to display the completed plot before moving on to the next feature in the loop.

### **The Purpose of This Code**
The goal of running this visualization is to see which features help **discriminate** between the two types of particles. For example, after running this code, it becomes clear that if a particle has a smaller `fLength` or a smaller `fAlpha` value, it is statistically **more likely to be a gamma** than a hadron.

---

```
train, valid, test = np.split(df.sample(frac=1), [int(0.6len(df)), int(0.8len(df))])
```
This specific line of code is designed to **shuffle and split your dataset** into three distinct subsets: **Training, Validation, and Testing**. This is a critical step in machine learning to ensure the model can generalize to new data rather than just memorizing the training set,.

Here is the breakdown of what each part of that line does:

### **1. Shuffling the Data**
*   **`df.sample(frac=1)`**: This part of the code shuffles the data frame. By setting `frac=1`, you are telling Pandas to return 100% of the data but in a completely randomized order. Shuffling is important to ensure that any inherent ordering in the original file doesn't bias the training process.

### **2. Calculating the Split Indices**
The code uses a list `[int(0.6*len(df)), int(0.8*len(df))]` to tell the computer exactly where to "cut" the data frame.
*   **`int(0.6*len(df))`**: This identifies the index at the **60% mark** of the dataset. Everything from the start of the file to this point (the first 60%) becomes the **Training set**,.
*   **`int(0.8*len(df))`**: This identifies the index at the **80% mark**. The data between the 60% mark and the 80% mark (a 20% slice) becomes the **Validation set**,.
*   **The Remainder**: Everything from the 80% mark to the end (the final 20%) is assigned as the **Test set**.

### **3. Purpose of the Three Sets**
*   **Train (60%)**: This is the data used to actually teach the model and adjust its weights,.
*   **Valid (20%)**: This set acts as a **"reality check"** during training to see how the model performs on data it hasn't "seen" before. Crucially, the loss from this set is never fed back into the model to avoid bias.
*   **Test (20%)**: This is used for the **final reported performance** of the model after all training is complete to see how well the chosen model generalizes to completely new information,.

### **4. Final Assignment**
*   **`train, valid, test = np.split(...)`**: The `np.split` function takes the shuffled data frame and the cut points and returns three separate data frames, which are then assigned to the variables `train`, `valid`, and `test` respectively,.
---