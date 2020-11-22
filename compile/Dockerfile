FROM ouvocl/rstudio-base

RUN cd rstudio; mkdir build; cd build; cmake .. -DRSTUDIO_TARGET=Server -DCMAKE_BUILD_TYPE=Release; make install

# Push as: ouvocl:rstudio-compiled
