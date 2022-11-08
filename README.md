# Beethoven Piano Sonata Motif Dataset

This dataset contains annotations of musical moitfs for the 1st movements from Beethoven's 32 piano sonatas. The dataset can be used for repeated pattern recognition in music and melody similarity analysis.

## Overview
For the csv file in the folder "csv_notes", each row represents a note event from the original movement. There are 7 columns to describe the properties of a note event.
* onset (in crotchet beats)
* MIDI note number
* morphetic pitch number
* duration (in crotchet beats)
* staff number (integers from zero for the top staff)
* measure (-1 for incomplete measure)
* motif type (no value means the note doesn't belong to a motif)

In the folder "motif_midi", all tempi of midi files are 60 quarter notes per minute, and they only contain notes belonging to motifs instead of complete notes. To retrieve a certain motif, we can utilize the label in the folder "label_csv".
For the csv file in "label_csv", each row carries the informations of a motif. 
The most important informations (columns) are "start_midi", "end_midi", "track", and "type". Other informations are only useful for checking and debugging.
* start_midi: the start time (in second) of the motif.
* end_midi: the end time (in second) of the motif.
* track: the track number of the motif in the midi file. (Since multiple motifs may overlap, we wrote these motifs into different tracks.)
* type: the type of the motif.
