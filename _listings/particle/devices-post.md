---
swagger: "2.0"
info:
  title: Particle Add Devices
  description: Claim a new or unclaimed device to your account or request transfer
    from another user.
  version: 1.0.0
host: api.particle.io
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /devices:
    post:
      summary: Add Devices
      description: Claim a new or unclaimed device to your account or request transfer
        from another user
      operationId: postDevices
      parameters:
      - in: query
        name: No Name
      - in: formData
        name: request_transfer
        description: Include this and set to true to request transfer of an existing
          device
      responses:
        200:
          description: OK
      tags:
      - devices
definitions:
  AccessTokenInfo:
    properties:
      expires_at:
        description: This is a default description.
        type: delete
      client:
        description: This is a default description.
        type: delete
  DeviceInfo:
    properties:
      name:
        description: This is a default description.
        type: delete
      last_app:
        description: This is a default description.
        type: delete
      last_ip_address:
        description: This is a default description.
        type: delete
      last_heard:
        description: This is a default description.
        type: delete
      connected:
        description: This is a default description.
        type: delete
      last_iccid:
        description: This is a default description.
        type: delete
      imei:
        description: This is a default description.
        type: delete
x-collection-name: Particle
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