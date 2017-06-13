# Reading Experiment
## Overview
Self-Paced Reading (SPR) with Cumulative Window followed by a two pictures choice task.

Participant's task is to read sentences. The sentences present in a segment-by-segment fashion.
Participant reveals next segment by hitting a button.
After reading the fist sentence (context) the second sentence (i.e. target sentence) shows.
After the second sentence the participant sees two pictures.

This particular SPR implementation uses a cumulative window:
On each response the segment window grows by one segment, thus revealing a larger part of the sentence.

Current button setup is SPACE_BAR to show next segment and LEFT and RIGHT SHIFT for the choice.

Alternative one can use an attached [BeexyBox](http://www.beexy.org/responseboxes/) which will result in more accurate reaction time measurements.

The participant field reverse_side needs to set to either true or false. If _true_, the location of the two pictures reverse.

## Instructions on how to Zep
* [Installing an Experiment](https://www.beexy.nl/zep/wiki/doku.php?id=experiment:installing)
* [Running an Experiment](https://www.beexy.nl/zep/wiki/doku.php?id=experiment:running)
* [Extracting Experiment Results](https://www.beexy.nl/zep/wiki/doku.php?id=experiment:results)

## Output
* Participant' reading time of the target sentence.
* Participant' reaction time (onset of picture to button press).
* Participant' figure choice.

## Pseudorandomisation
* No more than three of the same type in following properties in sequence (filler/target)

You can test the pseudoranomisation by running
 `zep test_pseudorandomisation.zp`

## Targeted Language
Dutch

## Adding Stimuli
See `stimuli/prac_items.csv` and `stimuli/test_items.csv` for how stimuli are read.

If you want to split a sentence at specific places you can add a "/". The script automatically removes leading and trailing whitespaces of thus created segment and adds a single whitespace at the end.

For instance:
 "Octocat really/loves/that/he/or she/is being used like this."
Will split into:
* Octocat really
* loves
* that
* he
* or she
* is being used like this.

## Image Width and other settings
See `test/defs.zm` for settings.

The width of images can be globally set by changing the value of `IMAGE_WIDTH_PX` to some pixel value.

## DISCLAIMER
This experiment script is released under the terms of the GNU General Public License (see http://www.gnu.org/licenses/gpl-2.0.html). It is distributed in the hope that it will be useful, but with absolutely no warranty. It is your responsibility to carefully study and test the script before using it with real participants.

## Request details
### Script Author
[C. van Run](http://www.uu.nl/staff/CPAvanRun)
### Client
[dr. L. Meroni](https://www.uu.nl/staff/LMeroni/0)
