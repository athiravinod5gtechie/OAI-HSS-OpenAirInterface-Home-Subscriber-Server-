# OAI-HSS (OpenAirInterface-Home-Subscriber-Server)
 OAI HSS (OpenAirInterface Home Subscriber Server) is a critical component in the OpenAirInterface (OAI) project, which is an open-source software-defined mobile network infrastructure. 
 The OAI project aims to provide a flexible and customizable platform for building and experimenting with wireless communication networks, including 4G LTE and 5G.
# Steps for Installation
1. git clone https://github.com/OPENAIRINTERFACE/openair-hss.git
2. cd openair-hss/
3. git checkout v1.2.0
4. git log
5. cd ..
6. vim HSS-Patch.diff ( see file attached)
7. cd openair-hss/
8. patch --dry-run -p1 < ../HSS-Patch.diff
9. patch  -p1 < ../HSS-Patch.diff
10. docker build -t oai-hss --file docker/Dockerfile.ubuntu18.04 .
11. sudo apt  install docker.io
12. sudo docker build -t oai-hss --file docker/Dockerfile.ubuntu18.04 . 
