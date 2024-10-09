# InTraSeq

This repository contains code for the InTraSeq paper:

Ariss, M.M., Huang, L., Ding, X., Sheth, S., Levy, T., Fisher, J., Loebelenz, J., Arlotta, K., Dixon, K., Polakiewicz, R. and Kuchroo, V.K., 2024. InTraSeq: A Multimodal Assay that Uncovers New Single-Cell Biology and Regulatory Mechanisms. bioRxiv, pp.2024-09.


`
> SessionInfo()
R version 4.3.3 (2024-02-29)
Platform: x86_64-redhat-linux-gnu (64-bit)
Running under: CentOS Stream 8

Matrix products: default
BLAS:   /usr/lib64/R/lib/libRblas.so 
LAPACK: /usr/lib64/R/lib/libRlapack.so;  LAPACK version 3.11.0

locale:
 [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C               LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8    
 [5] LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8    LC_PAPER=en_US.UTF-8       LC_NAME=C                 
 [9] LC_ADDRESS=C               LC_TELEPHONE=C             LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       

time zone: America/New_York
tzcode source: system (glibc)

attached base packages:
 [1] parallel  grid      stats4    stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] ROCR_1.0-11                 KernSmooth_2.23-24          fields_14.1                 viridis_0.6.5              
 [5] viridisLite_0.4.2           spam_2.9-1                  DoubletFinder_2.0.4         circlize_0.4.16            
 [9] ComplexHeatmap_2.16.0       sparseMatrixStats_1.12.2    Matrix_1.6-5                data.table_1.15.4          
[13] DropletUtils_1.20.0         SingleCellExperiment_1.22.0 SummarizedExperiment_1.30.2 Biobase_2.60.0             
[17] GenomicRanges_1.52.1        GenomeInfoDb_1.36.4         IRanges_2.34.1              S4Vectors_0.38.2           
[21] BiocGenerics_0.46.0         MatrixGenerics_1.12.3       matrixStats_1.3.0           ggsignif_0.6.4             
[25] ggbeeswarm_0.7.2            cowplot_1.1.1               openxlsx_4.2.6.1            RColorBrewer_1.1-3         
[29] Seurat_5.1.0                SeuratObject_5.0.2          sp_2.1-2                    lubridate_1.9.3            
[33] forcats_1.0.0               stringr_1.5.1               dplyr_1.1.4                 purrr_1.0.2                
[37] readr_2.1.5                 tidyr_1.3.1                 tibble_3.2.1                ggplot2_3.4.4              
[41] tidyverse_2.0.0            

loaded via a namespace (and not attached):
  [1] RcppAnnoy_0.0.21          splines_4.3.3             later_1.3.2               bitops_1.0-8             
  [5] R.oo_1.26.0               polyclip_1.10-6           fastDummies_1.7.3         lifecycle_1.0.4          
  [9] doParallel_1.0.17         edgeR_3.42.4              globals_0.16.2            lattice_0.22-6           
 [13] MASS_7.3-60.0.1           magrittr_2.0.3            sass_0.4.9                limma_3.56.2             
 [17] plotly_4.10.3             rmarkdown_2.28            jquerylib_0.1.4           yaml_2.3.10              
 [21] httpuv_1.6.15             sctransform_0.4.1         zip_2.3.1                 spatstat.sparse_3.0-2    
 [25] reticulate_1.34.0         pbapply_1.7-2             maps_3.4.2                abind_1.4-5              
 [29] zlibbioc_1.46.0           Rtsne_0.17                R.utils_2.12.3            RCurl_1.98-1.16          
 [33] GenomeInfoDbData_1.2.10   ggrepel_0.9.5             irlba_2.3.5.1             listenv_0.9.0            
 [37] spatstat.utils_3.0-3      goftest_1.2-3             RSpectra_0.16-1           dqrng_0.3.2              
 [41] spatstat.random_3.1-6     fitdistrplus_1.1-11       parallelly_1.36.0         DelayedMatrixStats_1.22.6
 [45] leiden_0.4.3              codetools_0.2-20          DelayedArray_0.26.7       scuttle_1.10.3           
 [49] shape_1.4.6.1             tidyselect_1.2.1          farver_2.1.2              spatstat.explore_3.2-3   
 [53] jsonlite_1.8.8            GetoptLong_1.0.5          progressr_0.14.0          iterators_1.0.14         
 [57] ggridges_0.5.4            survival_3.7-0            foreach_1.5.2             tools_4.3.3              
 [61] ica_1.0-3                 Rcpp_1.0.13               glue_1.7.0                gridExtra_2.3            
 [65] xfun_0.47                 HDF5Array_1.28.1          withr_3.0.1               fastmap_1.2.0            
 [69] rhdf5filters_1.12.1       fansi_1.0.6               digest_0.6.37             timechange_0.3.0         
 [73] R6_2.5.1                  mime_0.12                 colorspace_2.1-1          scattermore_1.2          
 [77] tensor_1.5                spatstat.data_3.0-1       R.methodsS3_1.8.2         RhpcBLASctl_0.23-42      
 [81] utf8_1.2.4                generics_0.1.3            renv_1.0.5                httr_1.4.7               
 [85] htmlwidgets_1.6.4         S4Arrays_1.0.6            uwot_0.1.16               pkgconfig_2.0.3          
 [89] gtable_0.3.5              lmtest_0.9-40             XVector_0.40.0            htmltools_0.5.8.1        
 [93] dotCall64_1.0-2           clue_0.3-65               scales_1.3.0              png_0.1-8                
 [97] harmony_1.2.0             knitr_1.48                rstudioapi_0.16.0         rjson_0.2.21             
[101] tzdb_0.4.0                reshape2_1.4.4            nlme_3.1-166              cachem_1.1.0             
[105] GlobalOptions_0.1.2       zoo_1.8-12                rhdf5_2.44.0              miniUI_0.1.1.1           
[109] vipor_0.4.7               pillar_1.9.0              vctrs_0.6.5               RANN_2.6.1               
[113] promises_1.3.0            beachmat_2.16.0           xtable_1.8-4              cluster_2.1.6            
[117] beeswarm_0.4.0            evaluate_0.24.0           isoband_0.2.7             locfit_1.5-9.10          
[121] cli_3.6.3                 compiler_4.3.3            rlang_1.1.4               crayon_1.5.3             
[125] future.apply_1.11.1       labeling_0.4.3            plyr_1.8.9                stringi_1.8.4            
[129] deldir_2.0-4              BiocParallel_1.34.2       munsell_0.5.1             lazyeval_0.2.2           
[133] spatstat.geom_3.2-5       RcppHNSW_0.5.0            hms_1.1.3                 patchwork_1.1.3          
[137] future_1.33.1             Rhdf5lib_1.22.1           shiny_1.9.1               highr_0.11               
[141] igraph_2.0.2              bslib_0.8.0 
`
