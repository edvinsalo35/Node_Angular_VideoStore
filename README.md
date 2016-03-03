# COA 

## Patch guide for Node Mongo Working

1. First off, install XCode
2. After that, add the kerberos & mongodb with the right version number.
	```
	"kerberos": "~0.0",
    "mongodb": "~1.4"
	```
3. Thirdly, fix the bson error as below. 

	Find in npm module mongodb 
	```
	..node_modules\mongodb\node_modules\bson\ext\index.js
	```
	and change path to js version in catch block
	```
	bson = require('../build/Release/bson');
	```	
	to
	```
	bson = require('../browser_build/bson');
	```

## Contents

Includes Node + Express + Mongo + Angular Usage.