FROM nvcr.io/nvidia/rapidsai/rapidsai:0.15-cuda10.2-runtime-ubuntu18.04
RUN apt-get update && apt-get install -y libfontconfig1 libxrender1 
RUN source activate rapids \ 
    && conda install -y -c conda-forge python-graphviz
# RUN /opt/conda/condabin/conda install -y -c conda-forge graphviz python-graphviz
USER root
RUN mkdir /workshop
COPY workshop /workshop
EXPOSE 8888
EXPOSE 8787
EXPOSE 8786
WORKDIR /workshop
#ENTRYPOINT /bin/bash -c 'source activate rapids; /bin/bash'
#ENTRYPOINT /bin/bash -c 'source activate rapids; jupyter-lab --allow-root --ip=0.0.0.0 --no-browser --NotebookApp.token='

