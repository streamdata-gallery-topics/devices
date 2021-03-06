swagger: "2.0"
x-collection-name: Server Density
x-complete: 1
info:
  title: Widgets API
  description: the-widgets-api-
  version: 1.0.0
host: api.serverdensity.io.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /inventory/devices:
    "":
      summary: Creating a device
      description: |-
        You can create new devices via the API, useful if you want to automatically provision new devices and start monitoring automatically.
        This API method is used by our Puppet manifest, Chef cookbook and installer shell script to automatically create devices during the agent installation.
      operationId: creating-a-device
      x-api-path-slug: inventorydevices-
      parameters:
      - in: body
        name: cpuCores
        description: Item???s number of cores
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: group
        description: Name of group
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: hostname
        description: Device???s hostname
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: installedRAM
        description: RAM installed
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: location
        description: A dictionary containing countryCode, text (which is the city)
          and countryName
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: name
        description: Name of device
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: os
        description: A dictionary containing code and name
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: privateIPs
        description: Item???s private IP addresses as a JSON encoded list
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: provider
        description: The provider dependent string that identifies this item
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: publicIPs
        description: Item???s public IP addresses as a JSON encoded list
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: swapSpace
        description: Item???s swap space
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: tags
        description: A JSON list of tag IDs
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: token
        description: Your API token
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: token
        description: Your API token
        type: string
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Devices
  /inventory/devices/deviceId:
    "":
      summary: Updating a device
      description: Update a device and the associated metadata.
      operationId: updating-a-device
      x-api-path-slug: inventorydevicesdeviceid-
      parameters:
      - in: path
        name: cpuCores
        description: Item???s number of cores
        type: string
      - in: body
        name: cpuCores
        description: Item???s number of cores
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: deviceId
        description: The ID of the device to update
        type: string
      - in: path
        name: group
        description: Name of group
        type: string
      - in: body
        name: group
        description: Name of group
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: hostname
        description: Item???s hostname
        type: string
      - in: body
        name: hostname
        description: Item???s hostname
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: installedRAM
        description: RAM installed
        type: string
      - in: body
        name: installedRAM
        description: RAM installed
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Name of the device
        type: string
      - in: body
        name: name
        description: Name of the device
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: os
        description: Operating system that it runs
        type: string
      - in: body
        name: os
        description: Operating system that it runs
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: privateIPs
        description: Item???s private IP addresses as a JSON encoded list
        type: string
      - in: body
        name: privateIPs
        description: Item???s private IP addresses as a JSON encoded list
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: provider
        description: Provider where the item is hosted
        type: string
      - in: body
        name: provider
        description: Provider where the item is hosted
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: providerId
        description: The provider dependent string that identifies this item
        type: string
      - in: body
        name: providerId
        description: The provider dependent string that identifies this item
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: publicIPs
        description: Item???s public IP addresss as a JSON encoded list
        type: string
      - in: body
        name: publicIPs
        description: Item???s public IP addresss as a JSON encoded list
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: swapSpace
        description: Item???s swap space
        type: string
      - in: body
        name: swapSpace
        description: Item???s swap space
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tags
        description: A JSON list of tag IDs
        type: string
      - in: body
        name: tags
        description: A JSON list of tag IDs
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: token
        description: Your API token
        type: string
      - in: body
        name: token
        description: Your API token
        schema:
          $ref: '#/definitions/holder'
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Devices
  /inventory/devices/agentKey/byagentkey:
    "":
      summary: View device by agent key
      description: View device by agent key.
      operationId: view-device-by-agent-key
      x-api-path-slug: inventorydevicesagentkeybyagentkey-
      parameters:
      - in: path
        name: agentKey
        description: The key used by the agent
        type: string
      - in: path
        name: token
        description: Your API token
        type: string
      - in: query
        name: token
        description: Your API token
        type: string
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Devices
  /alerts/service_alerts.json:
    "":
      summary: Listing service alert metrics
      description: Devices and services have different alert metrics which you can
        configure in the ui. The section correspond to the top-level of the alert
        metric whereas field corresponds to the subsection of the given section.
      operationId: listing-service-alert-metrics
      x-api-path-slug: alertsservice-alerts-json-
      parameters:
      - in: query
        name: token
        description: Your API token
        type: string
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Alerts