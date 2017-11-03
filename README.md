# JS-808 Practice exercise

The goal of this exercise is to practice designing models and interfaces, and to get a feel for how you architect front-end code.

There aren't good or bad solutions; rather, there are solutions that match the requirements and some that don't. There are solutions that might be considered elegant by some by some and solutions that would be considered clever.

## Time Expectations
We ask that you set aside about 4 hours to complete the exercise. It's ok to go over if you're having fun (drum kits are very fun), but we respect your time. If after 4 hours the exercise is incomplete, share your code and tell us how you would finish it in the form of comments, diagrams, long ramblings with links to things you're thinking about, or anything that will help us understand how you would troubleshoot your way through a task.

Our engineering team cares about having a good work/life balance. Some of our team have done this exercise recently as part of the hiring process. We empathize with any stress you might be under when looking for a career change. Do your best, let your self come through in your work, and try not to stress out. 

## The Exercise:  Building a (Soundless) Drum Machine

This exercise assumes you are somewhat familiar with drum machines.
If you aren't please read http://en.wikipedia.org/wiki/Drum_machine

Your challenge is to code the sequencer part of our Drum Machine, which we called JS-808. Your sequencer should be able to support the famous [four-on-the-floor](http://en.wikipedia.org/wiki/Four_on_the_floor_(music)) rhythm pattern, but be flexible enough to let a user edit the pattern to fit their musical whims.

Here is a wireframe of an example interface. 
![Example interface](/sequence-diagram.png?raw=true)
You can build your app to look like this wireframe. If you're someone who loves css and beautifying the UI, show us that. Approach this task as your way of displaying your
favorite parts of frontend development. 

**READ THIS IT IS REALLY IMPORTANT:**     
This drumkit does **NOT NEED TO PLAY SOUND.** Instead we want to see a real time **VISUAL** representation of the sequence being played.

### REQUIRED FEATURES

Your drum machine should include the following features:

- [ ] Play & stop controls.
- [ ] The ability for the user to alter the tempo of the sequence. This tempo change can occur while the song is stopped or playing – whatever makes the most sense for your code structure.
- [ ] Playback readout - there should be a visual indication of the active step while the sequence is playing. Ideally, the playback speed will also match the
sequence tempo.
- [ ] There should be 3 premade drum pattern sequences that can be loaded into your drumkit. The UI element is up to you; in the wireframe it is the dropdown. 
- [ ] The pattern is expected to be 8 steps or more. eg- if you look at that wireframe, there are 16 columns.
- [ ] The time signature is expected to be 4/4 (if you don't know what that is, don't worry and ignore this instruction).

### Useful Timing Info

At a 4/4 time signature of 60 BPM (beats per minute), we get 1 beat per second.
We can assume that 8 steps = 1 bar, representing 4 beats.
In other words, a 8 step pattern would take `(60/BPM)*4` seconds to play and each step would take `((60/BPM)*4)/8` seconds.

### Extra mile
If you have done all the required features and want to keep going because you just made a cool drumkit, try doing the following:

* Output sound - you might want to look at some higher-level libraries that allow you to load and play sounds rather than getting mired in the details of managing and playing the sounds directly (though you're certainly welcome to do that too).
* Try mix and matching patterns of different durations (8, 16, 32 steps),
  note that if you have 2 patterns, one 8 and one 16, the 8 should play
  twice while the 16 plays once.
* Add support for velocity (the amplitude/volume of a note).
* You don't have to limit yourself to the features/layout/parts on the diagram. Take inspiration from existing drum machines and feel free to get creative!

### What can I use & are we looking for?
- Use the tools you are comfortable with! You can use any framework. You can use plugins & libraries. You can write this entirely in vanilla JS. Want to use canvas? Go for it. 
- Please include a readme. If we need to run the code locally to see it work, please give us instructions.
- Please use this exercise as a way to show us what you like about Frontend Development. Some people live for performance, others for a11y, or great UX or writing tests. We are aware of the time constraint, if what you love takes time, put comments in. 

### Splice Evaluation

If you are given this exercise as a code challenge, we are going to
discuss a few things with you. In order to help you prepare, here is a
list of various specific parts and general aspects of programming we are
interested in discussing:

* How much time did you spend on the exercise, what parts took longer?
* What were the hard parts, what parts did you enjoy most?
* Data modeling - How did you model the concepts of songs and
  tracks/patterns, can you explain why?
* Simplicity vs Flexibility - How flexible is your solution? Can a user
  define patterns of different lengths? Can they play at the same time?
  Can the patterns be changed in real time? Can the velocity be set?
  None of these features are expected, what is needed for you to add
  support for these?
* Is your code tested? Why/why not? How would you test it (or test it better)?


### Submitting your solution

As soon as you're ready, send us a link to your repo (either a fork of this repo or a new one that you created). You don't have to send us the link before you're ready, but we recommend committing code early and often, with clear descriptive commit messages. This helps us follow your thought process as you build your solution.
