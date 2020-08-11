# DatasetCovid

Este repositório tem o intuito de manter maior organização e melhorar as decisões sobre como os datasets serão utilizados.
De forma a manter o versionamento dos conjuntos, ao fazer qualquer alteração, por favor, crie um novo branch com um nome explicativo (ex: /limpezaGabriel) e faça alterações nesse branch. Ao finalizar as alterações necessárias, efetue um pull request e peça para um dos colegas de equipe revisar o seu trabalho, assim evitamos erros ao fazer qualquer modificação. O colega solicitado deve revisar e permitir o merge.

Caso não conheça o funcionamento do GitHub, siga o seguinte tutorial: https://guides.github.com/activities/hello-world/. Suficiente para aprender todas as funcionalidades aqui necessárias.

Caso esteja adicionando um arquivo ao invés de alterando algum já existente no repositório, adicione uma breve descrição sobre tal arquivo neste read.me, seguindo a descrição dos outros arquivos.

Arquivos:

 - metadate_cleaned.csv é o banco de dados após a limpeza e numerização feita pelo Pedro. Este dataset será utilizado como base para os próximos particionamentos e alterações no banco de dados. Será utilizado para a realização de testes do Pedro e da Natália para as apresentações a partir do dia 19.
 
 - metadata_option1.csv corresponde ao banco de dados acordado para análise na reunião sobre tratamento de dados, no qual foi feita a eliminação de todas as instâncias com NaN na coluna 'intubated', que apresenta o menor número razoável para utilização dos dados clínicos em um modelo de predição. Esse dataset é para os testes iniciais do Alberto e do Gabriel.

 - metadata_option2.csv é uma segunda alternativa para os dados clínicos. Foram removidas todas as instâncias com dados faltantes na coluna 'intubated' e após isso foram removidas todas as instâncias com dados faltantes na coluna 'in_icu'. Esse dataset é para os testes iniciais do Alberto e do Gabriel.
