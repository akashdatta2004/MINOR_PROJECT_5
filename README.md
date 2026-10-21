# Customer Segmentation Using K-Means Clustering
**AIML Minor Project — Unsupervised Learning**

## Dataset
Mall Customer Segmentation Data (Kaggle):  
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

Download `Mall_Customers.csv` from the Kaggle dataset page and put it beside the notebook.

## Problem and objective
Group mall customers by annual income and spending score, explore how age relates to customer behaviour, and create interpretable segments to inform potential marketing experiments.

## Files
- `Customer_Segmentation_KMeans.ipynb` 
- `Project_Report.md` 
- `Presentation_Script.md` 
- `Customer_Segmentation_Presentation.pptx` 
- `requirements.txt` 

## Run the project
1. Install Python 3.10+ or open Google Colab/Jupyter.
2. Install dependencies: `pip install -r requirements.txt`
3. Download `Mall_Customers.csv` from Kaggle and place it next to the notebook.
4. Run all notebook cells from top to bottom.
5. Review the elbow and silhouette charts, then verify the chosen number of clusters makes business sense.
6. Use the actual profile table, silhouette score and cluster sizes in your final presentation. The notebook exports `customer_segments_output.csv` and `segment_profile.csv`.

## Method
- EDA and data-quality checks
- StandardScaler for numeric features
- K-Means clustering
- Elbow/inertia and silhouette score for internal evaluation
- Cluster profiling and visual interpretation

## Important evaluation note
This is unsupervised learning and the dataset has no ground-truth segment labels. Accuracy, precision, recall, and F1 are not suitable. Do not claim results until the notebook has been run on the downloaded dataset. Interpret clusters as patterns in this sample, not proof of customer motivation or causation.
