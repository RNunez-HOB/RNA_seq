# RNA sequence analysis project
The idea for this project is to look for a connection between RNA expression counts and the binary outcome of post-COVID in peripheral blood mononuclear cells in 44 Post-COVID patients and 44 age-, sex- and vaccine-matched persons.\
\
The RNA-counts dataset is publicly available at:\
[GEO Accession viewer](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE286325)

All the samples from the series in the link above can be loaded with the accession-code `GSE286325` \
Or individual samples can be retrieved per run with the codes below.

| Sample accession-code | Sample info |
|-----:|---------------|
|GSM8723640|Run1: 6x post-COV, 5x Control|
|GSM8723641|Run2: 5x post-COV, 6x Control|
|GSM8723642|Run3: 6x post-COV, 5x Control|
|GSM8723643|Run4: 5x post-COV, 6x Control|
|GSM8723644|Run5: 6x post-COV, 5x Control|
|GSM8723645|Run6: 5x post-COV, 6x Control|
|GSM8723646|Run7: 6x post-COV, 5x Control|
|GSM8723647|Run8: 5x post-COV, 6x Control|

# Outline of research steps
Here is a broad outline of steps to start anyone off on their RNA-expression analysis. Keep note of what particular steps were undertaken in your project.
## Load the samples
Using the [GEOparse](https://geoparse.readthedocs.io/en/latest/GEOparse.html) package, load the desired samples
## Clean up data
Look at the convention for dealing with outliers in gene-expression data.\
Dealing with null-values may be sample specific. Sometimes a null-value for gene-expression data may be due to a too low rate-of-detection, meaning it may be a very low value but not quite zero.\
## Dimension reduction
Perform some kind of dimension reduction on the RNA-sequences (I have no idea what this data looks like, but it's almost certainly highly dimensional). Genes and proteins often function in cascades, meaning many will correlate in some way (either positively or negatively, promotion or inhibition).\
`PCA`, `Feature Selection` or `Feature Extraction` should be particularly valuable.
## Analyse data
Random forest methods are typical machine learning approaches used in genomics for bioinformatics. Gradient Boosting and Support Vector Machine are most often used. 
## Research results
