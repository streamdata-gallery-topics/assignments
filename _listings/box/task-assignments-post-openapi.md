---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Create Task Assignment
  description: Used to assign a task to a single user. There can be multiple assignments
    on a given task.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tasks/{TASK_ID}/assignments:
    get:
      summary: Get Assignments
      description: Retrieves all of the assignments for a given task.
      operationId: getTaskAssignments
      x-api-path-slug: taskstask-idassignments-get
      parameters:
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: TASK_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Tasks
      - Task
      - ""
      - Assignments
  /task_assignments:
    post:
      summary: Create Task Assignment
      description: Used to assign a task to a single user. There can be multiple assignments
        on a given task.
      operationId: createTaskAssignment
      x-api-path-slug: task-assignments-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Task
      - Assignments
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