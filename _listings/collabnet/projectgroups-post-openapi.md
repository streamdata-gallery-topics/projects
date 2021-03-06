---
swagger: "2.0"
x-collection-name: CollabNet
x-complete: 0
info:
  title: CollabNet TeamForge API Documentation Creates project group
  version: 1.0.0
  description: Creates project group.
basePath: /ctfrest/foundation/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{userid}/projects/{projectid}:
    put:
      summary: Adds a user to specified project's member list by user id
      description: Adds a user to specified project's member list by user id.
      operationId: addUserById
      x-api-path-slug: usersuseridprojectsprojectid-put
      parameters:
      - in: path
        name: projectid
        description: Project id
      - in: path
        name: userid
        description: User id
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Specified
      - Projects
      - Member
      - List
      - By
      - User
  /users/myself/projects/{projectid}:
    put:
      summary: Adds current user to specified project's member list
      description: Adds current user to specified project's member list.
      operationId: addMyself
      x-api-path-slug: usersmyselfprojectsprojectid-put
      parameters:
      - in: path
        name: projectid
        description: Project id
      responses:
        200:
          description: OK
      tags:
      - Current
      - User
      - To
      - Specified
      - Projects
      - Member
      - List
  /users/by-username/{username}/projects/{projectid}:
    put:
      summary: Adds a user to specified project's member list by username
      description: Adds a user to specified project's member list by username.
      operationId: addUserByUsername
      x-api-path-slug: usersbyusernameusernameprojectsprojectid-put
      parameters:
      - in: path
        name: projectid
        description: Project id
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Specified
      - Projects
      - Member
      - List
      - By
      - Username
  /projectgroups/{projectgroupid}/projects:
    get:
      summary: Gets project group projects
      description: Gets project group projects.
      operationId: getProjectGroupProjects
      x-api-path-slug: projectgroupsprojectgroupidprojects-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Projects
  /users/{userid}/projects:
    get:
      summary: Gets a user's project list by user id
      description: Gets a user's project list by user id.
      operationId: getProjectsByUserid
      x-api-path-slug: usersuseridprojects-get
      parameters:
      - in: query
        name: fetchHierarchyPath
      - in: query
        name: sortby
        description: Sort by column name
      - in: path
        name: userid
        description: User id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Project
      - List
      - By
      - User
  /users/myself/projects:
    get:
      summary: Gets current user's project list
      description: Gets current user's project list.
      operationId: getMyProjects
      x-api-path-slug: usersmyselfprojects-get
      parameters:
      - in: query
        name: fetchHierarchyPath
      - in: query
        name: sortby
        description: Sort by column name
      responses:
        200:
          description: OK
      tags:
      - Current
      - Users
      - Project
      - List
  /users/by-username/{username}/projects:
    get:
      summary: Gets a user's project list by username
      description: Gets a user's project list by username.
      operationId: getProjectsByUsername
      x-api-path-slug: usersbyusernameusernameprojects-get
      parameters:
      - in: query
        name: fetchHierarchyPath
      - in: query
        name: sortby
        description: Sort by column name
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Users
      - Project
      - List
      - By
      - Username
  /projecttemplates:
    get:
      summary: Gets paginated project template list.
      description: Gets paginated project template list..
      operationId: getProjectTemplates
      x-api-path-slug: projecttemplates-get
      parameters:
      - in: query
        name: count
        description: Max
      - in: query
        name: offset
        description: Offset
      - in: query
        name: sortby
        description: Sort by column name
      responses:
        200:
          description: OK
      tags:
      - Paginated
      - Project
      - Template
      - List
  /projects/{projectid}/{username}:
    delete:
      summary: Removes project member
      description: Removes project member.
      operationId: removeProjectMember
      x-api-path-slug: projectsprojectidusername-delete
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - Member
    put:
      summary: Adds project member
      description: Adds project member.
      operationId: addProjectMember
      x-api-path-slug: projectsprojectidusername-put
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Project
      - Member
  /projects/{projectid}/roles/{roleid}/members/{username}:
    delete:
      summary: Removes user from a project role
      description: Removes user from a project role.
      operationId: removeUserFromProjectRole
      x-api-path-slug: projectsprojectidrolesroleidmembersusername-delete
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      - in: path
        name: username
        description: username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - User
      - From
      - Project
      - Role
    put:
      summary: Add user to project role
      description: Add user to project role.
      operationId: addUserToProjectRole
      x-api-path-slug: projectsprojectidrolesroleidmembersusername-put
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      - in: path
        name: username
        description: username
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Project
      - Role
  /projects/{projectid}/roles/{roleid}/members:
    get:
      summary: Gets project role members
      description: Gets project role members.
      operationId: getProjectRoleMembers
      x-api-path-slug: projectsprojectidrolesroleidmembers-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
      - Members
  /projects/{projectid}/roles/{roleid}/auto-grant:
    delete:
      summary: Stop granting a role automatically in a given project
      description: Stop granting a role automatically in a given project.
      operationId: removeAutoGrantRoleInProject
      x-api-path-slug: projectsprojectidrolesroleidautogrant-delete
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Granting
      - Role
      - Automatically
      - In
      - Given
      - Project
    put:
      summary: Grant a role automatically in a given project
      description: Grant a role automatically in a given project.
      operationId: autoGrantRoleInProject
      x-api-path-slug: projectsprojectidrolesroleidautogrant-put
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      responses:
        200:
          description: OK
      tags:
      - Grant
      - Role
      - Automatically
      - In
      - Given
      - Project
    get:
      summary: Gets whether a role is granted automatically in a project or not.
      description: Gets whether a role is granted automatically in a project or not..
      operationId: isRoleAutoGrantInProject
      x-api-path-slug: projectsprojectidrolesroleidautogrant-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      - in: path
        name: roleid
        description: Role identifier
      responses:
        200:
          description: OK
      tags:
      - Whether
      - Role
      - Is
      - Granted
      - Automatically
      - In
      - Project
      - Not
  /projects/{projectid}/roles/{roleid}:
    patch:
      summary: Updates project role.
      description: Updates project role..
      operationId: updateProjectRole
      x-api-path-slug: projectsprojectidrolesroleid-patch
      parameters:
      - in: body
        name: body
        description: Updated role info
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: If-Match
        description: Role version
      - in: path
        name: projectid
        description: Project or project group identifier
      - in: path
        name: roleid
        description: Role identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
    delete:
      summary: Deletes a project role
      description: Deletes a project role.
      operationId: deleteProjectRole
      x-api-path-slug: projectsprojectidrolesroleid-delete
      parameters:
      - in: path
        name: projectid
        description: Project or project group identifier
      - in: path
        name: roleid
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
  /projects/{projectid}/roles/inherited-roles:
    get:
      summary: Gets inherited project role list
      description: Gets inherited project role list.
      operationId: getInheritedProjectRoles
      x-api-path-slug: projectsprojectidrolesinheritedroles-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Inherited
      - Project
      - Role
      - List
  /projects/{projectid}/roles:
    post:
      summary: Creates project role.
      description: Creates project role..
      operationId: createProjectRole
      x-api-path-slug: projectsprojectidroles-post
      parameters:
      - in: body
        name: body
        description: New role data
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: projectid
        description: Project or project group identifier
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Project
      - Role
    get:
      summary: Gets project role list
      description: Gets project role list.
      operationId: getProjectRoles
      x-api-path-slug: projectsprojectidroles-get
      parameters:
      - in: query
        name: includeInherited
        description: Include inherited roles? This parameter is relevant for Project
          type only
      - in: path
        name: projectid
        description: Project or project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
      - List
  /projects/{projectid}/members:
    get:
      summary: Gets project members
      description: Gets project members.
      operationId: getProjectMembers
      x-api-path-slug: projectsprojectidmembers-get
      parameters:
      - in: query
        name: count
        description: Max
      - in: query
        name: offset
      - in: path
        name: projectid
        description: Project identifier
      - in: query
        name: searchvalue
        description: Filter value for project member name
      - in: query
        name: sortby
        description: Sorting column name
      responses:
        200:
          description: OK
      tags:
      - Project
      - Members
  /projects/{projectid}/lock:
    delete:
      summary: Unlocks a project
      description: Unlocks a project.
      operationId: unlockProject
      x-api-path-slug: projectsprojectidlock-delete
      parameters:
      - in: path
        name: projectid
      responses:
        200:
          description: OK
      tags:
      - Unlocks
      - Project
    put:
      summary: Locks a project
      description: Locks a project.
      operationId: lockProject
      x-api-path-slug: projectsprojectidlock-put
      parameters:
      - in: path
        name: projectid
      responses:
        200:
          description: OK
      tags:
      - Locks
      - Project
  /projects/{projectid}/diskusage:
    get:
      summary: Gets project disk usage in bytes
      description: Gets project disk usage in bytes.
      operationId: getProjectDiskUsage
      x-api-path-slug: projectsprojectiddiskusage-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Disk
      - Usage
      - In
      - Bytes
  /projects/{projectid}/admins:
    get:
      summary: Gets project administrators
      description: Gets project administrators.
      operationId: getProjectAdmins
      x-api-path-slug: projectsprojectidadmins-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Administrators
  /projects/{projectid}:
    patch:
      summary: Updates project data
      description: Updates project data.
      operationId: updateProject
      x-api-path-slug: projectsprojectid-patch
      parameters:
      - in: body
        name: body
        description: Updated project info
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: If-Match
        description: Project version
      - in: path
        name: projectid
      responses:
        200:
          description: OK
      tags:
      - Project
      - Data
    delete:
      summary: Deletes a project
      description: Deletes a project.
      operationId: deleteItem
      x-api-path-slug: projectsprojectid-delete
      parameters:
      - in: query
        name: force
      - in: query
        name: notify
      - in: path
        name: projectid
      responses:
        200:
          description: OK
      tags:
      - Project
    get:
      summary: Gets project information
      description: Gets project information.
      operationId: getProject
      x-api-path-slug: projectsprojectid-get
      parameters:
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Information
  /projects/requests/count:
    get:
      summary: Gets the number of pending project requests
      description: Gets the number of pending project requests.
      operationId: getProjectRequestCount
      x-api-path-slug: projectsrequestscount-get
      responses:
        200:
          description: OK
      tags:
      - Number
      - Of
      - Pending
      - Project
      - Requests
  /projects/requests:
    get:
      summary: Gets paginated project request list
      description: Gets paginated project request list.
      operationId: getProjectRequests
      x-api-path-slug: projectsrequests-get
      parameters:
      - in: query
        name: count
        description: Max
      - in: query
        name: offset
        description: Offset
      responses:
        200:
          description: OK
      tags:
      - Paginated
      - Project
      - Request
      - List
  /projects:
    post:
      summary: Creates project
      description: Creates project.
      operationId: createProject
      x-api-path-slug: projects-post
      parameters:
      - in: body
        name: body
        description: New project data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Project
    get:
      summary: Gets paginated project list.
      description: Gets paginated project list..
      operationId: getProjects
      x-api-path-slug: projects-get
      parameters:
      - in: query
        name: count
        description: Max
      - in: query
        name: fetchHierarchyPath
      - in: query
        name: offset
        description: Offset
      - in: query
        name: searchvalue
      - in: query
        name: sortby
        description: Sort by column name
      responses:
        200:
          description: OK
      tags:
      - Paginated
      - Project
      - List
  /projectgroups/{projectgroupid}/projects/{projectid}:
    delete:
      summary: Removes project from group
      description: Removes project from group.
      operationId: removeProjectFromGroup
      x-api-path-slug: projectgroupsprojectgroupidprojectsprojectid-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - From
      - Group
    put:
      summary: Adds project to project group
      description: Adds project to project group.
      operationId: addProjectToGroup
      x-api-path-slug: projectgroupsprojectgroupidprojectsprojectid-put
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: projectid
        description: Project identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - To
      - Project
      - Group
  /projectgroups/{projectgroupid}/members/{username}:
    delete:
      summary: Removes project group member
      description: Removes project group member.
      operationId: removeProjectGroupMember
      x-api-path-slug: projectgroupsprojectgroupidmembersusername-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - Group
      - Member
    put:
      summary: Adds project group member
      description: Adds project group member.
      operationId: addProjectGroupMember
      x-api-path-slug: projectgroupsprojectgroupidmembersusername-put
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Member
  /projectgroups/{projectgroupid}/members:
    get:
      summary: Gets project group members
      description: Gets project group members.
      operationId: getProjectGroupMembers
      x-api-path-slug: projectgroupsprojectgroupidmembers-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Members
  /projectgroups/{projectgroupid}/admins/{username}:
    delete:
      summary: Removes project group admin
      description: Removes project group admin.
      operationId: removeProjectGroupAdmin
      x-api-path-slug: projectgroupsprojectgroupidadminsusername-delete
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Removes
      - Project
      - Group
      - Admin
    put:
      summary: Adds project group admin
      description: Adds project group admin.
      operationId: addProjectGroupAdmin
      x-api-path-slug: projectgroupsprojectgroupidadminsusername-put
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Admin
  /projectgroups/{projectgroupid}/admins:
    get:
      summary: Gets project group admins
      description: Gets project group admins.
      operationId: getProjectGroupAdmins
      x-api-path-slug: projectgroupsprojectgroupidadmins-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Admins
  /projectgroups/{projectgroupid}:
    patch:
      summary: Updates project group data
      description: Updates project group data.
      operationId: updateProjectGroup
      x-api-path-slug: projectgroupsprojectgroupid-patch
      parameters:
      - in: body
        name: body
        description: Updated project group info
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: If-Match
        description: Project version
      - in: path
        name: projectgroupid
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Data
    delete:
      summary: Deletes a project group
      description: Deletes a project group.
      operationId: deleteProjectGroup
      x-api-path-slug: projectgroupsprojectgroupid-delete
      parameters:
      - in: query
        name: force
      - in: path
        name: projectgroupid
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
    get:
      summary: Gets project group information
      description: Gets project group information.
      operationId: getProjectGroup
      x-api-path-slug: projectgroupsprojectgroupid-get
      parameters:
      - in: path
        name: projectgroupid
        description: Project group identifier
      responses:
        200:
          description: OK
      tags:
      - Project
      - Group
      - Information
  /projectgroups:
    post:
      summary: Creates project group
      description: Creates project group.
      operationId: createProjectGroup
      x-api-path-slug: projectgroups-post
      parameters:
      - in: body
        name: body
        description: New project group data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Project
      - Group
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