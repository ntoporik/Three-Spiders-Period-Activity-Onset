# Three-Spiders-Period-Activity-Onset
The goal of this project is to idetntify a pattern in spider circadian activity. Circadian activity of a spider is the cycling of periodic activities over a certain amount of time. This is usually observed to be 24 hours in nature, as the spiders are entrained to the 24 hour cycle of the daily period of light and dark. THis allows the spiders to have anticipatory activities, including eating, locomotion, and resting. However, in environments lacking of entrainment signals and cues from nature (ie complete darkness, constant temperature) the spiders are still able to maintain a periodic cycling of their locomotor activity period, which could range from 17 to 31 hours. This is called the free running period (FRP). Spiders normally have two distinct spouts of activities throughout the day, one as the light turns on, the other occurs right after the light turns off. The onset of activity of interest in this experiment measures the amount of time it takes for the spider to start locomotor activity when the light turns off. 

We were using behavior data of three spider specise (Latrodectus mactans, Anelosimus studiosus, and Parasteatoda tepidariorum). Spiders were housed in a LD 12:12 cycle in the chambers. Throughout the experiment, the infrared bean crossing was used to measure the locomotive activity of spiders. Our primary question for analysis was is the  period of spider activity in the total darkness depend on activity onset after the light goes of. 

[Describe our methodology]
1. Clean data 
2. save activity to full rastor plots 
3. Visual inspection of dead and live spiders -> delete dead keep alive 
4. split data into day and night 
5. make plots: rastor on the left, acf on the right 
6. detect activity onset for ecah spider 
7. find period of each spider during LD, if they are entraiend to 24 hour period, then find their FRP
8. plot FRP against Onset

[Tell the reader about a content of files in the directory]
# data.zip
These files contain data of locomotor activity meters of 32 monitors (S1-S32) for three species: Latrodectus, Parasteatoda, and studiosus.  The infrared bean crossing was used to measure the locomotive activity of spiders. Some of the monitors contained living spiders and some were empty. The numerical value in columns S1-S32 is the number of times the infrared bean installed in the monitor has been cross during the time indicated in the second column(Time). Column "Light" contains a light indicator: if 1, the light was on in the chamber, if zero, the light was off.

# Latrodectus.zip
1. code
  a. Clean_up.ipynb: cleans up original txt files to csv 
  b. Make_Images.ipynb
  c. Activity.ipynb: finds FRP and onset of activity, plot periodogram and acf, and plot scatter plot of FRP vs onset
2. Data;
  a. Latrodectus.txt: orginal data file
  b. Alive.csv: alive spiders
  c. LD.csv
  d. DD.csv
3. Figures
  a. Full_Rastor_Plots
  b. LD_Rastors_with_ACF
  c. DD_Rastors_with_ACF
  d. Onset: Raster plots with onset of activity indicated by red star
  e. pgram: periodograms and acf of each spider
  f. FRP vs. Onset.png: scatter plot of FRP vs onset

[Provide specific instructions how to use files provided to reapeat your analysis

