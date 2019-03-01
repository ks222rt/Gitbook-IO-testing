# Roles

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/roles.get" %}
{% api-method-summary %}
/roles.get
{% endapi-method-summary %}

{% api-method-description %}
Get role by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "id": "Role id",
  "serviceId": "Service id",
  "name": {
    "value": "user"
  },
  "description": "Description of speicific part xxx"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/roles.list" %}
{% api-method-summary %}
/roles.list
{% endapi-method-summary %}

{% api-method-description %}
List roles
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
[
  {
    "id": "Role id",
    "serviceId": "Service id",
    "name": {
      "value": "user"
    },
    "description": "Description of speicific part xxx"
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/roles.listMappedGroups" %}
{% api-method-summary %}
/roles.listMappedGroups
{% endapi-method-summary %}

{% api-method-description %}
List all mapped groups by role id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
[
  {
    "roleId": "Role id",
    "unitId": "Unit id",
    "organizationId": "Organization id",
    "group": {
      "value": "Auth team"
    }
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.assignToGroup" %}
{% api-method-summary %}
/roles.assignToGroup
{% endapi-method-summary %}

{% api-method-description %}
Add group to role mapping
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="string" required="true" %}
Organization group name
{% endapi-method-parameter %}

{% api-method-parameter name="unitId" type="string" required="true" %}
Unit id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "roleId": "Role id",
  "organizationId": "Organization id",
  "group": {
    "value": "Auth team"
  },
  "unitId": "Unit id"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.create" %}
{% api-method-summary %}
/roles.create
{% endapi-method-summary %}

{% api-method-description %}
Create role
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required="true" %}
Service role name
{% endapi-method-parameter %}

{% api-method-parameter name="parentRoleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required="true" %}
Description of speicific part xxx
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "id": "Role id",
  "serviceId": "Service id",
  "name": {
    "value": "user"
  },
  "description": "Description of speicific part xxx",
  "permissions": []
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.delete" %}
{% api-method-summary %}
/roles.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete role by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
No Content
{% endapi-method-response-example-description %}

```javascript
""
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.mapPermission" %}
{% api-method-summary %}
/roles.mapPermission
{% endapi-method-summary %}

{% api-method-description %}
Map permissision to role
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="permissionId" type="string" required="true" %}
Permission id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "roleId": "Role id",
  "permissionId": "Permission id"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.setDescription" %}
{% api-method-summary %}
/roles.setDescription
{% endapi-method-summary %}

{% api-method-description %}
Set role description by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required="true" %}
Description of speicific part xxx
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "description": "Description of speicific part xxx"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.setName" %}
{% api-method-summary %}
/roles.setName
{% endapi-method-summary %}

{% api-method-description %}
Set role name by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required="true" %}
Service role name
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "name": {
    "value": "user"
  }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.setParentRole" %}
{% api-method-summary %}
/roles.setParentRole
{% endapi-method-summary %}

{% api-method-description %}
Set role parent role by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="parentRoleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}

```javascript
{
  "parentRoleId": "Role id"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.unassignFromGroup" %}
{% api-method-summary %}
/roles.unassignFromGroup
{% endapi-method-summary %}

{% api-method-description %}
Delete group to role mapping
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="string" required="true" %}
Organization group name
{% endapi-method-parameter %}

{% api-method-parameter name="unitId" type="string" required="true" %}
Unit id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
No Content
{% endapi-method-response-example-description %}

```javascript
""
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/roles.unmapPermission" %}
{% api-method-summary %}
/roles.unmapPermission
{% endapi-method-summary %}

{% api-method-description %}
Unmap permission from role
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="roleId" type="string" required="true" %}
Role id
{% endapi-method-parameter %}

{% api-method-parameter name="permissionId" type="string" required="true" %}
Permission id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
No Content
{% endapi-method-response-example-description %}

```javascript
""
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Bad Request
{% endapi-method-response-example-description %}

```javascript
"errors.api.BadRequestError"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
"errors.api.InternalServerError"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

