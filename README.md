Criando um Assistente de Delivery com AWS Step Functions e Bedrock

O que foi aprendido

Este projeto foi uma experiência prática para explorar o uso de AWS Step Functions e Bedrock, combinando serviços de orquestração e IA para criar um Assistente de Delivery. Aqui, desenvolvi habilidades em engenharia de prompts, integração de serviços AWS e boas práticas de desenvolvimento para soluções baseadas em nuvem.

Pré-Requisitos

Antes de iniciar, é necessário:

Conhecimento básico de AWS: familiaridade com serviços como IAM, Lambda e Step Functions.

Configuração de perfil AWS CLI: garantir acesso e permissões adequadas.

Noções de engenharia de prompts: habilidade para criar prompts eficientes para Bedrock.

Acesso à AWS Bedrock: disponível apenas em regiões específicas.

Situação Problema

Criar um assistente de delivery capaz de:

Receber uma entrada do usuário (tipo de experiência e item principal).

Sugerir acompanhamentos, bebidas, sobremesas e locais.

Consultar serviços externos ou APIs para fornecer informações reais.

Retornar os resultados de forma estruturada.

Step Functions Oficial Page

Utilizamos a página oficial do Step Functions (AWS Step Functions) para entender a documentação e acessar exemplos de templates para workflows prontos.

Documentação Oficial

A documentação da AWS foi essencial para:

Configurar o serviço.

Compreender o Amazon States Language (ASL).

Aprender sobre permissões e preços.

Links úteis:

AWS Bedrock Documentation

AWS Step Functions Documentation

Localizando o Serviço

Acesse o console AWS.

Vá para a seção Step Functions.

Certifique-se de estar na região compatível com Bedrock.

Verifique os modelos disponíveis para iniciar o projeto.

Começando com um Projeto Template

Iniciei com um template de Dynamic Parallelism no Step Functions.

Esse modelo foi personalizado para incluir integrações com Bedrock e APIs externas.

Workflow Studio & ASL

Workflow Studio: Interface gráfica para criar e editar workflows.

Amazon States Language (ASL): Linguagem JSON usada para definir o fluxo de estados.

Aprendi a alternar entre a interface gráfica e a edição de ASL para maior controle sobre o projeto.

Criando um Hello World

Antes de iniciar o projeto real, um exemplo simples foi implementado:

Um Lambda recebia uma entrada e retornava "Hello World!".

Isso ajudou a validar permissões e testar configurações.

Precificação e Custos

Step Functions: Baseado no número de transições de estado.

Bedrock: Custo calculado com base no uso do modelo (número de tokens).

Monitorei os custos no AWS Cost Explorer para evitar surpresas.

Nível 1 de Configuração - Permissão de Perfil

As permissões foram configuradas usando políticas do IAM:

bedrock:InvokeModel

stepfunctions:StartExecution

lambda:InvokeFunction

Criação de um perfil de execução para o Step Functions.

Nível 2 de Configuração - Disponibilidade de Serviço

Certifiquei-me de que o Bedrock e Step Functions estavam habilitados na região correta.

Realizei testes para garantir conectividade entre serviços.

Criando um Assistente de Delivery na Prática

Entrada do Usuário:

Tipo de experiência e prato principal.

Processamento com Bedrock:

Geração de sugestões com engenharia de prompts.

Consulta a APIs Externas:

Reforço das informações com dados do mundo real.

Entrega de Resultados:

Formatação final e retorno estruturado para o usuário.
