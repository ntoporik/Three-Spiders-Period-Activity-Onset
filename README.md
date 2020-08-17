# Three-Spiders-Period-Activity-Onset
The goal of this project is to idetntify a pattern in spider circadian activity. Circadian activity of a spider is the cycling of periodic activities over a certain amount of time. This is usually observed to be 24 hours in nature, as the spiders are entrained to the 24 hour cycle of the daily period of light and dark. THis allows the spiders to have anticipatory activities, including eating, locomotion, and resting. However, in environments lacking of entrainment signals and cues from nature (ie complete darkness, constant temperature) the spiders are still able to maintain a periodic cycling of their locomotor activity period, which could range from 17 to 31 hours. This is called the free running period (FRP). Spiders normally have two distinct spouts of activities throughout the day, one as the light turns on, the other occurs right after the light turns off. The onset of activity of interest in this experiment measures the amount of time it takes for the spider to start locomotor activity when the light turns off. 

We were using behavior data of three spider specise (Latrodectus mactans, Anelosimus studiosus, and Parasteatoda tepidariorum). Spiders were housed in a LD 12:12 cycle in the chambers. Throughout the experiment, the infrared bean crossing was used to measure the locomotive activity of spiders. Our primary question for analysis was is the  period of spider activity in the total darkness depend on activity onset after the light goes off. 

## Methodology
1. Clean up original data (move incomplete date)
2. Save activity to full rastor plots 
3. Visual inspection of dead and live spiders -> delete dead spiders
4. Split the cleaned data into two periods--LD and DD 
5. Make raster plots and ACF plots for each spider in LD and DD separately
6. Detect activity onset for ecah spider 
7. Find period of each spider during LD, if they are entraiend to 24 hour period, then find their FRP
8. Plot FRP against Onset

## Content of Files in the Directory
#### Data.zip
These files contain data of locomotor activity meters of 32 monitors (S1-S32) for three species: Latrodectus, Parasteatoda, and studiosus.  The infrared bean crossing was used to measure the locomotive activity of spiders. Some of the monitors contained living spiders and some were empty. The numerical value in columns S1-S32 is the number of times the infrared bean installed in the monitor has been cross during the time indicated in the second column(Time). Column "Light" contains a light indicator: if 1, the light was on in the chamber, if zero, the light was off.

#### Latrodectus.zip
1. Code
  a. Clean_up.ipynb: cleans up the original .txt file
  b. Make_Images.ipynb: make images of raster plots and ACF plots for each live spiders in LD and DD separately
  c. Activity.ipynb: finds FRP and onset of activity, plot periodogram and acf, and plot scatter plot of FRP vs onset
2. Data
  a. Latrodectus.txt: orginal data file
  b. Alive.csv: data of dead and live spiders
  c. LD.csv: the activity data in LD period
  d. DD.csv: the activity data in DD period
3. Figures
  a. Full_Raster_Plots: raster plots for each spider in LD and DD together
  b. LD_Rasters_with_ACF: raster and ACF plots for each live spider in LD period--raster on the left and ACF on the right
  c. DD_Rasters_with_ACF: raster and ACF plots for each live spider in DD period--raster on the left and ACF on the right
  d. Onset: Raster plots with onset of activity indicated by red star
  e. pgram: periodograms and acf of each spider
  f. FRP vs. Onset.png: scatter plot of FRP vs onset

## Instructions on How to Use Files 

