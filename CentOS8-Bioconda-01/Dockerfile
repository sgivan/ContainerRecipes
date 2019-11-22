FROM centos
RUN yum install -y vim wget
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
RUN sh ./Miniconda3-latest-Linux-x86_64.sh -b
RUN /root/miniconda3/bin/conda init
RUN source /root/.bashrc
RUN conda config --add channels defaults
RUN conda config --add channels bioconda
RUN conda config --add channels conda-forge
