FROM ubuntu:16.04
LABEL maintainer="Julio Waissman <julio.waissman@unison.mx>"
RUN apt-get clean && apt-get update && apt-get install -y locales
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# Actualiza el SO e instala librerías necesarias
# (en particular python3
RUN apt-get update && apt-get install -yq \
                        python3 python3-pip htop nano git wget \
                        curl libglib2.0-0 autoconf automake \
                        libtool build-essential unzip \
                        libarchive-dev vim cowsay

# Instala Fasttext de Facebook de acuerdo a las instrucciones
# (https://github.com/facebookresearch/fastText)
RUN wget https://github.com/facebookresearch/fastText/archive/v0.1.0.zip && \
    unzip v0.1.0.zip && \
    cd fastText-0.1.0 && \
    make && \
    cp -Rf fasttext /usr/local/bin

# Instala las librerías de Python
ADD modulos-python.txt /
RUN pip3 install -r modulos-python.txt

# Instala las extensiones de jupyter y lo configura
RUN jupyter nbextension enable --py --sys-prefix widgetsnbextension
RUN jupyter contrib nbextension install
RUN jupyter nbextension enable codefolding/main
RUN echo "c.NotebookApp.ip = '*'" >> /root/.jupyter/jupyter_notebook_config.py
RUN echo "c.NotebookApp.port = 8080" >> /root/.jupyter/jupyter_notebook_config.py
RUN echo "c.NotebookApp.token = ''" >> /root/.jupyter/jupyter_notebook_config.py
RUN echo "jupyter notebook --no-browser --allow-root" >> /usr/local/bin/run_notebook && chmod +x /usr/local/bin/run_notebook

# Saludamos al entrar
ADD saludo.txt /
RUN echo '[ ! -z "$TERM" -a -r /etc/motd ] && cat /etc/motd' \
        >> /etc/bash.bashrc \
        ; cat saludo.txt | /usr/games/cowsay -W 60 > /etc/motd

# Directorio considerado el de usuario (superusuario del contenedor)
WORKDIR /root

# Descarga el modelo en español (pequeño) de spacy
RUN python3 -m spacy download es_core_news_sm

# Descarga los datos necesarios para NLTK
RUN python3 -m nltk.downloader punkt stopwords spanish_grammars

# Instala la libraría que se me escapó para no tener que recompilar todas las estapas
RUN pip3 install pyldavis

# Expone al SO original el puerto 8080 para poder usar jupyter
EXPOSE 8080
