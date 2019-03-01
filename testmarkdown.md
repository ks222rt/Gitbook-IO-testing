# TestMarkdown

* [ExpressMiddleware](testmarkdown.md#ExpressMiddleware)
  * [ServiceAuthorizationMiddleware](testmarkdown.md#ServiceAuthorizationMiddleware)
    * * [authorize\(authParams\)](testmarkdown.md#authorize)
    * * [errorHandler\(\[err\], req, res, next\)](testmarkdown.md#errorHandler)
  * [FullAuthorizationParameters](testmarkdown.md#FullAuthorizationParameters)
  * [AccessRule](testmarkdown.md#AccessRule)
  * [AuthorizationMode](testmarkdown.md#AuthorizationMode)

## ExpressMiddleware <a id="ExpressMiddleware"></a>

### ServiceAuthorizationMiddleware <a id="ServiceAuthorizationMiddleware"></a>

ServiceAuthorizationMiddleware

#### new ServiceAuthorizationMiddleware\(options\) <a id="ServiceAuthorizationMiddleware"></a>

| Param | Type | Description |
| :--- | :--- | :--- |
| options | `Object` | **Required** - |
| options.serviceTokenSignSecret | `string` | **Required** - Secret to validate token signature against |

#### authorize\(authParams\) <a id="authorize"></a>

Extract and authorize token using the provided auth params

| Param | Type | Description |
| :--- | :--- | :--- |
| authParams | `FullAuthorizationParameters` \| `AuthorizationMode` | **Required** - Authorization parameters to pass to |

#### errorHandler\(\[err\], req, res, next\) <a id="errorHandler"></a>

Error handler for errors thrown by ServiceAuthorizationMiddleware

Will handle telling IMSG to redirect unauthorized requests, but will pass on any other errors to next\(\)

| Param | Type | Description |
| :--- | :--- | :--- |
| err | `Object` | Express err |
| req | `Object` | **Required** - Express req |
| res | `Object` | **Required** - Express res |
| next | `function` | **Required** - Express next |

### FullAuthorizationParameters - Typedef definition <a id="FullAuthorizationParameters"></a>

The type definition of the full auhtorization object with all parameters.  
Passed to the authorize function.

**Properties**

| Name | Type | Description |
| :--- | :--- | :--- |
| onPreAuth | `function` | Function to run before authorize is called |
| org | `string` \| `function` \| `Boolean` | **Required** - Organiztion to authorize against |
| accessRules | `Array.<AccessRule>` | Optional access rules to authorize against |
| suppressLoginTrigger | `Boolean` | If true, do not redirect failed authorization to login |

### AccessRule - Typedef definition <a id="AccessRule"></a>

The type definition of the access rule.  
Passed to the authorize function within the  object as a list of access rules.

All properties are optional, but at least one must exist

**Properties**

| Name | Type | Description |
| :--- | :--- | :--- |
| unit | `string` \| `function` | Unit that should match token |
| permission | `string` \| `function` | Permission that should match token |
| sub | `string` \| `function` | Subject that should match token |

### AuthorizationMode - Typedef definition <a id="AuthorizationMode"></a>

Type defintion of the authorization mode.  
SERVICE\_ADMIN\_ENDPOINT - Authorization validates if you are a service admin and have a valid token. Either accessed or thrown out.  
OPEN\_ENDPOINT - Authorization validates if you have a valid token and lets you through to the open endpoint. Either accessed or thrown out.

Either SERVICE\_ADMIN\_ENDPOINT or OPEN\_ENDPOINT

