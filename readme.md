# Serverless - Hello world

Site oficial https://serverless.com/

Documentação https://serverless.com/framework/docs/providers/aws/guide/intro/

Você vai precisar...

+ ter uma conta no AWS
+ ter o nodejs instalado
+ ter instalado o AWS CLI

Eu explico isso no caminho...


### Instalando o serverless

Antes do serverless, vem a instalação do __nodejs__.

Estando o node devidamente instalado em sua máquina, execute...

    // Step 1. Install serverless globally
    $ npm install serverless -g

Não precisa configurar variáveis de ambiente.

Instalei em um Windows 10.

__Teste sua instalação__

Abra um terminal e digite

     serverless


### Criando o "Hello World"

     // Step 2. Create a serverless function
     $ serverless create --template hello-world

Este repositório é o resultado do comando acima, quero dizer que já executei o comando.
Então, caso queira fazer um clone deste repositório e vê-lo funcionando, experimente...

     // clonando...
     git clone https://github.com/flaviomicheletti/serverless-hello-world.git

	// instalando
     cd serverless-hello-world
     serverless install --url https://github.com/flaviomicheletti/serverless-hello-world



### Deployando

Para fazer o deploy, precisa instalar o [AWS CLI](https://docs.aws.amazon.com/cli/).

Precisa criar um arquivo chamado `seu-usuario/.aws/credentials` conforme a [documentação](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/cli-configure-files.html).

Configure o [proxy](configurando-o-proxy.md) caso precise.

Efetue...

    // Step 3. deploy to cloud provider
     $ serverless deploy

Se tudo der certo, você verá algo semelhanta a...

     $ serverless deploy
     Serverless: Packaging service...
     Serverless: Excluding development dependencies...
     Serverless: Creating Stack...
     Serverless: Checking Stack create progress...
     .....
     Serverless: Stack create finished...
     Serverless: Uploading CloudFormation file to S3...
     Serverless: Uploading artifacts...
     Serverless: Uploading service serverless-hello-world.zip file to S3 (1.7 KB)...
     Serverless: Validating template...
     Serverless: Updating Stack...
     Serverless: Checking Stack update progress...
     .................................
     Serverless: Stack update finished...
     Service Information
     service: serverless-hello-world
     stage: dev
     region: us-east-1
     stack: serverless-hello-world-dev
     resources: 11
     api keys:
     None
     endpoints:
     GET - https://gelefrwtzl.execute-api.us-east-1.amazonaws.com/dev/hello-world
     functions:
     helloWorld: serverless-hello-world-dev-helloWorld
     layers:
     None


### Teste final

     // Your function is deployed!
     $ http://xyz.amazonaws.com/hello-world

Onde `xyz` deve ser atualizado pela sua informação.

Quando eu não tiro do ar, a minha fica disponível aqui https://gelefrwtzl.execute-api.us-east-1.amazonaws.com/dev/hello-world


### Curso free na Udemy

Onde eu aprendi tudo isso ?

https://www.udemy.com/nanosservicos-serverless-orientados-a-eventos/
