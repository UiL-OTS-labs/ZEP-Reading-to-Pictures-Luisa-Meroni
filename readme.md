# Implicatures Experiment
Self-Paced Reading with Cumulative Window with picture for implicatures.

Participant's task is to read sentences that are shown beneath a picture. The sentences are presented in a segment-by-segment fashion. Participant reveals next segment by hitting a button. At the final word the participant is to make an additional choice about the sentence and picture.

This particular SPR implementation uses a cumulative window: On each response the segment window grows by one segment, thus revealing a larger part of the sentence.

Current button setup is SPACE_BAR to show next segement and LEFT and RIGHT SHIFT for the additional choice. Alternative one can use an attached [BeexyBox](http://www.beexy.org/responseboxes/).

The value of the left and right button (i.e. 'true' or 'false') is swapped for every other participant. Note that you can
still change this by updating the participant record `left_button`.
## Output
RT between onset exposure of last word and the following button choice.

## Pseudorandomisation
* No more than three of the same type in following properties in sequence (filler/target)
* No same structures may follow each other.
* In a 3-sized window each subject may only occur once.

You can test the pseudoranomisation by running
 zep test_pseudorandomisation.zp

## Targeted Language
Dutch

## Stimuli format
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

## DISCLAIMER
This experiment script is released under the terms of the GNU General Public License (see http://www.gnu.org/licenses/gpl-2.0.html). It is distributed in the hope that it will be useful, but with absolutely no warranty. It is your responsibility to carefully study and test the script before using it with real participants.

## Request details
### Author
[C. van Run](http://www.uu.nl/staff/CPAvanRun)
### Client
Ying Liu
### Supervisors
* [Rick Nouwen](http://www.uu.nl/medewerkers/RWFNouwen)
* [Yaron McNabb](http://www.uu.nl/medewerkers/YMcNabb)
