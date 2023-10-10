# OAI-HSS (OpenAirInterface-Home-Subscriber-Server)
 OAI HSS (OpenAirInterface Home Subscriber Server) is a critical component in the OpenAirInterface (OAI) project, which is an open-source software-defined mobile network infrastructure. 
 The OAI project aims to provide a flexible and customizable platform for building and experimenting with wireless communication networks, including 4G LTE and 5G.
# Steps for Installation
 git clone https://github.com/OPENAIRINTERFACE/openair-hss.git
 cd openair-hss/
 git checkout v1.2.0
 git log
 cd ..
 vim HSS-Patch.diff ( see file attached)
 cd openair-hss/
 patch --dry-run -p1 < ../HSS-Patch.diff
 patch  -p1 < ../HSS-Patch.diff
 docker build -t oai-hss --file docker/Dockerfile.ubuntu18.04 .
 sudo apt  install docker.io
 sudo docker build -t oai-hss --file docker/Dockerfile.ubuntu18.04 .
