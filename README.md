From new os

deprecated out of order !!!!!!


###################################################################################################



Prune old data from udm unifi

How to. . . . . 

ssh root@192.168.10.1 (udm-pro ip)

sudo -i

```
sudo apt install nano
```

//make the file
```
nano mongo_prune_js.js
```

// copy txt from the file mongo_prune_js.js above //

//Close and save the file

CTRL X and Y 


//Perform a test run. To run a "dry run" issue the following commands:

```
sed -i 's/dryrun=false/dryrun=true/g' mongo_prune_js.js
```
then
```
mongo --port 27117 < mongo_prune_js.js
```

//Run the script. This will run the script without "dry run":

```
sed -i 's/dryrun=true/dryrun=false/g' mongo_prune_js.js
```
then
```
mongo --port 27117 < mongo_prune_js.js
```
