# MurilloAPI

### Apresentação do Projeto

Você foi contratado para desenvolver um sistema de gerenciamento de tarefas utilizando Laravel. O sistema deve fornecer uma API para realizar operações básicas de criação, leitura, atualização e exclusão (CRUD) de tarefas.

Requisitos:

A API deve ser capaz de lidar com as seguintes operações:

- Listar todas as tarefas
- Obter detalhes de uma tarefa específica
- Criar uma nova tarefa
- Atualizar os dados de uma tarefa existente
- Excluir uma tarefa

Cada tarefa deve conter as seguintes informações:

- Título (obrigatório)
- Descrição (obrigatório)
- Status (concluída ou não concluída)
A API deve seguir as práticas recomendadas para design de APIs RESTful e utilizar os métodos HTTP adequados para cada operação.

A resposta da API deve estar no formato JSON.

Implemente validações adequadas para garantir que os dados fornecidos estejam corretos antes de executar as operações no banco de dados.

Teste a API utilizando uma ferramenta de testes de API, como o Postman ou o Insomnia.

Documente a API, incluindo informações sobre as rotas disponíveis, os parâmetros necessários e as respostas esperadas.

Dicas:

Use os recursos do Laravel, como rotas, controladores e modelos, para facilitar o desenvolvimento da API.
Utilize o sistema de migração do Laravel para criar a tabela de tarefas no banco de dados.
Crie um controlador dedicado para manipular as operações relacionadas às tarefas.
Utilize o Eloquent ORM para interagir com o banco de dados.
Lembre-se de adicionar as validações necessárias nos controladores para garantir a integridade dos dados.
Bônus (opcional):

Implemente recursos de paginação e ordenação para a listagem de tarefas.
Adicione autenticação na API para garantir que apenas usuários autenticados possam acessar as operações de criação, atualização e exclusão de tarefas.
Implemente recursos de busca para permitir que os usuários pesquisem tarefas por título, descrição ou status.
Observação: Esta atividade foca na criação da API, portanto, não é necessário incluir interface HTML. O objetivo é praticar a criação de endpoints e a manipulação dos dados utilizando o Laravel.

Baixando as Dependências de um Projeto Laravel
Ao clonar um projeto Laravel de um repositório Git, é necessário baixar as dependências do projeto para garantir que todas as bibliotecas e pacotes necessários estejam instalados corretamente. Para isso, siga as etapas abaixo:

Certifique-se de ter o PHP instalado em sua máquina. Recomenda-se usar a versão suportada pelo projeto Laravel. Você pode verificar a versão suportada no arquivo composer.json do projeto.

Abra um terminal e navegue até o diretório raiz do projeto Laravel clonado.

Execute o comando composer install para baixar as dependências do projeto. O Composer irá ler o arquivo composer.json do projeto e instalar todas as dependências listadas.

Aguarde até que o Composer conclua o processo de instalação das dependências. Isso pode levar alguns minutos, dependendo da velocidade da sua conexão com a internet.

Após a conclusão, o Composer terá criado um diretório chamado vendor no diretório raiz do projeto. Esse diretório contém todas as dependências do projeto Laravel.

Se houver arquivos de ambiente (.env) no projeto, copie o arquivo .env.example para .env e configure as variáveis de ambiente necessárias, como informações do banco de dados e chaves de acesso.

Agora você está pronto para executar o projeto Laravel. Use um servidor web local (por exemplo, o servidor embutido do PHP ou um servidor como o Apache ou Nginx) e acesse o projeto em seu navegador.

Com essas etapas, você poderá baixar e configurar corretamente as dependências do projeto Laravel ao cloná-lo de um repositório Git.

Lembre-se de consultar a documentação oficial do Laravel para obter mais informações sobre a configuração e execução de projetos Laravel.



### Listar todas as tarefas


GET /tasks


Retorna uma lista de todas as tarefas existentes.

#### Respostas

- *200 OK*: Requisição bem-sucedida. A resposta contém um array de objetos representando as tarefas.

### Criar uma nova tarefa


POST /tasks


Cria uma nova tarefa com base nos dados fornecidos.

#### Parâmetros

- *title* (obrigatório): O título da tarefa (até 50 caracteres).
- *description* (obrigatório): A descrição da tarefa (até 250 caracteres).
- *status* (obrigatório): O status da tarefa (valores permitidos: "completed" ou "not completed").

#### Respostas

- *200 OK*: Requisição bem-sucedida. A resposta contém os dados da tarefa criada.

### Obter detalhes de uma tarefa específica


GET /tasks/{id}


Retorna os detalhes da tarefa com o ID especificado.

#### Parâmetros

- *id* (obrigatório): O ID da tarefa a ser recuperada.

#### Respostas

- *200 OK*: Requisição bem-sucedida. A resposta contém os dados da tarefa solicitada.

### Atualizar os dados de uma tarefa existente


PUT /tasks/{task}


Atualiza os dados da tarefa com base nos novos dados fornecidos.

#### Parâmetros

- *task* (obrigatório): O ID ou o objeto JSON da tarefa a ser atualizada.
- *title* (opcional): O novo título da tarefa (até 50 caracteres).
- *description* (opcional): A nova descrição da tarefa (até 250 caracteres).
- *status* (opcional): O novo status da tarefa (valores permitidos: "completed" ou "not completed").

#### Respostas

- *200 OK*: Requisição bem-sucedida. A resposta contém os dados da tarefa atualizada.

### Excluir uma tarefa


DELETE /tasks/{task}


Exclui a tarefa com o ID ou objeto JSON especificado.

#### Parâmetros

- *task* (obrigatório): O ID ou o objeto JSON da tarefa a ser excluída.

#### Respostas

- *200 OK*: Requisição bem-sucedida. A tarefa foi excluída com sucesso.

- *405 Method Not Allowed*: Método não permitido. A tarefa especificada não existe.



Link do PostMain em Fase de teste: https://youtu.be/jTY3gu_l3K4



Documentação finalizada 
