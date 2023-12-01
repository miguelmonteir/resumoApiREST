#resumo sobre Api Rest e a implementação RESTFul além dos verbos http e http status code.

#Api REST e RESTFul

#Uma API RESTful é um conjunto de regras e ferramentas que permite a comunicação entre sistemas de forma consistente. Seguindo os princípios do REST, utiliza métodos HTTP como GET, POST, PUT e DELETE para operar em recursos através de URLs definidas. Sua característica fundamental é a ausência de estado, tornando cada requisição independente e autocontida, o que possibilita alta escalabilidade. Para criar uma API assim, é crucial projetar endpoints claros, oferecer respostas consistentes em formatos como JSON ou XML, e providenciar documentação detalhada e exemplos para facilitar o uso por parte dos desenvolvedores. Em resumo, uma API RESTful é uma interface de comunicação entre sistemas que segue os princípios do REST, sendo consistente, escalável e de fácil utilização para integrar aplicações e trocar dados de forma padronizada e eficiente.




#Diferenças entre REST e RESTFul

#REST é um estilo arquitetural que define princípios para serviços web, incluindo recursos, URLs únicas para identificar recursos, operações HTTP (GET, POST, PUT, DELETE), uso de hypermedia (HATEOAS) e a ideia de ser stateless, sem manter estado entre requisições.

Por outro lado, "RESTful" descreve uma implementação ou serviço que adere aos princípios do REST. Em suma, algo é chamado de RESTful quando segue as diretrizes e práticas definidas pelo REST, incluindo métodos HTTP adequados, URLs bem definidas e a ausência de estado na comunicação entre cliente e servidor




#HTTP verbs

#DELETE: Remove um recurso específico conforme identificado pela URL.

PATCH: Usado para aplicar modificações parciais em um recurso. Envia dados para atualizar parcialmente um recurso, em vez de enviar a representação completa do recurso.

OPTIONS: Pergunta ao servidor quais métodos HTTP são permitidos para um recurso. É útil para checar as permissões de acesso antes de enviar uma solicitação.

HEAD: Similar ao GET, mas solicita apenas os headers (cabeçalhos) da resposta, sem o corpo (payload) da resposta. É útil para obter informações de cabeçalho de um recurso sem solicitar toda a sua representação.

TRACE: Utilizado para diagnosticar a conexão, retorna a requisição de volta ao cliente, geralmente para fins de depuração.

GET: Usado para solicitar dados de um recurso específico. Não deve ter efeito colateral no servidor, ou seja, deve ser uma operação segura e idempotente, retornando apenas os dados do recurso solicitado.

POST: Utilizado para enviar dados para um recurso a fim de criar ou atualizar sub-recursos. Geralmente é usado para criar novos recursos, aceitando entidades com dados a serem processados pelo recurso identificado pela URL.

PUT: Serve para atualizar um recurso específico, geralmente especificado pela URL. Ele envia a representação atualizada do recurso, e se o recurso não existir, pode criar um novo recurso com o conteúdo enviado.




#HTTP Status Code

#Os códigos de status HTTP são indicadores numéricos fornecidos em respostas de requisições feitas a servidores web. Eles fornecem informações sobre o estado da requisição e são divididos em cinco categorias principais:

1xx - Informacional: Indica que a requisição foi recebida e está em processo.

2xx - Sucesso: Indica que a requisição foi recebida, compreendida e aceita com sucesso.

200 OK: Requisição foi bem-sucedida.
201 Created: Recurso foi criado com sucesso.
204 No Content: Requisição foi bem-sucedida, mas não há conteúdo a ser retornado.
3xx - Redirecionamento: Indica que é necessário realizar mais ações para completar a requisição.

301 Moved Permanently: Recurso foi movido permanentemente para uma nova URL.
302 Found: Recurso foi temporariamente movido para uma nova URL.
4xx - Erro do Cliente: Indica que ocorreu um erro na requisição devido a informações fornecidas pelo cliente.

400 Bad Request: Requisição inválida.
401 Unauthorized: Requer autenticação para acessar o recurso.
404 Not Found: Recurso não encontrado.
5xx - Erro do Servidor: Indica que o servidor encontrou um erro ao processar a requisição.

500 Internal Server Error: Erro interno no servidor.
503 Service Unavailable: Servidor indisponível, geralmente temporariamente.
Esses códigos são cruciais para entender o resultado de uma requisição e podem ser usados para depurar e resolver problemas em aplicações web, fornecendo informações sobre o status da requisição feita pelo cliente e a resposta do servidor.