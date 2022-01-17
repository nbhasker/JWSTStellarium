# JWSTStellarium
This is a Stellarium script to plot the position of the James Webb Space Telescope (JWST) and the Sun-Earth-Moon-Barycenter L2 Lagrange (SEMB-L2) point using coordinates from the Nasa Horizons service.

## How to use

This assumes you have the free open source Stellarium planetarium software installed. More details can be found at https://stellarium.org/.

Download the script to your local computer and rememebr where you've saved it. Then there are two distinct steps to running the script to display the JWST and Sun-Earth-Moon-Barycenter L2
* Modifying the script with the latest coordinates from the NASA Horizons service
* Loading and running the script in Stellarium

### Modifying the script with the latest coordinates from the NASA Horizons service
NASA publishes the coordinates of the JWST and SEMB-L2 on their Horizons System website at https://ssd.jpl.nasa.gov/horizons/. 

Select the "App" tab. Then set Ephemeris Type to "Observer Table", the Target Body to JWST. Enter your location and the date range of interest and click the "Generate Ephemeris" button. 

Then scroll down and you'll see the generated ephemeris with the Right Ascension (RA) and Declination (Dec) for each requested date and time. For each date of interest, edit the JWST[] array in the script following the example in the script.

Repeat for the SEMB-L2 position by obtaining the position again from NASA Horizons and editing the SEMB_L2 array in the script.

### Loading and running the script in Stellarium
First launch Stellarium. Then open the script window by hitting the F12 key. 

Here you can load the script using the button with the folder icon which you'll find on the left and then run it by hitting the "play" button on the right. You should now see the JWST and L2 markers on the screen. 

## Troubleshooting
The script moves Stellarium to display the position of the first entry for JWST. But this may not always show the markers. 

The L2 point is directly away from the sun so you'll have to set a time when the sun has set and look in the opposite direction for the markers to be above the horizon and visible. (In January 2022, JWST is between the belt of Orion and Procyon.)

The Search Window in Stellarium (F3 or the magnifying glass icon on the left menu) also takes positions and so you can enter one of the RA/Dec positions directly there to point Stellarium to the right place. (Remember to use hms and dms formats as required for the RA and Dec coordinates. The NASA Horizons data doesn't have this format and you'll have to modify the data appropriately by adding the hms and dms letters in the blank spaces.)
