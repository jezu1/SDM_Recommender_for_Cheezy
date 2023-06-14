# SDM_Recommender
Building a recommender for Cheezy start-up idea

## Table of Contents
1. [General Info](#general-info)
2. [Set up and requirements](#set-up-and-requirements)
3. [Neo4j Graph Creation](#Neo4j-Graph-Creation)
4. [Recommender](#recommender)

## General Info
***
This git repository is part of the university project Cheezy, which is a start up idea that recommends users the best restaurant based on their preferences, swips and location. In this git we have build a property graph in neo4j as the exploation layer of our architecture. The grpah is created from the Delta tables, thought pyspark with Neo4j connector and a recommendor is build on top of it.

## Set up and requirements
***
A virtual machine on OpenNebula with the following specifications is used for this project: 
50 gb GB and OS - Ubuntu 18.04.3 LTS

Other technologies used within the project:
*Delta Lake: io.delta:delta-core_2.12:2.1.0
*Pyspark: 3.3.0
*Neo4j connector: neo4j-connector-apache-spark_2.12_3.0-4.0.0
*Neo4j: 4.4.20
*VM Credentials: VM user: masterBD01 -- Password: tKtyPg4nNn
*Ubuntu user: User: hadoop -- Password: foodie
*Neo4j user: User: neo4j -- Password: foodie

## Neo4j Graph Creation
Neo4j is running in the vitual machine, so please enter to the VM with the credetials above and to start neo4j perform: 
sudo /opt/neo4j/bin/neo4j restart
and you will be able to access neo4j in your brwoser in this address: http://10.4.41.56:7474/browser/
To run the graph creation script, please run neo4j * **Neo4JConnect.py**: file, which already has all the neccesary conections to the delta tables and neo4j and directly performs the node and relationship creation/update if the nodes already exist.
After runnig the script you will be aple to see the results imediatly in the GUI of Neo4j runing at http://10.4.41.56:7474/browser/.

### Recommender
The file **recommender.cql** includes all the cypher queries to create and query the recommender for our Graph in Neo4J. To be able to execute all the queries the Neo4J Graph Data Science Library must be installed.


