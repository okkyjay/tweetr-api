# Endpoints


## Handles user signup




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/signup"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

let body = {
    "name": "ea",
    "username": "officia",
    "email": "vitae",
    "password": "reiciendis"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: JSON.stringify(body),
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/signup"  \
    -d '{"name":"ea","username":"officia","email":"vitae","password":"reiciendis"}'


```


> Example response (400):

```json
{"status":"error","message":"There was a problem creating the user, please try again later."}
```
<div id="execution-results-POST-signup" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-signup"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-signup"></code></pre>
</div>
<div id="execution-error-POST-signup" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-signup"></code></pre>
</div>

<form id="form-POST-signup" data-method="POST" data-path="/signup" data-authed="0" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json"}' onsubmit="event.preventDefault(); executeTryOut('POST-signup', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-signup" onclick="tryItOut('POST-signup');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-signup" onclick="cancelTryOut('POST-signup');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-signup" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/signup</b></code>
</p>
<h4 class="fancy-heading-panel"><b>Body Parameters</b></h4>

<p>
<b><code>name</code></b>&nbsp;&nbsp;<small>string</small> 
    <i>optional</i>
<input type="text" name="name" data-endpoint="POST-signup" data-component="body" hidden>
<br>
</p>
<p>
<b><code>username</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="username" data-endpoint="POST-signup" data-component="body" required hidden>
<br>
</p>
<p>
<b><code>email</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="email" data-endpoint="POST-signup" data-component="body" required hidden>
<br>
</p>
<p>
<b><code>password</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="password" data-endpoint="POST-signup" data-component="body" required hidden>
<br>
</p>
</form>

## Handles user authentication




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

let body = {
    "email": "molestiae",
    "password": "quasi"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: JSON.stringify(body),
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/login"  \
    -d '{"email":"molestiae","password":"quasi"}'


```


> Example response (200):

```json
{
   "status": "success",
   "data": "YOUR_TOKEN"
 }
```
<div id="execution-results-POST-login" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-login"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-login"></code></pre>
</div>
<div id="execution-error-POST-login" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-login"></code></pre>
</div>

<form id="form-POST-login" data-method="POST" data-path="/login" data-authed="0" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json"}' onsubmit="event.preventDefault(); executeTryOut('POST-login', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-login" onclick="tryItOut('POST-login');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-login" onclick="cancelTryOut('POST-login');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-login" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/login</b></code>
</p>
<h4 class="fancy-heading-panel"><b>Body Parameters</b></h4>

<p>
<b><code>email</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="email" data-endpoint="POST-login" data-component="body" required hidden>
<br>
</p>
<p>
<b><code>password</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="password" data-endpoint="POST-login" data-component="body" required hidden>
<br>
</p>
</form>

## Get details of the currently authenticated user

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/account/me"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer Vga81Pb6f4Eh6ek35vZcaDd",
};


fetch(url, {
    method: "GET",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X GET \
    -G "http://127.0.0.1:3333/account/me" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-GET-account-me" hidden>
    <blockquote>Received response<span id="execution-response-status-GET-account-me"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-GET-account-me"></code></pre>
</div>
<div id="execution-error-GET-account-me" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-GET-account-me"></code></pre>
</div>

<form id="form-GET-account-me" data-method="GET" data-path="/account/me" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer Vga81Pb6f4Eh6ek35vZcaDd"}' onsubmit="event.preventDefault(); executeTryOut('GET-account-me', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-GET-account-me" onclick="tryItOut('GET-account-me');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-GET-account-me" onclick="cancelTryOut('GET-account-me');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-GET-account-me" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-green">GET</small>
 <b><code>/account/me</b></code>
</p>
<p>
    <label id="auth-GET-account-me" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="GET-account-me" data-component="header"></label>
</p>
</form>

## Update user profile

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/account/update_profile"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer 4ebV1kDg3hvdPa56Zc8E6af",
};


fetch(url, {
    method: "PUT",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X PUT \
    "http://127.0.0.1:3333/account/update_profile" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-PUT-account-update_profile" hidden>
    <blockquote>Received response<span id="execution-response-status-PUT-account-update_profile"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-PUT-account-update_profile"></code></pre>
</div>
<div id="execution-error-PUT-account-update_profile" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-PUT-account-update_profile"></code></pre>
</div>

<form id="form-PUT-account-update_profile" data-method="PUT" data-path="/account/update_profile" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer 4ebV1kDg3hvdPa56Zc8E6af"}' onsubmit="event.preventDefault(); executeTryOut('PUT-account-update_profile', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-PUT-account-update_profile" onclick="tryItOut('PUT-account-update_profile');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-PUT-account-update_profile" onclick="cancelTryOut('PUT-account-update_profile');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-PUT-account-update_profile" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-darkblue">PUT</small>
 <b><code>/account/update_profile</b></code>
</p>
<p>
    <label id="auth-PUT-account-update_profile" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="PUT-account-update_profile" data-component="header"></label>
</p>
</form>

## Change user password

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/account/change_password"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer c4bDVaZ8dgk13E65Paefhv6",
};


fetch(url, {
    method: "PUT",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X PUT \
    "http://127.0.0.1:3333/account/change_password" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-PUT-account-change_password" hidden>
    <blockquote>Received response<span id="execution-response-status-PUT-account-change_password"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-PUT-account-change_password"></code></pre>
</div>
<div id="execution-error-PUT-account-change_password" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-PUT-account-change_password"></code></pre>
</div>

<form id="form-PUT-account-change_password" data-method="PUT" data-path="/account/change_password" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer c4bDVaZ8dgk13E65Paefhv6"}' onsubmit="event.preventDefault(); executeTryOut('PUT-account-change_password', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-PUT-account-change_password" onclick="tryItOut('PUT-account-change_password');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-PUT-account-change_password" onclick="cancelTryOut('PUT-account-change_password');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-PUT-account-change_password" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-darkblue">PUT</small>
 <b><code>/account/change_password</b></code>
</p>
<p>
    <label id="auth-PUT-account-change_password" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="PUT-account-change_password" data-component="header"></label>
</p>
</form>

## Fetch user and followers tweets

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/users/timeline"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer ka4c56861Dde3gfahbEPVZv",
};


fetch(url, {
    method: "GET",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X GET \
    -G "http://127.0.0.1:3333/users/timeline" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-GET-users-timeline" hidden>
    <blockquote>Received response<span id="execution-response-status-GET-users-timeline"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-GET-users-timeline"></code></pre>
</div>
<div id="execution-error-GET-users-timeline" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-GET-users-timeline"></code></pre>
</div>

<form id="form-GET-users-timeline" data-method="GET" data-path="/users/timeline" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer ka4c56861Dde3gfahbEPVZv"}' onsubmit="event.preventDefault(); executeTryOut('GET-users-timeline', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-GET-users-timeline" onclick="tryItOut('GET-users-timeline');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-GET-users-timeline" onclick="cancelTryOut('GET-users-timeline');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-GET-users-timeline" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-green">GET</small>
 <b><code>/users/timeline</b></code>
</p>
<p>
    <label id="auth-GET-users-timeline" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="GET-users-timeline" data-component="header"></label>
</p>
</form>

## Users to follow

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/users/users_to_follow"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer h6kb3ada5DeV41f68EcPZvg",
};


fetch(url, {
    method: "GET",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X GET \
    -G "http://127.0.0.1:3333/users/users_to_follow" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-GET-users-users_to_follow" hidden>
    <blockquote>Received response<span id="execution-response-status-GET-users-users_to_follow"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-GET-users-users_to_follow"></code></pre>
</div>
<div id="execution-error-GET-users-users_to_follow" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-GET-users-users_to_follow"></code></pre>
</div>

<form id="form-GET-users-users_to_follow" data-method="GET" data-path="/users/users_to_follow" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer h6kb3ada5DeV41f68EcPZvg"}' onsubmit="event.preventDefault(); executeTryOut('GET-users-users_to_follow', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-GET-users-users_to_follow" onclick="tryItOut('GET-users-users_to_follow');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-GET-users-users_to_follow" onclick="cancelTryOut('GET-users-users_to_follow');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-GET-users-users_to_follow" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-green">GET</small>
 <b><code>/users/users_to_follow</b></code>
</p>
<p>
    <label id="auth-GET-users-users_to_follow" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="GET-users-users_to_follow" data-component="header"></label>
</p>
</form>

## Follow a user

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/users/follow"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer veDVfhPkE8caba16d365gZ4",
};


fetch(url, {
    method: "POST",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/users/follow" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-POST-users-follow" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-users-follow"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-users-follow"></code></pre>
</div>
<div id="execution-error-POST-users-follow" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-users-follow"></code></pre>
</div>

<form id="form-POST-users-follow" data-method="POST" data-path="/users/follow" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer veDVfhPkE8caba16d365gZ4"}' onsubmit="event.preventDefault(); executeTryOut('POST-users-follow', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-users-follow" onclick="tryItOut('POST-users-follow');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-users-follow" onclick="cancelTryOut('POST-users-follow');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-users-follow" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/users/follow</b></code>
</p>
<p>
    <label id="auth-POST-users-follow" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="POST-users-follow" data-component="header"></label>
</p>
</form>

## Unfollow a user

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/users/unfollow/58251"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer 4k6vbcVa38hgaDeP6fdE51Z",
};


fetch(url, {
    method: "DELETE",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X DELETE \
    "http://127.0.0.1:3333/users/unfollow/58251" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-DELETE-users-unfollow--id" hidden>
    <blockquote>Received response<span id="execution-response-status-DELETE-users-unfollow--id"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-DELETE-users-unfollow--id"></code></pre>
</div>
<div id="execution-error-DELETE-users-unfollow--id" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-DELETE-users-unfollow--id"></code></pre>
</div>

<form id="form-DELETE-users-unfollow--id" data-method="DELETE" data-path="/users/unfollow/:id" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer 4k6vbcVa38hgaDeP6fdE51Z"}' onsubmit="event.preventDefault(); executeTryOut('DELETE-users-unfollow--id', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-DELETE-users-unfollow--id" onclick="tryItOut('DELETE-users-unfollow--id');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-DELETE-users-unfollow--id" onclick="cancelTryOut('DELETE-users-unfollow--id');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-DELETE-users-unfollow--id" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-red">DELETE</small>
 <b><code>/users/unfollow/:id</b></code>
</p>
<p>
    <label id="auth-DELETE-users-unfollow--id" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="DELETE-users-unfollow--id" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>id</code></b>&nbsp;&nbsp;<small>number</small> 
<input type="number" name="id" data-endpoint="DELETE-users-unfollow--id" data-component="url" required hidden>
<br>
</p>
</form>

## Post a tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/tweet"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer 686fEaa4PZgehdvDc53bk1V",
};


fetch(url, {
    method: "POST",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/tweet" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-POST-tweet" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-tweet"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-tweet"></code></pre>
</div>
<div id="execution-error-POST-tweet" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-tweet"></code></pre>
</div>

<form id="form-POST-tweet" data-method="POST" data-path="/tweet" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer 686fEaa4PZgehdvDc53bk1V"}' onsubmit="event.preventDefault(); executeTryOut('POST-tweet', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-tweet" onclick="tryItOut('POST-tweet');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-tweet" onclick="cancelTryOut('POST-tweet');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-tweet" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/tweet</b></code>
</p>
<p>
    <label id="auth-POST-tweet" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="POST-tweet" data-component="header"></label>
</p>
</form>

## Fetch a tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/tweets/77714"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer 8a5dvePk63DaV6hZbE4gcf1",
};


fetch(url, {
    method: "GET",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X GET \
    -G "http://127.0.0.1:3333/tweets/77714" 

```


> Example response (404):

```json
{"status":"error","message":"Tweet not found"}
```
<div id="execution-results-GET-tweets--id" hidden>
    <blockquote>Received response<span id="execution-response-status-GET-tweets--id"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-GET-tweets--id"></code></pre>
</div>
<div id="execution-error-GET-tweets--id" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-GET-tweets--id"></code></pre>
</div>

<form id="form-GET-tweets--id" data-method="GET" data-path="/tweets/:id" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer 8a5dvePk63DaV6hZbE4gcf1"}' onsubmit="event.preventDefault(); executeTryOut('GET-tweets--id', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-GET-tweets--id" onclick="tryItOut('GET-tweets--id');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-GET-tweets--id" onclick="cancelTryOut('GET-tweets--id');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-GET-tweets--id" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-green">GET</small>
 <b><code>/tweets/:id</b></code>
</p>
<p>
    <label id="auth-GET-tweets--id" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="GET-tweets--id" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>id</code></b>&nbsp;&nbsp;<small>number</small> 
<input type="number" name="id" data-endpoint="GET-tweets--id" data-component="url" required hidden>
<br>
</p>
</form>

## Reply a tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/tweets/reply/6181"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer 6f8adbZPcvk3ha16Eg4DeV5",
};


fetch(url, {
    method: "POST",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/tweets/reply/6181" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-POST-tweets-reply--id" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-tweets-reply--id"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-tweets-reply--id"></code></pre>
</div>
<div id="execution-error-POST-tweets-reply--id" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-tweets-reply--id"></code></pre>
</div>

<form id="form-POST-tweets-reply--id" data-method="POST" data-path="/tweets/reply/:id" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer 6f8adbZPcvk3ha16Eg4DeV5"}' onsubmit="event.preventDefault(); executeTryOut('POST-tweets-reply--id', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-tweets-reply--id" onclick="tryItOut('POST-tweets-reply--id');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-tweets-reply--id" onclick="cancelTryOut('POST-tweets-reply--id');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-tweets-reply--id" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/tweets/reply/:id</b></code>
</p>
<p>
    <label id="auth-POST-tweets-reply--id" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="POST-tweets-reply--id" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>id</code></b>&nbsp;&nbsp;<small>number</small> 
<input type="number" name="id" data-endpoint="POST-tweets-reply--id" data-component="url" required hidden>
<br>
</p>
</form>

## Delete a tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/tweets/destroy/84883"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer ZcaEe68a5dvhP1Df3V4g6kb",
};


fetch(url, {
    method: "DELETE",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X DELETE \
    "http://127.0.0.1:3333/tweets/destroy/84883" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-DELETE-tweets-destroy--id" hidden>
    <blockquote>Received response<span id="execution-response-status-DELETE-tweets-destroy--id"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-DELETE-tweets-destroy--id"></code></pre>
</div>
<div id="execution-error-DELETE-tweets-destroy--id" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-DELETE-tweets-destroy--id"></code></pre>
</div>

<form id="form-DELETE-tweets-destroy--id" data-method="DELETE" data-path="/tweets/destroy/:id" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer ZcaEe68a5dvhP1Df3V4g6kb"}' onsubmit="event.preventDefault(); executeTryOut('DELETE-tweets-destroy--id', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-DELETE-tweets-destroy--id" onclick="tryItOut('DELETE-tweets-destroy--id');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-DELETE-tweets-destroy--id" onclick="cancelTryOut('DELETE-tweets-destroy--id');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-DELETE-tweets-destroy--id" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-red">DELETE</small>
 <b><code>/tweets/destroy/:id</b></code>
</p>
<p>
    <label id="auth-DELETE-tweets-destroy--id" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="DELETE-tweets-destroy--id" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>id</code></b>&nbsp;&nbsp;<small>number</small> 
<input type="number" name="id" data-endpoint="DELETE-tweets-destroy--id" data-component="url" required hidden>
<br>
</p>
</form>

## Favorite a specified tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/favorites/create"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer VvDegh8abP1Zc6a3f6kd45E",
};


fetch(url, {
    method: "POST",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X POST \
    "http://127.0.0.1:3333/favorites/create" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":284,"column":7,"context":{"start":279,"pre":"      const { parsed, raw } = await this._parseJSON(request.request)\n\n      request.body = parsed\n      request._raw = raw\n","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is Url encoded form, so parse it and move forward"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-POST-favorites-create" hidden>
    <blockquote>Received response<span id="execution-response-status-POST-favorites-create"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-POST-favorites-create"></code></pre>
</div>
<div id="execution-error-POST-favorites-create" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-POST-favorites-create"></code></pre>
</div>

<form id="form-POST-favorites-create" data-method="POST" data-path="/favorites/create" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer VvDegh8abP1Zc6a3f6kd45E"}' onsubmit="event.preventDefault(); executeTryOut('POST-favorites-create', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-POST-favorites-create" onclick="tryItOut('POST-favorites-create');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-POST-favorites-create" onclick="cancelTryOut('POST-favorites-create');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-POST-favorites-create" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-black">POST</small>
 <b><code>/favorites/create</b></code>
</p>
<p>
    <label id="auth-POST-favorites-create" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="POST-favorites-create" data-component="header"></label>
</p>
</form>

## Unfavorite a specified tweet

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/favorites/destroy/54467"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer kEdPb6843h5fDaeVa6Zvgc1",
};


fetch(url, {
    method: "DELETE",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X DELETE \
    "http://127.0.0.1:3333/favorites/destroy/54467" 

```


> Example response (401):

```json
{"error":{"message":"E_INVALID_JWT_TOKEN: jwt malformed","name":"InvalidJwtToken","status":401,"frames":[{"file":"node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Exceptions\\index.js","method":"Function.invoke","line":222,"column":12,"context":{"start":217,"pre":" *\n * @class InvalidJwtToken\n */\nclass InvalidJwtToken extends GE.LogicalException {\n  static invoke (message) {","line":"    return new this(message || 'The Jwt token is invalid', 401, 'E_INVALID_JWT_TOKEN')","post":"  }\n}\n\n/**\n * This exception is raised when jwt refresh token is"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Schemes\\Jwt.js","method":"JwtScheme.check","line":402,"column":32,"context":{"start":397,"pre":"      this.jwtPayload = await this._verifyToken(token)\n    } catch ({ name, message }) {\n      if (name === 'TokenExpiredError') {\n        throw CE.ExpiredJwtToken.invoke()\n      }","line":"      throw CE.InvalidJwtToken.invoke(message)","post":"    }\n\n    this.user = await this._serializerInstance.findById(this.jwtPayload.uid)\n\n    /**"},"isModule":true,"isNative":false,"isApp":false},{"file":"internal/process/task_queues.js","filePath":"internal/process/task_queues.js","method":"processTicksAndRejections","line":93,"column":5,"context":{},"isModule":false,"isNative":true,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth._authenticate","line":67,"column":9,"context":{"start":62,"pre":"     * via anyone\n     */\n    for (const scheme of schemes) {\n      try {\n        const authenticator = auth.authenticator(scheme)","line":"        await authenticator.check()","post":"\n        debug('authenticated using %s scheme', scheme)\n\n        /**\n         * Swapping the main authentication instance with the one using which user"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\auth\\src\\Middleware\\Auth.js","method":"async Auth.handle","line":109,"column":5,"context":{"start":104,"pre":"   *                             If no scheme is defined, then default scheme from config is used.\n   *\n   * @return {void}\n   */\n  async handle ({ auth, view }, next, schemes) {","line":"    await this._authenticate(auth, schemes)","post":"\n    /**\n     * For compatibility with the old API\n     */\n    auth.current = auth.authenticatorInstance"},"isModule":true,"isNative":false,"isApp":false},{"file":"node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","filePath":"C:\\Users\\shalvah\\Projects\\Temp\\tweetr-api\\node_modules\\@adonisjs\\bodyparser\\src\\BodyParser\\index.js","method":"async BodyParser.handle","line":242,"column":7,"context":{"start":237,"pre":"    /**\n     * Don't bother when request does not have body\n     */\n    if (!request.hasBody()) {\n      debug('skipping body parsing, since request body is empty')","line":"      await next()","post":"      return\n    }\n\n    /**\n     * Body is multipart/form-data and autoProcess is set to"},"isModule":true,"isNative":false,"isApp":false}]}}
```
<div id="execution-results-DELETE-favorites-destroy--id" hidden>
    <blockquote>Received response<span id="execution-response-status-DELETE-favorites-destroy--id"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-DELETE-favorites-destroy--id"></code></pre>
</div>
<div id="execution-error-DELETE-favorites-destroy--id" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-DELETE-favorites-destroy--id"></code></pre>
</div>

<form id="form-DELETE-favorites-destroy--id" data-method="DELETE" data-path="/favorites/destroy/:id" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer kEdPb6843h5fDaeVa6Zvgc1"}' onsubmit="event.preventDefault(); executeTryOut('DELETE-favorites-destroy--id', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-DELETE-favorites-destroy--id" onclick="tryItOut('DELETE-favorites-destroy--id');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-DELETE-favorites-destroy--id" onclick="cancelTryOut('DELETE-favorites-destroy--id');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-DELETE-favorites-destroy--id" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-red">DELETE</small>
 <b><code>/favorites/destroy/:id</b></code>
</p>
<p>
    <label id="auth-DELETE-favorites-destroy--id" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="DELETE-favorites-destroy--id" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>id</code></b>&nbsp;&nbsp;<small>number</small> 
<input type="number" name="id" data-endpoint="DELETE-favorites-destroy--id" data-component="url" required hidden>
<br>
</p>
</form>

## Show user profile

<small class="badge badge-darkred">requires authentication</small>




> Example request:

```javascript
const url = new URL(
    "http://127.0.0.1:3333/eaque"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer Z3aPcfEDde4a815g6Vv6bhk",
};


fetch(url, {
    method: "GET",
    headers: headers,
})
.then(response => response.json())
.then(json => console.log(json));
```

```bash
curl -X GET \
    -G "http://127.0.0.1:3333/eaque" 

```


> Example response (404):

```json
{"status":"error","message":"User not found"}
```
<div id="execution-results-GET--username" hidden>
    <blockquote>Received response<span id="execution-response-status-GET--username"></span>:</blockquote>
    <pre class="json"><code id="execution-response-content-GET--username"></code></pre>
</div>
<div id="execution-error-GET--username" hidden>
    <blockquote>Request failed with error:</blockquote>
    <pre><code id="execution-error-message-GET--username"></code></pre>
</div>

<form id="form-GET--username" data-method="GET" data-path="/:username" data-authed="1" data-hasfiles="0" data-headers='{"Content-Type":"application/json","Accept":"application/json","Authorization":"Bearer Z3aPcfEDde4a815g6Vv6bhk"}' onsubmit="event.preventDefault(); executeTryOut('GET--username', this);">
<h3>
    Request
    <button type="button" style="background-color: #8fbcd4; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-tryout-GET--username" onclick="tryItOut('GET--username');">Try it out ⚡</button>
    <button type="button" style="background-color: #c97a7e; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-canceltryout-GET--username" onclick="cancelTryOut('GET--username');" hidden>Cancel</button>&nbsp;&nbsp;
    <button type="submit" style="background-color: #6ac174; padding: 5px 10px; border-radius 5px; border-width: thin;" id="btn-executetryout-GET--username" hidden>Send Request 💥</button>
</h3>
<p>
<small class="badge badge-green">GET</small>
 <b><code>/:username</b></code>
</p>
<p>
    <label id="auth-GET--username" hidden>Authorization header: <b><code>Bearer </code></b><input type="text" name="Authorization" data-prefix="Bearer " data-endpoint="GET--username" data-component="header"></label>
</p>
<h4 class="fancy-heading-panel"><b>URL Parameters</b></h4>
<p>
<b><code>username</code></b>&nbsp;&nbsp;<small>string</small> 
<input type="text" name="username" data-endpoint="GET--username" data-component="url" required hidden>
<br>
</p>
</form>


