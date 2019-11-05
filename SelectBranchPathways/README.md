# Script to select pathways belong to specific branch
select_pathway.pl is a script to select a specific branch from reactome pathways gmt file. This script is useful if you need to do the enrichment pathway analysis for all pathways from "Immune System" for example.

## The command for analysis is:

Download the SelectedBranchPathways
```
wget ""
```

## How to execute script
```
cd SelectBranchPathways
perl select_pathways.pl --gmt-file ReactomePathways.gmt --relation ReactomePathwaysRelation.txt --search-code "R-HSA-168256" | sort | uniq > ReactomePathwaysOnlyImmuneResponseBranch.gmt
```
