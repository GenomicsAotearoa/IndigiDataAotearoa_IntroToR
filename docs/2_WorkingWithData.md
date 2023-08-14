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

Let's use some other functions to inspect the data and learn basic facts about the structure of our data object:

!!! r-project "r"

    ```r
    # The dim function will tell us how many rows (individuals) and columns the dataset contains:

    dim(snpData)

    ## [1] 2504     9
    ```

This tells us there are 2504 rows and 9 columns. We know that the rows are individuals, but what are the columns? 

The 'names' function can be used to the column names:

!!! r-project "r"

    ```r
    names(snpData)
    ```

??? success "Output"

    ```
## [1] "SubjectID"  "Population" "rs3826656"  "rs13387042" "rs4779584"  "rs2398162"  "rs1344706"  "rs7659604"  "rs734553"
    ```
This function shows us the names of the nine columns: The first two tell us the SubjectID (an identifier for the individual from whom the data was collected) and Population (where the individual came from). The next seven names are "rs" followed by a string of numbers. These rs numbers are SNP names - each known SNP has a unique identifier. 

What **are** SNPs?

SNPs (Single Nucleotide Polymorphisms) are places in the genome where some individuals in the population have variation at a single DNA base (e.g., some people may have an "A" base at a certain location in the genome, while others have a "G" at that exact same location). The majority of SNPs don't have a (known) impact on health or function, but some do. One of the things we often ask about a SNP is how common is it in the population.


To look at the full dataset, you can use the View() function:
!!! r-project "r"

    ```r
    View(snpData)
    ```

