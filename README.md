## The data
I worked with the ev_battery_charging_data.csv file that tracks:

- Charging mode (Fast/Normal)
- Efficiency percentages
- Number of charging cycles
- How fast the battery degrades
- Voltage and current readings
- Battery and ambient temperatures

### Key Findings

Surprisingly, my analysis revealed that fast charging doesn't compromise EV battery performance as commonly believed. 
Both fast and normal charging modes maintained nearly identical efficiency rates of approximately 98%, with statistical validation 
through Welch's t-test yielding a p-value of 0.846 (well above the 0.05 significance threshold), confirming no meaningful difference between the methods. 
The data further showed matching degradation patterns over time, minimal temperature variation (only about 2°C higher for fast charging), and consistent 
long-term performance metrics across increasing charging cycles, challenging conventional wisdom about fast charging's presumed negative impacts on battery health.

### How I analyzed everything

#### Stats testing:

Checked if the data was normally distributed (Shapiro-Wilk)
Compared the means while accounting for different variances (Welch's t-test)


#### Visualizations:

Plotted efficiency distributions as histograms
Created scatter plots with trend lines to see how things change over time
Looked at voltage/current patterns and temperature differences
Built a correlation matrix to spot relationships between variables



### Tools I used

pandas for data wrangling
numpy for calculations
scipy for statistical tests
matplotlib and seaborn for visualizations
