## Stats Collection DIR

OSMSG Runs on Regular Interval , Generates Stats and Stores them to github , You can Access Historical Stats by looking at older github commit and recent one on the Repo itself ! 

Currrently It Runs Globally and Also monitors the Specific Country if Requested and Running Period is : 
- Daily 
- Weekly 
- Monthly 
- Yearly

It will replace the old one each time it gets updated , Those stats updates are also twitted to it's twitter bot and can be accessed as top 100 PNG format there too

Navigate to the dir to access stats 

## What does stats' column mean ? 

### map_changes 
Map changes is sum of ```nodes_create+nodes_modify+nodes_delete+ways_create+ways_modify+ways_delete+relation_create+relation_modify+relation_delete```  , the default ordering of table is based on the map changes , for eg : if you add a big building with 10 corners it will have 11 map changes (10 nodes created and 1 way created) , Create/ modify is determined from changefiles action provided by replication changefiles 

### poi 
POI are count of nodes with tags and they are not repeated . If you create a poi with 5 tags it will still count as a 1 POI create , tags info will be displayed on tags section 

### tags (tags.create , tags.modify)
it is a sum of unique tags key that user added , if you add a poi and there are 5 tags , all of 5 tags' key count will be appeared here like , tag1:1 ,tag2:1 - like this and will be added if you add similar tag in other changes 

### feature count ( building , highway , waterway , amenity etc)
Feature count will be added if it matches the key supplied , if a change has building key it will add it as a  building = 1 similar for all the features irrespective of values 
