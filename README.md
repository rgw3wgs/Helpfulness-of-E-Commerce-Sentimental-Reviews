# Helpfulness-of-E-Commerce-Sentimental-Reviews
## Section 1: Software and platform section
- The software we used for this project was Python
- The names of add-on packages that needed to be installed with the software:

  - Packages for EDA:
    - warnings
    - numpy
    - pandas 
    - matplotlib.pyplot
    - seaborn
    - rcParams
    - TextBlob
    - tools
    - plotly.graph_objs
    - iplot
   
  - Packages for Analysis
    - numpy
    - pandas 
    - ttest_ind
    - kstest
    - bartlett
    - wilcoxon

- The platform that was used was a Mac

## Section 2: A Map of your documentation
- DATA
  - original_data
  - final_data 
- OUTPUTS
  - KS_test.png
  - bartlett.png
  - bigram.png
  - boxplot.png
  - piechart.png
  - t_test.png
  - table.png
  - violinplot.png
  - violinplot2.png
- SCRIPTS
  - EDA_code.ipynb
  - analysis_code.ipynb
  - clean_data.ipynb
  - master_script.ipynb

## Section 3: Instructions for reproducing your results
Step 1: Cleaning the data
  - check for NA values and fill as 'Missing' instead of empty
  - combine review text and summary columns into a column called review, then drop the former 2 columns
  - create sentiment column: if 'overall' is 1 or 2, assign as Negative. if 'overall' is 4 or 5, assign as Positive. otherwise, delete the row
  - drop unnecessary columns: reviewerID, unixReviewTime, and asin columns
  - change reviewTime to date/year format
  - create column with helpfulness rate of a review
  - drop date column and keep year
  - clean review column *remove text in square brackets, make text lowercase, remove links,       remove punctuation, remove words containing numbers
  
Step 2: Creating EDA 
  - generate table for sentiment vs. helpfulness
  - create boxplot that shows sentiment and helpfulness
  - create violin plot
  - remove 0 values in helpful rate column and create new violin plot with removed observations
  - create new table for sentiment vs. helpfulness with removed observations
  - create pie chart
  - create bigram plot

Step 3: Performing Analysis
  - split data into Positive and Negative groups
  - test for normality: kolmogorov smirnov test
  - test for constant variance: bartlett's
  - perform independent t test
  - perform Wilcoxon signed rank test
