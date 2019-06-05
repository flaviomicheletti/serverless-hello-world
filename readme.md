# Serverless - Hello world

https://serverless.com/


### Instalação

     # Step 1. Install serverless globally
     $ npm install serverless -g

Não precisa configurar variáveis de ambiente.

Instalei em um Windows 10.

__Testando__

    serverless

### Hello World

     # Step 2. Create a serverless function
     $ serverless create --template hello-world

### Deploy

Para fazer o deploy, precisa instalar o (AWS CLI)[https://docs.aws.amazon.com/cli/].

Precisa criar um arquivo chamado `seu-usuario/.aws/credentials` conforme a (documentação)[https://docs.aws.amazon.com/pt_br/cli/latest/userguide/cli-configure-files.html].


Configure o [proxy](configurando-o-proxy.md) caso precise.

Efetue...

     # Step 3. deploy to cloud provider
     $ serverless deploy

### Teste final

   # Your function is deployed!
   $ http://xyz.amazonaws.com/hello-world

A minha ficou [aqui](https://wavwtms5c8.execute-api.us-east-1.amazonaws.com/dev/hello-world) 


### Curso free na Udemy

https://www.udemy.com/nanosservicos-serverless-orientados-a-eventos/