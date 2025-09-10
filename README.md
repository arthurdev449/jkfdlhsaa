[#work](https://prod.liveshare.vsengsaas.visualstudio.com/join?33BDCD0E2C3A84535AD5FC7EBBCD8E631BB1)

aws drs get-replication-configuration --source-server-id <SOURCE_SERVER_ID> --query "{Subnet:stagingAreaSubnetId, InstanceType:replicationServerInstanceType, Dedicated:useDedicatedReplicationServer, AutoReplicateNewDisks:autoReplicateDisks, VolumeType:replicatedDisks[0].stagingDiskType, EncryptionType:ebsEncryption, PITPolicy:pitPolicy, DataRouting:dataPlaneRouting, Tags:stagingAreaTags}" --output json
