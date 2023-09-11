FROM local/x11vnc-desktop:jupyter

USER root

# # apt-get may result in root-owned directories/files under $HOME
# RUN chown -R $NB_UID:$NB_GID $HOME

ADD . /opt/install
# RUN fix-permissions /opt/install

# USER $NB_USER
RUN cd /opt/install && \
   mamba env update -n base --file environment.yml

CMD ["start-notebook.sh"]