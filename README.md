# Redis Cluster Implementation


# Get all ips in cluster, connect to them using normal tcp and support redis specifications for command transfer
# Get Slots by connecting to one of the node and save them as Map (slotstart, slotend) (masterip, slaveip)
# Whenever command has to be executed, compute the slot id and send to slave if read else to master
# In above case if MOVED comes update the slots and serve the request
