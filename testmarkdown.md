
<div id="contentMenu"></div>

* [ExpressMiddleware](#ExpressMiddleware)
    * [ServiceAuthorizationMiddleware](#ServiceAuthorizationMiddleware)
        * 
            * [authorize(authParams)](#authorize)
        * 
            * [errorHandler([err], req, res, next)](#errorHandler)
    * [FullAuthorizationParameters](#FullAuthorizationParameters)
    * [AccessRule](#AccessRule)
    * [AuthorizationMode](#AuthorizationMode)

## ExpressMiddleware{#ExpressMiddleware}



### ServiceAuthorizationMiddleware{#ServiceAuthorizationMiddleware}

ServiceAuthorizationMiddleware



#### new ServiceAuthorizationMiddleware(options) {#ServiceAuthorizationMiddleware}


| Param | Type | Description |
| --- | --- | --- |
| options | <code>Object</code> | **Required** -  |
| options.serviceTokenSignSecret | <code>string</code> | **Required** - Secret to validate token signature against |



#### authorize(authParams) {#authorize}

Extract and authorize token using the provided auth params


| Param | Type | Description |
| --- | --- | --- |
| authParams | <code>FullAuthorizationParameters</code> &#124; <code>AuthorizationMode</code> | **Required** - Authorization parameters to pass to |



#### errorHandler([err], req, res, next) {#errorHandler}

Error handler for errors thrown by ServiceAuthorizationMiddleware

Will handle telling IMSG to redirect unauthorized requests, but will pass on
any other errors to next()


| Param | Type | Description |
| --- | --- | --- |
| err | <code>Object</code> | Express err |
| req | <code>Object</code> | **Required** - Express req |
| res | <code>Object</code> | **Required** - Express res |
| next | <code>function</code> | **Required** - Express next |


---

### FullAuthorizationParameters - Typedef definition{#FullAuthorizationParameters}

The type definition of the full auhtorization object with all parameters.  
Passed to the authorize function.


**Properties**

| Name | Type | Description |
| --- | --- | --- |
| onPreAuth | <code>function</code> | Function to run before authorize is called |
| org | <code>string</code> &#124; <code>function</code> &#124; <code>Boolean</code> | **Required** - Organiztion to authorize against |
| accessRules | <code>Array.&lt;AccessRule&gt;</code> | Optional access rules to authorize against |
| suppressLoginTrigger | <code>Boolean</code> | If true, do not redirect failed authorization to login |

---

### AccessRule - Typedef definition{#AccessRule}

The type definition of the access rule.  
Passed to the authorize function within the <FullAuthorizationParameter> object as a list of access rules.  

All properties are optional, but at least one must exist


**Properties**

| Name | Type | Description |
| --- | --- | --- |
| unit | <code>string</code> &#124; <code>function</code> | Unit that should match token |
| permission | <code>string</code> &#124; <code>function</code> | Permission that should match token |
| sub | <code>string</code> &#124; <code>function</code> | Subject that should match token |

---

### AuthorizationMode - Typedef definition{#AuthorizationMode}

Type defintion of the authorization mode.  
SERVICE_ADMIN_ENDPOINT - Authorization validates if you are a service admin and have a valid token. Either accessed or thrown out.  
OPEN_ENDPOINT - Authorization validates if you have a valid token and lets you through to the open endpoint. Either accessed or thrown out.  

Either SERVICE_ADMIN_ENDPOINT or OPEN_ENDPOINT


