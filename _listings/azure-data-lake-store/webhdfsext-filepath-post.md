---
swagger: "2.0"
info:
  title: DataLakeStoreFileSystemManagementClient
  description: Creates an Azure Data Lake Store filesystem client.
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /WebHdfsExt/{filePath}:
    post:
      summary: File System Concurrent Append
      description: Appends to the specified file, optionally first creating the file
        if it does not yet exist
      operationId: FileSystem_ConcurrentAppend
      parameters:
      - in: query
        name: appendMode
        description: Indicates the concurrent append call should create the file if
          it doesn't exist or just open the existing file for append
      - in: path
        name: filePath
        description: The Data Lake Store path (starting with '/') of the file to which
          to append using concurrent append
      - in: query
        name: No Name
      - in: query
        name: op
        description: The constant value for the operation
      - in: body
        name: streamContents
        description: The file contents to include when appending to the file
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: syncFlag
        description: Optionally indicates what to do after completion of the concurrent
          append
      - in: header
        name: Transfer-Encoding
        description: Indicates the data being sent to the server is being streamed
          in chunks
      responses:
        200:
          description: OK
      tags:
      - file system
definitions:
  UpdateFirewallRuleProperties:
    properties:
      startIpAddress:
        description: This is a default description.
        type: get
      endIpAddress:
        description: This is a default description.
        type: get
  UpdateFirewallRuleParameters:
    properties: []
  FirewallRuleProperties:
    properties:
      startIpAddress:
        description: This is a default description.
        type: get
      endIpAddress:
        description: This is a default description.
        type: get
  FirewallRule:
    properties: []
  UpdateTrustedIdProviderProperties:
    properties:
      idProvider:
        description: This is a default description.
        type: get
  UpdateTrustedIdProviderParameters:
    properties: []
  TrustedIdProviderProperties:
    properties:
      idProvider:
        description: This is a default description.
        type: get
  TrustedIdProvider:
    properties: []
  DataLakeStoreTrustedIdProviderListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  DataLakeStoreFirewallRuleListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  EncryptionIdentity:
    properties:
      type:
        description: This is a default description.
        type: get
      principalId:
        description: This is a default description.
        type: get
      tenantId:
        description: This is a default description.
        type: get
  EncryptionConfig:
    properties:
      type:
        description: This is a default description.
        type: get
  KeyVaultMetaInfo:
    properties:
      keyVaultResourceId:
        description: This is a default description.
        type: get
      encryptionKeyName:
        description: This is a default description.
        type: get
      encryptionKeyVersion:
        description: This is a default description.
        type: get
  DataLakeStoreAccountProperties:
    properties:
      provisioningState:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      creationTime:
        description: This is a default description.
        type: get
      encryptionState:
        description: This is a default description.
        type: get
      encryptionProvisioningState:
        description: This is a default description.
        type: get
      firewallState:
        description: This is a default description.
        type: get
      firewallRules:
        description: This is a default description.
        type: get
      trustedIdProviderState:
        description: This is a default description.
        type: get
      trustedIdProviders:
        description: This is a default description.
        type: get
      lastModifiedTime:
        description: This is a default description.
        type: get
  UpdateDataLakeStoreAccountProperties:
    properties:
      firewallState:
        description: This is a default description.
        type: get
      trustedIdProviderState:
        description: This is a default description.
        type: get
      defaultGroup:
        description: This is a default description.
        type: get
      newTier:
        description: This is a default description.
        type: get
      firewallAllowAzureIps:
        description: This is a default description.
        type: get
  DataLakeStoreAccountUpdateParameters:
    properties:
      tags:
        description: This is a default description.
        type: get
  DataLakeStoreAccount:
    properties: []
  DataLakeStoreAccountListResult:
    properties:
      value:
        description: This is a default description.
        type: get
      nextLink:
        description: This is a default description.
        type: get
  ErrorDetails:
    properties:
      code:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      target:
        description: This is a default description.
        type: get
  Resource:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
      location:
        description: This is a default description.
        type: get
      tags:
        description: This is a default description.
        type: get
  SubResource:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  FileOperationResult:
    properties:
      boolean:
        description: This is a default description.
        type: put
  AclStatus:
    properties:
      entries:
        description: This is a default description.
        type: put
      group:
        description: This is a default description.
        type: put
      owner:
        description: This is a default description.
        type: put
      permission:
        description: This is a default description.
        type: put
      stickyBit:
        description: This is a default description.
        type: put
  AclStatusResult:
    properties: []
  ContentSummary:
    properties:
      directoryCount:
        description: This is a default description.
        type: put
      fileCount:
        description: This is a default description.
        type: put
      length:
        description: This is a default description.
        type: put
      spaceConsumed:
        description: This is a default description.
        type: put
  ContentSummaryResult:
    properties: []
  FileStatusProperties:
    properties:
      accessTime:
        description: This is a default description.
        type: put
      blockSize:
        description: This is a default description.
        type: put
      childrenNum:
        description: This is a default description.
        type: put
      msExpirationTime:
        description: This is a default description.
        type: put
      group:
        description: This is a default description.
        type: put
      length:
        description: This is a default description.
        type: put
      modificationTime:
        description: This is a default description.
        type: put
      owner:
        description: This is a default description.
        type: put
      pathSuffix:
        description: This is a default description.
        type: put
      permission:
        description: This is a default description.
        type: put
  FileStatuses:
    properties:
      FileStatus:
        description: This is a default description.
        type: put
  FileStatusesResult:
    properties: []
  FileStatusResult:
    properties: []
  AdlsRemoteException:
    properties:
      exception:
        description: This is a default description.
        type: put
      javaClassName:
        description: This is a default description.
        type: put
      message:
        description: This is a default description.
        type: put
  AdlsError:
    properties: []
x-collection-name: Azure Data Lake Store
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---