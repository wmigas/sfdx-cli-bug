# assumptions
1. you have configured connection to the dev hub
2. you have namespace connected to the dev hub

# create new package
command
```
sfdx force:package:create -v devhub -d "case42830117" -n "package_name" -r force-app\main -t Unlocked
```

output
```
Successfully created a package. 0Ho4x000000KyyHCAS
=== Ids
 Name       Value
 ────────── ──────────────────
 Package Id 0Ho4x000000KyyHCAS
 ```
 
 
# create package version
command
```
sfdx force:package:version:create --package "package_name" -v devhub -w 60 -b hercules -t "commit-hash" -k installationpassword
```

output
```
Request in progress. Sleeping 30 seconds. Will wait a total of 3600 more seconds before timing out. Current Status='Queued'
Request in progress. Sleeping 30 seconds. Will wait a total of 3570 more seconds before timing out. Current Status='Initializing'
ERROR running force:package:version:create:  Multiple errors occurred:
(1) TacticColor.Feature: invalid cross reference id
(2) TacticColor.Display: invalid cross reference id
(3) TacticColor.Demos: invalid cross reference id
(4) TacticColor.Feature_Display: invalid cross reference id
(5) TacticColor.TPR: invalid cross reference id
(6) TacticColor.Slotting: invalid cross reference id
(7) TacticColor.Fees: invalid cross reference id
```
