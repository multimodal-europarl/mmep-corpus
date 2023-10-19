# the audio-video directory

This directory contains 
- subdirectories corresponding to each media file
- a list of original media files

## Why subdirectories?

1. The media related to this project takes up a lot of space. The idea of organizing into sub-directories allows for targeted inclusion/deletion from a local machine. One way of working (supported by the mmep-process-corpus development), is to symlink files to a more static location.
2. Original media contains audio tracks for each interpreted language that necessarily need to be extracted for the curation process. It will be handy to have them in a dedicated container.