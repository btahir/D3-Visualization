### Background

This visualization captures the flights to and from the Virginia region (Central Virginia and Wasginton DC) in January 2015. The reason I chose this dataset was because, around the same time when I was working on this project, I was also participating in a Data Visualization competition within my company and this dataset was provided to us. I figured this would be a great way to work on this project and test it out.

### Summary

The data visualization captures all the flight paths and delay information based on airport. It categorizes the airports by color based on the most frequent cause of the delay in that airport. There is also a bar chart that summarizes the average delays for each airport. The visualization is interactive as you have can hover over which airport you want to see the information for.

### Process

I initially just wanted to show the flight patterns with some text information (see index_old.html). After getting feedback, this evolved to lighter colors and a bar chart display at the bottom. I also took out the Voronoi checkbox as it was determined it was not really adding any value to the visulization.

### Feedback

I got feedback from my team members of the visualization competition (talk about killing two birds with one stone!). To be clear, I alone worked on this and no one helped me with my coding. What we eventually presented was a tableau dashboard (which everyone else worked on) with my D3 visualization embedded within it (we didn't win).

#### Feedback 1

I was asked to show the text information (average delays etc.) as a bar chart rather than as text to make it easier to read.

#### Feedback 2

I was asked to take out the Voronoi checkbox as it was not adding much value to the visualization.

#### Feedback 3

I was asked to adjust the font/ opacity of the visual to make it lighter. We also debated on how best to categorize the airports based on delay. Initially, I was categorizing based on the sum of all Carrier delays versus Weather delays etc. This was eventually changed to the frequency of the different delays. We felt it made more sense to compare that rather than the total amount of one type of delay versus the other.

I also made minor adjustments to the margins and placement of the boxes throughout the process.

### Inspiration

My visualization was inspired by some other examples I came across when I was doing my research.
https://mbostock.github.io/d3/talk/20111116/airports.html
https://lichangny.github.io/d3/v3/index.html
http://bl.ocks.org/NPashaP/96447623ef4d342ee09b

I also had invaluable help through the Udacity instructors on the forum and Stack overflow whenever I hit a roadblock.

### Data Sources

The original dataset was provided to us (see DCAH_data.csv). 
I had to manipulate and derive the data into a form I could use easily (see flight-airports_all.csv).

The metadata can be found here: http://transtats.bts.gov/Fields.asp?Table_ID=236
The dataset can also be queried from the main site: http://transtats.bts.gov/Fields.asp?Table_ID=236
I found the US map data here: https://github.com/mbostock/topojson/tree/master/examples 

