
# organizations


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/organizations.get" %}
{% api-method-summary %}
/organizations.get
{% endapi-method-summary %}

{% api-method-description %}
Get organization by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-query-parameters %}
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
{
  "id": "Organization id",
  "name": {
    "value": "infomaker"
  },
  "wellKnownConfigUrl": {
    "value": "http://example.com/.well-known.json"
  },
  "scope": {
    "value": "openid profile email"
  },
  "clientId": {
    "value": "foobarbaz"
  },
  "responseMode": {
    "value": "query"
  },
  "validatorsTokenGroupsAttribute": {
    "value": "Groups"
  },
  "sanitizedClientSecret": {
    "value": "foobarbaz"
  },
  "whitelistCallbackUrls": {
    "value": "infomaker.io"
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

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/organizations.list" %}
{% api-method-summary %}
/organizations.list
{% endapi-method-summary %}

{% api-method-description %}
List organizations
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}
```javascript
undefined
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

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/organizations.listGroupToRoleMappings" %}
{% api-method-summary %}
/organizations.listGroupToRoleMappings
{% endapi-method-summary %}

{% api-method-description %}
List group to service role mappings by organization id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-query-parameters %}
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
undefined
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.block" %}
{% api-method-summary %}
/organizations.block
{% endapi-method-summary %}

{% api-method-description %}
Block org by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.create" %}
{% api-method-summary %}
/organizations.create
{% endapi-method-summary %}

{% api-method-description %}
Create org
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required="true" %}
Organization name
{% endapi-method-parameter %}
{% api-method-parameter name="wellKnownConfigUrl" type="string" required="true" %}
undefined
{% endapi-method-parameter %}
{% api-method-parameter name="scope" type="string" required="true" %}
OIDC scope
{% endapi-method-parameter %}
{% api-method-parameter name="clientId" type="string" required="true" %}
OIDC client ID
{% endapi-method-parameter %}
{% api-method-parameter name="responseMode" type="string" required="true" %}
OIDC response mode
{% endapi-method-parameter %}
{% api-method-parameter name="orgTokenGroupsAttribute" type="string" required="true" %}
Token groups attribute
{% endapi-method-parameter %}
{% api-method-parameter name="whitelistCallbackUrls" type="string" required="true" %}
undefined
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
  "id": "Organization id",
  "name": {
    "value": "infomaker"
  },
  "wellKnownConfigUrl": {
    "value": "http://example.com/.well-known.json"
  },
  "scope": {
    "value": "openid profile email"
  },
  "clientId": {
    "value": "foobarbaz"
  },
  "responseMode": {
    "value": "query"
  },
  "orgTokenGroupsAttribute": {
    "value": "Groups"
  },
  "whitelistCallbackUrls": {
    "value": "infomaker.io"
  },
  "sanitizedClientSecret": "null",
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.delete" %}
{% api-method-summary %}
/organizations.delete
{% endapi-method-summary %}

{% api-method-description %}
Delete org by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.logout" %}
{% api-method-summary %}
/organizations.logout
{% endapi-method-summary %}

{% api-method-description %}
Logout org by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setClientId" %}
{% api-method-summary %}
/organizations.setClientId
{% endapi-method-summary %}

{% api-method-description %}
Set organization clientId
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="clientId" type="string" required="true" %}
OIDC client ID
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
  "clientId": {
    "value": "foobarbaz"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setClientSecret" %}
{% api-method-summary %}
/organizations.setClientSecret
{% endapi-method-summary %}

{% api-method-description %}
Update org client secret
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="clientSecret" type="string" required="true" %}
OIDC client secret
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
  "sanitizedClientSecret": {
    "value": "foobarbaz"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setName" %}
{% api-method-summary %}
/organizations.setName
{% endapi-method-summary %}

{% api-method-description %}
Set organization name
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="name" type="string" required="true" %}
Organization name
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
    "value": "infomaker"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setOrgTokenGroupsAttribute" %}
{% api-method-summary %}
/organizations.setOrgTokenGroupsAttribute
{% endapi-method-summary %}

{% api-method-description %}
Set organization orgTokenGroupsAttribute
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="orgTokenGroupsAttribute" type="string" required="true" %}
Token groups attribute
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
  "orgTokenGroupsAttribute": {
    "value": "Groups"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setResponseMode" %}
{% api-method-summary %}
/organizations.setResponseMode
{% endapi-method-summary %}

{% api-method-description %}
Set organization responseMode
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="responseMode" type="string" required="true" %}
OIDC response mode
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
  "responseMode": {
    "value": "query"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setScope" %}
{% api-method-summary %}
/organizations.setScope
{% endapi-method-summary %}

{% api-method-description %}
Set organization scope
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="scope" type="string" required="true" %}
OIDC scope
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
  "scope": {
    "value": "openid profile email"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setWellKnownConfigUrl" %}
{% api-method-summary %}
/organizations.setWellKnownConfigUrl
{% endapi-method-summary %}

{% api-method-description %}
Set organization wellKnownConfigUrl
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="wellKnownConfigUrl" type="string" required="true" %}
Organization well known config url
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
  "wellKnownConfigUrl": {
    "value": "http://example.com/.well-known.json"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setWhitelistCallbackUrls" %}
{% api-method-summary %}
/organizations.setWhitelistCallbackUrls
{% endapi-method-summary %}

{% api-method-description %}
Set organization whitelist callback urls
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
{% endapi-method-parameter %}
{% api-method-parameter name="whitelistCallbackUrls" type="string" required="true" %}
Callback whitelist URL
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
  "whitelistCallbackUrls": {
    "value": "infomaker.io"
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

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.unblock" %}
{% api-method-summary %}
/organizations.unblock
{% endapi-method-summary %}

{% api-method-description %}
Unblock org by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-body-parameters %}
{% api-method-parameter name="organizationId" type="string" required="true" %}
Organization id
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
