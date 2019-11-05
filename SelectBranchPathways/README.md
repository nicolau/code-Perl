# Script to select pathways belong to specific branch
select_pathway.pl is a script to select a specific branch from reactome pathways gmt file. This script is useful if you need to do the enrichment pathway analysis for all pathways from "Immune System" for example.

## The command for analysis is:

Download the SelectedBranchPathways
```
mkdir SelectBranchPathways
cd SelectBranchPathways
wget https://raw.githubusercontent.com/nicolau/code-Perl/master/SelectBranchPathways/ReactomePathways.gmt
wget https://raw.githubusercontent.com/nicolau/code-Perl/master/SelectBranchPathways/ReactomePathwaysRelation.txt
wget https://raw.githubusercontent.com/nicolau/code-Perl/master/SelectBranchPathways/select_pathways.pl
```

## How to execute script
```
perl select_pathways.pl --gmt-file ReactomePathways.gmt --relation ReactomePathwaysRelation.txt --search-code "R-HSA-168256" | sort | uniq > ReactomePathwaysOnlyImmuneResponseBranch.gmt
```
