## TokenUtils{#TokenUtils}

Module with helper functions for the Tokens.


### extractServiceTokenFromRequest(request) {#extractServiceTokenFromRequest}⇒ <code>Object</code>

Extracts and decodes a service token from a raw request

**Returns**: <code>Object</code> - The service token  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getSubject(request) {#getSubject}⇒ <code>String</code>

Get the subject from the service token

**Returns**: <code>String</code> - organization - The subject identifier set on the service token  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getOrganization(request) {#getOrganization}⇒ <code>String</code>

Get the subject's organization

**Returns**: <code>String</code> - organization - The organization the subject belongs to  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getUnits(request) {#getUnits}⇒ <code>Array.&lt;String&gt;</code>

Get the subject's mapped units

**Returns**: <code>Array.&lt;String&gt;</code> - units - An array of all units the subject belongs to  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getSelectedUnit(request) {#getSelectedUnit}⇒ <code>null</code> \| <code>String</code>

Get the subject's selected unit

**Returns**: <code>null</code> \| <code>String</code> - unit - The subject's selected unit, null if no unit selected  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getOrgPermissions(request) {#getOrgPermissions}⇒ <code>Array.&lt;String&gt;</code>

Get the subject's organization permissions

Organization permissions are located under permissions.org

**Returns**: <code>Array.&lt;String&gt;</code> - } permissions - The subject's org permissions  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getUnitPermissions(request, unit) {#getUnitPermissions}⇒ <code>Array.&lt;String&gt;</code>

Get the subject's permissions for the specified unit

Unit permissions are located under permissions.units[unit]

**Returns**: <code>Array.&lt;String&gt;</code> - permissions - The subject's permissions for the specified unit  

| Param | Type | Description |
| --- | --- | --- |
| request | <code>http.IncomingMessage</code> | **Required** -  |
| unit | <code>String</code> | **Required** - The unit permissions should be checked in |


### isServiceAdmin(request) {#isServiceAdmin}⇒ <code>Boolean</code>

Checks if a token belogs to an admin for the service

**Returns**: <code>Boolean</code> - isServiceAdmin - True if the token belongs to an admin for the service  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


### getUserinfo(request) {#getUserinfo}⇒ <code>Object</code>

Get the subject's userinfo

**Returns**: <code>Object</code> - userinfo - The userinfo object set on the subject  

| Param | Type |
| --- | --- |
| request | <code>http.IncomingMessage</code> | 


