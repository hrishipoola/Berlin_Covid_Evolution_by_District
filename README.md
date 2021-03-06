# Berlin_Covid_Evolution_by_District

More striking than Berlin's recent covid case spike is how differently covid has evolved by district throughout the year. Let's analyze and visualize Berlin's case evolution over time and the spread and distribution of incidence (per 100,000) by district. Keep in mind, we don't factor in or attribute exogenous variables like increased testing and the fact that the true positivity rate in the population may be much higher than that indicated by confirmed positive tests.

We'll scrape confirmed case data by district (https://www.berlin.de/lageso/gesundheit/infektionsepidemiologie-infektionsschutz/corona/tabelle-bezirke-gesamtuebersicht/) and convert it to a dataframe with the data types and index we need. We'll calculate the rolling 7-day average of cases by district and create a visual, including custom text highlighting events over the course of the pandemic. As district populations vary widely, incidence would provide a better apples-to-apples comparison. Let's scrape population data (https://en.wikipedia.org/wiki/Demographics_of_Berlin), calculate incidence by district, and create a dataframe. While population data is from the last census in Germany in 2010 and Berlin's population has grown quite dramatically since then, it's sufficient for the purpose here of calculating an approximate incidence to make comparisons. Lastly, let's compare incidence by district, create a boxplot highlighting differences in spread, and create a density plot highlighting difference in distribution.

Key findings:

Berlin's most recent total rolling 7-day average of confirmed cases on October 21, 2020 was 3x of the peak of the 1st wave in March, with the most dramatic case averages in Mitte, Neukolln, Tempelhof-Shoneberg, and Friedrichshain.

Most district incidence means are higher than medians, indicating a right skew with higher-end outliers (as we can see with the max values). Mitte and Neukolln's mean incidence of 5 is roughly 2x that of Pankow, Spandau, and Steglitz. Tempelhof-Schoneberg, Charlottenburg, and Reinickendorf feature a mean incidence of about 3. Mitte and Neukolln's median, which is less vulnerable to outliers, of >2 is nearly 2x higher than most other districts. Most striking, the current incidence (not the 7-day avereage) is many factors higher than the mean, with Mitte, Neukolln, and Friedrichshain-Kreuzberg's at >50 and Friedrichshain-Kreuzberg approaching 45. Additionally, Mitte and Neukolln's standard deviation of >8 is significantly higher the other districts.

The boxplot reveals Mitte and Friedrichshain-Kreuzberg feature the highest IQR, while Neukolln features more higher-end outliers. Interestingly, Pankow, which has the lowest median, also features a much tighter spread and fewer outliers.

The density plot of incidence reveals that Pankow, Charlottenburg, and Tempelhof-Schoneberg have a fairly tight distribution around the mean, while Mitte and Neukolln have a much broader, right-skewed distribution around a higher mean. The purpose of this is to visualize Berlin's current covid landscape by district.

Taken together, Mitte and Neukolln, even accounting for differences in population (though we don't incorporate population density here), has fared far worse than districts like Pankow.
