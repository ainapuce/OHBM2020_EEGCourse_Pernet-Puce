# OHBM2020_EEGCourse_Pernet-Puce
Slides, video & data from Puce's talk in OHBM2020 Educational Course entitled: EEG data acquisition & appropriate data pre-processing: not so basic after all?

Here is the link to the video of the talk: https://www.dropbox.com/s/gcgkfpsp5wczf22/OHBM2020_EEG_Course_Video_final_%28Source%29.mp4?dl=0
Below is some information on the files related to the video that are stored in this repo:

1.	Slides themselves: Puce_OHBM2020Course_SlidesFINAL.pdf

2.	Muse portable EEG headset headshot: MuseLiveDemo_headshot.jpeg

3.	Muse portable EEG headset data: mindMonitor_2020-07-10--14-46-45.csv
Note: this is a very short ~5 sec file that displays Muse Monitor app output format. I did not record all the data during the presentation, but just a quick sample so that the format of the file can be seen.

4.	CGX portable EEG headset headshot: CGX_8channelEEG_headshot.jpg

5.	CGX portable EEG headset data, 3 output files consisting of EEG data, header file & marker file in CGX standard format: CGX_rawdata_2020-07-10.eeg, CGX_rawdata_2020-07-10.vhdr, CGX_rawdata_2020-07-10.vmrk
The latter 2 files contain header information, such as 13 channels of data (8 EEG channels, 3 accelerometers, 1 packet counter channel & 1 digital trigger channel) & mrker information (if present).

6.	EEGLAB compatible CGX portable EEG headset data files: CGX_EEGLABcompatible.set, CGX_EEGLABcompatible_filtered1.set, CGX_EEGLABcompatible_filtered2.set
These files are all EEGLAB readable. Their output can be best viewed in the scrolling display using a sensitivity setting of ~250 microvolts.

The 1st file shows the actual data that were acquired at 500 Hz (with bandpass filtering of DC-131 Hz) during the video presentation. Note that during the actual video demonstration, Dr Ben Ramsden adjusted the display on the CGX software so that we could see the signals better (the filtering of the display was initially 0.5-60 Hz, and then later was set to 2-60 Hz – the video shows when these adjustments were made). These adjustments to the display DID NOT affect the data acquisition. The EEG data in this file are noisy - the aim here was to demonstrate artifacts & sources of interference!

The 2nd file shows the EEG data after baseline correction and bandpass filtering of 0.5-100 Hz has been made on the data. The aim here was to allow the EEG signals & artifacts to be viewed more clearly.

The 3rd file shows the EEG data after an additional post hoc low pass filter of 40 Hz has been applied. No artifact rejection has been attempted - again the purpose here is to show what artifacts look like with further filtering using a low pass of 40 Hz. This has been a commonly used filter setting in the EEG/MEG literature. As can be seen, some of these artifacts have now been masked by the filtering – this can be problematic, as only some of the muscle activity might be filtered out. Different facial muscles can produce EMG activity at different frequencies – sdepending on the muscle - some of which can dip right down into EEG frequency bands (gamma, beta & even alpha)! This can be particularly problematic for those studying variations in frequency content of EEG signals.
-Aina
