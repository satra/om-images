# This container will run mriqc via singularity

BootStrap: docker
From: poldracklab/mriqc:0.9.0-0-python35

%runscript
    exec /usr/local/miniconda/bin/mriqc "$@"

%post
    chmod -R a+rx /root    
    echo "
    export PATH=/usr/local/miniconda/bin:$PATH
    export PYTHONPATH=/usr/local/miniconda/lib/python3.5/site-packages
    export PYTHONNOUSERSITE=1
    export LANG=C.UTF-8
    export LC_ALL=C.UTF-8    

. /etc/fsl/fsl.sh
. /etc/afni/afni.sh
    
" >> /environment

    mkdir /om
    mkdir /cm
