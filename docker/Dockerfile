FROM nvcr.io/nvidia/rapidsai/rapidsai:0.14-cuda10.2-runtime-ubuntu18.04
USER root
RUN source activate rapids \ 
    && mkdir /.local /.jupyter /.config /.cupy  \
    && chmod 777 /.local /.jupyter /.config /.cupy
RUN source activate rapids \ 
    && pip install -U scikit-learn==0.23.1

RUN mkdir /workshop
COPY workshop /workshop
EXPOSE 8888
EXPOSE 8787
EXPOSE 8786
WORKDIR /workshop

#ENTRYPOINT /bin/bash -c 'source activate rapids; /bin/bash'
ENTRYPOINT /bin/bash -c 'source activate rapids; jupyter-lab --allow-root --ip=0.0.0.0 --no-browser --NotebookApp.token='

