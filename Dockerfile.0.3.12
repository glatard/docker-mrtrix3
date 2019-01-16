FROM centos:latest
RUN yum update -y
RUN yum install git gcc-c++ zlib-devel gsl-devel qt-devel -y
ENV PATH=$PATH:/usr/lib64/qt4/bin
RUN git clone https://github.com/MRtrix3/mrtrix3.git
ENV ARCH='x86-64'
RUN cd mrtrix3 && git checkout tags/0.3.12 && ./configure && ./build
ENV PATH=$PATH:/mrtrix3/bin
