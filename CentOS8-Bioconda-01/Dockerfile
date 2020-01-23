FROM centos
RUN yum install -y vim wget
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
RUN sh ./Miniconda3-latest-Linux-x86_64.sh -b
RUN /root/miniconda3/bin/conda init
RUN source /root/.bashrc
RUN /root/miniconda3/bin/conda config --add channels defaults
RUN /root/miniconda3/bin/conda config --add channels bioconda
RUN /root/miniconda3/bin/conda config --add channels conda-forge
RUN /root/miniconda3/bin/conda create -n rnaseq star samtools bioconductor-edger bioconductor-deseq2 kallisto salmon rsem bioconductor-tximport snakemake
RUN /root/miniconda3/bin/conda install -n rnaseq --freeze-installed snakemake
RUN /root/miniconda3/bin/conda create -n aligners bowtie bowtie2 bwa samtools
