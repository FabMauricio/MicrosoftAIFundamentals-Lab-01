Curso Microsoft Azure AI fundamentals - Laboratório 01

o objetivo é utilizar a ferramenta -MAchine Learning Automatizado- para treinar e avaliar um modelo de aprendizado de máquina.

o link descreve o exerxício: https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html

01 - Criar uma conta no microsoft Azure
02 - Escolha a opção que fornece creditos...
03 - Com o Azure em execução - Na guia - basico / Do lado esquerdo clicar em: Ia + machine learning
04 - Na barra de pesquisa digitar: machine learning
05 - Clicar em azure machine learning / Criar

06 - Configurar com os seguintes dados:
    assinatura : deixa preenchido com o nome que o azure forneceu
    grupo de recursos: nome que vc desejar
    nome : o nome que vc desejar 
    Região : east us
    conta de armazenamento: : deixa preenchido com o nome que o azure forneceu
    cofre de chaves: : deixa preenchido com o nome que o azure forneceu
    applications insights: : deixa preenchido com o nome que o azure forneceu
    registro de contêiner: em branco

07 - Seleciona: examinar + criar e aguarde a validação ser aprovada
08 - Selecione: criar e aguarde até a finalização... 
10 - Finalizado o processo clique em : ir para o recurso
11 - Selecione -iniciar o estúdio- no fim da página
12 - No lado esquerdo selecione : ML automatizado
13 - selecione : novo trabalho de ML automatizado
    Nome do trabalho : mslearn-bike-automl
    Novo nome do experimento : mslearn-bike-rental
    Descrição : Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
    Marcadores : nenhum

14 - Avança
    Selecione o tipo de tarefa : Regressão
    Seleciona criar
    Nome : aluguel de bicicletas
    Descrição : dados históricos de aluguel de bicicletas
    Tipo : Tabular
    Escolha uma fonte para o ativo de dados – de arquivos da web

15 - Avança
    URL da Web :https://aka.ms/bike-rentals
    Ignorar validação de dados : não selecionar

16 - Avança
    Formato de arquivo : Delimitado
    Delimitador : Vírgula
    Codificação : UTF-8
    Cabeçalhos de coluna : apenas o primeiro arquivo possui cabeçalhos
    Pular linhas : Nenhum
    O conjunto de dados contém dados multilinhas : não selecione

17 - Avança
    Incluir todas as colunas exceto path
    Revise os tipos detectados automaticamente

18 - Avança
19 - Criar
20 - Avança
    Tipo de tarefa : Regressão
    Conjunto de dados : aluguel de bicicletas
    Coluna de destino : rentals (integer)

---------
  Selecione exibir configurações adicionais
    Métrica primária : NormalizadRootMeanSquaredError
    Desmarca as três opções
    Modelos permitidos : Selecione apenas RandomForest e LightGBM —
    Salvar
-------
-------
  Limites : expanda esta seção
    Máximo de testes : 3
    Máximo de testes simultâneos : 3
    Máximo de nós : 3
    Limite de pontuação da métrica : 0,085
    Tempo limite : 15
    Tempo limite de interação : 15
    Habilitar rescisão antecipada : selecionado
--------
--------
  Validação e teste :
    Tipo de validação : divisão de validação de treinamento
    Percentual de dados : 10
    dados de teste : Nenhum
---------

21 - Avança

    Selecione o tipo de computação : sem servidor
    Tipo de máquina virtual : CPU
    Camada de máquina virtual : Dedicada
    Tamanho da máquina virtual : Standard_DS3_V2*
    Número de instâncias : 1

22 - Avança
23 - Resumo
24 - Seleciona - enviar trabalho de treinamento
25 - Aguardar – demora um pouco
26 - Finalizado a criação
27 - Na guia tarefas na esqueda clique em : mslearn-bike-rental / mslearn-bike-automl / Nome do algoritmo - VotingEnsemble
28 - Selecione a guia métrica
29 - Analise os gráficos


30 - Clique na guia modelo
31 - Selecione implantar / de serviço web
    Nome : prever-aluguéis
    Descrição : Prever aluguel de bicicletas
    Tipo de computação : Instância de Contêiner do Azure
    Habilitar autenticação : selecionado
    Implantar

32 - Na guia esquerda clique em ponto de extremidade/ Prever alugueis/ E selecione a guia testar
33 - Clique em testar

34 - Duvidas: segue as figuras:
![figura 01](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/84d2c91d-22c3-49d0-bcf9-2e7eae397432)
![2](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/bc962633-29e6-4194-b4a8-c7abbc5b380b)
![3](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/93991366-9df0-4976-b269-4cfed080c6e9)
![4](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/d77eed25-da7b-4b0e-8629-6e833dd01d93)
![5](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/b22652d0-5b1e-4eb3-a4bd-4afbb73571da)
![6](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/5e89d212-cd31-4e7b-bab8-d26106731ebe)
![7](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/6f0b2f02-e98b-4c4d-ab1a-2879f2a9a411)
![8](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/f9657839-a2cb-44a8-b379-74b64a385e49)
![9](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/1c0ff94b-20a9-4189-a28a-3467124b7d14)
![10](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/0a927274-5940-4c6a-b044-743ba63dc006)
![11](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/cc30027a-aea6-4044-a379-a3c37f2f75dd)
![12](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/542245a1-b56a-464d-a722-16874520dd22)
![13](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/2acca50f-f7ee-4dbc-a876-b4b911f975d9)
![14](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/8a5bdf4c-98b2-4da5-b845-e771e22f94fb)
![15](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/8017c90c-5279-448e-9010-f6deb6ae31b9)
![16](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/8a0946d6-52ba-4156-93dd-7edb32f6fcd5)
![17](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/99f744a6-b547-486a-a21b-c2716ea4aa71)
![18](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/4e6c9353-2daf-4675-9137-250067d6a352)
![19](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/5d296e69-3a5e-4846-91c8-c748a3780795)
![20](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/410206a9-fdff-4b41-a9ce-030e13146971)
![21](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/4b61ac53-574d-4ee6-9fea-58658b56a828)
![22](https://github.com/FabMauricio/MicrosoftAIFundamentals-Lab-01/assets/153826437/21224737-5967-4825-9cd3-a9b85e1c7dff)























