# mmpalx
Multi-mixer Music Production Audio Library (x=for opensource version)

Most of the information has been placed in the "Wiki"... the wiki has pictures... LOL... but still..

HOW IT ALL STARTED
One day while utilizing a Popular DAWS (Digital Audio Workstation Software)(Music Production Software), I was getting annoyed with the interface.  Each time I added a beat I had to STOP and stretch it to the bar count. I had to STOP and align a new clip added.  I had to STOP and answer a prompt about stretching.  And then when I added another loop… I had to repeat this process… over and over again. It was interfering with the creative process.  I’m thinking music but manipulating software. As a Systems Analyst and Software Engineer, I recognized, I was doing the work… not the software.

I realized it was the TRACK VIEW interface.  What is TRULY amazing… is that EACH and EVERY music production software package developed (new and old)(100+) each continued this trend of making it a Track View interface.  I noted 2 software packages that finally discovered that the Track view interface hindered productivity, and developed alternate views (e.g. Ableton – I love the look). To them I say thank you. Now I keep the trend going. One more problem, they all pretty much did the same thing. Of course some better than others.
I went old school, back to the band days and the Recording studio days when the controller would say “Bring in the bass after 8 beats”, and would just click a button on the Mixer board. They didn’t stop to align a track on a screen. And there it was… the old mixer board (Sectional and fluid). And it was a small diagram of mine that made it happen.

THE INVENTION
After isolating each aspect of Music production software into separate parts, I had been looking at my diagram sideways. 
The idea… Isolate the task of the mixer… create an object to handle samples, create a controller, create mini-mixers.  
 
1) The Sampler object handles the samples (pcm, midi, oneshots, etc). 
2) The Mixer handles Multiple Samples
3) The controller handles MULTIPLE MIXERS!

SO NOW;
The user tells the controller “I’m working on 4 bars”. The controller tells the Mixers, the Mixers tells the Samplers. The Samplers trims or duplicates the loop. Beats per minute… the controller relays to mixers and mixers tell the Samplers. Etc Etc Etc.
On call the controller wants to play data… calls the mixers in order (by sections). The mixer calls each of its Samplers which streams the data (at the proper bpm) to the mixer. The mixer mixes and streams the samples to the control which Plays, Saves or Master the data. It calls the next mixer which repeats the process.

The User DOES NOT have to stop and stretch each clip. The user does not have to stop and answer bpm per each loop. The USER just clicks and Adds a loop at each section (1, 2, 4, 8 bars or measures).  SPEEDING up the creation process and allowing the user to focus on the music.

BUT THERES MORE….
Lets make it even faster.   The Sampler also knows if the samples are in pitch groups. IF SO… the user can create a basic harmony from a sequencer.  So now the mixer relays this to the Sampler… that had loaded the samples by the specified scale. So now when the mixer tells the Sampler to give up data… the sampler knows (PER BEAT) which 7 files to extract data, HENCE harmonizing the stream.  OF COURSE the clips may get different melody later.  But while the Producer is creating… he may just want to load the clips and get them ready… and things fit.

PROGRAMMERS DELIGHT…
Each Component (Wave view, Track View, Saving, Loading, Mastering, Exporting, Importing) are SEPARATE components. The main program just passes the mixers to the components and makes the call. The component like Saving just saves the song produced. No tampering with the main program. Mastering.  The mixers are just passed to the component… which process the mixers. No tampering with the main program.

MEMORY
Each Sample(s) loaded by the Sampler is registered.  Each time it is loaded it is checked. Even 1 minute in the song… if it is reloaded it is still checked. ONLY 1 DRY MIX of a loop. Separate wet mix.
Memory before a song.  Memory After a song.

IT STARTED OUT… as a project to make a professional DAWs application more productive, by cleaning up the interface. The “Mixer Tracks Interface” becomes secondary tool. It was designed to Simplify Adding Elements like beats, loops, etc. It was designed to Speed up the Music Making Process. The results…

IT BECAME POWERFUL! It manipulates loops on the fly.  
 The interface is now so clean and intelligent, ANYONE can make professional quality music. Users can be Moms, Pops, Teen, Hobbyist as well as Music STUDENTS, Instructors and Professional Producers
 

