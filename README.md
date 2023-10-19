# MultiModal Europarl Corpus

This is a repository for MultiModal Europarl Corpus. 

NB. This is a git submodule of `mmep-corpus-process`.

## contents

- `audio/`: empty/git placeholder --place to symlink audio files when working with them
- `metadata/` various kinds of metadata
- `transcribed-audio/`: subdirs of elan projects
	- pfsx files in the gitignore!
- `written-records/`: written versions and translations of Europarl
	- TODO: how to organize this in the best way?
	

## Why submodule?

- keep data conceptually and practically distinct from code that curates data and issues relating to analyses
- allows reuse of data without necessarily relying on the ecosystem developed in the mama-corpus -- [`mmep-corpus-process`](https://github.com/multimodal-europarl/mmep-corpus-process)
 