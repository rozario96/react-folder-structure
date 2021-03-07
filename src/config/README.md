# Config Files

In React, all UI components can be separated and hence are the building blocks for the whole app. In some cases, a developer might want to manage a static global variable across different components. Ideally, this variable would be a constant that could store data such as the app URL, server URL, theme colors, etc.

<u>1. Using a JSON file</u>
```
    "SERVER_URL": "https://example.com/api",
    "THEME_COLORS": {
        "PRIMARY": "#007BFF"
    }
```

Just like a component, the JSON file can be loaded using the import statement.

```import configData from "./config.json";```

And then the data can be used as any other JavaScript object. For example, ```configData.SERVER_URL``` will give the server URL specified in the config.json file.

<u>2. Using .env file</u>
A .env file creates environment variables that work similarly to variables declared in local JavaScript files but are accessible globally. An environment variable is read-only. That means, it cannot be changed dynamically in JavaScript files.

To declare environment variables, a .env file must be created in the root directory of a React project. Note that the environment variables in React must be prefixed with ```REACT_APP_```, otherwise React will ignore the variable during bundling.

```
REACT_APP_SERVER_URL: https://example.com/api
REACT_APP_CLIENT_ID: 109HX6754
```

Now these variables can be directly accessed using the ```process.env``` global object, with adding any import statements.

```const SERVER_URL = process.env.REACT_APP_SERVER_URL;```
