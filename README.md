# MurilloAPI

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
