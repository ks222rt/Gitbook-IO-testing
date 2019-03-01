# Units

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/units.get" %}
{% api-method-summary %}
/units.get
{% endapi-method-summary %}

{% api-method-description %}
Get unit by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="unitId" type="string" required="true" %}
UUIDv4
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
  "id": "Unit id",
  "organizationId": "Organization id",
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

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/units.list" %}
{% api-method-summary %}
/units.list
{% endapi-method-summary %}

{% api-method-description %}
List units
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
    "id": "Unit id",
    "organizationId": "Organization id",
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/units.create" %}
{% api-method-summary %}
/units.create
{% endapi-method-summary %}

{% api-method-description %}
Create unit
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required="true" %}
Unit name
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
  "id": "Unit id",
  "organizationId": "Organization id",
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/units.delete" %}
{% api-method-summary %}
/units.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete unit by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="unitId" type="string" required="true" %}
UUIDv4
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/units.setDescription" %}
{% api-method-summary %}
/units.setDescription
{% endapi-method-summary %}

{% api-method-description %}
Set unit description by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="unitId" type="string" required="true" %}
UUIDv4
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/units.setName" %}
{% api-method-summary %}
/units.setName
{% endapi-method-summary %}

{% api-method-description %}
Set unit name by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="unitId" type="string" required="true" %}
UUIDv4
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required="true" %}
Unit name
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

