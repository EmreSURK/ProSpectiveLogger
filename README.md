# ProSpectiveLogger
A logger for NodeJS that splits logs per user and date. It is super-easy to see what is going on 
Automatically splits logs into folders according to date.
Also automatically creates logs that splitted per user.
Also automatically creates a combined logs file that is not splitted into users or dates. It includes all logs.

A little hard to understand but super-easy to use.

```
npm install --save prospectivelogger
```

```
/**
* Logs to user
*/
proSpectiveLogger.logToUser( userID, stringOrObectToLog );
```


```
/**
* You can also log for all users with a line of code.
*/
proSpectiveLogger.logToAllUsers( stringOrObectToLog );
```

For exaple;

```
var proSpectiveLogger = require("prospectivelogger");

proSpectiveLogger.logToUser(1 + "-Emre","Nobir..");
proSpectiveLogger.logToUser(1 + "-Emre", { addedItem: "a panth" });
proSpectiveLogger.logToUser(32 + "-Hoca", { addedItem: "a panth" });
proSpectiveLogger.logToAllUsers(" * * System deleted all items.");
proSpectiveLogger.logToUser(32 + "-Hoca", { addedItem: "a panth" });
```
Creates these files and folders : 

dateBasedLogs/31-10-2017/1-Emre.log

dateBasedLogs/31-10-2017/32-Hoca.log

userBasedLogs/1-Emre.log

userBasedLogs/32-Hoca.log

combinedLogs.log


