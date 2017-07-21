# JS-808 Practice exercise

The goal of this exercise is to practice designing models and
interfaces, and to get a feel for how you architect front-end code.

There aren't good or bad solutions, there are solutions that
match the requirements and some that don't. There are solutions that
might be considered elegant by some and solutions that would be
considered clever.

## Building a Drum Machine

This exercise assumes you are somewhat familiar with drum machines.
If you aren't
please read http://en.wikipedia.org/wiki/Drum_machine

Your challenge is to code the sequencer part of our Drum Machine which
we called JS-808. Your sequencer should be able to support the famous [four-on-the-floor](http://en.wikipedia.org/wiki/Four_on_the_floor_(music)) rhythm pattern, but be flexible enough to let a user edit the pattern to fit their musical whims.

![Example interface](/sequence-diagram.png?raw=true)

Note that instead of hearing an actual sound, you are expected to
generate a real time visual representation of the sequence being played.

### Expected Features

Your drum machine should include the following features:

* Basic transport controls (play, stop).
* The ability to alter the tempo of the sequence.
* Playback readout - there should be a visual indication of the current steps
while the sequence is playing. Ideally, the playback speed will also match the
sequence tempo.
* A list of at least 3 preset sequence patterns.


### Extra Info

* A song contains multiple patterns being sequenced for different
  samples.
* A song plays at a given tempo (AKA bpm), the tempo does not need to
  be able change while the song plays.
* The time signature is expected to be 4/4 (if you don't know what that
  is, don't worry and ignore this instruction).
* The pattern is expected to be 8 steps or more.

### Tools and Frameworks

Feel free to use whatever framework you want or no framework at all.

### Useful Timing Info

At a 4/4 time signature of 60 BPM (beats per minute), we get 1 beat per second.
We can assume that 8 steps = 1 bar, representing 4 beats.
In other words, a 8 step pattern would take `(60/BPM)*4` seconds to play and each step would take `((60/BPM)*4)/8` seconds.


### Extra mile

* Try mix and matching patterns of different durations (8, 16, 32 steps),
  note that if you have 2 patterns, one 8 and one 16, the 8 should play
  twice while the 16 plays once.
* Add support for velocity (the amplitude/volume of a note).
* Try to output sound - you might want to look at some higher-level libraries that allow you to load and play sounds rather than getting mired in the details of managing and playing the sounds directly (though you're certainly welcome to do that too).
* You don't have to limit yourself to the features/layout/parts on the diagram. Take inspiration from existing drum machines and feel free to get creative!

##### If you can't stop:

* How about live play? Can you allow users to add/remove/change patterns
  while playing?
* If you added sound playback, how about adding some visualizations? The Web Audio API provides some useful primitives for generating visual feedback.


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
* Is your code tested? Why/why not? How would you test it (or better)?


### Submitting your solution

As soon as you're ready, send us a link to your repo (either a fork of this repo or a new one that you created). You don't have to send us the link before you're ready, but we recommend committing code early and often, with clear descriptive commit messages. This helps us follow your thought process as you build your solution.
