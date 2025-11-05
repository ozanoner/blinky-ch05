FROM espressif/idf:v5.5

RUN apt update && apt install -y tree vim-tiny
RUN echo "set -o vi" >> ~/.bashrc
RUN echo "source /opt/esp/idf/export.sh > /dev/null 2>&1" >> ~/.bashrc

RUN curl -L https://wokwi.com/ci/install.sh | sh
RUN echo '[ -f /workspaces/wokwi.sh ] && source /workspaces/wokwi.sh' >> ~/.bashrc

ENTRYPOINT [ "/opt/esp/entrypoint.sh" ]

CMD ["/bin/bash"]