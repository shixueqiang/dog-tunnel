# dog-tunnel
狗洞端口映射

源地址 https://github.com/vzex/dog-tunnel

Installation
Run dog tunnel with docker container
Install dtunnel on Fedora 20/21 or CentOS 6/7

We provided a bash scripts to install dtunnel on fresh linux box.

see scripts/install_linux.sh
Install dtunnel on Ubuntu/Kubuntu 14.04 and 14.10

See scripts/install_ubuntu.sh
Specification
udp make session flow :

s -> c1 : query_addrlist_a
c1 -> s : report_addrlist
s -> c2 : query_addrlist_b  c2 have c1's addresses
c2 -> s : report_addrlist
s -> c1 : tell_bust_a  c1 have c2's addresses
c1 -> s : success_bust_a
s -> c2 : tell_bust_b
c2 -> s : makeholeok or makeholefail
