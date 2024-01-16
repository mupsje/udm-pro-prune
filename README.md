How to. . . . . 

ssh root@192.168.10.1 (udm-pro ip)

sudo -i


//make the file
nano mongo_prune_js.js

// copy txt from the file mongo_prune_js.js above //

//Close and save the file

CTRL X and Y 


//Perform a test run. To run a "dry run" issue the following commands:

sed -i 's/dryrun=false/dryrun=true/g' /tmp/mongo_prune_js.js
mongo --port 27117 < /tmp/mongo_prune_js.js



//Run the script. This will run the script without "dry run":

sed -i 's/dryrun=true/dryrun=false/g' /tmp/mongo_prune_js.js
mongo --port 27117 < /tmp/mongo_prune_js.js
