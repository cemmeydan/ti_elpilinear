#######################################################################################
## DO NOT EDIT THIS FILE! This file was automatically generated from the dockerfile. ##
## Run babelwhale::convert_dockerfile_to_singularityrecipe() to update this file.    ##
#######################################################################################

Bootstrap: shub

From: dynverse/dynwrap:r

%labels
    version 0.1.5


    
    
    
    
    

%files

    . /code

%post
    mkdir /scratchLocal
    mkdir /pbtech_mounts
    mkdir /pbtech_mounts/softlib001
    mkdir /athena
    mkdir /zenodotus



    chmod -R 755 '/code'
    apt-get -y install libudunits2-dev
    Rscript -e 'devtools::install_cran("udunits2", configure.args =  c(udunits2 = "--with-udunits2-include=/usr/include/udunits2"))'
    R -e "devtools::install_github('Albluca/ElPiGraph.R')"

%runscript
    exec Rscript /code/run.R

