FROM ouvocl/debian-build-r-base

ENV RSTUDIO_DISABLE_CRASHPAD=1

#compile 

RUN git clone https://github.com/rstudio/rstudio
RUN cd rstudio && git checkout 0665c604f53d0c0a37dabf40d48fc471bd308c2d
RUN cd rstudio/dependencies/linux;./install-dependencies-debian --exclude-qt-sdk

# Push as: ouvocl:rstudio-base
