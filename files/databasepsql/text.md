# Cara Install Docker-Swam and join
docker swarm init --advertise-addr eth0
# Cek Node
docker node ls 
# node add label cek node id di node ls
docker node update --label-add type=primary ${node1_id?}
# cek service running
docker service ls
docker service ps pg-stack_primary
docker service ps pg-stack_replica
# ngescale
docker service scale pg-stack_replica=2
