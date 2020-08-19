# Three-Spiders-Period-Activity-Onset
The goal of this project is to idetntify a pattern in spider circadian activity. Circadian activity of a spider is the cycling of periodic activities over a certain amount of time. This is usually observed to be 24 hours in nature, as the spiders are entrained to the 24 hour cycle of the daily period of light and dark. This allows the spiders to have anticipatory activities, including eating, locomotion, and resting. However, in environment lacking of entrainment signals and cues from nature (ie complete darkness, constant temperature), the spiders are still able to maintain a periodic cycling of their locomotor activity period, which could range from 17 to 31 hours. This is called the free-running period (FRP). Spiders normally have two distinct spouts of activities throughout the day, one as the light turns on, the other occurs right after the light turns off. The onset of activity of interest in this experiment measures the amount of time it takes for the spider to start locomotor activity when the light turns off. 

We were using behavior data of three spider specise (Latrodectus mactans, Anelosimus studiosus, and Parasteatoda tepidariorum). Spiders were housed in a LD 12:12 cycle in the chambers. Throughout the experiment, the infrared bean crossing was used to measure the locomotive activity of spiders. Our primary question for analysis was does the period of spider activity in the total darkness depend on activity onset after the light goes off. 

## Methodology
1. Clean up original data (move incomplete dates)
2. Save activity to full rastor plots 
3. Visual inspection of dead and live spiders -> delete dead spiders
4. Split the cleaned data into two periods--LD and DD 
5. Make raster plots and ACF plots for each spider in LD and DD separately
6. Detect activity onset for ecah spider 
7. Find period of each spider during LD, if they are entraiend to 24 hour period, then find their FRP
8. Plot FRP against Onset

## Content of Files in the Directory
#### Original_Data.zip
These files contain data of locomotor activity meters of 32 monitors (S1-S32) for three species: Latrodectus, Parasteatoda, and studiosus.  The infrared bean crossing was used to measure the locomotive activity of spiders. Some of the monitors contained living spiders and some were empty. The numerical value in columns S1-S32 is the number of times the infrared bean installed in the monitor has been cross during the time indicated in the second column(Time). Column "Light" contains a light indicator: if 1, the light was on in the chamber, if zero, the light was off.

### Latrodectus
#### 1. Latrodectus_Code.zip
  <br>a. Clean_up.ipynb: cleans up the original .txt file
  <br>b. Make_Images.ipynb: make images of raster plots and ACF plots for each live spiders in LD and DD separately
  <br>c. Activity.ipynb: finds FRP and onset of activity, plot periodogram and acf, and plot scatter plot of FRP vs onset
#### 2. Latrodectus_Data.zip
  <br>a. Latrodectus.txt: orginal data file
  <br>b. Alive.csv: data of dead and live spiders
  <br>c. LD.csv: the activity data in LD period
  <br>d. DD.csv: the activity data in DD period
#### 3. Latrodectus_Figures.zip
  <br>a. Full_Raster_Plots: raster plots for each spider in LD and DD together
  <br>b. LD_Rasters_with_ACF: raster and ACF plots for each live spider in LD period--raster on the left and ACF on the right
  <br>c. DD_Rasters_with_ACF: raster and ACF plots for each live spider in DD period--raster on the left and ACF on the right
  <br>d. Onset: Raster plots with onset of activity indicated by red star
  <br>e. pgram: periodograms and acf of each spider
  <br>f. FRP vs. Onset.png: scatter plot of FRP vs onset

## Instructions on How to Use Files 
1. Use **Clean_Up.ipynb**. In the original .txt file, the last 32 columns are sure to be the activity of the 32 spiders. However, there are some useless columns exists before the last 32 columns. Visually inpect or plot some columns to find the columns represents the 'lights' and add column names to the list named 'colum' accordingly. Then, delete the useless columns (e.g. 'Number'). In **Latrodectus.txt**, only the column 'Number' is useless but in **Parasteatoda.txt** and **Studiosus.txt**, there are six more useless columns that contains only 0 or 1.
2. When plotting the raster plots, since there are some slightly differences with the number of days of different species, adjust the 'figsize' parameter to avoid overlapping.
3. Visually inspect the raster plots and decide whether the spider is alive or not. Save in the **Alive.csv** file (0 for Dead and 1 for Alive).
   <br> Dead (0): if no activity for 4 or more consecutive days
   <br> Alive (1): not dead 
4. **LD.csv** represents the fully cleaned data during LD period and **DD.csv** represents the fully cleaned data during DD period.
5. In **Make_Images.ipynb**, the rolling window can be adjusted according to different species (e.g. since Latrodectus spiders move less frequently, the rolling widow is set to be '2.5 H' and Parasteatoda spiders move more frequently so the rolling widow is set to be '1 H').
6. When making the raster and ACF plots, since the number of days in LD and DD period is different, LD and DD period have to be run separately and adjust the 'figsize' parameter to make the rasters better fit in the figure and avoid overlapping.
7. Run **Activity.ipynb**. The second cell/figure returns FRP/Onset plot using periodogram of period detection. Visual inspection of periodogram and autocorrelation for each spider is also generated for later visual inspections. 
