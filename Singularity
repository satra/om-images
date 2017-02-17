# This container will run mriqc via singularity

BootStrap: docker
From: poldracklab/mriqc:0.9.0-0-python35

%runscript
    exec /usr/bin/run_mriqc "$@"

%post
    echo "

. /etc/fsl/fsl.sh
. /etc/afni/afni.sh
    
" >> /environment

    mkdir /om
    mkdir /cm
