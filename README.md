# WEBSCRAPPING LOK SABHA ELECTION DATA 2024
### Scraping Election Results:
  1. The code uses the requests library to fetch the HTML content from the Election Commission of India website.
  2. BeautifulSoup is used to parse the HTML content and extract relevant data like table rows, links, and header values.
     
### Data Cleaning and Preparation:

  1. Text extracted from HTML elements is stripped of leading/trailing whitespaces.
  2. Numeric columns like 'Won', 'Leading', and 'Total Votes' are converted to appropriate data types using pd.to_numeric.
  3. Missing values (NaN) introduced during data type conversion are filled with 0.
     
### Data Analysis and Visualization:
  1. Party-wise seat victories are calculated using groupby and sum.
  2. Win percentages are calculated by dividing the number of seats won by the total number of seats contested.
  3. Close contest performance is evaluated by comparing the number of leading candidates to twice the number of winning candidates.
  4. Vote shares are calculated by grouping the data by party and summing the total votes.
  5. Pie charts are generated using matplotlib to visualize party-wise seat victories and vote shares.
  6. Histograms are used to show the distribution of the margin of victory.
     
### Data Storage:
  1. The processed dataframes are saved to CSV files using df.to_csv.

### State-wise and Candidate-wise Analysis:
  1. State-wise results are analyzed by scraping data from specific state result pages.
  2. Candidate-wise information is extracted from elements with the class "cand-info".
  3. Winning candidate statistics, highest and lowest turnouts, and most competitive constituencies are calculated.


### PARTY WISE SEAT VICTORY

![Screenshot 2024-07-02 233422](https://github.com/harshdhiman03/LokSabhaWebScrapping/assets/122113456/180c30ba-24fd-4604-adf4-ef353652c0b8)


### DISTRIBUTION OF MARGIN OF VICTORY

![Screenshot 2024-07-02 233456](https://github.com/harshdhiman03/LokSabhaWebScrapping/assets/122113456/c698b50e-2367-4869-ba81-c07f2de59276)

### PARTY WISE VOTE SHARE
![Screenshot 2024-07-02 233521](https://github.com/harshdhiman03/LokSabhaWebScrapping/assets/122113456/6290f61f-6626-4e0f-9890-2e2cd5ff1371)

