### Background

This visualization captures the flights to and from the Virginia region (Central Virginia and Washington DC) in January 2015. The reason I chose this dataset was because, around the same time when I was working on this project, I was also participating in a Data Visualization competition within my company and this dataset was provided to us. I figured this would be a great way to work on this project and test it out.

### Summary

The data visualization captures all the flight paths and delay information based on airport. It categorizes the airports by color based on the most frequent cause of the delay in that airport. There is also a bar chart that summarizes the average delays for each airport (in minutes). The visualization is interactive as you can hover over which airport you want to see the information for.

### Findings

The visualization is based on flights to and from the Virginia area and so it makes sense the majority of flights are centered around that area (the size of the circles for Washington and Richmond airports are by far the largest). It is also immediately apparent the majority of most frequent delays at airports are Carrier Delays with a few airports having more Weather Delays. This is consistent throughout the country regardless of region.

The average delays also tend to be correlated with the number of flights at a particular airport. This makes intuitive sense as there is more likelihood of a delay happening over a bigger number of flights - however the average tends to go up with the number which can be attributable to really long delays skewing the average. Late Aircraft and Carrier Delays tend to be the longest on average with Security and Weather Delays being on the lower end.

### Design Development

Since I was a part of a team that was to present a dashboard of visualizations, I focused on one particular aspect of the data i.e. the aiports. My visual would focus on showing data based on airports which would complement the other visualizations which would focus on information based on the actual flight.

My goal was to group the information by airports and show how they stack up against each other. I had a variety of metrics such as flight counts, cancellations, types of delays etc. to choose from. 

I decided to show the information on a US map in case there were any geographical patterns (east coast v west coast) that would pop out. I was inspried by Mike Bostock's flight patterns map example: <https://mbostock.github.io/d3/talk/20111116/airports.html> 
and wanted to show a similar map where you can see the different flight paths based on hovering on the airport of choice. 

I wanted to add to this by showing some information about the airport (flight counts, delays etc.) and it made sense to add this to the hovering event. I initially showed this information as text (indexOld2.html) but later changed this partially to a bar chart so the reader can more easily compare the various types of delays.

Another changed I ended up making was to add a color legend which categorized the airports by the most frequent delay. I thought this visual information blended nicely with the average delay times already being shown in the bar chart.

### Process

My goal was to look at the flight information based on airport and see how the data (cancellations/delays) varied based on airport. I decided I wanted to lay out the data on an actual US map to understand the geographical spread of the data. 

I initially just wanted to show the flight patterns with some text information (see indexOld1.html). After getting feedback, this evolved to lighter colors and adding a color legend (indexOld2.html) and a bar chart display at the bottom which more clearly showed the differences in average delay times for the different types of delays. I also took out the Voronoi checkbox as it was determined it was not really adding any value to the visualization. Below is a breakdown of the changes:

indexOld1.html: US map showing flight patterns with text information of airports at the bottom.

indexOld2.html: Map was made lighter and color legend was added. The title and Voronoi checkbox were taken out and the text font was made smaller and lighter in line with the rest of the visualization. The text was also moved to the right of the map. 

index.html: In the final version, the text information was partly replaced by a bar chart to show average delays. The text and the bar chart were both moved to the bottom again which made for a better usage of space. I ended up taking out cancellations/deiverted counts since there were very few of these to begin with based on the data and they were not really telling any meaningful story.

### Feedback

I got feedback from my team members of the visualization competition (talk about killing two birds with one stone!). To be clear, I did this whole visualization on my own without any help from the rest of the team members. What we eventually presented was a tableau dashboard (which everyone else worked on) with my D3 visualization embedded within it (we didn't win). The feedback was given in in-person meetings as well as frequent check-ins thorughout our lead up to the competition. Below are the 3 main changes that came about from the feedback from the team: 

##### Feedback 1

I initially presented the visualization in indexOld1.html. It was a darker background and just had text information for the airports. I was asked to show the text information (average delays etc.) as a bar chart rather than as text to make it easier to compare the different types of delays.

##### Feedback 2

I had kept the Voronoi checkbox because it looked 'cool' but after a less than enthusiastic reponse from my team members (who were even having a hard time understanding what it was doing), I decided to take it out as it was not adding much value to the visualization.

##### Feedback 3

I was asked to adjust the font/ opacity of the visual to make it lighter. We also debated on how best to categorize the airports based on delay. Initially, I was categorizing based on the total aggregate sum of all the different type of delays (Carrier delays versus Weather delays etc.). This was eventually changed to the frequency of the different delays. We felt it made more sense to compare that rather than the total amount of one type of delay versus the other.

I also made minor adjustments to the margins and placement of the boxes throughout the process.

### Inspiration

My visualization was inspired by some other examples I came across when I was doing my research.
<https://mbostock.github.io/d3/talk/20111116/airports.html>
<https://lichangny.github.io/d3/v3/index.html>
<http://bl.ocks.org/NPashaP/96447623ef4d342ee09b>

I also had invaluable help through the Udacity instructors on the forum and Stack overflow whenever I hit a roadblock.

### Data Sources

The original dataset was provided to us (see DCAH_data.csv). 

I had to manipulate and derive the data into a form I could use easily (see flight-airports_all.csv).

The metadata can be found here: <http://transtats.bts.gov/Fields.asp?Table_ID=236>

The dataset can also be queried from the main site: <http://transtats.bts.gov/Fields.asp?Table_ID=236>

The US map data came from here: <https://github.com/mbostock/topojson/tree/master/examples> 

The airports data was found here: <http://openflights.org/data.html>