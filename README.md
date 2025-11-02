# Desafio de Projeto 2: Workflows Automatizados com AWS Step Functions

Repositório criado para a entrega do Desafio de Projeto 2 do bootcamp Santander Code Girls, focado em orquestração de fluxos de trabalho (workflows) com o serviço **AWS Step Functions**.

O objetivo deste laboratório foi entender como o Step Functions atua como um "gerente" que garante a ordem e a lógica de execução de múltiplos serviços.
## Meu Aprendizado e Execução

O principal insight adquirido é sobre o conceito de **orquestração** e a diferença para a **simples chamada** de funções.

1.  **O que é Step Functions:** É uma máquina de estados (State Machine) que permite **visualizar** e **gerenciar** todo o fluxo de uma aplicação. Ele garante que um passo só comece se o anterior for concluído com sucesso.

2.  **Passos Práticos Executados:**
    * **Criação das Tarefas:** Foram criadas duas Funções AWS Lambda (`IniciaProcesso` e `FinalizaProcesso`) que serviram como as "tarefas" a serem executadas no fluxo.
    * **Criação do Workflow:** Usando o **Workflow Studio**, o fluxo de trabalho foi definido com dois estados: `Iniciar` (chamando a Lambda 1) e `Finalizar` (chamando a Lambda 2).
    * **Teste:** O fluxo de trabalho foi iniciado e concluído com sucesso (status `Succeeded`), provando que o Step Functions conseguiu gerenciar a transição entre as duas funções Lambda.

3.  **Conceito Chave:** O Step Functions separa o código (que está no Lambda) da lógica de negócios (que está no Step Functions). Isso torna a manutenção muito mais fácil.

---
## Limpeza de Recursos

Para evitar custos desnecessários, todos os recursos utilizados no laboratório foram removidos após a conclusão do teste: as duas Funções Lambda e a State Machine (máquina de estado) no Step Functions foram excluídas, juntamente com a Role de execução criada automaticamente.
