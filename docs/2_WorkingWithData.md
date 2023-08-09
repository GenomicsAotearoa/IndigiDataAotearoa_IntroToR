# Analysing genetic variant data in R

!!! info
    
    === "Keypoints"
    
        - R can hold data as Objects and Functions can be used to ask questions of that data
        - The 1000 Genomes Project is a public resource for genetic data
        - SNPS (Single Nucleotide Polymorphisms) are small changes to our DNA that can be medically relevant

    === "Objectives"

        - Load publicly (freely) available data from The 1000 Genomes Project into R
        - 


## The data: Single Nucleotide Polymorphisms (SNPS) from the 1000 Genomes Project

The data you will be working with today is publicly available high-throughput sequencing data from a resource called the 1000 genomes project. 

We have downloaded a (small) subset of the 1000 genomes data, called the file snpData.txt, and placed it in your home directory (`/home/$USER/IndigiData_IntroToR/`). To read the 'snpData.txt' data file into R, we will use the read.table() function:

!!! r-project "r"

    ```r
    # Read in the txt file and save it as 'snpData'

    snpData <- read.table("/home/<USERID>/IndigiData_IntroToR/snpData.txt",sep='\t',header=T)
    ```

Reminder: the format here is to create a new object (snpData) and store some information in it, in this case storing information that is obtained using the read.table function. The format for function is 'function(target of the function, refining or specifying the details)'.




