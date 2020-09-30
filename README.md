# Improbable beef
## Overview and Background
Rosa is a biological researcher working in a microbiology laboratory. She is trying to discovery and better understand bacteria.
Specifically, she focused on bacteria that have the ability to synthesize proteins that taste like beef. He lab has partnered with Improbable Beef, a food startup.
Rosa is looking at bacteria found in people's belly buttons for this type of bacteria with a synthesizing ability who's results taste like beef. She’s collected large sample of belly button bacteria
button bacteria to hopefully find this desired bacteria.
## Project Overview
The goal of this project is to build a dashboard that can be viewed by both her research participants and partners and those people who have donated samples.
### Data Overview
Those who donated can visit the web site and see what bacteria are growing in their belly button. Those3 who donated are anonymous in the data. They have been assigned an id number
to use to locate their specific information. The data collected is composed of 3 arrays based on 153 people samples. The metadata array contains information regarding the person
who donated. The names array contains the id number assigned the person. This id number is also in the metadata array. The sample values array contains the corresponding species and name for each bacterial
ID number, the OTU ID. Some bacterial species have different ID numbers, but are clumped together under the same otu_label. OTU stands for Operational Taxonomic Unit, and here it means species or bacterial type. In this
 instance, there were 80 bacterial types with distinct ID numbers.
## The Web Site Build, available here (https://davidmcbee.github.io/improbable_beef/) is created using 5 files:
1.	The samples.json file. This the is data in json array format. (https://github.com/davidmcbee/improbable_beef/blob/master/samples.json).
2.	The index.html file. This is the file that renders the web page. (https://github.com/davidmcbee/improbable_beef/blob/master/index.html).
3.	The style.css file. This is a file that modifies the index.html file to render certain styles. (https://github.com/davidmcbee/improbable_beef/blob/master/style.css)
4.	The image file. This is the image used within the jumbotron, the top part of the web page. (https://github.com/davidmcbee/improbable_beef/blob/master/bb.jpg)
5.	The charts.js file. This is the code, available here (https://github.com/davidmcbee/improbable_beef/blob/master/charts.js) that does the following:
	*  Gathers the data and assigns it to various parts of the html
	* The buildMetadata function reads the data and fills the Test Subject IS selector and the Demographic Info panel.
	* The buildCharts function filters the data to display the correct data in each of the three graphs.
		* the bubble chart shows the bacteria ID and the number of those samples. By hovering over a particular bubble, which is sized proportionally to the number of sample,
		one can see the OTU_ID, the number of samples and the text stating what those bacteria samples are.
	* The bar chart shows the OTU_IDs and the number of samples of that bacteria horizontally in a descending order.
	* The gauge chart shows how many times that person cleans their belly button per week.
	* There is also a options changed function that initiates the changes once  user selects a particular ID.

## Other Modifications
In addition to the base product the following was modified:
1.	An image is now displayed in the jumbotron. to do this a style.css file was added.
2.	A background color was added.
3.	The order of the charts was changed to highlight the bubble chart. To do this the "well" Class was used for each of the graphs to alleviate overlap and spacing. Additionally padding was added via the CSS style sheet.
4.	The text font was changed for the "Use the interactive charts below to explore the dataset"
5. 	The web site is mobile responsive but I didn't do anything in particular to make it so.
