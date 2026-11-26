1. Cluster must already have all nodes on same network with hostnames configured on each node as well as static ip addresses
2. Edit this repo so that your hostnames and ip addresses replace the default ones here (search for 192. or something)
3. Use scp to copy the folder into your vm management node and then run it with "ansible-playbook -i inventory.ini playbook.yml -K" I think, check google if it doesn't work
4. Test by running "touch /shared/test.txt" on a compute node and then ssh to a storage node and check its in "ls -ld /srv/nfs/shared"