# workflows-auto-AWS-Step-Functions
É um serviço de orquestração visual de workflows que ajuda a criar aplicações distribuídas, automatizar processos, microserviços  e criar pipelines de dados e machine learning (ML).
Por exemplo, você pode processar um único arquivo JSON ou CSV que contém grandes quantidades de dados. Ou você pode processar um grande conjunto de objetos do Amazon S3.

1. ⚙️ Workflow Básico 
Objetivo: Orquestrar uma única função AWS Lambda.

Crie uma função Lambda simples (ex: que retorne uma mensagem JSON de sucesso).
Crie uma Máquina de Estado que chame essa função (Task State).
Execute e observe o fluxo no console visual.

2. 🚦 Workflow com Fluxo de Controle (Choice e Wait)
Objetivo: Adicionar lógica condicional e pausas.

Modifique a Lambda inicial para que a saída inclua um campo (ex: "status": "APPROVED" ou "status": "REJECTED").

Adicione um Choice State que use esse campo para decidir o próximo passo.

Se for "APPROVED", use um Wait State para simular uma espera (ex: 5 segundos) antes de finalizar.

Se for "REJECTED", vá diretamente para o Fail State.

3. 🔄 Workflow de Processamento Paralelo 
Objetivo: Executar tarefas em paralelo para economizar tempo ou processar uma coleção de itens.

Parallel State: Crie uma Máquina de Estado que execute duas ou três funções Lambda diferentes (simulando, por exemplo, envio de notificação e atualização de banco de dados) ao mesmo tempo.

