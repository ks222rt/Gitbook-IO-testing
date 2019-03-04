
# permissions


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/permissions.get" %}
{% api-method-summary %}
/permissions.get
{% endapi-method-summary %}

{% api-method-description %}
Get permission by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="permissionId" type="string" required="true" %}
Permission id
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
  "id": "Permission id",
  "serviceId": "Service id",
  "name": {
    "value": "plugin/getAvailable"
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


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/permissions.list" %}
{% api-method-summary %}
/permissions.list
{% endapi-method-summary %}

{% api-method-description %}
List permissions
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}
```javascript
[
  {
    "id": "Permission id",
    "serviceId": "Service id",
    "name": {
      "value": "plugin/getAvailable"
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/permissions.create" %}
{% api-method-summary %}
/permissions.create
{% endapi-method-summary %}

{% api-method-description %}
Create permission
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
{% endapi-method-parameter %}
{% api-method-parameter name="name" type="string" required="true" %}
Service permission name
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
  "id": "Permission id",
  "serviceId": {
    "value": "dashboard"
  },
  "name": {
    "value": "plugin/getAvailable"
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/permissions.delete" %}
{% api-method-summary %}
/permissions.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete permission by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
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
{}
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/permissions.setDescription" %}
{% api-method-summary %}
/permissions.setDescription
{% endapi-method-summary %}

{% api-method-description %}
Set permission description by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="permissionId" type="string" required="true" %}
Permission id
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/permissions.setName" %}
{% api-method-summary %}
/permissions.setName
{% endapi-method-summary %}

{% api-method-description %}
Set permission name by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="permissionId" type="string" required="true" %}
Permission id
{% endapi-method-parameter %}
{% api-method-parameter name="name" type="string" required="true" %}
Service permission name
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
    "value": "plugin/getAvailable"
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

