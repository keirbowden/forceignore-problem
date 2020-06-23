# .forceignore problem repo

## Check everything deploys okay
1. Create a scratch org
1. Copy `.forceignore_deploy_all` to `.forceignore`
1. Execute `sfdx force:source:push` and note the first and second objects and layouts are deployed
1. Delete the scratch org

## Reproduce problem
1. Create a scratch org
1. Copy `.forceignore_exclude_second` to `.forceignore`
1. Execute `sfdx force:source:push` and note the second object and layout are not deployed, as expected
1. Copy `.forceignore_deploy_all` to `.forceignore`
1. Execute `sfdx force:source:push` and note that no results found is displayed, so the updated `.forceignore` file isn't having the desired affect.