FROM ouvocl:rstudio-compiled

# post installation

RUN useradd -ms /bin/bash rstudio-server

RUN cd rstudio/build; pwd;  ls

RUN cp /usr/local/lib/rstudio-server/extras/init.d/debian/rstudio-server /etc/init.d/rstudio-server
RUN cd /etc/init.d; chmod +x rstudio-server

RUN ln -f -s /usr/local/lib/rstudio-server/bin/rstudio-server /usr/sbin/rstudio-server

RUN mkdir -p /var/run/rstudio-server
RUN mkdir -p /var/lock/rstudio-server
RUN mkdir -p /var/log/rstudio-server
RUN mkdir -p /var/lib/rstudio-server


RUN useradd rstudio \
        && echo "rstudio:rstudio" | chpasswd \
	&& mkdir /home/rstudio \
	&& chown rstudio:rstudio /home/rstudio 


EXPOSE 8787

CMD rstudio-server start && sleep infinity

# Push as: ouvocl/vce-rstudio
