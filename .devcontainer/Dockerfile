FROM espressif/idf:v5.5

RUN apt update && apt install -y tree vim-tiny
RUN echo "set -o vi" >> ~/.bashrc
RUN echo "source /opt/esp/idf/export.sh > /dev/null 2>&1" >> ~/.bashrc

RUN curl -L https://wokwi.com/ci/install.sh | sh
RUN echo '[ -f /workspaces/wokwi.sh ] && source /workspaces/wokwi.sh' >> ~/.bashrc

ENV PATH="/opt/esp/python_env/idf5.5_py3.12_env/bin:${PATH}"
RUN python -m pip install --upgrade pip && \
    pip install robotframework
RUN echo 'export PATH="/opt/esp/python_env/idf5.5_py3.12_env/bin:$PATH"' >> ~/.bashrc

ENTRYPOINT [ "/opt/esp/entrypoint.sh" ]

CMD ["/bin/bash"]