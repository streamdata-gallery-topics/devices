---
swagger: "2.0"
x-collection-name: Azure Storage
x-complete: 0
info:
  title: Azure Storage API Devices List By Manager
  version: 1.0.0
  description: Returns the list of devices for the specified manager.
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/configureDevice
  : post:
      summary: Devices Configure
      description: Complete minimal setup before using the device.
      operationId: Devices_Configure
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernameconfiguredevice-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The minimal properties to configure a device
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Devices
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/devices:
    get:
      summary: Devices List By Manager
      description: Returns the list of devices for the specified manager.
      operationId: Devices_ListByManager
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevices-get
      parameters:
      - in: query
        name: $expand
        description: Specify $expand=details to populate additional fields related
          to the device
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Devices
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