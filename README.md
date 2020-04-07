# Covid-19: Genomic Data Retrieval, Genomic Epidemiology and Evolutionary Genomics 

> Data is the most powerful weapon humans possess to combat Covid-19.

At an unprecedented scale, the research community came together in the past months to
combat Covid-19. The most significant contribution any researcher can do to fight this virus is: data collection and data analytics. __Everyone can and should make a contribution__.

Here, we aim to provide tools to make it easier for virologists and virus bioinformaticians to retrieve and analyse the genomic sequences of all viruses and in particular, Covid-19.

Unfortunately, we are neither virologists nor virus bioinformaticians, so we are not aware
of all available resources and required analytics that would help the virus community.
__Please contact us or [open issues on this GitHub page](https://github.com/HajkD/covid19/issues) to indicate how we can add further tools or functionality to
make the life of virus researchers easier.__ 

Here some useful data analytics resources we found so far:

- [New York Times article with beautiful data analytics](https://www.nytimes.com/2020/03/20/health/coronavirus-data-logarithm-chart.html)
    - data can be found here: https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports

- [Top 15 R resources on Novel COVID-19 Coronavirus](https://towardsdatascience.com/top-5-r-resources-on-covid-19-coronavirus-1d4c8df6d85f)

- [Coronavirus Datasets](https://www.reddit.com/r/datasets/comments/exnzrd/coronavirus_datasets/)


# Table of Contents
- [1. Data Collection](#data-collection)
    - [1.1. Epidemiological Data](#epidemiological-data)
    - [1.2. Genome Sequencing](#genome-sequencing)
    - [1.3. Genome Assembly](#genome-assembly)
- [2. Data Analytics](#data-analytics)
    - [2.1. Epidemiology](#epidemiology)
    - [2.2. Genomic Data Retrieval and Genomic Epidemiology](#genomic-data-retrieval-and-genomic-epidemiology)
        - [2.2.1. Retrieval of meta-data and genomic sequences](#retrieval-of-meta-data-and-genomic-sequences)


    
## Data Collection

### Epidemiological Data

### Genome Sequencing

Several sequencing companies decided to dedicate significant resources to fight Covid-19.

- [Oxford Nanopore](https://nanoporetech.com/about-us/news/uk-creates-covid-19-genome-sequencing-alliance-large-scale-analysis-virus-oxford) -> [News Timeline](https://nanoporetech.com/about-us/news/covid19-community)
- [SARS-CoV-2 Sequencing Resources](https://github.com/CDCgov/SARS-CoV-2_Sequencing)

### Genome Assembly

- [Genome Assembly — The Holy Grail of Genome Analysis](https://towardsdatascience.com/genome-assembly-the-holy-grail-of-genome-analysis-fae8fc9ef09c)

## Data Analytics

### Epidemiology

- [COVID-19 epidemiology with R](https://rviews.rstudio.com/2020/03/05/covid-19-epidemiology-with-r/)

### Genomic Data Retrieval and Genomic Epidemiology

#### Retrieval of meta-data and genomic sequences



```r
# retrieve genome, proteome, cds, gff/gtf, rna, repeat masker, assembly stats files for SARS-Cov-2
# alternatively, users can specify the taxid -> 'organism = 2697049' 
biomartr::getCollection(db = "refseq", 
                        organism = "Severe acute respiratory syndrome coronavirus 2", 
                        path = "sars_cov_2")
```

```
Starting collection retrieval (genome, proteome, cds, gff/gtf, rna, repeat masker, assembly stats) for Severe_acute_respiratory_syndrome_coronavirus_2 ...
Starting genome retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
Genome download of Severe_acute_respiratory_syndrome_coronavirus_2 is completed!
Checking md5 hash of file: sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt ...
The md5 hash of file 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt' matches!
The genome of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_genomic_refseq.fna.gz'.


Starting proteome retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


Proteome download of Severe_acute_respiratory_syndrome_coronavirus_2 is completed!
Checking md5 hash of file: sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt ...
The md5 hash of file 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt' matches!
The proteome of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_protein_refseq.faa.gz' .


Starting CDS retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
CDS download of Severe_acute_respiratory_syndrome_coronavirus_2 is completed!
Checking md5 hash of file: sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt ...
The md5 hash of file 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt' matches!
The genomic CDS of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_cds_from_genomic_refseq.fna.gz' .


Starting GFF retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
GFF download of Severe_acute_respiratory_syndrome_coronavirus_2 is completed!
Checking md5 hash of file: sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt ...
The md5 hash of file 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt' matches!
Importing 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_genomic_refseq.gff.gz' ...


Starting RNA retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
The download session seems to have timed out at the FTP site 'ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/009/858/895/GCF_009858895.2_ASM985889v3/GCF_009858895.2_ASM985889v3_rna_from_genomic.fna.gz'. This could be due to an overload of queries to the databases. Please restart this function to continue the data retrieval process or wait for a while before restarting this function in case your IP address was logged due to an query overload on the server side.
The genomic RNA of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_rna_from_genomic_refseq.fna.gz' .


Starting Repeat Masker retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
The download session seems to have timed out at the FTP site 'ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/009/858/895/GCF_009858895.2_ASM985889v3/GCF_009858895.2_ASM985889v3_rm.out.gz'. This could be due to an overload of queries to the databases. Please restart this function to continue the data retrieval process or wait for a while before restarting this function in case your IP address was logged due to an query overload on the server side.
The Repeat Masker output file of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_rm_refseq.out.gz'.


Starting assembly quality stats retrieval of 'Severe acute respiratory syndrome coronavirus 2' from refseq ...


|===========================================================================| 100%   53 MB
|===========================================================================| 100%   53 MB
Genome assembly quality stats file download completed!
Checking md5 hash of file: sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt ...
The md5 hash of file 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2/Severe_acute_respiratory_syndrome_coronavirus_2_md5checksums.txt' matches!
The assembly statistics file of 'Severe_acute_respiratory_syndrome_coronavirus_2' has been downloaded to 'sars_cov_2/refseq/Severe_acute_respiratory_syndrome_coronavirus_2' and has been named 'Severe_acute_respiratory_syndrome_coronavirus_2_assembly_stats_refseq.txt'.
Collection retrieval finished successfully!
```

```r
# install.packages("readr")
sars_cov_2_info_all_strains <-
  readr::read_csv(
    "sars_db/sars_cov_2_info_all_strains.csv",
    col_types = readr::cols(
        Accession = readr::col_character(),
        Release_Date = readr::col_datetime(format = ""),
        Species = readr::col_character(),
        Genus = readr::col_character(),
        Family = readr::col_character(),
        Length = readr::col_double(),
        Nuc_Completeness = readr::col_character(),
        Genotype = readr::col_character(),
        Genome_Region = readr::col_character(),
        Segment = readr::col_character(),
        Authors = readr::col_character(),
        Publications = readr::col_double(),
        Geo_Location = readr::col_character(),
        Host = readr::col_character(),
        Isolation_Source = readr::col_character(),
        Collection_Date = readr::col_character(),
        BioSample = readr::col_character(),
        GenBank_Title = readr::col_character()
      ), col_names = TRUE
  )
```


```r
table(sars_cov_2_info_all_strains$Species)
```

```
Severe acute respiratory syndrome-related coronavirus 
                                                 1147
```

```r
table(sars_cov_2_info_all_strains$Geo_Location)
```

```
  Australia     Belgium      Brazil       China     Finland       India        Iran 
         17           2          10         313          12          22          11 
      Italy       Japan    Malaysia       Nepal     Nigeria Philippines South Korea 
         14          11           3          10           1           4          10 
      Spain      Sweden      Taiwan    Thailand         USA    Viet Nam 
         29          10          30           2         553          20 
```


## Genomic Data Retrieval from NCBI RefSeq


```r
biomartr::getGroups(kingdom = "viral")
```

```
[1] "Ackermannviridae"    "Adenoviridae"        "Adomaviridae"       
  [4] "Alloherpesviridae"   "Alphaflexiviridae"   "Alphasatellitidae"  
  [7] "Alphatetraviridae"   "Alvernaviridae"      "Amalgaviridae"      
 [10] "Amnoonviridae"       "Ampullaviridae"      "Anelloviridae"      
 [13] "Arenaviridae"        "Arteriviridae"       "Ascoviridae"        
 [16] "Asfarviridae"        "Aspiviridae"         "Astroviridae"       
 [19] "Avsunviroidae"       "Bacilladnaviridae"   "Baculoviridae"      
 [22] "Barnaviridae"        "Benyviridae"         "Betaflexiviridae"   
 [25] "Bicaudaviridae"      "Bidnaviridae"        "Birnaviridae"       
 [28] "Botourmiaviridae"    "Bromoviridae"        "Caliciviridae"      
 [31] "Carmotetraviridae"   "Caulimoviridae"      "Chrysoviridae"      
 [34] "Chuviridae"          "Circoviridae"        "Clavaviridae"       
 [37] "Closteroviridae"     "Coronaviridae"       "Corticoviridae"     
 [40] "Cruliviridae"        "Cystoviridae"        "Deltaflexiviridae"  
 [43] "Dicistroviridae"     "Endornaviridae"      "Euroniviridae"      
 [46] "Filoviridae"         "Fimoviridae"         "Flaviviridae"       
 [49] "Fusariviridae"       "Fuselloviridae"      "Gammaflexiviridae"  
 [52] "Geminiviridae"       "Genomoviridae"       "Globuloviridae"     
 [55] "Guttaviridae"        "Hantaviridae"        "Hepadnaviridae"     
 [58] "Hepeviridae"         "Herelleviridae"      "Herpesviridae"      
 [61] "Hypoviridae"         "Hytrosaviridae"      "Iflaviridae"        
 [64] "Inoviridae"          "Iridoviridae"        "Kitaviridae"        
 [67] "Lavidaviridae"       "Leviviridae"         "Lipothrixviridae"   
 [70] "Luteoviridae"        "Malacoherpesviridae" "Marnaviridae"       
 [73] "Marseilleviridae"    "Matonaviridae"       "Medioniviridae"     
 [76] "Megabirnaviridae"    "Mesoniviridae"       "Metaviridae"        
 [79] "Microviridae"        "Mimiviridae"         "Mononiviridae"      
 [82] "Mymonaviridae"       "Myoviridae"          "Mypoviridae"        
 [85] "Nairoviridae"        "Nanoviridae"         "Narnaviridae"       
 [88] "Nimaviridae"         "Nodaviridae"         "Nudiviridae"        
 [91] "Nyamiviridae"        "Orthomyxoviridae"    "Other"              
 [94] "Ovaliviridae"        "Papillomaviridae"    "Paramyxoviridae"    
 [97] "Partitiviridae"      "Parvoviridae"        "Peribunyaviridae"   
[100] "Permutotetraviridae" "Phasmaviridae"       "Phenuiviridae"      
[103] "Phycodnaviridae"     "Picobirnaviridae"    "Picornaviridae"     
[106] "Pithoviridae"        "Plasmaviridae"       "Pleolipoviridae"    
[109] "Pneumoviridae"       "Podoviridae"         "Polycipiviridae"    
[112] "Polydnaviridae"      "Polyomaviridae"      "Portogloboviridae"  
[115] "Pospiviroidae"       "Potyviridae"         "Poxviridae"         
[118] "Qinviridae"          "Quadriviridae"       "Reoviridae"         
[121] "Retroviridae"        "Rhabdoviridae"       "Roniviridae"        
[124] "Rudiviridae"         "Secoviridae"         "Siphoviridae"       
[127] "Smacoviridae"        "Solemoviridae"       "Solinviviridae"     
[130] "Sphaerolipoviridae"  "Spiraviridae"        "Sunviridae"         
[133] "Tectiviridae"        "Tobaniviridae"       "Togaviridae"        
[136] "Tolecusatellitidae"  "Tombusviridae"       "Tospoviridae"       
[139] "Totiviridae"         "Tristromaviridae"    "Turriviridae"       
[142] "Tymoviridae"         "unclassified"        "Virgaviridae"       
[145] "Wupedeviridae"       "Xinmoviridae"        "Yueviridae"
```

```r
coronaviruses <- biomartr::listGenomes(db = "refseq", type = "subgroup", subset = "Coronaviridae")
# look at results
coronaviruses
```

```
[1] "Human coronavirus 229E"                               
 [2] "Camel alphacoronavirus"                               
 [3] "Porcine epidemic diarrhea virus"                      
 [4] "Human coronavirus NL63"                               
 [5] "Human coronavirus HKU1"                               
 [6] "Swine enteric coronavirus"                            
 [7] "Rhinolophus bat coronavirus HKU2"                     
 [8] "Scotophilus bat coronavirus 512"                      
 [9] "Miniopterus bat coronavirus HKU8"                     
[10] "Rousettus bat coronavirus HKU9"                       
[11] "Tylonycteris bat coronavirus HKU4"                    
[12] "Pipistrellus bat coronavirus HKU5"                    
[13] "Severe acute respiratory syndrome-related coronavirus"
[14] "Severe acute respiratory syndrome coronavirus 2"      
[15] "Beluga whale coronavirus SW1"                         
[16] "Bat coronavirus BM48-31/BGR/2008"                     
[17] "Common moorhen coronavirus HKU21"                     
[18] "Magpie-robin coronavirus HKU18"                       
[19] "Night heron coronavirus HKU19"                        
[20] "Sparrow coronavirus HKU17"                            
[21] "White-eye coronavirus HKU16"                          
[22] "Wigeon coronavirus HKU20"                             
[23] "Rabbit coronavirus HKU14"                             
[24] "Rousettus bat coronavirus HKU10"                      
[25] "Ferret coronavirus"                                   
[26] "Middle East respiratory syndrome-related coronavirus" 
[27] "BtRf-AlphaCoV/YN2012"                                 
[28] "Bat coronavirus"                                      
[29] "Lucheng Rn rat coronavirus"                           
[30] "Wencheng Sm shrew coronavirus"                        
[31] "Bat coronavirus CDPHE15/USA/2006"                     
[32] "Coronavirus AcCoV-JC34"                               
[33] "Porcine coronavirus HKU15"                            
[34] "Betacoronavirus Erinaceus/VMC/DEU/2012"               
[35] "BtRf-AlphaCoV/HuB2013"                                
[36] "BtMr-AlphaCoV/SAX2011"                                
[37] "BtNv-AlphaCoV/SC2013"                                 
[38] "NL63-related bat coronavirus"                         
[39] "Betacoronavirus HKU24"                                
[40] "Bat Hp-betacoronavirus/Zhejiang2013"                  
[41] "Rousettus bat coronavirus"  
```

```r
sars <- coronaviruses[stringr::str_detect(coronaviruses, 
              "Severe acute respiratory syndrome")]
# look at sars annotation in NCBI RefSeq
sars
```

```
[1] "Severe acute respiratory syndrome-related coronavirus"
[2] "Severe acute respiratory syndrome coronavirus 2"
```

Users can now download the genome, proteome, CDS, RNA, GFF, Repeat Masker, and AssemblyStats files for both SARS viruses:

```r
# Retrieve a Collection for SARS and SARS2: 
# Genome, Proteome, CDS, RNA, GFF, Repeat Masker, AssemblyStats
biomartr::getCollectionSet(db = "refseq", organisms = sars, path = "SARS")
```


