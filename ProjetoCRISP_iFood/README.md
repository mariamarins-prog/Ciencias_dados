# Projeto CRISP-DM: Campanhas de Marketing (Case iFood)

Disciplina: Ciência de Dados aplicada ao Marketing - CEUB

Professora: Kadidja Valéria Reginaldo de Oliveira

Grupo 1: Greyci Dias, Maria Antônia e Lucas Rogoski

## O problema

Uma empresa de varejo de alimentos ligou para 2.240 clientes oferecendo um produto novo. Só 15% aceitaram e a campanha deu prejuízo. Nosso objetivo foi descobrir quais clientes têm mais chance de aceitar, para a empresa ligar só para eles.

## A base de dados

Usamos a base do case de CRM que o iFood usa em processos seletivos para analista de dados. São 2.240 clientes, com dados de perfil, compras e respostas a campanhas anteriores. A empresa do case é um varejista criado para o teste, não o app de delivery do iFood.

## O que fizemos (CRISP-DM)

Fase 1 - Negócio: definimos o problema e os critérios de sucesso. Como cada ligação custa 3 e cada venda rende 11, a campanha só dá lucro com mais de 27,3% de aceite.

Fase 2 - Dados: exploramos a base, achamos problemas de qualidade e levantamos hipóteses sobre quem aceita a campanha.

Fase 3 - Preparação: removemos duplicados, registros contraditórios e erros de idade, renda e estado civil, e criamos novas variáveis. A base ficou com 2.014 clientes.

Fase 4 - Modelagem: comparamos Regressão Logística e Árvore de Decisão. A Regressão Logística foi melhor (AUC de 0,91).

Fase 5 - Avaliação: simulamos a campanha. Ligando para todos, ela dá prejuízo de 847. Ligando só para os clientes indicados pelo modelo, dá lucro de 341, com 75% menos ligações. Os dois critérios de sucesso foram atingidos.

Fase 6 - Implantação: geramos a lista de clientes priorizados para a próxima campanha e definimos como integrar, documentar e monitorar o modelo.

## Arquivos

- CRISP_iFood.ipynb: notebook com as 6 fases
- dados/ml_project1_data.csv: base original
- dados/dados_preparados.csv: base limpa, usada pelo modelo
- dados/lista_campanha.csv: lista de clientes priorizados para a campanha

## Como rodar

Abra o notebook no Google Colab pelo link abaixo e use Ambiente de execução > Executar tudo. A base é carregada direto deste repositório.

https://colab.research.google.com/github/LucasRogoski/DataScience_Mkt/blob/main/ProjetoCRISP_iFood/CRISP_iFood.ipynb

## Referências

- Material da disciplina: Framework CRISP-DM (CEUB)
- Guia CRISP-DM da IBM: https://www.ibm.com/docs/pt-br/spss-modeler/saas?topic=dm-crisp-help-overview
- Case do iFood: https://github.com/nailson/ifood-data-business-analyst-test
- Solução de referência de Noa P. Prada Schnor: https://github.com/npradaschnor/ifood_Case
