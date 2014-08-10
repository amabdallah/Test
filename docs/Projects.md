In WaM-DaM, projects provid general information about the user who creates or gathers data in WaM-DaM, the project which the user is working on, the objects the user creates for their project, and their attributes. These objects and their attributes can be reused for many networks. The Users table organizes data about the user name, organization, address, etc. A user can create zero or many projects. The Projects table contains all the data and metadata of the user’s work. It has metadata like the project name and its description. It can have zero or many networks. The Objects table is a container that describes general metadata for nodes and links (e.g., reservoir and canal). Each object can be associated with one or more attributes. For example, a reservoir can have attributes like capacity, dam height, and inflow. The use of node and link object names is controlled by a set of vocabularies like “Reservoir” and “Canal”. Finally, the Attributes table defines one or more parameters or variables like elevation and storage for an Object.  


One peson can have one project or many 


many people can work on the same project and then networks

***One Project can have many networks But can a network belong to many projects?*** YES BUT <P>
The concept of Project is just to contain all the objects and their attributes so you can share them between networks. Also the project concept keeps track of the users and who is working on developing the database. <P>

Lets assume that I have the Little Bear River Network that belongs into two projects where each projetc has its own metadata like the purpose, description, time frame, and the people who work on it. The question here is, are the two networks identical? Maybe but chances are heigh that they're different because each project has a different interest and focus on examining the network and its representation of the real world. So it seems that two networks are most likely not to share the same project. 

***Can we track of who added or deleted what in a project?***
For now, NO. But the way to do that is to add a reference key to the users in the ScenarioAttribuyeData table just like a scenario can keep track of the changes. But in this case we can keep track of indivitual changes that are made by users. Its going to be hectic for users to keeping adding the foreigh key of the user in each recored in that table. But is it worth it?



