FROM fedora
RUN dnf install -y vim git iproute openssh-server passwd cracklib-dicts procps-ng
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
RUN ssh-keygen -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key
RUN ssh-keygen -t ed25519 -f /etc/ssh/ssh_host_ed25519_key

EXPOSE 22

#CMD ["/usr/sbin/sshd", "-D"]

