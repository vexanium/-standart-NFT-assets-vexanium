# Smart Contract: stdvexassets
Standard Vexanium Assets
## create BY <a href="https://github.com/proitlab/stdvexassets">proit</a> 
## NFT - Non Fungible Token

### CREATE

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets create '{"author": "<author account>", "category":"certificate","owner": "<owner account>", "idata": "{\"name\":\"Diamond Certificate\"}", "mdata": "{\"name\": \"Blue Safir\"}", "requireclaim": 0}' -p <author account>`

### LIST

`./cleos http://api.vex.proit.id:8080 get table stdvexassets <account> sassets`

### UPDATE

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets update '{"author": "<author account>", "owner": "<owner account>", "assetid": <asset id> "mdata": "{\"name\": \"Red Diamond\"}"}' -p <account>`

### TRANSFER

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets transfer '{"from": "<account>", "to": "<account>", "assetids": [<assetid>], "memo": "NFT Transfer" }' -p <account_from>`

### BURN

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets burn '{"owner": "<owner account>", "assetids": [<asset id>], "memo":"First NFT Burn"}' -p <owner account>`

### DELEGATE/BORROW

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets delegate '{"owner": "<NFT owner account>", "to": "<NFT receiver account>", "assetids": <array [] of asset ids>, "period": <wait in seconds until undelegate will be possible, 86400=1day>, "redelegate": <set 1 will allow redelegate asset,0 -not>, "memo": "<text memo>" }' -p <NFT owner account>`

### UNDELEGATE/UNBORROW

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets undelegate '{"owner": "<NFT real owner account>", "assetids": <array [] of asset ids> }' -p <NFT real owner account>`

### DELEGATEMORE (extend period of delegation)

`./cleos --url http://api.vex.proit.id:8080 push action stdvexassets delegatemore '{"owner": "<NFT owner account>", "assetidc": <array [] of asset ids>, "period": <will add to existing period  seconds until undelegate will be possible, 86400=1day>, }' -p <NFT owner account>`
