import matplotlib.pyplot as plt

# Yıllar
years = [2017, 2018, 2019, 2020, 2021, 2022, 2023]

# Veriler
asia_sales = [333.30, 352.20, 373.40, 392.10, 423.70, 456.40, 484.30]
eu_sales = [208.20, 222.60, 212.60, 216.30, 233.40, 242.60, 251.90]
nafta_sales = [338.50, 351.00, 371.80, 375.80, 393.40, 419.60, 438.10]
south_america_sales = [54.19, 49.59, 47.41, 45.32, 48.11, 51.98, 53.73]

# Sütun grafik
plt.figure(figsize=(10, 6))
plt.bar(years, asia_sales, color='b', width=0.2, label='Asia')
plt.bar([year + 0.2 for year in years], eu_sales, color='r', width=0.2, label='EU-27')
plt.bar([year + 0.4 for year in years], nafta_sales, color='g', width=0.2, label='NAFTA')
plt.bar([year + 0.6 for year in years], south_america_sales, color='y', width=0.2, label='South America')

plt.xlabel('Year')
plt.ylabel('Sales')
plt.title('Pharmaceutical Sales by Region (2017-2023)')
plt.xticks(years)
plt.legend()
plt.tight_layout()
plt.show()
