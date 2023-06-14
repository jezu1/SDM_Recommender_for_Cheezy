# SDM_Recommender
Building a recommender for Cheezy start-up idea

##Prerequisite 

Delta Lake:
io.delta:delta-core_2.12:2.1.0

Pyspark:
3.3.0

Neo4j connector:
neo4j-connector-apache-spark_2.12_3.0-4.0.0

Neo4j:
4.4.20

VM Credentials: 
VM user: masterBD01 -- Password: tKtyPg4nNn

Ubuntu user:
User: hadoop -- Password: foodie

Neo4j user:
User: neo4j -- Password: foodie

Neo4j is running in the vitual machine, so please enter to the VM with the credetials above and to start neo4j perform: 
sudo /opt/neo4j/bin/neo4j restart
and you will be able to access neo4j in your brwoser in this address: http://10.4.41.56:7474/browser/

### Running the graph creattion

To run the graph creation script, please run neo4j Neo4jConnect.py file, which already has all the neccesary conections to the delta tables and neo4j and directly performs the node and relationship creation/update if the nodes already exist.

After runnig the script you will be aple to see teh results imediatly in the GUI of Neo4j runing at http://10.4.41.56:7474/browser/.



