## Configurando o Serverless para trabalhar com proxy

No Windows 10, abra o arquivo `C:\Program Files\nodejs\node_modules\serverless\lib\plugins\aws\provider\awsProvider.js`

Procure por...

     // Use HTTPS Proxy (Optional)
        const proxy = process.env.proxy
          || process.env.HTTP_PROXY
          || process.env.http_proxy
          || process.env.HTTPS_PROXY
          || process.env.https_proxy;

Acrescente na última linha o seu proxy...

     // Use HTTPS Proxy (Optional)
        const proxy = process.env.proxy
          || process.env.HTTP_PROXY
          || process.env.http_proxy
          || process.env.HTTPS_PROXY
          || process.env.https_proxy
          || 'http://your-awesome-proxy:port';

Agora, para desabilitar foi treta, veja este [gist](https://gist.github.com/flaviomicheletti/baf818cd2bafafc68e604c8929ad14a2)


Fonte

https://github.com/serverless/serverless/issues/3256#issuecomment-469214220
