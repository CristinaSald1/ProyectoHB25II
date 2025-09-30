# ProyectoHB25II; Identificación de bacerias zoonóticas mediante análisis de secuencias 16S
Este repositorio contiene un flujo de trabajo para el análisis de secuencias 16S rRNA con el fin de identificar bacterias zoonóticas, utilizando datos de referencia del estudio:
Dueholm, M. S., Andersen, K. S., McIlroy, S. J., Kristensen, J. M., Yashiro, E., Karst, S. M., Albertsen, M., & Nielsen, P. H. (2020). Generation of Comprehensive Ecosystem-Specific Reference Databases with Species-Level Resolution by High-Throughput Full-Length 16S rRNA Gene Sequencing and Automated Taxonomy Assignment (AutoTax). mBio, 11(5), e01557-20. https://doi.org/10.1128/mbio.01557-20

## Objetivo  
Implementar un pipeline reproducible para:  
- Procesar secuencias 16S rRNA.  
- Asignar taxonomía con resolución a nivel de especie.  
- Identificar posibles bacterias zoonóticas según bases de datos de referencia.

## Metodología  
1. **Obtención de secuencias**: datos crudos en formato FASTA/FASTQ.  
2. **Preprocesamiento**: control de calidad, trimming y filtrado.  
3. **Clustering/denoising**: con herramientas como DADA2 o QIIME2.  
4. **Asignación taxonómica**: empleando AutoTax y la base de datos generada en el estudio de referencia.  
5. **Filtrado zoonótico**: comparación con literatura y bases de datos de bacterias zoonóticas.

## Estructura del repositorio  
```bash
├── data/            # Secuencias de entrada y de referencia
├── results/         # Archivos de salida: taxonomía, tablas OTUs/ASVs, gráficas
├── scripts/         # Scripts en R/Python para análisis
├── environment.yml  # Dependencias del entorno Conda
└── README.md        # Este archivo
