# Investigation of the performance of driver mutation identification methods using biological networks and enriched biological networks

## Scripts do trabalho desenvolvido e apresentado em formato de artigo completo no 22° Congresso Brasileiro de Computação Aplicada à Saúde (SBCAS 2022)

### 1. Limpeza de todos os MAFs extraídos do cBioPortal.
[MAFcBioPortal -> MAFClean]

- https://github.com/alfredog/SBCAS2022/blob/main/1_convert_mafcBioPortal_mafClean.ipynb

- Pega todos os MAF’s da pasta '/content/drive/MyDrive/Colab Notebooks/mafs_cBioPortal/Original/'
- Faz a limpeza em todos e gera todos os MAFs limpos na pasta '/content/drive/MyDrive/Colab Notebooks/mafs_cBioPortal/Clean/'.


### 2. Conversão de MAFs limpos (MAFClean) para MAFs para o nCop.
[MAFClean -> MAFnCop]

- https://github.com/alfredog/SBCAS2022/blob/main/2_convert_mafClean_nCop.ipynb

- Pega todos os MAFs limpos da pasta '/content/drive/MyDrive/Colab Notebooks/mafs_cBioPortal/Clean/'
- Converte todos os MAFs para o formato padrão do nCop na pasta '/content/drive/MyDrive/Colab Notebooks/mafs_nCop/'.


### 3. Geração das listas de genes para o Endeavour.
[MAFnCop -> MAFGenesList]
[Networks -> NetGenesList]

- https://github.com/alfredog/SBCAS2022/blob/main/3_gerenerate_endeavour_gene_lists.ipynb

- Pega todos os MAFs da pasta'/content/drive/MyDrive/Colab Notebooks/mafs_nCop/' já convertidos para o nCop
- Extraí todos os genes de cada MAF e gera uma lista de genes para cada MAF na pasta '/content/drive/MyDrive/Colab Notebooks/enriquecimento/Endeavour/MAF_lists/' *(Estas listas são usadas como lista de genes de treinamento).*
- Pega todas as redes do caminho '/content/drive/MyDrive/Colab Notebooks/redes/' 
- Extraí todos os genes e gera uma lista de genes para cada rede na pasta '/content/drive/MyDrive/Colab Notebooks/enriquecimento/Endeavour/NET_lists/'. *(Estas listas são usadas como listas de genes candidatos)*.


### 4. Conversão dos resultados do Endeavour para o weights do nCop.
[EndeavourResults -> weights]

- https://github.com/alfredog/SBCAS2022/blob/main/4_convert_EndeavourResults_nCop.ipynb

- Pega todos os resultados do endeavour da pasta '/content/drive/MyDrive/Colab Notebooks/enriquecimento/Endeavour/EndeavourResults/'  e o arquivo de pesos de exemplo do nCop da pasta '/content/drive/MyDrive/Colab Notebooks/enriquecimento/Endeavour/nCopWeightExample/weights.txt'
- Gera novos arquivos de pesos para cada resultado do endeavour na pasta '/content/drive/MyDrive/Colab Notebooks/enriquecimento/Endeavour/nCopWeights/'.

### 5. Geração de script para rodar o nCop no notebook e no Cluster.

- https://github.com/alfredog/SBCAS2022/blob/main/5_generate_script_nCop_execution.ipynb

### 6. Script de avaliação 

- https://github.com/alfredog/SBCAS2022/blob/main/Evaluation_BSB.ipynb

- Precisão (Cosmic)
- Intogen
- CancerMine (avaliações usando dados do Cancer Mine não foram incluidas no trabalho final).





