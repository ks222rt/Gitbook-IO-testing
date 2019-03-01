
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
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://admin-api.infomaker.io" path="/v1/organizations.list" %}
{% api-method-summary %}
/organizations.list
{% endapi-method-summary %}

{% api-method-description %}
List organizations
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% endapi-method-spec %}
{% endapi-method %}

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
{% endapi-method-spec %}
{% endapi-method %}

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
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.create" %}
{% api-method-summary %}
/organizations.create
{% endapi-method-summary %}

{% api-method-description %}
Create org
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="whitelistCallbackUrls" type="string" required="true" %}
undefined
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

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
{% endapi-method-spec %}
{% endapi-method %}

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
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setClientId" %}
{% api-method-summary %}
/organizations.setClientId
{% endapi-method-summary %}

{% api-method-description %}
Set organization clientId
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="clientId" type="string" required="true" %}
OIDC client ID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setClientSecret" %}
{% api-method-summary %}
/organizations.setClientSecret
{% endapi-method-summary %}

{% api-method-description %}
Update org client secret
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="clientSecret" type="string" required="true" %}
OIDC client secret
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setName" %}
{% api-method-summary %}
/organizations.setName
{% endapi-method-summary %}

{% api-method-description %}
Set organization name
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="name" type="string" required="true" %}
Organization name
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setOrgTokenGroupsAttribute" %}
{% api-method-summary %}
/organizations.setOrgTokenGroupsAttribute
{% endapi-method-summary %}

{% api-method-description %}
Set organization orgTokenGroupsAttribute
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="orgTokenGroupsAttribute" type="string" required="true" %}
Token groups attribute
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setResponseMode" %}
{% api-method-summary %}
/organizations.setResponseMode
{% endapi-method-summary %}

{% api-method-description %}
Set organization responseMode
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="responseMode" type="string" required="true" %}
OIDC response mode
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setScope" %}
{% api-method-summary %}
/organizations.setScope
{% endapi-method-summary %}

{% api-method-description %}
Set organization scope
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="scope" type="string" required="true" %}
OIDC scope
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setWellKnownConfigUrl" %}
{% api-method-summary %}
/organizations.setWellKnownConfigUrl
{% endapi-method-summary %}

{% api-method-description %}
Set organization wellKnownConfigUrl
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="wellKnownConfigUrl" type="string" required="true" %}
Organization well known config url
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://admin-api.infomaker.io" path="/v1/organizations.setWhitelistCallbackUrls" %}
{% api-method-summary %}
/organizations.setWhitelistCallbackUrls
{% endapi-method-summary %}

{% api-method-description %}
Set organization whitelist callback urls
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-parameter name="whitelistCallbackUrls" type="string" required="true" %}
Callback whitelist URL
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% endapi-method-spec %}
{% endapi-method %}

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
{% endapi-method-spec %}
{% endapi-method %}
