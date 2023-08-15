# R for statistical tools and tests

!!! info
    
    === "Keypoints"
    
        - R is popular for statistical tests
        - PCA can make your data easier to comprehend
        - Genetic variation can be population-specific

    === "Objectives"

        - Investigate diversity in population-specific genetic variation
        - Understand PCA and how to run it in R
        

## Population diversity

We will now load a second dataset which contains a new set of SNPs. Rather than being medically relevant, these SNPs were chosen because they are informative about ancestry. That is, variation in their genotype frequencies tends to be associated with differences between population groups. 

!!! r-project "r"

    ```r
    ## Load ancestry data
    snpAns = read.table('GENE360snpAncestry.txt', header=T, sep='\t')
    ## Check dimensionality of data
    dim(snpAns)
    ```
    ## [1] 2504 2305

Now we now have a *much* larger dataset: 2504 individuals and 2302 SNP genotypes for each individual. 
**Note**: I've said there are 2302 SNP genotypes, but the dim function above returned 2305 columns. Think back to some of the functions you have used earlier and use one (or more) to check what the other three columns are. 

??? success "Solution"

        A)

        !!! r-project "r"

            ```r
            View(snpAns)
            ```
        
        
        B)

        !!! r-project "r"

            ```r
            names(snpAns)
            ```
        

