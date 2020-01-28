FROM fedora:latest
RUN dnf install -y vim git wget rust cargo zlib zlib-devel libzip libzip-devel \
bzip2-devel xz-devel clang clang-devel

RUN dnf groupinstall -y 'Development Tools'

RUN git clone https://github.com/10XGenomics/bamtofastq.git
WORKDIR bamtofastq
RUN cargo build --release
