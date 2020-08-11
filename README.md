# DatasetCovid

Este repositório tem o intuito de manter maior organização e melhorar as decisões sobre como os datasets serão utilizados.
De forma a manter o versionamento dos conjuntos, ao fazer qualquer alteração, por favor, crie um novo branch com um nome explicativo (ex: /limpezaGabriel) e faça alterações nesse branch. Ao finalizar as alterações necessárias, efetue um pull request e peça para um dos colegas de equipe revisar o seu trabalho, assim evitamos erros ao fazer qualquer modificação. O colega solicitado deve revisar e permitir o merge.

Caso não conheça o funcionamento do GitHub, siga o seguinte tutorial: https://guides.github.com/activities/hello-world/. Suficiente para aprender todas as funcionalidades aqui necessárias.

Caso esteja adicionando um arquivo ao invés de alterando algum já existente no repositório, adicione uma breve descrição sobre tal arquivo neste read.me, seguindo a descrição dos outros arquivos.

## Descrição das features:
 - patientid = Identificador interno do paciente
 - offset    = Número de dias desde o início dos sintomas ou hospitalização para cada imagem. Se um relatório indicar "depois de alguns dias", serão considerados 5 dias. Isso é muito importante quando existem várias imagens para o mesmo paciente acompanhar a progressão.
 - sex       = Masculino (1), Feminino (0) ou em Branco
 - age       = Idade do paciente em anos
 - finding   = Tipo de pneumonia
 - RT_PCR_positive = Sim (1) ou não (0) ou em branco se não for relatado
 - survival  = Sim (1) ou não (0) ou em branco se desconhecido
 - intubated = Sim (1) se o paciente foi intubado (ou ventilado) em qualquer momento da doença ou Não (0) ou em branco, se desconhecido.
 - went_icu  = Sim (1) se o paciente estava na UTI (unidade de terapia intensiva) ou na UTI em qualquer momento da doença ou Não (0) ou em branco, se desconhecido.
 - needed_supplemental_O2 = Sim (1) se o paciente necessitou de oxigênio suplementar em qualquer momento da doença ou Não (0) ou em branco se desconhecido
 - extubated = Sim (1) se o paciente foi extubado com sucesso ou Não (0) ou em branco se desconhecido
 - temperature = Temperatura do paciente em Celsius no momento da imagem
 - pO2_Saturation = Pressão parcial da porcentagem de saturação de oxigênio no momento da imagem
 - wbc_count = Contagem de glóbulos brancos em unidades de 10^3 / uL no momento da imagem
 - neutrophil_count = Contagem de células neutrófilas em unidades de 10^ 3 / uL no momento da imagem
 - lymphocyte_count = Contagem de células linfocitárias em unidades de 10 ^ 3 / uL no momento da imagem
 - view      = Posteroanterior (AP), Anteroposterior (AP), AP Supino (APS) ou Lateral (L) para raios-X; 
Axial ou Coronal para tomografias computadorizadas. Traduções: Notaufnahme> Supine, Liegend-> Supine
 - modality  = Raio-x, CT
 - date      = Data em que a imagem foi adquirida
 - location  = Nome do hospital, cidade, estado, país
 - filename  = Nome com a extensão
 - doi       = Identificador digital de objeto (DOI) do artigo de pesquisa
 - url       = URL do artigo ou site de onde a imagem veio
 - license   = Licença da imagem como CC BY-NC-SA. Em branco se desconhecido
 - clinical_notes = Notas clínicas sobre a imagem e / ou o paciente
 - other_notes = e.g. credit

## Arquivos:

 - metadate_cleaned.csv é o banco de dados após a limpeza e numerização feita pelo Pedro. Este dataset será utilizado como base para os próximos particionamentos e alterações no banco de dados. Será utilizado para a realização de testes do Pedro e da Natália para as apresentações a partir do dia 19.
 
 - metadata_option1.csv corresponde ao banco de dados acordado para análise na reunião sobre tratamento de dados, no qual foi feita a eliminação de todas as instâncias com NaN na coluna 'intubated', que apresenta o menor número razoável para utilização dos dados clínicos em um modelo de predição. Esse dataset é para os testes iniciais do Alberto e do Gabriel.

 - metadata_option2.csv é uma segunda alternativa para os dados clínicos. Foram removidas todas as instâncias com dados faltantes na coluna 'intubated' e após isso foram removidas todas as instâncias com dados faltantes na coluna 'in_icu'. Esse dataset é para os testes iniciais do Alberto e do Gabriel.
