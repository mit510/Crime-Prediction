🔍 Crime Prediction Dashboard 🌦️

Analyze crime patterns with weather influences in an interactive Python dashboard!

📖 Overview

Welcome to the Crime Prediction Dashboard, a data-driven project that explores the relationship between crime occurrences and weather conditions. Built with Python in a Jupyter Notebook, this project merges crime and weather datasets to create an interactive dashboard for visualizing trends across crime categories, seasons, and temperature ranges. Whether you're a data enthusiast, researcher, or urban planner, this tool provides insights into how environmental factors might influence crime patterns. 🚓🌡️

Key Features:

📊 Interactive dashboard with dropdown filters for crime categories (e.g., Assault, Robbery), seasons, and temperature ranges.

📈 Visualizations including heatmaps, bar plots, and line graphs to uncover trends.

🔗 Merged crime and weather datasets for comprehensive analysis.

🐍 Powered by Python libraries: pandas, matplotlib, seaborn, and ipywidgets.


🎯 Objectives

Analyze Crime Patterns: Understand how crimes like Assault, Break and Enter, or Auto Theft vary by season or temperature.

Visualize Trends: Create intuitive visualizations to identify correlations between weather and crime.

Enable Exploration: Provide an interactive interface for users to filter and explore data dynamically.


🛠️ Tech Stack

Language: Python 3 🐍

Libraries:

pandas for data manipulation

matplotlib and seaborn for visualizations

ipywidgets for interactive dashboard controls

Environment: Jupyter Notebook 📓

Datasets: Custom crime and weather datasets (not included in repo due to size; contact for access)


📂 Project Structure

Crime-Prediction-Dashboard/

├── ADT_Project.ipynb       # Main Jupyter Notebook with code and dashboard

├── datasets/              # Placeholder for crime and weather CSV files

├── README.md              # This file

└── requirements.txt       # Python dependencies

🚀 Getting Started

Follow these steps to set up and run the project locally.

Prerequisites

Python 3.8+ installed

Jupyter Notebook or JupyterLab

Git for cloning the repository

Installation

Clone the Repository:

git clone https://github.com/your-username/Crime-Prediction-Dashboard.git

cd Crime-Prediction-Dashboard


Set Up a Virtual Environment (recommended):

python -m venv venv

source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies:

pip install -r requirements.txt


Add Datasets:

Place your crime.csv and weather.csv files in the datasets/ folder.

Ensure the files match the expected format (see ADT_Project.ipynb for column details).


Launch Jupyter Notebook:

jupyter notebook

Open ADT_Project.ipynb in the browser.


Running the Dashboard

Execute all cells in ADT_Project.ipynb.

Use the dropdown menus to select:

Crime Category: All, Assault, Break and Enter, etc.

Season: All, Winter, Summer, Fall.

Temperature Category: All, Cold (<0°C), Mild (0-10°C), Warm (10-20°C), Hot (>20°C).


Click the Update Dashboard button to refresh visualizations.


📊 Visualizations

The dashboard generates four plots:

Heatmap: Crime categories vs. seasons, showing frequency patterns.

Bar Plot: Crime counts by temperature category.

Line Plot: Crime trends over time, filtered by selection.

Pie Chart: Distribution of crime types within the selected filters.

Note: If you encounter a ValueError: zero-size array to reduction operation fmin, it’s likely due to an empty filtered dataset. Ensure your filters (e.g., specific crime and season) return non-empty results, or modify the update_dashboard function to handle empty data (see Troubleshooting).

💡 Usage Example

Select Crime Category: Assault, Season: Summer, and Temp Category: Hot (>20°C).

Click Update Dashboard.

Observe the heatmap showing Assault frequency in Summer, the bar plot for temperature impacts, and more.


🛠️ Troubleshooting

ValueError: zero-size array to reduction operation fmin:

Cause: The heatmap tries to plot an empty dataset when filters exclude all data.

Fix: Add a check in the update_dashboard function:if filtered_df.empty:

    print("No data matches the selected filters. Please adjust your selection.")
    
    return

Insert this before the heatmap code (line 109 in your notebook).

Missing Datasets: Ensure crime.csv and weather.csv are in the datasets/ folder with correct column names.

Library Issues: Verify all dependencies are installed (pip install pandas matplotlib seaborn ipywidgets).


📝 Future Improvements

🧠 Add predictive modeling (e.g., Random Forest or LSTM) to forecast crime rates.

🌐 Deploy the dashboard as a web app using Streamlit or Dash.

📍 Incorporate geospatial analysis for crime hotspot mapping.

🔧 Enhance error handling for empty filter results.


🤝 Contributing

Contributions are welcome! To contribute:

Fork the repository.

Create a new branch (git checkout -b feature/your-feature).

Commit changes (git commit -m "Add your feature").

Push to the branch (git push origin feature/your-feature).

Open a Pull Request.

Please follow the Code of Conduct.

📜 License

This project is licensed under the MIT License. See the LICENSE file for details.

📬 Contact

For questions or dataset access, reach out via:

GitHub Issues: Create an issue

Email: patel77b@uwindsor.ca


🌟 Star this repository if you find it useful! Happy analyzing! 🌟
