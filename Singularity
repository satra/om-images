# This container will run mriqc via singularity

BootStrap: docker
From: poldracklab/mriqc:latest

%runscript
    exec /usr/local/miniconda/bin/mriqc "$@"

%setup
    cp -r $SINGULARITY_ROOTFS/root/src $SINGULARITY_ROOTFS/opt
    chmod -R a+r $SINGULARITY_ROOTFS/opt/src

%post
    export PATH=/usr/local/miniconda/bin:$PATH
    pip install /opt/src/mriqc
    echo "
export PATH=/usr/local/miniconda/bin:$PATH
export LANG=C.UTF-8
export LC_ALL=C.UTF-8    

. /etc/fsl/fsl.sh
. /etc/afni/afni.sh
    
" >> /environment

    mkdir /om
    mkdir /cm
