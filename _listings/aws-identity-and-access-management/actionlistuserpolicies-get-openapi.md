---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API List User Policies
  version: 1.0.0
  description: Lists the names of the inline policies embedded in the specified IAM
    user.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AttachUserPolicy:
    get:
      summary: Attach User Policy
      description: Attaches the specified managed policy to the specified user.
      operationId: attachUserPolicy
      x-api-path-slug: actionattachuserpolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          attach
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) of the IAM user to attach the
          policy to
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=DeleteUserPolicy:
    get:
      summary: Delete User Policy
      description: |-
        Deletes the specified inline policy that is embedded in the specified IAM
              user.
      operationId: deleteUserPolicy
      x-api-path-slug: actiondeleteuserpolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name identifying the policy document to delete
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) identifying the user that the
          policy is embedded      in
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=DetachUserPolicy:
    get:
      summary: Detach User Policy
      description: Removes the specified managed policy from the specified user.
      operationId: detachUserPolicy
      x-api-path-slug: actiondetachuserpolicy-get
      parameters:
      - in: query
        name: PolicyArn
        description: The Amazon Resource Name (ARN) of the IAM policy you want to
          detach
        type: string
      - in: query
        name: UserName
        description: The name (friendly name, not ARN) of the IAM user to detach the
          policy      from
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=GetUserPolicy:
    get:
      summary: Get User Policy
      description: |-
        Retrieves the specified inline policy document that is embedded in the specified IAM
              user.
      operationId: getUserPolicy
      x-api-path-slug: actiongetuserpolicy-get
      parameters:
      - in: query
        name: PolicyName
        description: The name of the policy document to get
        type: string
      - in: query
        name: UserName
        description: The name of the user who the policy is associated with
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
  /?Action=ListUserPolicies:
    get:
      summary: List User Policies
      description: Lists the names of the inline policies embedded in the specified
        IAM user.
      operationId: listUserPolicies
      x-api-path-slug: actionlistuserpolicies-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: UserName
        description: The name of the user to list policies for
        type: string
      responses:
        200:
          description: OK
      tags:
      - User Policies
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