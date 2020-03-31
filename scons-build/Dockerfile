FROM perl:slim-buster
RUN apt-get update && apt-get install -y \
  clang \
  lld \
  git \
  scons \
  libc6-dev \
  libc6-dev-i386

RUN git clone https://github.com/concurrency/occam-compiler

WORKDIR occam-compiler
RUN scons -c ; scons
