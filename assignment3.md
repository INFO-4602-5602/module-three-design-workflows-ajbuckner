## Background
1. For this assignment, as well as the previous, I have a unique opportunity to use data i collected from a high altitude balloon payload. This payload gathered data from the implemented sensors on board (ext./int. temp, humidity, pressure, acceleration), and returned this via microSD in relation to time. After recovering the payload, we are left with a massive .csv file of all the sensor readings at small time increments. My problem is using the massive data dump to create a useful and accurate visualization of the data collected, as well as using the data to pinpoint certain events during the flight of my payload (takeoff, atmoshpheric layers, balloon burst and post-burst chaotic whipping).



2. As mentioned, my data is sent via serial bus to a micro SD card from the Arduino onboard the payload. At this point, it is hard to imagine bias in a system like this, as i designed and built the physical payload alone. But, my notions of what the data should look like prior to the launch may play some effect into how I create the visualization, so this may be bias to take into account. There is no article to link this data from, but here is some more info on the payload project, and my source data will be referenced in this notebook as well. https://www.colorado.edu/spaceminor/space-minor-balloon-payload-program-information

![IMG_0121.JPG](attachment:IMG_0121.JPG)


## Discover & Design
3. Using the data gathered, my aim is to 1: Create clear, concise graphs to represent the massive amount of data recorded, and 2: Use the sensor data to examine events in the payload flight.



4. For my sketch, I created a rough prototype of what I want my visualization to look like. Note the main graph, which includes all of the sensor data over time, and id like to create auxillary graphs to break down specific sensor data as well. The goal is to create functional graphics for a visual representation of the data. This is a rough prototype of what i want my graphics to look like:

![payl.PNG](attachment:payl.PNG)


## Implement, Deploy, Iterate
5. To create my visualizations I used Google Sheets, and although it was a bit laggy, it proved to work pretty well for a project like this. My final payload data file was over 10,000 lines long, with 7 columns of data for each line at a specific time during payload flight. I went with clean, comprehensible axes and titles, and made sure to include units for maximum clarity.

![finaldatanice.jpg](attachment:finaldatanice.jpg)

6. Using the generated graphs, mainly the acceleration readings, we can see the payload takeoff pretty easily. The early spikes in both the X and Z directions indicate the sharp force put on the payload as it is pulled from the ground, and the general down trend in temperature occurs after this initial spike as the payload ascends. We can also see when the balloon bursts, with similar indicators to launch. Big spikes in the acceleration graphs, and a downtrend in temperature as the payload falls back to the cooler part of the atmosphere.

![tempandaccarrowjpg.jpg](attachment:tempandaccarrowjpg.jpg)

6. (cont.) After burst, chaotic whipping occurs due to low air resistance. As you can see, the payload was pulling almost 8 Gs! For reference, the max G force a fighter pilot endures is around 8 Gs, and this is only the select few, and for a short time. I was definitely suprised by the extent of the forces my payload endured, as well as it's ability to continue datalogging through such intense movement.



7. One immediate idea I had after seeing this data visualized was to try recording acceleration in all 3 directions. In turn, this data could be used to create a 3-dimensional vizualtiation of the orientation and movement of my payload, which could be very helpful information for optimizing mass distribution on my next project.





## Analysis
My visualizations fulfilled my target problem effectively. My inital problem was a bunch of data with no way to comprehend it, and through the solutions i developed i was able to visualize that data, and more. With this in mind, there is plenty to expand on.

Ultimately, my solution was not severely complicated, so there is definetley room for expansion. Creating a script to store and visualize the data manually is something that is definetely on the horizon, and with this comes room for more customization on the visualization, rather that being constricted to the chart maker in Google Sheets.


```python

```
