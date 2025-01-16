# Deciphering the Genomic Landscape Through ECG Signal Analysis: During Movement and Rest
## Bachelor's degree final project
### Problem Statement:
To find the connection between physiological signals, like ECG, and genetic variations to enhance understanding of genetic influences on our health using deep learning.

---
---
### **The data:**
---
The dataset consists of nearly 100,000 ECG recordings from cycling sessions documented in the UK Biobank. Each session includes both rest and active phases, captured during a 7.5-minute fitness test. This dataset offers rich information, including:

        o Multi-channel ECG signals during physical activity and rest.
        o Associated metadata such as heart rate, RPM, and session configurations.
        o Genetic profiles of the participants for SNP (Single Nucleotide Polymorphism) analysis.

---
---
### **Methodology:**
---
This project leverages a 1D-Convolutional Neural Network Autoencoder (1D-CNN-AE) to extract latent features from time-dependent ECG signals. These features are then associated with genetic variations using genome-wide association study (GWAS) techniques.
_Key steps include:_

        > Data Preprocessing: Filtering ECG signals to remove high and low-frequency noise.
        > Feature Extraction: Training a 1D-CNN-AE model to represent the signals in a compressed latent space with minimal information loss.
        > Genomic Analysis: Testing SNPs for associations with the latent features using PLINK2, with multiple testing corrections via Bonferroni.
        > Gene Clustering: Identifying significant SNPs, mapping them to genes using HaploReg, and clustering these genes based on functional relationships using STRING.


---
---
### **Scientific Innovation:**

1) Applying CNN autoencoder.
2) Using ECG information with additional clinical data.
3) Comparing ECG during rest vs. exercise training.
4) Filtering the data before the autoencoder.
---



### Files Included:
1. `search_frontend.py` - contains the method search that will retreive the final ranked list of ('doc_id','title')
2. `QueryProcessor.py` - contains the query extension (Word2Vec), query preprocess methods for the retrieval results.
3. `Pagerank_creator.py` - contains the methods used for ranking the documents: using generating of graph with vertices and edegs.
4. `Pageview_creator.py` - contains Wikipedia pageview data from August 2021 and a dictionary of this pageviews
5. `Index_title_creator.py` - contains the inverted index of the title and all the methods for using this index in BM-25 algorithm. 
6. `Index_body_creator.py` - contains the inverted index of the body and all the methods for using this index in BM-25 algorithm. 
7. `Inverted_index_gcp.py` - contains the inverted index file and all the methods for creating an index.
8. `Buckets_body_title_bins.txt` - contains the files list from the buckets as required.

