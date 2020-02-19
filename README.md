# reproducibility-tutorial
FOSS 2020
    1  cd /scratch
    2  df -h
    4  git clone https://github.com/dlgeiser/reproducibility-tutorial.git
    5  ls
    6  clear
    7  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    8  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    9  ln -s /opt/conda/pkgs/*/bin/* /bin
   10  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   11  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   12  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   13  /opt/conda/bin/pip install bash_kernel
   14  /opt/conda/bin/pip install ipykernel
   15  /opt/conda/bin/python3 -m bash_kernel.install
   16  /opt/conda/bin/conda search htseq
   17  /opt/conda/bin/conda search -c bioconda htseq
   18  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   19  /opt/conda/bin/conda search -c bioconda snakemake
   20  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   21  ln -s /opt/conda/bin/* /bin
   22  ln -s /opt/conda/lib/* /usr/lib
   23  snakemake --version
   24  clear
   25  sudo apt-get update
   26  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   27  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   28  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   29  sudo apt-get update
   30  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   31  docker run hello-world
   32  cd /scratch/reproducibility-tutorial/
   33  history >>README.md
