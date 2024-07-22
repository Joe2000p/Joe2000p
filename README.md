pip install pandas openpyxl
import pandas as pd

# Real-world population data for the 100 most populous countries
real_population_data = {
    "Country": [
        "China", "India", "United States", "Indonesia", "Pakistan", "Brazil", "Nigeria", "Bangladesh",
        "Russia", "Mexico", "Japan", "Ethiopia", "Philippines", "Egypt", "Vietnam", "DR Congo",
        "Turkey", "Iran", "Germany", "Thailand", "United Kingdom", "France", "Italy", "South Africa",
        "Tanzania", "Myanmar", "South Korea", "Colombia", "Kenya", "Spain", "Argentina", "Algeria",
        "Sudan", "Ukraine", "Uganda", "Iraq", "Poland", "Canada", "Morocco", "Uzbekistan",
        "Saudi Arabia", "Peru", "Angola", "Malaysia", "Mozambique", "Ghana", "Yemen", "Nepal",
        "Venezuela", "Madagascar", "Cameroon", "Côte d'Ivoire", "North Korea", "Australia", "Niger",
        "Sri Lanka", "Burkina Faso", "Mali", "Malawi", "Zambia", "Romania", "Chile", "Kazakhstan",
        "Guatemala", "Ecuador", "Syria", "Netherlands", "Senegal", "Cambodia", "Chad", "Somalia",
        "Zimbabwe", "Guinea", "Rwanda", "Benin", "Burundi", "Tunisia", "Bolivia", "Belgium",
        "Haiti", "Cuba", "South Sudan", "Dominican Republic", "Czech Republic", "Greece", "Jordan",
        "Portugal", "Azerbaijan", "Sweden", "Honduras", "United Arab Emirates", "Hungary", "Tajikistan",
        "Belarus", "Austria", "Papua New Guinea", "Serbia", "Israel", "Switzerland", "Togo", "Sierra Leone",
        "Hong Kong"
    ],
    "Population (Millions)": [
        1441, 1393, 332, 276, 231, 214, 206, 169, 146, 130, 125, 121, 113, 109, 98, 97, 86, 85, 83, 70,
        68, 68, 60, 60, 60, 54, 52, 51, 50, 47, 45, 44, 44, 41, 41, 40, 40, 39, 37, 35, 35, 34, 34, 34,
        33, 33, 31, 30, 30, 30, 27, 27, 26, 26, 25, 24, 24, 23, 20, 19, 19, 19, 19, 18, 18, 18, 17, 17,
        16, 15, 15, 13, 12, 12, 12, 11, 11, 11, 11, 11, 11, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 9,
        9, 9, 9, 9, 9, 9, 9, 9
    ]
}

# Creating the DataFrame with corrected real population data
df_real_population_corrected = pd.DataFrame(real_population_data)

# Sorting the DataFrame by population in descending order
df_real_population_sorted_corrected = df_real_population_corrected.sort_values(by="Population (Millions)", ascending=False).reset_index(drop=True)

# Saving the sorted DataFrame to an Excel file
df_real_population_sorted_corrected.to_excel("real_population_sorted_corrected.xlsx", index=False)
