# bash-ipsweep-script
bash script for a sub 24 subnet. "grabs device ips inn a network"

#code starts here

#!/bin/bash

if [ "$1" == "" ] <br />
then <br />
echo "You forgot an IP address" <br />
echo "Syntax: ./ipsweep.sh 192.168.4" <br />
 <br />
for ip in `seq 1 254`; do <br />
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" & <br />
done <br />




