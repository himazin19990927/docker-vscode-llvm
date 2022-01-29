FROM buildpack-deps:bullseye

RUN DEBIAN_FRONTEND=noninteractive apt install -y gcc make git binutils libc6-dev

RUN apt-get update; \
    apt-get install -y software-properties-common; \
    apt-get install -y lsb-release;

RUN wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -; \
    apt-add-repository "deb http://apt.llvm.org/bullseye/ llvm-toolchain-bullseye-13 main"; \
    apt-get update; \
    apt-get install -y llvm-13 llvm-13-dev clang-13;