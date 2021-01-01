# bash-ipsweep-script
bash script for a sub 24 subnet. "grabs device ips inn a network"

#code starts here

#!/bin/bash

if [ "$1" == "" ]
then
echo "You forgot an IP address"
echo "Syntax: ./ipsweep.sh 192.168.4"

for ip in `seq 1 254`; do
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
done




