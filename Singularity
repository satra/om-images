BootStrap: docker
From: poldracklab/mriqc:0.9.0-0-python35

%runscript
    exec /usr/bin/run_mriqc "$@"

%post
    echo "

source /etc/fsl/fsl.sh
source /etc/afni/afni.sh
    
" >> /environment

    mkdir /om
    mkdir /cm
