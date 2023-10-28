# MultiModal Europarl Corpus

This is a repository for MultiModal Europarl Corpus. 

NB. This is a git submodule of `mmep-corpus-process`.


## contents

### The `audio-video/` directory

- `audio/`: empty/git placeholder --place to symlink audio files when working with them


### The `medatada/` directory

- `metadata/` various kinds of metadata

### The `transcribed-audio/` directory

The structure of `transcribed-audio/` mirrors the `audio-video/` directory. Each subdirectory contains 

- symlinks to corresponding audio/video files
- an elan `.eaf` document
- `.xml` or `.csv` files with document level metadata
- [UNTRACKED] a `.pfsx` file (incl. in gitignore)

#### Document Level metadata

Elan doesn't allow for the use of unspecified xml elements or attributes -- of course one can add them to a file, but opening/work/saving will overright/remove these elements, or in exreme cases, Elan will fail to load a file that's too strange.

This means that metadata cannot be directly added to `.eaf` files, but since we want to preserve usability of the corpus files with elan to facilitate corrections to the transcriptions, we make use of an external metadata file.

Elan annotation IDs are given a more elaborate value (defaule = "a1", "a2", etc.) --> "a-uuid_1", "a-uuid_2", etc. This allows 

- (a) to keep fragment-level metadata (e.g. who is the speaker of a given fragment) as well as document-level metadata (date, part of debate type, or whatever)
- (b) refer to specific fragments for both quality control and ensuring that manually corrected fragments are not overwritten

We store all this in a document with the (to be defined/identified) schema.


### The `written-records/` directory

- `written-records/`: written versions and translations of Europarl
	- TODO: how to organize this in the best way?
	

## Why submodule?

- keep data conceptually and practically distinct from code that curates data and issues relating to analyses
- allows reuse of data without necessarily relying on the ecosystem developed in the mama-corpus -- [`mmep-corpus-process`](https://github.com/multimodal-europarl/mmep-corpus-process)
 