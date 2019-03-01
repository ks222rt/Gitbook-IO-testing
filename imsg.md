
# imsg-service


{% api-method method="get" host="https://admin-api.infomaker.io" path="//imsg-service/v1/callback" %}
{% api-method-summary %}
/imsg-service/v1/callback
{% endapi-method-summary %}

{% api-method-description %}
Callback from IMAS login
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="imid_token" type="string" required="undefined" %}
IM ID JWT
{% endapi-method-parameter %}
{% api-method-parameter name="serviceCallback" type="string" required="undefined" %}
Where to redirect client after login
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}
Found
{% endapi-method-response-example-description %}
```javascript
"Redirected to the service callback url"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="get" host="https://admin-api.infomaker.io" path="//imsg-service/v1/health" %}
{% api-method-summary %}
/imsg-service/v1/health
{% endapi-method-summary %}

{% api-method-description %}
Health status
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}
```javascript
{
  "inGrace": false,
  "stateChecksum": "A checksum string"
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}
```javascript
{
  "inGrace": false,
  "stateChecksum": "No checksum string"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="get" host="https://admin-api.infomaker.io" path="//imsg-service/v1/token-is-set" %}
{% api-method-summary %}
/imsg-service/v1/token-is-set
{% endapi-method-summary %}

{% api-method-description %}
Check if request contains IMID token
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}
```javascript
{
  "msg": "ok"
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Unauthorized
{% endapi-method-response-example-description %}
```javascript
"errors.auth.MissingToken"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="get" host="https://admin-api.infomaker.io" path="//imsg-service/v1/org/{org}/login" %}
{% api-method-summary %}
/imsg-service/v1/org/{org}/login
{% endapi-method-summary %}

{% api-method-description %}
Trigger login flow
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="callback" type="string" required="true" %}
Where to redirect client after login
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}
Found
{% endapi-method-response-example-description %}
```javascript
"Redirected after login"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="post" host="https://admin-api.infomaker.io" path="//imsg-service/v1/logout" %}
{% api-method-summary %}
/imsg-service/v1/logout
{% endapi-method-summary %}

{% api-method-description %}
Log out
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="callback" type="string" required="undefined" %}
Where to redirect client after logout
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
  "msg": "You are logged out"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="post" host="https://admin-api.infomaker.io" path="//imsg-service/v1/unit" %}
{% api-method-summary %}
/imsg-service/v1/unit
{% endapi-method-summary %}

{% api-method-description %}
Set preferred unit
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="unit" type="string" required="null" %}
Preferred unit
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
  "msg": "Unit set"
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Forbidden
{% endapi-method-response-example-description %}
```javascript
"errors.auth.Forbidden"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
