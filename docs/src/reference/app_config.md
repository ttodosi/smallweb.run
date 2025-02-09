# App Configuration Reference

The smallweb configuration can be defined in a `smallweb.json[c]` file at the root of the project. This config file is optional, and sensible defaults are used when it is not present.

## Available Fields

### `entrypoint`

The `entrypoint` field defines the file to serve. If this field is not provided, the app will look for a `main.[js,ts,jsx,tsx]` file in the root directory.

### `root`

The `root` field defines the root directory of the app. If this field is not provided, the app will use the app directory as the root directory.

### `private`

If the `private` field is set to `true`, the app will ask for your admin username and password before serving the app using basic auth.

### `privateRoutes`

If you only want to protect a subset of routes, you can use the `privateRoutes` field. This field is an array of routes that require authentication.

```json
{
  "privateRoutes": [
    "/private",
    "/admin/*"
  ]
}
```

### `publicRoutes`

If you want to make a subset of routes public, you can use the `publicRoutes` field. This field is an array of routes that do not require authentication.

```json
{
  "private": true,
  "publicRoutes": [
    "/public/*",
  ]
}
```
