# GFC AI Chatbot Project
This project will develop an AI-powered chatbot designed to extract and analyze key financial data from the 10-K documents of Apple, Microsoft, and Tesla. This financial chatbot aims to interpret data and deliver insights interactively and in a user-friendly manner, empowering users with sophisticated financial analysis tools.

## Specific project requirements and outcomes

- Efficiency: The solution must significantly reduce the time taken to analyze financial documents compared to traditional methods.
- Accuracy: The chatbot should provide precise and reliable financial insights backed by thorough data analysis.
- User-friendly interface: The chatbot should be intuitive and easy to use for GFC’s diverse client base, regardless of their financial expertise.
- Scalability: The solution should be scalable – capable of handling an increasing number of documents and user queries.

## Determining important factors for AI integration

- Data quality assessment: The success of AI heavily depends on the quality of data it is fed. Through this task, I've leart to identify and extract high-quality, relevant financial data, setting a strong foundation for accurate AI modeling.
- Understanding data structure: AI models require data in specific formats. This task has helpped me comprehend the structuring of financial data, which is a pivotal step in preparing it for AI integration.

# Project context:

Extract meaningful insights from 10-K financial reports.
These insights will feed into the AI chatbot, enabling it to provide in-depth financial performance analysis.

## My  role and responsibilities

### Data extraction:
  - Research and review 10-K documents.
  - Focus on key financial figures and ratios.
    
  ### Basic analysis:
  - Identify significant financial trends and indicators.
  - Assess the financial health and performance of the companies.

### Data preparation:
  - Format and clean the data for AI model integration.

### Deliverable:
  - A comprehensive data analysis report, which should include:findings and summary providing insights into the financial health of the analyzed companies.
    
### Chatbot development:
 - Chatbot logic: Write a Python script that uses if-else statements to match user input (the predefined queries) to the responses I prepared. Use a simple Flask app for web-based interaction to get a more interactive experience.


## Techniques for extracting key financial data from 10-Ks 
Help resouce: [https://www.sec.gov/oiea/investor-alerts-and-bulletins/how-read-10-k10-q]


### Key sections to focus on for financial data extraction:
#### Income statement: This section provides information about the company's revenue, costs, and expenses over a specific period of time.
##### Key data points: 
Total revenue, cost of goods sold (COGS), operating expenses, and net income.
#### Extraction technique: 
Look for the income statement summary, typically in the early pages of the reports. Pay attention to year-over-year changes.

### Balance sheet: 
This section outlines the company’s assets, liabilities, and the shareholders’ equity at a specific point in time.
##### Key data points: 
Current assets, long-term assets, current liabilities, long-term liabilities, and total shareholders’ equity.
##### Extraction technique: 
Focus on the balance sheet summary. Compare assets against liabilities to understand the company’s financial health and note any large changes in assets or liabilities.

### Cash flow statement: This shows how changes to the balance sheet and income impact cash and cash equivalents.
#### Key data points: 
Cash from operating activities, investing activities, and financing activities.
#### Extraction technique: 
Analyze the cash flow statement to understand how the company generates and spends its cash. This can provide insights into a company's liquidity.


## Steps
### Step 1: Data extraction
### Step 2: Preparing my Jupyter Notebook environment
### Step 3: Python analysis in Jupyter

#### Load the data:
Convert my Excel file to a CSV file for easier handling, then loaded it into a DataFrame.

df = pd.read_csv('path_to_my_csv_file.csv')

#### Analyzing trends with pandas:
Use pandas to calculate year-over-year changes for each financial metric. I did this by creating new columns in my DataFrame that represent the percentage change from one year to the next.

df['Revenue Growth (%)'] = df.groupby(['Company'])['Total Revenue'].pct_change() * 100
df['Net Income Growth (%)'] = df.groupby(['Company'])['Net Income'].pct_change() * 100

Explore other aggregate functions or groupings to analyze the data across different dimensions (by company, over years, etc.).

### Step 4: Chatbot design and data preparation
- Define predefined queries: "What is the total revenue?", "How has net income changed over the last year?"
- Prepare responses: Use the analyzed financial data to create canned responses for these queries.

### Step 5: Chatbot development


### Step 6: Demonstration and documentation

