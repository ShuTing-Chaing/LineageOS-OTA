# LineageOS-OTA port from ivanmeler/ota_provider
 
Simple automated LineageOS OTA provider Uses github releases for hosting and requires no extra server

to craft response and auto upload you will need

jq
gh
unzip
git
To upload rom and generate json simply run source release.sh ../path/to/lineageos.zip

if you want to host this on your own git you can change URL= value inside of release.sh

On device side changes either add overlay for updater_server_urlor add prop lineage.updater.uri that points to json e.g. lineage.updater.uri=https://raw.githubusercontent.com/ShuTing-Chaing/LineageOS-OTA/master/18.1/{device}.json

do note you can either hardcode {device} or leave it to updater to handle that tho in that case user might break otas by changing props