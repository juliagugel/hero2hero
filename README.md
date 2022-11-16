# hero2hero

Hero + Hero = Superhero?

This contains the step by step instruction I ran during the pgconf.eu in Berlin 2022.

In case you want to try the Patroni + pgBackRest setup, you need 3 VMs for the patroni cluster and another for the pgBackRest repository. Please install all the prerequisites needed for pgBackRest and patroni. To run the script, you also need to install PostgreSQL and you need to download the etcd.tar and the pgbackrest.tar. For a snmooth setup, don't forget to exchange the SSH keys of all four servers and grant sudo permissions to the postgres user.

1. You need to adjust the setup_patroni_node.txt to your needs (IP address aso), further you need to change the IP addresses/node name if you setup the second and the third node.
2. Keep in mind, that the etcd setup must be done quite simultanious to make sure that all nodes see each other.
3. Once all three patroni nodes are up and running. You can setup the pgbackrest repository server as well. 

In case of any errors during the setup. Just check the configuration. Maybe there is a typo somewhere ;-)

Please keep in mind that this playbooks use the DMK of dbi services as well. As this tool is only for our customers, you need to adjust the playbooks according to this.

If you want to bootstrap a complete patroni cluster from pgBackRest, you can find the instruction for that on my blog: https://www.dbi-services.com/blog/bootstrap-patroni-cluster-from-pgbackrest-backup/

If you want to recreate a node from pgBackRest, you can find the instruction on my blog: https://www.dbi-services.com/blog/recreate-a-patroni-node-using-pgbackrest
