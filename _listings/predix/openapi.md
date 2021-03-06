swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/proxy/projects/{id}:
    put:
      summary: Load/Create Project
      description: API to Load/Create project in ESP server.
      operationId: loadOrCreateProjectUsingPUT
      x-api-path-slug: v1proxyprojectsid-put
      parameters:
      - in: body
        name: reqBody
        description: reqBody
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Load
      - Project
    delete:
      summary: Delete project.
      description: API to delete project from ESP server.
      operationId: deleteProjectUsingDELETE
      x-api-path-slug: v1proxyprojectsid-delete
      parameters:
      - in: body
        name: reqBody
        description: reqBody
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Project
  /v1/proxy/projects/{id}/state:
    put:
      summary: Update project status
      description: API to update project status etc. started, running, stopped
      operationId: projectStatusUsingPUT
      x-api-path-slug: v1proxyprojectsidstate-put
      parameters:
      - in: body
        name: reqBody
        description: reqBody
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Project
      - Status