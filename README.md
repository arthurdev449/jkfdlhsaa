[#work](https://prod.liveshare.vsengsaas.visualstudio.com/join?33BDCD0E2C3A84535AD5FC7EBBCD8E631BB1)

aws drs get-replication-configuration --source-server-id <SOURCE_SERVER_ID> --query "{Subnet:stagingAreaSubnetId, InstanceType:replicationServerInstanceType, Dedicated:useDedicatedReplicationServer, AutoReplicateNewDisks:autoReplicateDisks, VolumeType:replicatedDisks[0].stagingDiskType, EncryptionType:ebsEncryption, PITPolicy:pitPolicy, DataRouting:dataPlaneRouting, Tags:stagingAreaTags}" --output json

import os
import csv

list_servers_ids = os.system('aws drs describe-source-servers --query "items[].sourceServerID" --output json')

list_servers = []

for server_id in list_servers_ids:
    hostname = os.system(get hm command server_id)
    dict_server = {
        "id" : server_id, 
        "hostname" : hostname,
        "repl_cfg" : os.system('cat /etc/repl_cfg'),
        "launch_cfg" : os.system('cat /etc/launch_cfg')
    }
    list_servers.append(dict_server)



