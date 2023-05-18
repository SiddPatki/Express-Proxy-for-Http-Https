Steps:

1. 
    ```
    npm install
    ```

2. In your Wifi Settings, go to Details -> Proxies 

    ->Turn ON HTTP : ```Server = 127.0.0.1 Port = 8084```

    ->Turn ON HTTPS : ```Server = 127.0.0.1 Port = 8084```

3. 
    ```
    nodemon index.js
    ```


4. In your WebdriverIO project:

    ``` 
    npm install global-agent --save-dev 
    
    export GLOBAL_AGENT_HTTP_PROXY=http://127.0.0.1:8084
    ```

    Go to base.conf.js and add the following 2 lines at the top.
    ```
    const { bootstrap } = require('global-agent');
    bootstrap();
    ```
Here is the updated repo:

https://github.com/SiddPatki/WDIO-BROWSERSTACK-VIA-PROXY

Follow this guide: 

https://webdriver.io/docs/proxy/#proxy-between-driver-and-test