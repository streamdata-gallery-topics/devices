---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Get a single device provisioned to a merchant
  version: 1.0.0
  description: Returns a single device that is provisioned to a merchant.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/devices:
    get:
      summary: Get all devices provisioned to a merchant
      description: Returns a list of all devices that are provisioned to the a merchant.
        This list can be viewed from the Setup App on the merchant's device or web
        dashboard (https://www.clover.com/setupapp/m/{mId}/devices).
      operationId: GetMerchantDevices
      x-api-path-slug: v3merchantsmiddevices-get
      parameters:
      - in: query
        name: filter
        description: 'Filter fields: [id, model, name, orderPrefix, serial, deleted_time,
          merchant'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Devices
  /v3/merchants/{mId}/devices/{deviceId}:
    get:
      summary: Get a single device provisioned to a merchant
      description: Returns a single device that is provisioned to a merchant.
      operationId: GetMerchantDevice
      x-api-path-slug: v3merchantsmiddevicesdeviceid-get
      parameters:
      - in: path
        name: deviceId
        description: Device Id
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Devices
      - DeviceId
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