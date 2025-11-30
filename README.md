# HTTP

## O que é HTTP?
```
HTTP é um protocolo que permite a obtenção de recursos, como documentos HTML. É a base de qualquer troca de dados na Web e um protocolo cliente-servidor, o que significa que as requisições são iniciadas pelo um destinário, geralmente um navegador Web.
```

## O que são requests (solicitações) e responses (respostas)?
```
Clientes e servidores trocam mensagem um com outro quando são as mensagens enviadas pelo cliente são chamadas de requests (solicitações) e mensagens enviada pelos servidores são chamadas de responses (respostas).
```

## Onde o protocolo HTTP atua?
```
O protocolo HTTP atua na camada de aplicação que é enviada pelo protocolo TCP, e essa conexão TCP e criptografada com TLS. O HTTP atua também em partes de documentos para atualizar páginas da Web sob demanda.
```

## Quais são os componentes de sistema basicos do HTTP?
```
**Cliente o Agente-usuário** -> O agente-usuário é qualquer ferramenta que age em nome do usuário. Essa função é predominante realizada pelo navegador Web. O navegador sempre é a entidade que inicia as requisições, nunca ao lado do servidor.
```

```
**O servidor de páginas Web** -> O canal de comunicação está o servidor que serve o documento requisitado pelo usuário, Um servidor se apresenta apenas como uma máquina ou também como um programa complexo que acessa outros servidores por exemplo: cache, banco de dados, servidores de e-commerce gerando assim parte do documento solicitado.
```

```
**Proxies (ou representantes)** -> As maáquinas que operam na camada de aplicação são normalmente chamados de proxies (representantes ou procuradores) podem ser transparente ou não e podem desempenhar varias funções:

.cacheamento (o cache pode ser público ou privado, como o cache dos navegadores)

.filtragem (como um scanner de antivírus, controle de acesso, etc)
balanceamento de carga (para permitir que vários servidores possam responder a diferentes requisições)

.autenticação (para controlar quem tem acesso aos recursos)
autorização (para controlar quem tem acesso a determinada informação)

.registro de informação (permite o armazenamento de informações de histórico)
```

## Aspectos básicos do HTTP
```
**HTTP é simples** -> O HTTP é simples por conta da sua questão de ler, qualquer pessoa que não entende de HTTP conseguiria ler o codigo porém até o HTTP/2.0 depois dele o codigo não dava mais para ler por conta que ficava em código binário porém o seu módulo continua o mesmo de sempre.
```

```
**HTTP é extensível** -> Desde do HTTP/1.0, foram projetados o cabeçalho fazendo assim os protocolos ficam mais fácil de projetar e estender e introduzir novas coisas.
```

```
**HTTP não tem estado, mas tem sessões** -> O HTTP é originalmente sem estado com isso entra um problema para os usuários que interagem com as páginas de forma coerente. Com isso existe o fundamento básico do HTTP que são os cookies HTTP que permite a criação de sessão em cada requisição HTTP compartilhem o mesmo contexto e o mesmo estado.
```

```
**HTTP e conexões** -> No protocolo HTTP/1.0 uma conexão TCP era aberta para cada requisição/resposta trocada trazendo assim dois problemas: lentidão e abrir uma conexão de ida e volta. Assim para resolver esses problemas o HTTP/1.1 criou um conceito de linhas de produção e conexões persistentes as TCP feitas embaixo, podem ser parcialmente controladas usando o cabeçalho HTTP Connection.
```

## O que pode ser controlado pelo HTTP?
```
 .Cache

 .Relaxamento das restrições na origem para prevenir     invasores de privacidade

 .Autenticação

 .Proxy e Tunelamento

 .Sessões usando os cookies HTTP
```

## Fluxo HTTP
```
Como o cliente quer comunicar com o servidor:
1.Abrir conexão TCP: A conexão TCP será aberta para receber e enviar alguma resposta ao cliente.

2.Enviar uma mensagem HTTP: A mensagem de HTTP eram legiveis ate o HTTP/2.0 depois disso se tornou impossivel de ler porem o HTTP continua o mesmo.
```

```
GET / HTTP/1.1
Host: developer.mozilla.org
Accept-Language: fr
```

```
3. Ele lê a resposta do servidor
```

```
HTTP/1.1 200 OK
Date: Sat, 09 Oct 2010 14:28:02 GMT
Server: Apache
Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
ETag: "51142bc1-7449-479b075b2891b"
Accept-Ranges: bytes
Content-Length: 29769
Content-Type: text/html

<!DOCTYPE html... (here comes the 29769 bytes of the requested web page)
```

```
4. Fecha a conexão HTTP e reutiliza para conexões futuras.
```

## Mensagens HTTP
```
Desde do HTTP/1.1 toda mensagem HTTP recebe um método, caminho e o protocolo da versão então fica assim:

POST -> Método  / -> caminho  HTTP/2.0 -> Protocolo da versão


Host: lucas.fertonani       -> Cabeçalho
Accept-language: fr

O método é sempre um verbo POST, GET, DELETE e PUT
O caminho sempre vai ser **http://** 
e o protocolo da versão
e o cabeçalho que são informações adicionais do servidor
```

## RESPOSTAS DADAS PELO HTTP
```
Depois disso, o HTTP dá alguma resposta (response) para o cliente e seria assim a resposta assim dada pelo HTTP:

HTTP/1.0 -> Protocolo da versão  401 -> Status do codigo Error -> Código de mensagem
headers -> Cabeçalho
```