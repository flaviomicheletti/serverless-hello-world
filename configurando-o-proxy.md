## Configurando o Serverless para trablhar com proxy

No Windows 10, abra o arquivo `C:\Program Files\nodejs\node_modules\serverless\lib\plugins\aws\provider\awsProvider.js`

Procure por...

     // Use HTTPS Proxy (Optional)
        const proxy = process.env.proxy
          || process.env.HTTP_PROXY
          || process.env.http_proxy
          || process.env.HTTPS_PROXY
          || process.env.https_proxy
          || 'http://your-awesome-proxy:port';

... e altere para o seu proxy.

Fonte

https://github.com/serverless/serverless/issues/3256#issuecomment-469214220
