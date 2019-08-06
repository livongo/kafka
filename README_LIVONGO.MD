Livongo fork of Kafka
=================
We are maintaining a fork of kafka in order to have a RocksDBTTL Topic cache.
We tried to get this merged upstream without success: https://issues.apache.org/jira/browse/KAFKA-4212 

### First bootstrap and download the wrapper ###
    cd kafka_source_dir
    gradle

### publishing a new livongo version
- `git pull` from kafka upstream 
- add upstream commits onto Livonogo trunk
- compile & run tests (see kafka main README)
- update gradle.properties's `version` field to add `-LIVONGO` suffix
- update gradle.properties's `mavenUrl` field
- update gradle.properties's `mavenUsername` field
- update gradle.properties's `mavenPassword` field
- run ```./gradlew uploadArchivesAll``` to upload new jars to Livongo artifactory
