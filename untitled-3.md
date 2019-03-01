
# services


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/services.get" %}
{% api-method-summary %}
/services.get
{% endapi-method-summary %}

{% api-method-description %}
Get service by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
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
  "id": "Service id",
  "name": {
    "value": "dashboard"
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


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/services.list" %}
{% api-method-summary %}
/services.list
{% endapi-method-summary %}

{% api-method-description %}
List services
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
    "id": "Service id",
    "name": {
      "value": "dashboard"
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/services.create" %}
{% api-method-summary %}
/services.create
{% endapi-method-summary %}

{% api-method-description %}
Create service
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required="true" %}
Infomaker service name
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
  "id": "Service id",
  "name": {
    "value": "dashboard"
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/services.delete" %}
{% api-method-summary %}
/services.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete service by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/services.setDescription" %}
{% api-method-summary %}
/services.setDescription
{% endapi-method-summary %}

{% api-method-description %}
Set service description by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
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


{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/services.setName" %}
{% api-method-summary %}
/services.setName
{% endapi-method-summary %}

{% api-method-description %}
Set service name by id
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="serviceId" type="string" required="true" %}
Service id
{% endapi-method-parameter %}
{% api-method-parameter name="name" type="string" required="true" %}
Infomaker service name
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
    "value": "dashboard"
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
