# Cluster
A set of methods for managing PostgreSQL Cluster resources.
## JSON Representation {#representation}
```json 
 {
  "id": "string",
  "folderId": "string",
  "createdAt": "string",
  "name": "string",
  "description": "string",
  "labels": "object",
  "environment": "string",
  "monitoring": [
    {
      "name": "string",
      "description": "string",
      "link": "string"
    }
  ],
  "config": {
    "version": "string",
    "poolerConfig": {
      "poolingMode": "string"
    },
    "resources": {
      "resourcePresetId": "string",
      "diskSize": "string",
      "diskTypeId": "string"
    },
    "autofailover": true,

    // `config`includes only one of the fields `postgresqlConfig_9_6`, `postgresqlConfig_10`
    "postgresqlConfig_9_6": {
      "effectiveConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number",
        "sqlInheritance": true
      },
      "userConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number",
        "sqlInheritance": true
      },
      "defaultConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number",
        "sqlInheritance": true
      }
    },
    "postgresqlConfig_10": {
      "effectiveConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number"
      },
      "userConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number"
      },
      "defaultConfig": {
        "maxConnections": "integer",
        "sharedBuffers": "integer",
        "tempBuffers": "integer",
        "maxPreparedTransactions": "integer",
        "workMem": "integer",
        "maintenanceWorkMem": "integer",
        "replacementSortTuples": "integer",
        "autovacuumWorkMem": "integer",
        "tempFileLimit": "integer",
        "vacuumCostDelay": "integer",
        "vacuumCostPageHit": "integer",
        "vacuumCostPageMiss": "integer",
        "vacuumCostPageDirty": "integer",
        "vacuumCostLimit": "integer",
        "bgwriterDelay": "integer",
        "bgwriterLruMaxpages": "integer",
        "bgwriterLruMultiplier": "number",
        "bgwriterFlushAfter": "integer",
        "backendFlushAfter": "integer",
        "oldSnapshotThreshold": "integer",
        "walLevel": "string",
        "synchronousCommit": "string",
        "checkpointTimeout": "integer",
        "checkpointCompletionTarget": "number",
        "checkpointFlushAfter": "integer",
        "maxWalSize": "integer",
        "minWalSize": "integer",
        "maxStandbyStreamingDelay": "integer",
        "defaultStatisticsTarget": "integer",
        "constraintExclusion": "string",
        "cursorTupleFraction": "number",
        "fromCollapseLimit": "integer",
        "joinCollapseLimit": "integer",
        "forceParallelMode": "string",
        "clientMinMessages": "string",
        "logMinMessages": "string",
        "logMinErrorStatement": "string",
        "logMinDurationStatement": "integer",
        "logCheckpoints": true,
        "logConnections": true,
        "logDisconnections": true,
        "logDuration": true,
        "logErrorVerbosity": "string",
        "logLockWaits": true,
        "logStatement": "string",
        "logTempFiles": "integer",
        "searchPath": "string",
        "rowSecurity": true,
        "defaultTransactionIsolation": "string",
        "statementTimeout": "integer",
        "lockTimeout": "integer",
        "idleInTransactionSessionTimeout": "integer",
        "byteaOutput": "string",
        "xmlbinary": "string",
        "xmloption": "string",
        "ginPendingListLimit": "integer",
        "deadlockTimeout": "integer",
        "maxLocksPerTransaction": "integer",
        "maxPredLocksPerTransaction": "integer",
        "arrayNulls": true,
        "backslashQuote": "string",
        "defaultWithOids": true,
        "escapeStringWarning": true,
        "loCompatPrivileges": true,
        "operatorPrecedenceWarning": true,
        "quoteAllIdentifiers": true,
        "standardConformingStrings": true,
        "synchronizeSeqscans": true,
        "transformNullEquals": true,
        "exitOnError": true,
        "seqPageCost": "number",
        "randomPageCost": "number"
      }
    },
    // end of the list of possible fields`config`

  },
  "networkId": "string",
  "health": "string",
  "status": "string"
}
```

## Methods {#methods}
Method | Description
--- | ---
[addHosts](addHosts.md) | Creates new hosts for a cluster.
[backup](backup.md) | Creates a backup for the specified PostgreSQL cluster.
[create](create.md) | Creates a PostgreSQL cluster in the specified folder.
[delete](delete.md) | Deletes the specified PostgreSQL cluster.
[deleteHosts](deleteHosts.md) | Deletes the specified hosts for a cluster.
[get](get.md) | Returns the specified PostgreSQL Cluster resource.
[list](list.md) | Retrieves the list of PostgreSQL Cluster resources that belong to the specified folder.
[listBackups](listBackups.md) | Retrieves the list of available backups for the specified PostgreSQL cluster.
[listHosts](listHosts.md) | Retrieves a list of hosts for the specified cluster.
[listLogs](listLogs.md) | Retrieves logs for the specified PostgreSQL cluster. For more information about logs, see the [Logs](/docs/yandex-mdb-guide/concepts/logs) section in the Developer's Guide.
[listOperations](listOperations.md) | Retrieves the list of Operation resources for the specified cluster.
[restore](restore.md) | Creates a new PostgreSQL cluster using the specified backup.
[update](update.md) | Updates the specified PostgreSQL cluster.
[updateHosts](updateHosts.md) | Updates the specified hosts.