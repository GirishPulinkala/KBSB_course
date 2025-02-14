# KBSB_course
 Functions to use in Projects

## VisuArc
 An arc diagram presenting part of the given network and all its connections dervied from rules. For example, a hub (master regulator) and all genes connected to it.

### Arguments
* net - an output network from the VisuNet
* df - a data frame containing network connection in columns
* discrete - an integer that defines which column from df shall be taken
* dec - a character indciating decision class to be presented
* mainTitle - a character indciating title for the arch diagram
* feature - a string indicating feature of choice for investigation


Usage
```
#Download the file to your Desktop
source("PATH/visuArc.R")

#EXAMPLE
ros<-rosetta(autcon)
vis<-visunet(ros$main)
visuArc(net= vis,decision= 'autism',feature='ZSCAN18')
```

## Clustering of Model Rules
 Clustering of model rules groups similar patterns and helps to identify distinguishing features/rule. This enables detection of rules that are most effective in differentiating between distinct decisions or outcomes.

 ### Arguments
 * training_df - a dataframe used for training. e.g. 'autcon' dataset
 * recal - a dataframe consisting of recalulated rules
 * support - an integer specifying minimum support inorder to trim rules

Usage
```
#Download the file to your Desktop
source("PATH/cluster_rules.R")

#EXAMPLE
ros<-rosetta(autcon)
recal<-recalculateRules(autcon,ros$main)
cluster_rules(autcon,recal,support=20)
```
