# CS416 Narrative Visualization and D3 Library Final Project.

Original data and information was obtained from speedrun.com: [Website](https://www.speedrun.com/) [GitHub](https://github.com/speedruncomorg/api/tree/master/version1)

Links to all the original video creators:
- Games Done Quick: [Website](https://gamesdonequick.com/) [YouTube](https://www.youtube.com/@gamesdonequick)
- Player 5: [YouTube](https://www.youtube.com/@Player5SR)
- Venick: [YouTube](https://www.youtube.com/@Venick409)
- Gymnast86: [YouTube](https://www.youtube.com/@gymnast86)
- Zdi: [YouTube](https://www.youtube.com/@zdi6923)


Description:

This narrative visualization project attempts to explain the basics of speed-running within the games the Legend of Zelda: Breath of the Wild, and the Legend of Zelda: Tears of the Kingdom. It covers a little of information explaining how speed-running fits for each game and allows the user to explore several completed runs by other people. Finally, it plots together the speed-running data for both games to help visualize how the data for each game compares to the other.

This visualization is designed to follow the interactive slide-show structure. In order to be classified as an interactive slide-show, the visualization allows the viewer to interact with all three different scenes, which are organized into slides. In all three scenes, the viewer can move back or forth between slides, or hover over a datapoint to see more details. In the first two scenes, the viewer can click on an annotation to get more information, or filter the chart using the settings given at the top.

Visually, each scene follows an annotated chart by providing textual context to the scene. The text in the first scene explains how the data is structured and plotted, and annotations point out important pre-selected data points to the viewer. The text also contains instructions on how to interact with the data. Between each scene, similar color and font styles are used; for example, all the datapoints for Breath of the Wild use a light blue color, and all of the datapoints from Tears of the Kingdom use a light red color. The final scene is used to pull both datasets together, and visualize their relationship temporally.

There are three scenes within this visualization. The first scene uses speed-running data from only Breath of the Wild. The second scene uses speed-running data from only Tears of the Kingdom. These two scenes are ordered in this way because Breath of the Wild was released first, back in 2017. The final scene pulls both datasets together, and acts like a conclusion/summary.

There were two template types of annotations used in this visualization. The first annotation is the callout elbow annotation provided by the d3-annotation library, used only when the annotation needs to point to a specific datapoint. The second annotation is the XY threshold annotation also provided by the d3-annotation library. This annotation draws a line from the top to the bottom of the scatterplot, and is used to point out a specific date, not a datapoint. None of the annotations change within a single scene, but all are interactive.

Several parameters with used in this visualization. The first and foremost parameter is the slide number parameter, which determines which scatterplot to display, and which dataset to use for the points. The second parameter used is the description number parameter, which determines what text (and video) is displayed to the right of the scatterplot. Lastly, there are other parameters based on the filters provided for scenes 1 and 2, and correspond to the region, platform, and dates used in filtering.

Each user interaction has an associated trigger. When clicking on the next or previous slide buttons, the visualization changes the slide number and loads the appropriate chart and description. When clicking on the filter or reset buttons, the visualization determines the values for the input options, filters the data accordingly, and resets the chart. When clicking on an annotation, the visualization determines which description number parameter should be used, and loads the appropriate description. For the most part, HTML buttons and inputs are used to communicate when interactions as available. Previous and next buttons are only visible and active when necessary, and the filter inputs and buttons are hidden on slide three, when they are not used.
