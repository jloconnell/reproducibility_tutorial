# reproducibility_tutorial   

## Computer setup

1. Clone my git repo

  git clone https://github.com/jloconnell/reproducibility_tutorial

2. Download and install Miniconda

  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
  ln -s /opt/conda/pkgs/*/bin/* /bin
  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
  /opt/conda/bin/pip install bash_kernel
  /opt/conda/bin/pip install ipykernel
  /opt/conda/bin/python3 -m bash_kernel.install
  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
 
4. Jupyter Lab


   17  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility_tutorial/'
   18  /opt/conda/bin/conda search -c bioconda snakemake
   19  # Let's choose the 5.8.1.
   20  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   21  # hack conda again
   22  ln -s /opt/conda/bin/* /bin
   23  ln -s /opt/conda/lib/* /usr/lib
   24  # verify the installation
   25  conda snake make
   26  conda snakemake
   27  snakemake --version
   28  sudo apt-get update
   29  # install some needed packages
   30  # It's ok to say yes to any warnings
   31  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   32  # add the Docker key
   33  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   34  #add the repository
   35  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   36   $(lsb_release -cs) \
   37   stable"
   38  # update apt-get with new repository information
   39  sudo apt-get update
   40  # install docker
   41  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   42  history >>README.md
   43  dock run hello-world
   44  docker run hello-world
   45  cd /scratch/reproducibility-tutorial/
   46  # append your bash history to the README.MD file
   47  history >>README.md
   48  # Use nano to edit the history down to the relevant commands
   49  # use markdown to make this into a readable report
   50  nano README.md
   51  sudo apt-get update
   52  # install some needed packages
   53  # It's ok to say yes to any warnings
   54  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   55  # add the Docker key
   56  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   57  #add the repository
   58  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   59  # update apt-get with new repository information
   60  sudo apt-get update
   61  # install docker
   62  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   63  #test docker
   64  docker run hello-world
   65  ls
   66  git clone https://github.com/jloconnell/reproducibility_tutorial
   67  ls
   68  cd reproducibility_tutorial/
   69  history >> README.md
