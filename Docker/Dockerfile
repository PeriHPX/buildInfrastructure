# Copyright (c) 2019 Patrick Diehl
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)

FROM fedora:40
MAINTAINER Patrick Diehl <patrickdiehl@lsu.edu>
# install dependencies
RUN dnf update -y
RUN dnf install -y \ 
hpx-devel \
cmake \
blaze-devel \ 
vtk-devel \
yaml-cpp-devel \
doxygen \
graphviz \
git \
libXext-devel \
gmsh-devel \
metis-devel \
lcov \
python3 \
python3-pip \
gmsh-devel \
rpm-build 

# Install build tools
RUN dnf install @development-tools -y
 
# Install BlazeIterative
RUN git clone https://github.com/STEllAR-GROUP/BlazeIterative.git &&  \
cd BlazeIterative &&  \
cmake . && \
make install && \
cd .. && \
rm -rf BlazeIterative
