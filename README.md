# Running the application
- Please enter the correct credentials in twitter4j.properties file in twitter-to-kafka-service 
and enter your github password and url on bootstrap.yml file of config-server
- Then run mvn install -DskipTests command
- Then run docker-compose up command in docker-compose folder
- Check pom.xml of elastic-query-service, where we added build-image goal to spring-boot-maven-plugin
- Check services.yml in docker-compose folder, which is updated for elastic-query-service docker image

### setup for new clone
- move the exiting .git file from config-server-repository
- setup new keys from titter4j setup
- chmod -R 777 docker-logs in */docker-compose folder*
- check if environment keys for encryption exist
- remember to *switch to java 11*
- temporal increase heap size *sysctl -w vm.max_map_count=262144*
- change the kafka announcement host to DOCKER_HOST_INTERNAL
- likely root cause: java.nio.file.FileAlreadyExistsException: /usr/share/elasticsearch/config/elasticsearch.keystore.tmp
- may need to fully remove all elasticsearch image prior to relaunch
