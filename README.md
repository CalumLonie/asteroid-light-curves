# asteroid-light-curves

This repository contains the files related to a project called Asteroid Light Curves.
This was a group in my fourth year, where we were to pick an asteroid, taken image frames of it and extract the asteroid's brightness from each frame to determine its light curve, and from there determine its rotation period and its apparent magnitude.
We had so many issues with this project, including having the right weather for observing, and difficulties getting the analysis code to work.
The weather conditions only allowed us to take pictures of the asteroid on one night; the cloud cover was simply too high every day before and after.
This also affected the other groups that were working on this project, so we all shared the collected data of the same asteroid: 354 Eleonora.
We had originally wanted to study 433 Eros.
It then turned out we had mis-spotted the asteroid in our frames, meaning we were trying to centre the wrong object, and our target left the image frames around an hour into our oberving session.
Because we weren't able to go back to get better data, we had to work with, at best, a partial lightcurve.

I realised recently that I had somehow lost my python files, which did the analysis.
I still have the collected data, and the code is copied into my project report, but I can't work with it again.
So, I decided to take another stab at this project, where I would rewrite the analysis code a few years on, with hopefully more success.
The main aim was to obtain a better partial light curve for 354 Eleonora, using the original data; the difficulties during the original project meant we were never sure if our results were correct or not.
During the original project, we had also created simulated data, which we tried to use as verification our analysis code worked.
We had issues getting the code to track the correct object in the frames, so this was also something I wanted to try to fix, if I had the time to.


There are two main folders in this repository: the Actual_Data folder contains all the frames collected during the observing night (asteroid, star, dark and flat frames) in the Initial_Frames subfolder.
The other two subfolders contain: the asteroid and star frames but with the dark frames combined and removed (the flat frames are of poor quality so aren't used for frame cleaning); these were outputted by the new code (Cleaned_Frames), and the cleaned frames are combined into groups of 10, which are kept in the COmbined_Frames subfolder. These frames are also outputs of the new code.

The other main folder is for the simulated data, created during the original project.
In this folder you find the initial frames (asteroid and star are in the same frame), as well as simulated dark frames in two subfolders.
The other two subfolders contain cleaned frames, and the combined frames, as above.

The reason for star frames being present is that this star is used to correct for extra atmospheric absorption as the asteroid moves up and/or down in the night sky. 
This star was supposed to be as close to the asteroid in apparent magnitude as possible, and ideally in the same frame.


The Debug_Files folder contains two files which were used as test centres for the processes in the analysis code.

This analysis code is contained in four Jupyter Notebook files, two for the "normal" data, and the other two for the simulated data.
The frame_cleaning files do what they say in their titles, they create an average dark frame and remove that from all the image frames.
If the flat frames were any good, they would also be used to correct for aberrations, in the corners of the frames especially.
The tracking_plotting files also do what they say, they find the asteroid/star in each frame, collect their brightness, create a time axis and plot the brightness against this time.
It is possible to also plot apparent magnitude versus time, but I decided not to.


This was a quick project to see if I could get better results than the last time.
I got a more accurate light curve, which was the main aim, and I mostly left it there.
I could have spent mmore time making the code work with the simulated data, though it would have needed more manual corrections than ideal.
The most important was that I managed to get the analysis programs to work as they should, and with better data, some better results would have been possible to obtain.

My initial project report is also in the repository as the PDF file.
