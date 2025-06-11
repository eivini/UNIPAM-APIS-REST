# UNIPAM-APIS-REST
# InfoWeek ApiDay

REST

um acronimo para Representational Sate Transfer (Transferencia de Estado Representativo)

A transferência de dados de uma maneira figurativa, representativa e de maneira didatica.

A transferência de dados, geralmente, é realizada usando protocolo HTTP

O Rest delimita obrigações para nessas transferência de dados

Resource seria então: uma entidade ou um objeto.

Request/Response

### NECESSIDADES (Constraints) para ser RestFul

_Uniform Interface_: Manter uma uniformidade, ou uma constancia, e ou padrão para a construção desta interface. A nossa API tem que ser coerente com quem vai consumi-la. Usar somente uma linguagem de comunicação (JSON) e não várias ao mesmo tempo. Sempre enviar respostas aos clientes;

_Cliente server_: Separação do cliente e do armazenamento de dados (servidor), dessa forma, poder ter portabilidade entre os clientes como react-native (mobile) ou por exemplo react (web)

_Stateless_: Cada requisição que o cliente faz para o servidor, deverá conter as informações necessárias para o servidor entender e responder (Reponse) e a Requisição (Request). Exemplo: A sessão do usuário deverá ser enviada para todas as requisição, e o servidor não pode lembrar que o cliente foi autenticado na requisição anterior. No nosso portal por exemplo, temos por padrão usar tokens para as comunicações.

_Cacheable_: As respostas para uma requisição, deverão ser explicitas ao dizer se aquela requisição, pode ou não ser cacheada pelo cliente.

_Layered System_: O cliente acessa a um endpoint, sem precisar saber da complexidade, de quais passos estão sendo necessários para o servidor responder a requisição.

_Code on demanda (optional)_: Da a possibilidade da nossa aplicação (API) pegar códigos, com o javascript, e executar no cliente.

## RestFul

RestFul é a aplicação de todos os padrões REST

## BOAS PRATICAS

- utilizar verbos HTTP para nossas requisições
- utilizar plural ou singular na criação de endpoints? (Isso importa?)
- Não deixe barra final no seu endpoint (/Clinte/)
<!-- Cliente/filho -->
- Nunca deixe o cliente sem resposta

## VERBOS HTTP

- GET: Receber dados de um Resource
- POST: Enviar dados ou info para serem processadas por um Resource
- PUT: Atualizar dados de um Resource:
- DELETE: Deletar um Resource

## STATUS DA RESPOSTAS (REPONSE)

- 1XX: Informação
- 2XX: Sucesso
- 200: OK
    - 201: CREATED
    - 204: Não tem conteudo PUT POST DELETE
- 3XX: Redirection
- 4XX: Cliente Error
    - 400: Bad Request
    - 404: Not Found!
- 5XX: Server Error
    - 500: Internal Server Error

1 - API com /clientes para listar todos e /clientes/1 para detalhes - CERTO
2 - API que usa URLs como '/getUser' ou '/createUser' - ERRADO PORQUE deve ser enxuto
3 - API que guarda estado da sessão no servidor - ERRADO
