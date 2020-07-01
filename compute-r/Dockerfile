FROM ubuntu:bionic

# Get Cran Repository on the apt list
RUN sed -i '/deb-src/s/^# //' /etc/apt/sources.list && \
    apt-get update && \
    apt-get upgrade && \
    apt-get install -y apt-utils apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common tzdata gpg

RUN add-apt-repository -s 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/' && \
    gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9 && \
    gpg -a --export E298A3A825C0D65DFD57CBB651716619E084DAB9 | apt-key add -

RUN apt-get update && \

