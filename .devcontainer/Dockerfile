FROM buildpack-deps:bullseye

RUN DEBIAN_FRONTEND=noninteractive apt install -y gcc make git binutils libc6-dev

RUN apt-get update; \
    apt-get install -y software-properties-common; \
    apt-get install -y lsb-release;

RUN wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -; \
    apt-add-repository "deb http://apt.llvm.org/bullseye/ llvm-toolchain-bullseye-13 main"; \
    apt-get update; \
    apt-get install -y llvm-13 llvm-13-dev clang-13;

RUN update-alternatives --install /usr/bin/llvm-PerfectShuffle    llvm-PerfectShuffle     /usr/bin/llvm-PerfectShuffle-13 1; \
    update-alternatives --install /usr/bin/llvm-lib               llvm-lib                /usr/bin/llvm-lib-13 1; \
    update-alternatives --install /usr/bin/llvm-dis               llvm-dis                /usr/bin/llvm-dis-13 1; \
    update-alternatives --install /usr/bin/not                    not                     /usr/bin/not-13 1; \
    update-alternatives --install /usr/bin/clang++                clang++                 /usr/bin/clang++-13 1; \
    update-alternatives --install /usr/bin/llvm-link              llvm-link               /usr/bin/llvm-link-13 1; \
    update-alternatives --install /usr/bin/split-file             split-file              /usr/bin/split-file-13 1; \
    update-alternatives --install /usr/bin/llvm-opt-report        llvm-opt-report         /usr/bin/llvm-opt-report-13 1; \
    update-alternatives --install /usr/bin/llvm-bcanalyzer        llvm-bcanalyzer         /usr/bin/llvm-bcanalyzer-13 1; \
    update-alternatives --install /usr/bin/yaml-bench             yaml-bench              /usr/bin/yaml-bench-13 1; \
    update-alternatives --install /usr/bin/llvm-exegesis          llvm-exegesis           /usr/bin/llvm-exegesis-13 1; \
    update-alternatives --install /usr/bin/llvm-xray              llvm-xray               /usr/bin/llvm-xray-13 1; \
    update-alternatives --install /usr/bin/llvm-bitcode-strip     llvm-bitcode-strip      /usr/bin/llvm-bitcode-strip-13 1; \
    update-alternatives --install /usr/bin/llvm-tblgen            llvm-tblgen             /usr/bin/llvm-tblgen-13 1; \
    update-alternatives --install /usr/bin/llvm-ranlib            llvm-ranlib             /usr/bin/llvm-ranlib-13 1; \
    update-alternatives --install /usr/bin/llc                    llc                     /usr/bin/llc-13 1; \
    update-alternatives --install /usr/bin/llvm-readobj           llvm-readobj            /usr/bin/llvm-readobj-13 1; \
    update-alternatives --install /usr/bin/llvm-strip             llvm-strip              /usr/bin/llvm-strip-13 1; \
    update-alternatives --install /usr/bin/llvm-rc                llvm-rc                 /usr/bin/llvm-rc-13 1; \
    update-alternatives --install /usr/bin/llvm-mt                llvm-mt                 /usr/bin/llvm-mt-13 1; \
    update-alternatives --install /usr/bin/llvm-c-test            llvm-c-test             /usr/bin/llvm-c-test-13 1; \
    update-alternatives --install /usr/bin/asan_symbolize         asan_symbolize          /usr/bin/asan_symbolize-13 1; \
    update-alternatives --install /usr/bin/llvm-ar                llvm-ar                 /usr/bin/llvm-ar-13 1; \
    update-alternatives --install /usr/bin/llvm-gsymutil          llvm-gsymutil           /usr/bin/llvm-gsymutil-13 1; \
    update-alternatives --install /usr/bin/llvm-mc                llvm-mc                 /usr/bin/llvm-mc-13 1; \
    update-alternatives --install /usr/bin/llvm-libtool-darwin    llvm-libtool-darwin     /usr/bin/llvm-libtool-darwin-13 1; \
    update-alternatives --install /usr/bin/llvm-objcopy           llvm-objcopy            /usr/bin/llvm-objcopy-13 1; \
    update-alternatives --install /usr/bin/llvm-diff              llvm-diff               /usr/bin/llvm-diff-13 1; \
    update-alternatives --install /usr/bin/llvm-extract           llvm-extract            /usr/bin/llvm-extract-13 1; \
    update-alternatives --install /usr/bin/llvm-pdbutil           llvm-pdbutil            /usr/bin/llvm-pdbutil-13 1; \
    update-alternatives --install /usr/bin/llvm-reduce            llvm-reduce             /usr/bin/llvm-reduce-13 1; \
    update-alternatives --install /usr/bin/llvm-ifs               llvm-ifs                /usr/bin/llvm-ifs-13 1; \
    update-alternatives --install /usr/bin/llvm-config            llvm-config             /usr/bin/llvm-config-13 1; \
    update-alternatives --install /usr/bin/llvm-profdata          llvm-profdata           /usr/bin/llvm-profdata-13 1; \
    update-alternatives --install /usr/bin/llvm-cxxdump           llvm-cxxdump            /usr/bin/llvm-cxxdump-13 1; \
    update-alternatives --install /usr/bin/FileCheck              FileCheck               /usr/bin/FileCheck-13 1; \
    update-alternatives --install /usr/bin/llvm-dlltool           llvm-dlltool            /usr/bin/llvm-dlltool-13 1; \
    update-alternatives --install /usr/bin/llvm-cxxfilt           llvm-cxxfilt            /usr/bin/llvm-cxxfilt-13 1; \
    update-alternatives --install /usr/bin/llvm-tapi-diff         llvm-tapi-diff          /usr/bin/llvm-tapi-diff-13 1; \
    update-alternatives --install /usr/bin/llvm-objdump           llvm-objdump            /usr/bin/llvm-objdump-13 1; \
    update-alternatives --install /usr/bin/llvm-ml                llvm-ml                 /usr/bin/llvm-ml-13 1; \
    update-alternatives --install /usr/bin/dsymutil               dsymutil                /usr/bin/dsymutil-13 1; \
    update-alternatives --install /usr/bin/sanstats               sanstats                /usr/bin/sanstats-13 1; \
    update-alternatives --install /usr/bin/llvm-lipo              llvm-lipo               /usr/bin/llvm-lipo-13 1; \
    update-alternatives --install /usr/bin/llvm-jitlink-executor  llvm-jitlink-executor   /usr/bin/llvm-jitlink-executor-13 1; \
    update-alternatives --install /usr/bin/llvm-llvm-readelf      llvm-readelf            /usr/bin/llvm-readelf-13 1; \
    update-alternatives --install /usr/bin/llvm-sim               llvm-sim                /usr/bin/llvm-sim-13 1; \
    update-alternatives --install /usr/bin/llvm-profgen           llvm-profgen            /usr/bin/llvm-profgen-13 1; \
    update-alternatives --install /usr/bin/llvm-cov               llvm-cov                /usr/bin/llvm-cov-13 1; \
    update-alternatives --install /usr/bin/llvm-stress            llvm-stress             /usr/bin/llvm-stress-13 1; \
    update-alternatives --install /usr/bin/lli-child-target-13    lli-child-target-13     /usr/bin/lli-child-target-13 1; \
    update-alternatives --install /usr/bin/llvm-rtdyld            llvm-rtdyld             /usr/bin/llvm-rtdyld-13 1; \
    update-alternatives --install /usr/bin/llvm-otool             llvm-otool              /usr/bin/llvm-otool-13 1; \
    update-alternatives --install /usr/bin/clang-cpp              clang-cpp               /usr/bin/clang-cpp-13 1; \
    update-alternatives --install /usr/bin/clang                  clang                   /usr/bin/clang-13 1; \
    update-alternatives --install /usr/bin/count                  count                   /usr/bin/count-13 1; \
    update-alternatives --install /usr/bin/verify-uselistorder    verify-uselistorder     /usr/bin/verify-uselistorder-13 1; \
    update-alternatives --install /usr/bin/yaml2obj               yaml2obj                /usr/bin/yaml2obj-13 1; \
    update-alternatives --install /usr/bin/llvm-lto               llvm-lto                /usr/bin/llvm-lto-13 1; \
    update-alternatives --install /usr/bin/llvm-cvtres            llvm-cvtres             /usr/bin/llvm-cvtres-13 1; \
    update-alternatives --install /usr/bin/llvm-cfi-verify        llvm-cfi-verify         /usr/bin/llvm-cfi-verify-13 1; \
    update-alternatives --install /usr/bin/llvm-nm                llvm-nm                 /usr/bin/llvm-nm-13 1; \
    update-alternatives --install /usr/bin/llvm-windres           llvm-windres            /usr/bin/llvm-windres-13 1; \
    update-alternatives --install /usr/bin/llvm-addr2line         llvm-addr2line          /usr/bin/llvm-addr2line-13 1; \
    update-alternatives --install /usr/bin/bugpoint               bugpoint                /usr/bin/bugpoint-13 1; \
    update-alternatives --install /usr/bin/llvm-as                llvm-as                 /usr/bin/llvm-as-13 1; \
    update-alternatives --install /usr/bin/obj2yaml               obj2yaml                /usr/bin/obj2yaml-13 1; \
    update-alternatives --install /usr/bin/llvm-undname           llvm-undname            /usr/bin/llvm-undname-13 1; \
    update-alternatives --install /usr/bin/llvm-symbolizer        llvm-symbolizer         /usr/bin/llvm-symbolizer-13 1; \
    update-alternatives --install /usr/bin/llvm-strings           llvm-strings            /usr/bin/llvm-strings-13 1; \
    update-alternatives --install /usr/bin/llvm-dwarfdump         llvm-dwarfdump          /usr/bin/llvm-dwarfdump-13 1; \
    update-alternatives --install /usr/bin/llvm-size-13           llvm-size-13            /usr/bin/llvm-size-13 1; \
    update-alternatives --install /usr/bin/llvm-jitlink           llvm-jitlink            /usr/bin/llvm-jitlink-13 1; \
    update-alternatives --install /usr/bin/llvm-cxxmap            llvm-cxxmap             /usr/bin/llvm-cxxmap-13 1; \
    update-alternatives --install /usr/bin/llvm-lto2              llvm-lto2               /usr/bin/llvm-lto2-13 1; \
    update-alternatives --install /usr/bin/llvm-cat               llvm-cat                /usr/bin/llvm-cat-13 1; \
    update-alternatives --install /usr/bin/llvm-split             llvm-split              /usr/bin/llvm-split-13 1; \
    update-alternatives --install /usr/bin/llvm-dwp               llvm-dwp                /usr/bin/llvm-dwp-13 1; \
    update-alternatives --install /usr/bin/lli                    lli                     /usr/bin/lli-13 1; \
    update-alternatives --install /usr/bin/llvm-install-name-tool llvm-install-name-tool  /usr/bin/llvm-install-name-tool-13 1; \
    update-alternatives --install /usr/bin/llvm-modextract        llvm-modextract         /usr/bin/llvm-modextract-13 1; \
    update-alternatives --install /usr/bin/llvm-mca               llvm-mca                /usr/bin/llvm-mca-13 1; \
    update-alternatives --install /usr/bin/opt                    opt                     /usr/bin/opt-13 1; \
