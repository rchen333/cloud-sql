# cloud-sql
want to create a tool to execute sql query to get up to date information for your cloud data. So you can easily get that structure information. 
There are two different approach toward this. One is to parse the sql queries to api command to get the information on real time. It will require pretty sophisticate parsing schema. The return information will be relatively real time. 
The other approach is to get all information from the cloud and store them to a db and execute sql query aginst the db. 
I like the second approach a little bite better, it is due to the fact that your cloud data will not change really drastically in very short period of time. The amount of data is also pretty limited. Even if you have thusands instances, the data will mostly like be measured in size of GBs. 
The approach is to have a internal job schedule to get your aws information at certainly internal, so your query information is relatively real time. If the job scheduler run requently enough, you will more likely get the updated information than not. 
One thing is to make sure that if AWS, Google or AZsure change their data schema, it has to be updated here. 
