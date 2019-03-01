
# health


{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/health" %}
{% api-method-summary %}
/health
{% endapi-method-summary %}

{% api-method-description %}
Health
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful
{% endapi-method-response-example-description %}
```javascript
{
  "inGrace": "True or False, if the application is in grace."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
