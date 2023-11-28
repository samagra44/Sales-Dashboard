**This script essentially creates a Streamlit web app for a sales dashboard, allowing users to filter data and visualize sales information with interactive charts. It demonstrates the integration of pandas for data manipulation, Plotly Express for chart creation, and Streamlit for building the web application. The data is read from an Excel file, and the dashboard includes charts for sales by product line and sales by hour. The code is organized into different sections, each serving a specific purpose in creating the interactive dashboard.**

## Import Libraries:
```pandas```: A library for data manipulation and analysis.    
```plotly.express```: A library for creating interactive visualizations.    
```streamlit```: A framework for creating web applications with simple Python scripts.    

## Set Streamlit Page Configuration:
Configures the Streamlit app with a title ("Sales Dashboard"), an icon for the page (":bar_chart:"), and a wide layout.

## Read Excel Data:
@st.cache_data: Decorator for caching the function's output to improve performance by avoiding unnecessary data reading.     
Reads data from the "supermarkt_sales.xlsx" Excel file, skipping 3 rows, selecting columns "B:R", and reading only the first 1000 rows.     
Adds an "hour" column to the DataFrame based on the "Time" column.     
Assigns the resulting DataFrame to the variable df.    

## Create Sidebar for Filtering:
Adds a header in the sidebar.     
Provides multi-select widgets for selecting the City, Customer Type, and Gender.    
Filters the DataFrame (df_selection) based on the selected filter criteria.    

## Check if DataFrame is Empty:
Displays a warning message if the filtered DataFrame is empty.    
Stops the execution of the app to avoid further processing.    

## Main Page Title:
Sets the main title of the page using an emoji and adds a markdown subheader.

## Calculate Top KPIs:
Computes key performance indicators (KPIs) such as total sales, average rating, and average sales per transaction.

## Display Top KPIs:
Divides the page into three columns and displays the calculated KPIs in each column.

## Sales by Product Line (Bar Chart):
Groups the data by "Product line" and calculates the total sales.    
Creates a horizontal bar chart using Plotly Express.    

## Sales by Hour (Bar Chart):
Groups the data by "hour" and calculates the total sales.    
Creates a bar chart showing sales by hour using Plotly Express.   

**Clone the repository:**

```
git clone https://github.com/samagra44/Sales-Dashboard.git
```

**Install the requirements:**
```
pip install -r requirements.txt
```

**Run the application:**

```
streamlit run app.py
```

**Application is running on ```http://localhost:8501/```** .


![Sales](https://github.com/samagra44/Sales-Dashboard/assets/77968722/5a1b98e0-bb76-4477-88a5-67bbe7d319e4)



