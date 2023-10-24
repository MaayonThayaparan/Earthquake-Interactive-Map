# Earthquake-Interactive-Map

## Description: 
- This program reads earthquake data from a live RSS feed (https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/2.5_week.atom) and plots recent earthquake data on a map to highlight potential disaster zones. The map will show information such as:

     - Cities
         - Hovering will show the city name, country, and population.

    - Earthquakes
         - Hovering will show the magnitude and relative location
         - The size of the marker is relative to the magnitude.
         - The color of the marker determines depth (yellow = shallow [<70m], blue = intermediate [70-300m], red = deep [>300m], X = within past hour)
         - Shape determines whether land (circle) or ocean (square) quake.

![image](https://github.com/MaayonThayaparan/Earthquake-Interactive-Map/assets/43158629/598335f4-df6f-4ad6-b62a-f5679c8061f0)

## Getting Started 

### Dependencies
- Tested on Windows 10
- Requires Java 1.8 JDK (Java SE 8)
- Requires Eclipse 
- Requires e(fx)clipse

### Installation:

1. Download Java 1.8 JDK (Java SE 8)
     - Download at: https://www.oracle.com/java/technologies/downloads/
     - Tested on version Java SE Development Kit 8u381 → x86 Installer (https://www.oracle.com/java/technologies/downloads/#java8-windows)
     - Create a free Oracle account to download.
     - Note down where you save the folder. 
2. Download Eclipse
     - Download at: https://www.eclipse.org/downloads/
3. Open Eclipse
     - In Eclipse select ‘Window’ tab → Select ‘Preferences’ → Expand ‘Java’ → Select ‘Installed JREs’ → Click ‘Search’
     - Navigate to where  you installed the JDK 1.8 directory. Make sure you select the newly installed JDK directory and not the newly installed JRE directory.
     - After a moment, Eclipse should list a second JRE in the ‘Java → Installed JREs’ window. Select the JRE in the newly installed JDK folder and click ‘Apply and Close’
4. Requires e(fx)clipse
     - Go to www.eclipse.org/efxclipse/install.html
     - Under 'For the Ambitious' click 'View details'
     - Follow the on-screen instructions starting at step 2 or 3
5. In the 'Package Explorer' click 'Import Projects'
6. Under 'Git' select 'Projects from Git (with smart import)
7. Select 'Clone URl'
8. Input URL: https://github.com/MaayonThayaparan/Text-Editor-and-Generator.git
9. Click 'Next' then 'Next' and then 'Finish'
10. Select the root project folder in the 'Package Explorer' then click 'Project => Properties => Java Compiler'
11. Select 'Enable project specific settings'
12. Change the 'Compiler compliance level' to 1.8 then click 'Apply and Close'. Click 'Yes' when prompted. 

### Manual Installation: 
- Create new Java project
- Copy+Paste all files into project
- Add all lib/*.jars to build path
- Set native library location for jogl.jar. Choose appropriate folder for your OS.
- Add data/ as src

### Troubleshooting:
- Do the following if you get the following error: “java.lang.UnsupportedClassVersionError:”
     - Ensure root directory is selected in ‘Package Explorer’ → Click ‘Project’ in tool bar → ‘Properties’ → ‘Java Compiler’ → select ‘Use compliance from execution environment ‘JavaSE 1.6’... → then click ‘Apply and Close’


## Executing Program

- If you are working OFFLINE, open file ‘src → project → EarthquakeCityMap.java’ and change the private static variable ‘offline’ to be set to ‘true’ (this will use a copy of the same feed from Aug 7, 2015)
- If you want to add a city to the display, open the file named “src → data → city-data.json”  and modify the file so it includes your desired city. Ensure you match the format and data of other cities exactly! 

- Run the ‘EarthquakeCityMap.java’ file in ‘src → project’.
     - Use scroll bar to zoom in/out.
     - Click and drag screen to move around the map. 
     - Hover over a city marker (triangle) to display the city's name, country, and population.
     - Clicking on a city marker will lead to only that city and earthquakes which affect it being displayed on the map. Clicking once again will bring the rest of the map’s markers back.
     - Hover over an earthquake marker (circle or square) to display the earthquake’s magnitude and region.
     - Clicking on an earthquake marker will lead to only that earthquake and cities which it affects to be displayed on the map. Clicking once again will bring back the rest of the map’s markers back.
     - Filter Keys:
          - Hold key ‘m’ to filter out all earthquakes with magnitude above 5.
          - Hold key ‘n’ to filter out all earthquakes in the northern hemisphere
          - Hold key ‘s’ to filter out all earthquakes in the southern hemisphere.
     
## Future Optimizations: 
- When clicking on a city, display a popup menu either on or off the map (off will be easier) which displays a count for the number of nearby earthquakes (within threatCircle) the average magnitude, and most recent earthquake. 
- Use keyboard events to change which earthquakes are displayed by age or only display cities which are above a certain latitude. etc.

## Unfinished Projects:
- Starting map visualization for the following:

     - Airports and routes.
          - Can run file ‘src → project → AirportMap.java’
          - To see routes uncomment line 77 and line 83 in ‘AirportMap.java’. 

     - Life Expectancy
          - Can run file ‘src → project → LifeExpectancy.java’
          - Color coding of countries is based on the life expectancy of the country. 


