#Python Project -- ITP 125 -- Old Spice Commercial README

##Summary
This command-line tool allows users to construct a voice-answering machine .mp3 file using a set of options. This project was created for the ITP 125 Introduction to Computer Security at the University of Southern California.

##Logic
The logic of this type of tool is very basic and intuitive. In order to create an .mp3 file from specified options, we need to (1) get user data concerning the voicemail, (2) retrieve only the necessary files from the internet, (3) construct the mp3 file and (4) cleanup any unneeded files.

###User-data collection
This command-line tool has two main modes of user-data collection: (1) a walkthrough method accessed by the ```--assist``` option, and (2) the more straightforward command-line approach. Both of these options are described below:

####Walkthrough Method
In this version, the logic is quite straightforward, the user is prompted for each option that goes into making the commercial .mp3 file. In this system, much like the next, each option is checked for validity before actually constructing the .mp3 file.

####Command-line Method
Whereas the walkthrough method seeks to provide a step-by-step approach to selecting options for the voicemail, the command-line approach does all of this in a single shot. Ultimately the user will provide information in the format dictated by the ```--help``` command and then the application will create the .mp3 file and store it in the specified output file.

###File Retrieval
Though very straightforward, by recording which files the user will need from step 1, we can effectively download only the files we need form the internet in order to form the mp3 file.

###MP3 Construction
Because different operating systems have different ways of creating mp3 files, the program first checks to see what type of operating system is running, then takes the downloaded files, combines them in the proper order, and finally writes them to the proper output file. 

###Clean-up
The application downloads several files from the internet, but we really don't want the user to retain these files. So instead, the program, using the proper commands for the corresponding operating system, removes those files from the system, to clean-up the location for the user. 

##Version
Python 2.7 and Python 3.3 should both work.

##Command-line options
Command Line options: 
```shell
  -g	male or female (m/f)
	-n	phone number in one of the following formats: 
			123-456-7890
			(123) 456-7890
			123.456.7890
			1234567890
	-r	reasons: pick any of the following options (use one number):
			male: 
				[1] On top of a building
				[2] Cracking Walnuts
				[3] Polishing a monocle
				[4] Ripping weights
			female: 
				[1] Ingesting Old Spice
				[2] Listening to Reading
				[3] Lobster Dinner
				[4] Moon Kiss
				[5] Riding a Horse
	-e	endings: pick any of the following options (use one number):
			male: 
				[1] Riding a Horse
				[2] Listening to a jingle
				[3] On a phone
				[4] Swan dive
				[5] Voicemail
			female: 
				[1] She will get back to you
				[2] Thanks for Calling
	-o	output filename, not path

	--assist	walkthrough of this process
```
> Note that not all possible options used will appear here because some are used by default to make the .mp3 make more sense
