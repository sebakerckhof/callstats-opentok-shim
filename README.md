## Callstat OpenTok Shim

Track stats of your OpenTok/TokBox sessions using Callstats.

### Instructions

Just include the `dist/callstats-opentok-shim.min.js` file in your page after the Callstats script. (RequireJS support coming soon).

```html
<script src="https://api.callstats.io/static/callstats.min.js"></script>
<script src="/YOUR_STATIC_PATH/callstats-opentok-shim.min.js"></script>
```

And initialize it like shown below:

```javascript
CallstatsOpenTok.initialize(opts);
```

Supported options:

| Param. Name    | Required | Description                                                    | 
| -------------- |  :----:  | -------------------------------------------------------------- |
| `AppId`        | Yes      | Callstats AppId                                                |
| `AppSecret`    | Yes      | Callstats AppSecret                                            |
| `SessionId`    | Yes      | TokBox's Session Identifier                                    | 
| `Id`           | No       | Current conn. identifier, if not provided a uuid4 is generated |

#### Example

```javascript
CallstatsOpenTok.initialize({
  AppId: 834738451,
  AppSecret: 'sOTjsJEfwPUGW4SRJI4BhbprGJ3lfO6Kp+:ixCX1P9mzNThlsW+YNLlb=',
  SessionId: '1_eiTh54cMjNx4FNk-JkT15IXNTGtNnh8W03m0RwYTMxUMNMDyhU2gzMxezMXjaF0Mj0E-UH4'
});
```

### Building the project

Building is not required to use the shim, since there's a production ready version and it respective sourcemap in the `dist` directory, however, building the shim is fairly simple

After installing dependencies with `npm install`, run `grunt` in the project directory. 
This will generate new files in the `dist` directory.