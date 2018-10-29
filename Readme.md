# Pascalson/chatbot-data
The repository is a collection of all chatbot datasets I have used.
I will continually upload my preprocessed datasets to this repo.

The sources of these datasets are listed below:
## English
- OpenSubtitles (~100-180W): 2009 version [source](http://opus.nlpl.eu/OpenSubtitles.php)
- Counted OpenSubtitles: OpenSubtitles sorted by **one-to-many** input-outputs pairs.
- cornell movie-dialog (~22W): [source](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html)

## Chinese
- Chinese_Movie (~240W): [source](https://github.com/fateleak/dgk_lost_conv)
- PTT_Gossiping (~30W): [source](https://github.com/zake7749/Gossiping-Chinese-Corpussorted subtitles)
)

## Synthetics1&2
These are my self-defined synthetic tasks for conditional sequence learning. The two versions have different division of train, dev, and test sets.
- counting: [details](https://arxiv.org/pdf/1808.05599.pdf)
- sequence:
    - definition: continue the input sequence with a random legth.
    - e.g., given input:<1,2,3>, the possible outputs set is {<4, 5, ..., N>| N>=4}
- addition:
    - definition: randomly segment the input sequence; then add the two segmentations.
    - e.g., given input:<1,2,3>,
        - if we divide it into 1 and 23, we will get 24 as the output
        - if we divide it into 12 and 3, we will get 15 as the output
        - the above answers are both in the possible outputs set {<2,4>, <1,5>}
