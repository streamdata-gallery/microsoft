---
swagger: "2.0"
info:
  title: AutomationManagementClient
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}
  : patch:
      summary: Dsc Node Update
      description: Update the dsc node
      operationId: DscNode_Update
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: Parameters supplied to the update dsc node
      - in: body
        name: parameters
        description: Parameters supplied to the update dsc node
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - node
definitions:
  ActivityParameter:
    properties: []
x-collection-name: Azure Automation
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