---
swagger: "2.0"
info:
  title: TrafficManagerManagementClient
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
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficmanagerprofiles/{profileName}/{endpointType}/{endpointName}
  : patch:
      summary: Endpoints Update
      description: Update a Traffic Manager endpoint
      operationId: Endpoints_Update
      parameters:
      - in: path
        name: endpointName
        description: The name of the Traffic Manager endpoint to be updated
      - in: path
        name: endpointType
        description: The type of the Traffic Manager endpoint to be updated
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The Traffic Manager endpoint parameters supplied to the Update
          operation
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileName
        description: The name of the Traffic Manager profile
      - in: path
        name: resourceGroupName
        description: The name of the resource group containing the Traffic Manager
          endpoint to be updated
      responses:
        200:
          description: OK
      tags:
      - endpoints
definitions:
  DeleteOperationResult:
    properties:
      boolean:
        description: This is a default description.
        type: get
  EndpointProperties:
    properties:
      targetResourceId:
        description: This is a default description.
        type: get
      target:
        description: This is a default description.
        type: get
      endpointStatus:
        description: This is a default description.
        type: get
      weight:
        description: This is a default description.
        type: get
      priority:
        description: This is a default description.
        type: get
      endpointLocation:
        description: This is a default description.
        type: get
      endpointMonitorStatus:
        description: This is a default description.
        type: get
      minChildEndpoints:
        description: This is a default description.
        type: get
      geoMapping:
        description: This is a default description.
        type: get
  Endpoint:
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
  CheckTrafficManagerRelativeDnsNameAvailabilityParameters:
    properties:
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  DnsConfig:
    properties:
      relativeName:
        description: This is a default description.
        type: get
      fqdn:
        description: This is a default description.
        type: get
      ttl:
        description: This is a default description.
        type: get
  MonitorConfig:
    properties:
      profileMonitorStatus:
        description: This is a default description.
        type: get
      protocol:
        description: This is a default description.
        type: get
      port:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
  ProfileProperties:
    properties:
      profileStatus:
        description: This is a default description.
        type: get
      trafficRoutingMethod:
        description: This is a default description.
        type: get
      endpoints:
        description: This is a default description.
        type: get
  Profile:
    properties: []
  ProfileListResult:
    properties:
      value:
        description: This is a default description.
        type: get
  TrafficManagerNameAvailability:
    properties:
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
      nameAvailable:
        description: This is a default description.
        type: get
      reason:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
  Region:
    properties:
      code:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      regions:
        description: This is a default description.
        type: get
  GeographicHierarchyProperties:
    properties: []
  TrafficManagerGeographicHierarchy:
    properties: []
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
  CloudError:
    properties: []
  CloudErrorBody:
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
      details:
        description: This is a default description.
        type: get
x-collection-name: Azure Traffic Manager
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