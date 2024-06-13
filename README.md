# ATAC-seq-Consensus-Peak-Set

## Step 1
Merge beds -> cat f1 f2... `cat */peak_calling*/*normalized.narrowPeak`

## Step 2
Ffilter scores < 5 -> `awk '$5>=5'`

## Step 3
`bedtools genomecov -bg -i input.bed -g genome.file`

## Step 4
Filter coverage > 3 samples `awk '$4>=3'`

## Step 5
Merge adjacent peaks `bedtools merge`

## Step 5
Histogram of the distribution of peak width

## Step 6
Filter out peaks that are too short. bedtools length?
