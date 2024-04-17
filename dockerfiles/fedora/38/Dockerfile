# docker run --rm -itd --network=host -e SSH_PWD=**PASSWORD** -e SSH_PORT=**PORT** superjump22/linux-sshd:fedora-38
FROM fedora:38

COPY ./install-ssh.sh /usr/local/bin/install-ssh.sh
COPY ./start-ssh.sh /usr/local/bin/start-ssh.sh
COPY ./get-os.sh /usr/local/bin/get-os.sh

RUN chmod +x /usr/local/bin/install-ssh.sh && \
    chmod +x /usr/local/bin/start-ssh.sh && \
    chmod +x /usr/local/bin/get-os.sh && \
    /usr/local/bin/install-ssh.sh

CMD ["/usr/local/bin/start-ssh.sh"]