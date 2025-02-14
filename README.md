# KBSB_course
 Functions to use in Projects

## VisuArc
 Originally written by Mateusz Garbulowski.\
 An arc diagram presenting part of the given network and all its connections dervied from rules. For example, a hub (master regulator) and all genes connected to it.

### Arguments
* net - an output network from the VisuNet
* df - a data frame containing network connection in columns
* discrete - an integer that defines which column from df shall be taken
* dec - a character indciating decision class to be presented
* mainTitle - a character indciating title for the arch diagram


Usage
```
#Download the file to your Desktop
source("PATH/visuArc.R")
ros<-rosetta(autcon)
vis<-visunet(ros$main)
visuArc(vis,'autism',feature='ZSCAN18')
```

## Clustering of Model Rules
 Clustering of model rules groups similar patterns and helps to identify distinguishing features/rule. This enables detection of rules that are most effective in differentiating between distinct decisions or outcomes.
