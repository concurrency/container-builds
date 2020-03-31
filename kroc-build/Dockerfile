FROM ubuntu
RUN apt-get update && apt-get install -y \
  clang \
  lld \
  git \
  scons \
  libc6-dev \
  libc6-dev-i386 \
  autoconf \
  apt-utils \
  build-essential

RUN git clone https://github.com/concurrency/kroc

WORKDIR kroc
RUN mkdir /opt/kroc
RUN CC=clang \
  CFLAGS="-fPIC" \
  ./build \
  --prefix=/opt/kroc \
  --with-toolchain=tvm \
  --with-wrapper=posix  
