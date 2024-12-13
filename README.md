# Manipulando Jobs do watsonx.ai através da API

## Objetivo
Este guia tem como objetivo fornecer uma visão geral de como usar Jobs no watsonx.ai de forma programática. Ao final deste guia, você entenderá como listar, criar e executar Jobs usando a API. Isso é particularmente útil para automatizar tarefas complexas e de longa duração, garantindo execução eficiente e confiável.

## Quando os Jobs são úteis?
Os Jobs assíncronos são um recurso poderoso que permite lidar com tarefas que exigem tempo de processamento significativo sem bloquear outras operações. Eles são especialmente benéficos nos seguintes cenários:
- Código complexo e de longa duração: Tarefas que envolvem cálculos complicados, processamento de um grande volume de dados ou dependem de múltiplas ativações de outros sistemas podem ser transferidas para Jobs assíncronos. Isso garante que sua aplicação principal permaneça responsiva e possa continuar a lidar com outras solicitações.
- Tarefas agendadas: Os Jobs podem ser agendados para serem executados em intervalos específicos, tornando-os ideais para tarefas recorrentes, como backups diários de dados, geração de relatórios semanais ou arquivamento mensal de dados. Essa automação garante que tarefas críticas sejam realizadas consistentemente e no prazo, sem intervenção manual.

## Execução de Jobs do watsonx.ai
O watsonx.ai suporta a execução de Jobs de forma nativa via API ou interface, fornecendo um framework flexível e robusto para gerenciar suas tarefas. Aqui está uma explicação detalhada de como funciona:
- Criação do Job: Você cria Jobs para executar ativos em várias ferramentas, como fluxos de Refinaria de Dados, fluxos do SPSS Modeler, Notebooks e scripts, dentro de um projeto. Isso permite automatizar uma ampla gama de tarefas, desde pré-processamento de dados até treinamento e avaliação de modelos.
- Propriedades do Job: Ao criar um Job, você define várias propriedades que determinam seu comportamento. Essas propriedades incluem o nome do Job, definição (o script ou fluxo a ser executado), o ambiente de execução (capacidade de processamento), agendamento (quando o Job deve ser executado) e especificações de notificação (como você deve ser notificado sobre o status do Job). Você pode escolher executar um Job imediatamente ou agendá-lo para ser executado em intervalos específicos.
- Execuções de Job: Cada vez que um Job é iniciado, uma execução de Job é criada. Essas execuções podem ser monitoradas para rastrear o progresso e o status do Job. Você pode comparar o histórico de execuções de Jobs anteriores para identificar padrões, solucionar problemas e otimizar o desempenho. Informações detalhadas sobre cada execução de Job, incluindo alterações de estado do Job e falhas do Job, podem ser visualizadas no log de execução do Job.

## O que existe nesse repositório:
Este repositório contém dois Notebooks que demonstram como usar a API do watsonx.ai para criar e executar Jobs. O primeiro Notebook, chamado [Hello World Job](/[PT-BR]%20Hello%20World%20Job.ipynb), é um exemplo simples que imprime o valor de uma variável de ambiente. O segundo Notebook, [Job Creation API](/[PT-BR]%20Job%20Creation%20APIs.ipynb), fornece um guia passo a passo sobre como autenticar na API, listar Jobs, criar um novo Job, criar uma execução de Job e recuperar o status e os logs da execução do Job. Vamos fazer tudo isso usando o primeiro notebook como exemplo.

## Requisitos:
Para executar os códigos neste repositório, você precisará:
- Ter uma conta no IBM Cloud e ter acesso ao watsonx.ai.
- Ter um projeto criado no watsonx.ai.
- Adicionar os dois notebooks ao seu projeto: 
    - [Job Creation API](/[PT-BR]%20Job%20Creation%20APIs.ipynb) - Notebook principal com as orientações
    - [Hello World Job](/[PT-BR]%20Hello%20World%20Job.ipynb) - Exemplo para criação do Job
- Ter uma API Key da IBM Cloud para autenticar na API. (Existem orientações no Notebook principal)
- Ter um token de acesso criado no seu projeto no watsonx.ai com a função de Editor. (Existem orientações no Notebook principal)