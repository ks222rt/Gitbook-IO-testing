# Services

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/subjects.get" %}
{% api-method-summary %}
/subjects.get
{% endapi-method-summary %}

{% api-method-description %}
Get subject by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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
  "id": "Subject id",
  "organizationId": "Organization id",
  "organizationSubject": {
    "value": "user@infomaker.se"
  },
  "blocked": false
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

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/subjects.list" %}
{% api-method-summary %}
/subjects.list
{% endapi-method-summary %}

{% api-method-description %}
List subject by id
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
    "id": "Subject id",
    "organizationId": "Organization id",
    "organizationSubject": {
      "value": "user@infomaker.se"
    },
    "blocked": false
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.block" %}
{% api-method-summary %}
/subjects.block
{% endapi-method-summary %}

{% api-method-description %}
Login sub
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.create" %}
{% api-method-summary %}
/subjects.create
{% endapi-method-summary %}

{% api-method-description %}
Create sub
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}

{% api-method-parameter name="organizationSubject" type="string" required="true" %}
Organization subject
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
  "id": "Subject id",
  "organizationId": "Organization id",
  "organizationSubject": {
    "value": "user@infomaker.se"
  },
  "blocked": false
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.delete" %}
{% api-method-summary %}
/subjects.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete subject by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.login" %}
{% api-method-summary %}
/subjects.login
{% endapi-method-summary %}

{% api-method-description %}
Login sub
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.logout" %}
{% api-method-summary %}
/subjects.logout
{% endapi-method-summary %}

{% api-method-description %}
Login sub
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.setOrganizationSubject" %}
{% api-method-summary %}
/subjects.setOrganizationSubject
{% endapi-method-summary %}

{% api-method-description %}
Set organization subject by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
{% endapi-method-parameter %}

{% api-method-parameter name="organizationSubject" type="string" required="true" %}
Organization subject
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
  "organizationSubject": {
    "value": "user@infomaker.se"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/subjects.unblock" %}
{% api-method-summary %}
/subjects.unblock
{% endapi-method-summary %}

{% api-method-description %}
Login sub
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="subjectId" type="string" required="true" %}
Subject id
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

