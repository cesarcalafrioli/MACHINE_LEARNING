# MACHINE_LEARNING
Repositório de algoritmos de aprendizagem de máquina supervisionada e não supervisionada.

## Sobre a Aprendizagem de Máquina

Machine Learning (ML), ou aprendizagem de máquina, é o campo de estudo que dá aos computadores a capacidade de aprender sem serem 
explicitamente programados com o conhecimento. Tem como objetivo a construpção de sistemas para computadores que possam se adaptar e
aprender com sua experiência. A aprendisagem de máquina se baseia em algorítmos e modelos estatísticos para ensinar as máquinas a realizar
tarefas específicas sem a necessidade de programação explícita.

Um programa de computador aprende com a experiência E em relação a alguma classe de tarefas T e medidas de desempenho P se o seu desempenho
em tarefas T, quando medido por P, melhora com a experiência E ( Mitchell, 1997 ).

A aprendizagem de máquina utiliza diferentes áreas de conhecimento para criar sistemas de aprendizagem que extraem conhecimento de dados
para inferir, decidir ou prever sem usar intervenção humana. Algumas disciplinas que fundamentam a ML são: 
- Teoria da informação;
- Ciência da Computação;
- Otimização e controle;
- Estatísticas;
- Fìsica;
- Física Estatística;
- Neurociência;

O ML possui um processo a ser seguido, conforme o fluxograma abaixo:

![image](https://github.com/user-attachments/assets/4593e77f-8d62-4dc9-9d93-011db00dfedf)

Várias tarefas bem-sucedidas foram tratadas com algoritmos de aprendizagem, como reconhecimento e geração de padrões, reconhecimento de anomalias,
e predição. E Possui duas grandes classes: Aprendizagem indutiva e aprendizagem transdutiva.

A Aprendizagem Indutiva (ou Inferência Indutiva) busca aprender uma função geral a partir dos dados de treinamento que poss aser aplicada a qualquer novo exemplo, mesmo que ele ainda
não tenha sido visto. visa categorizar todo o espaço de entrada e estima a função do modelo considerando a relação dos dados com todo o espaço de hipóteses e usa esse
modelo para prever valores de saída para exemplos além do conjunto de treinamento. Por exemplo. um classificador treinado com scikit-learn, como uma SVM, MLP ou árvore
de decisão, após o treinamento, ele pode prever a classe de qualquer nova entrada.

A Aprendizagem Transdutiva (ou Inferência Transdutiva) visa rotular um conjunto-alvo de dados não previamente rotulados. Tenta prever os rótulos apenas para um conjunto específico de exemplos não
rotulados que estão disponíveis no momento do treinamento. O modelo não tenta generalizar para novos dados fora desse conjunto. Por exemplo, o algoritmo Transductive SVM (TSVM), ou método semi-supervisionados onde se conhece o conjunto completo (rotulado + não rotulado).

Enquanto a aprendizagem indutiva generaliza a partir de casos observados, enquanto aprendizagem transdutiva faz previsões específicas de casos observados. A tabela abaixo resume a diferença entre
as duas inferências:

| Característica                | Indutiva                | Transdutiva                                       |
| ----------------------------- | ----------------------- | ------------------------------------------------- |
| Generalização                 | Para qualquer novo dado | Apenas para os dados não rotulados já disponíveis |
| Exemplo de algoritmo          | SVM, Random Forest, MLP | Transductive SVM, Label Propagation               |
| Reutilizável para novos dados | Sim                     | Não necessariamente                               |
| Contexto comum                | Supervisão total        | Semi-supervisão ou poucos rótulos                 |

## Raciocínio científico

No contexto de ML, o raciocínio científico se refere à forma sistemática e fundamentada de pensar, testar e validar hipóteses, aplicado à construção de modelos preditivos ou descritivos a partir de
dados. É o uso dos princípios do método científico no desenvolvimento de sistemas de aprendizagem de máquina.

Exemplo de um Raciocínio Científico no ML:
- Hipótese: "Alunos com baixa frequência e nota tendem a evadir mais."
- Experimento: Você treina um modelo de classificação com esses atributos.
- Validação: Mede acurácia, precisão, recall em dados de teste.
- Análise: Descobre que a frequência é mais importante que a renda.
- Refinamento: Inclui novos atributos ou muda o tipo de modelo.

O Raciocínio científico é importante, pois sem ele o uso de ML vira uma tentativa e erro sem critério. Com isso, evitamos conclusões precipitadas ou incorretas; Garantimos reprodutibilidade dos
resultados, e tomamos decisões baseadas em evidências (dados + estatísticas).

Exemplo prático e detalhado:

1. Observação (Exploração dos dados)
Você nota que a universidade tem dados históricos sobre:
- Frequência em aula;
- Nota média por disciplina;
- Renda familiar;
- Idade;
- Tipo de escola de origem (pública ou privada);
- Resultado: se o aluno evadiu ou não.

2. Formulação da hipótese
"A frequência baixa e nota baixa são fortes preditores de evasão."

3. Construção de um modelo (teste da hipótese)
Você usa os dados históricos para treinar um modelo de classificação (por exemplo, Logistic Regression ou Random Forest) para prever evasão (variável binária: evadiu ou não).

4. Experimento
Divide os dados em conjunto de treinamento e teste. Treina o modelo no conjunto de treino e avalia o desempenho no teste.

5. Análise dos resultados
- Acurácia: 85%
- Recall para a classe “evadiu”: 60%
- A análise de importância dos atributos mostra que:
  - A frequência tem peso maior do que a nota;
  - A renda tem impacto menor que o esperado.

Você reformula parcialmente a hipótese:
- "A frequência é o fator mais relevante na evasão, mais até do que as notas."

6. Refinamento
Você decide:
- Adicionar o histórico de trancamentos de disciplina como novo atributo;
- Testar outro modelo (por exemplo, SVM ou XGBoost);
- Fazer tuning de hiperparâmetros.

Como Raciocínio Científico, temos o Dedutivo, Indutivo, e Abdutivo.

O raciocínio dedutivo é o ato de usar fatos específicos e tirar conclusões generalizadas deles. Consiste em obter uma 
conclusão de forma redutiva por meio da aplicação de regras gerais válidas para a totalidade de um domínio fechado,
estreitando seguidamente o intervalo em consideração até que restem apenas as conclusões. Também é conhecido como raciocínio
_top-down_. A primeira forma de raciocínio dedutivo é a lei do desapego, também conhecido como eliminação de implicações.
Consiste em uma regra de inferência em que, se P implica Q (P -> Q) e P for verdadeiro (V), então Q deve ser verdadeiro (Q).
Para chegar numa conclusão, esse tipo de método argumentativo parte do geral para o específico. Ou seja, a partir de premissas
universais ele chega no particular. Diferente do método indutivo, esse não cria conceitos novos.

Exemplo:
- Todos os animais são mortais.
- Peixe é um animal.
- Logo, o peixe é mortal.

Já o Raciocínio indutivo consiste em obter uma conclusão através da generalização ou extrapolação de casos específicos para regras
gerais, portanto, há incerteza epistemológica (dúvida ou à falta de certeza sobre o conhecimento, frequentemente devido à falta de
evidências ou à natureza limitada das informações disponíveis). É uma classe especial de técnicas supervisionadas de aprendizagem,
onde dado um conjunto de pares estímulo-resposta {xi, f (xi)}, determina-se uma hipótese h(xi) tal que h(xi) ≈ f (xi), ∀i.
Nesse tipo de raciocínio, deve-se formar um coneito que suporte a maioria dos vários exemplos positivos, mas nenhum negativo. Demanda
também uma série de instâncias de treinamento para formar um conceito de aprendizagem indutiva.
Em resumo, para chegar a uma conclusão, esse tipo de raciocínio parte do específico para o geral. Assim, de uma premissa particular
há uma generalização até chegar no universal. Note que ele pode criar conhecimentos novos.

Exemplo:
- Todo gato é mortal.
- Todo cão é mortal.
- Todo pássaro é mortal.
- Todo peixe é mortal.
- Logo, todo animal é mortal.

Exemplo2:
O Parlamento Europeu aprovou leis problemáticas antes, por isso não podemos acreditar que outras cortes vão admitir as novas leis.
Parlamento europeu --> uma corte apenas (ESPECÍFICO)
Outras cortes --> GERAL (generalização)

![image](https://github.com/user-attachments/assets/5757f77f-e687-4479-8128-9c6ec09a2c66)

E no Raciocínio abdutivo, parte-se de uma observação e depois procura-se a explicação mais simples e provável adotando provisoriamente uma
hipótese. Todas as consequências possíveis da hipótese podem ser verificadas experimentalmente. As premissas desse raciocínio NÃO GARANTEM
a conclusão, visto que a conclusão pode ser visto como uma inferência para a melhor explicação.
Abdutivo é o contrário de dedutivo e é um processo de pensamento que consiste em encontrar a explicação mais provável para um conjunto de
observações ou fatos. É também conhecido como inferência para a melhor explicação. 

## **Tipos de Aprendizagem**

Os tipos mais comuns de aprendizagem ssão a supervisionada (AS), não-supervisionada (ANs), e por reforço (AR), Semi-Supervisionada, e Ativa.

A aprendizagem supervisionada (AS) consiste em rotular todos os dados. Os parâmetros do modelo de aprendizagem são ajuistados por comparação direta
da saída do modelo com a saída desejada. Essa aprendizagem é orientada pela medida de erro, que consiste na diferença entre a saída obtida e 
aquela desejada para as amostras de treinamento. Nesse tipo de aprendizado, os computadores são treinados usando exemplos de entrada e saída
correspondente. Por exemplo, imagine que estamos construindo um modelo para classificar e-mails entre e-mails de spam e e-mails legítimos. Para
isso, utilizamos diversos e-mails que contêm a resposta à pergunta "É spam?". Através das características dos e-mails, como palavras-chave,
comprimento do texto e presença de links, o algoritmo aprende a rotular o conteúdo como spam. Esse modelo é conhecido como modelo de classificação.
Ele identifica padrões associados a cada categoria, permitindo que, posteriormente, o modelo classifique novos e-mails com base no treinamento
recebido. Dessa forma, é possível filtrar e organizar a caixa de entrada de maneira mais eficiente.

A aprendizagem supervisionada aprende a função de distribuição de probabilidade (pdf) de p(y|x). É largamente usada em classificação, aproximação,
controle, modelagem e identificação, processamento de sinais, e otimização.

Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/93b0c912-3521-4b77-9a41-5387827aeef0)

A aprendizagem não-supervisionada (ANs) não usa saídas desejadas e se basea apenas nas correlações dos dados de entrada. Logo, determina
compartilhamento de características significativas sem a participação de um professor. A Aprendizagem Não-supervisionada comumente é do tipo
hebbiana, ou seja, usa relações locais envolvendo dois neurônios e uma sinapse, e a mudança de peso sináptico é proporcional à correlação entre
os sinais pré e pós-sinápticos. Nesse tipo de aprendizado, os computadores exploram dados não rotulados para descobrir padrões e estruturas ocultas.
Uma técnica comum utilizada nesse tipo de aprendizado é o clustering, que é o processo de agrupar e categorizar grupos de dados.
Em um contexto de e-commerce, por exemplo, podemos identificar padrões e grupos de compras semelhantes. Você pode descobrir grupos de clientes que
tendem a comprar produtos de moda, outros grupos que preferem produtos eletrônicos, e assim por diante.

Essa análise de clustering permite entender melhor os perfis de compra dos clientes e identificar segmentos de clientes com interesses e preferências
semelhantes. Com base nisso, estratégias de marketing podem ser desenvolvidas de forma direcionada para cada grupo, como o envio de ofertas
personalizadas e recomendações de produtos relacionados aos interesses específicos de cada segmento. 

A aprendizagem nãos-supervisionada aprende a função de distribuição de probabilidade (pdf) de um conjunto de treinamento p(x). É comumente empregada para
agrupamento, quantização vetorial, extração de características, codificação de sinal e análise de dados.

Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/ff1b0f8b-6876-4161-925d-6dc67252dd0f)

A aprendizagem por reforço especifica como um agente aprende a selecionar ações para maximizar uma recompensa cumulativa. É um caso especial de Aprendizagem
supervisionada que utiliza sinais de retorno indicativos da qualidade da saída. Tal sinal de reforço consiste em um retorno avaliando o sucesso ou fracasso
de uma dada saída, ou seja, há recompensa para o modelo em caso de bom resultado de saída e penalização para mau resultado.
Esse tipo de aprendizado é o que mais se diferencia dos outros que falamos. No aprendizado por reforço, um agente é treinado para tomar sequências de decisões,
recebendo recompensas ou penalidades em troca. O objetivo é que o agente aprenda a tomar as melhores ações para maximizar as recompensas ao longo do tempo.
Esse tipo de aprendizado é amplamente aplicado na robótica e em jogos. É geralmente utilizado em controle e inteligência artificial.

Segue a figura a baixo:

![image](https://github.com/user-attachments/assets/e4f5973a-2353-488f-b63f-adc4636e0485)

A aprendizagem Semi-supervisionada tem como objetivo a utilização de uma grande coleção de dados não-rotulados juntamente com alguns exemplos rotulados para
melhorar a capacidade de generalização. Utiliza tanto amostras de dados rotuladas quanto não rotuladas no processo de treinamento. Aprender com hipótese de grupo
ou com hipótese de variedade (_manifold_), em ambos os dados dentro de um grupo ou em uma variedade têm maior probabilidade de ter o mesmo rótulo. 
Técnicas de aprendizagem semissupervisionadas modificam ou complementam um algoritmo supervisionado, conhecido como "aprendiz base", nesse contexto, para integrar
informações de exemplos não rotulados. Os pontos de dados rotulados são utilizados para fundamentar as previsões do aprendiz base e adicionar estrutura (como
quantas classes existem e as características básicas de cada uma) ao problema de aprendizado. Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/67f486dc-e036-4f0b-b216-dcf7a5a74f52)

A aprendizagem Ativa (AA) visa escolher ativamente os exemplos mais informativos para rotulagem manual na aprendizagem, ou seja, estabelecer sinais de entrada para generalização
ótima. Com base na expectativa condicional do erro de generalização, a Aprendizagem ativa pondera as amostras de treinamento de acordo com sua importância. Segue a
figura abaixo:

![image](https://github.com/user-attachments/assets/b6a296ae-1e73-4b90-81aa-a05f6f08a3cd)

Outros tipos de aprendizado incluem :
- Aprendizagem de variedade : Capacidade de um modelo de aprender a lidar com um conjunto diversificado de entradas e saídas, ou seja, com diferentes tipos de dados e
tarefas, incluindo a capacidade de aprender com dados incompletos, ambíguos ou em diferentes idiomas, bem como de generalizar para novas situações não vistas durante o
treinamento.
- TransferÊncia de aprendizagem : Reutiliza um modelo treinado para uma tarefa específica e o adapta para uma tarefa relacionada. Em vez de treinar um novo modelo desde o
início, a transferência de aprendizagem aproveita o conhecimento prévio do modelo para acelerar o treinamento e melhorar o desempenho em tarefas novas.
- Aprendizagem multirótulo (MR): Associa-se uma instância de dados a multiplas classes ao mesmo tempo, em ve de atribuir uma única instância a apenas uma classe. Essa aprendizagem
permite a associação de várias etiquetas ou rótulos a uma única instância. Como exemplo, temos classificação de filmes, que podem ser classificados como "ação" e "comédia
simultaneamente.
- Aprendizagem de múltiplas instâncias (MIL) : Aprendizado "fracamente supervisionado" em que um grupo de instância (Como imagens, por exemplo) é rotulado sem a rotulagem de instâncias indivi
duais. É conhecido como fracamente supervisionado pelo fato de nem todas as instâncias individuais serem realmente rotuladas. Nessa aprendizagem, um grupo de instâncias relacionadas
para um rótulo é chamado de "bag".
- Classificações paramétricas, semiparamétricas e não-paramétricas : Referem-se a diferentes abordagens para modelar relações estatísticas e analisar dados. A paramétrica assume uma distribuição
- específica (como a normal), enquanto a não-paramétrica não faz tal suposição, sendo mais flexível em situações onde a forma de distribuição é desconhecida ou não formal. E a Semiparamétrica
encontra-se entre as classificações paramétricas e não-paramétricas, permitindo alguma flexibilidade na forma de distribuição, mas ainda com alguns pressupostos.

![image](https://github.com/user-attachments/assets/36d1b1cc-540a-475c-91b9-3606a525f94a)

## **Aprendizagem**

A aprendizagem consiste na reconstrução de uma hipersuperfície baseada em exemplos. No contexto da matemática, é um ajuste NÃO-LINEAR de curva e se trata de um problema inverso
ill-posed, ou seja, os dados de entradas podem ser ruidososos ou imprecisos, bem como insuficientes para construir o mapeamento de maneira exclusiva.

![image](https://github.com/user-attachments/assets/927bc4e1-619f-41be-87b2-b5bd073f8849)

É necessário que o conjunto de treinamento seja suficientemente grande e diversificado par representar bem o problema, pois um algoritmo de aprendizagem é sobretreinado com muitos exemplos,
parâmetros ou épocas, sendo acurado, dessa forma, para dados de treinamento, mas impreciso para dados de teste, caracterizando assim o Overfitting (Sobreajuste).

O underfitting ocorre quando o modelo é simples demais e não consegue capturar as relações complexas nos dados, enquanto o overfitting ocorre quando o modelo se adapta demais aos dados
de treino, incluindo o ruído, e não generaliza bem para novos dados.

![image](https://github.com/user-attachments/assets/87e9931d-9642-4303-9342-abb1489257e0)


## Generalização

A generalização é a capacidade de um modelo aprender corretamente com os dados de treino e, em seguida, aplicar esses conhecimentos para prever com precisão dados novos e
não vistos durante o treinamento. Consiste em estimar o valor na hipersuperfície de uma entrada não-treinada. É essencial que um modelo não apenas memorize os dados de treino,
mas também que aprenda os padrões subjacentes para que possa ser aplicado em situações reais. A generalização é uma técnica amplamente reconhecida no mundo do aprendizado de
máquina e da inteligência artificial, que capacita cientistas de dados a construir modelos que transcendem as limitações dos dados de treinamento e se destacam em cenários
do mundo real. Em resumo, tendo em vista que, no mundo real, os dados são confusos, imprevisíveis e em constante evolução, a generalização é a capacidade de um modelo treinado
de fazer previsões precisas sobre dados novos e inéditos a fim de compreender os padr~´oes e relacionamento em seus dados de treinamento e aplicá-los a exemplos inéditos dentro
da mesma distribuição do conjunto de treinamento.

Matematicamente, a generalização é a interpolação e extrapolação de dados de entrada.

Um dos prinicipais desafios no campo do ML é o **erro de generalização**, que ocorre quando um modelo de aprendizado de máquina se torna ou muito complexo
ou muito simples para o conjunto de dados em questão. Dessa forma um modelo treinado não consegue realizar previsões precisas em dados não vistos anteriormente e é
tipicamente composto por Erro de aproximação (EA) e Erro de estimação (EE). 

Quando o modelo é muito complexo, ele pode se ajustar demais aos dados de treinamento, capturando padrões e ruídos irrelevantes, resultando em mau desemepnho em dados não vistos.
Quando inverso, modelo simples demais pode se tornar incapaz de capturar a complexidade dos dados, resultando em desempenho insatisfatório.

O Erro de aproximação ocorre devido ao número finito de parâmetros do esquema de aproximação usado e a ruído desconhecido nos dados de treinamento. É um erro implícito pela escolha
 da classe de função e é definido como a diferença de risco obtida entre o melhor modelo dentro da classe de função e o modelo ótimo.

O erro de estimação ocorre devido a um número finito de dados disponíveis, sendo assim um erro IMPLÍCITO, e reflete apenas parcialmente a distribuição real dos dados.

O erro de gerneralização pode ser visto na representação gráfica abaixo:

![image](https://github.com/user-attachments/assets/73bc3613-6213-4077-b6eb-c41b07496074)

A fim de melhorar a capacidade de generalização e evitar seus erros, várias técnicas são propostas, como a Esparsidade e estabilidade, a tolerância a falhas, o Descarte (dropout),
a Generalização por regularização, e o Critério de Parada. Também para evitar o erro de generalização, é adotado o uso de conjuntos de treinamento, validação e teste. O conjunto de
treinamento treina o modelo, o de validação é utilizado para ajustar os hiperparâmetros do modelo, e o conjunto de teste é utilizado para avaliar o desempenho final do modelo em dados
não vistos.

O critério de parada visa evitar o sobretreinamento interrompendo o treinamento antes que o Mínimo Erro Absoluto seja atingido. A rede, assim, não aprenderá o ruído de alta frequência
se o treinamento for interrompido em ponto apropriado. O erro de treinamento tende a diminuir até seu mínimo enquanto o erro de generalização deve atingir seu mínimo antes e depois passa
a crescer. É definido _da mesma forma que o erro de aprendiagem, só que para um conjunto de dados de validação. Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/aad1963a-e5fe-495a-afed-10c3509f3e7e)

A Generalização por regularização consiste em adicionar uma penalidade aos parâmetros do modelo para evitar o ajuste excessivo aos dados de treinamento, e pode ser feita de várias formas
, como a adição de termos de penalidade na função de perda do modelo. Emprega um termo de restrição (Ec), que penaliza a complexidade, que é a causa de generalização baixa, de uma solução,
tornando a função de custo: –ET= EA + λEC. Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/20c0c0b6-0aea-4a0a-8368-34c9e99f2255)

O Descarte (_dropout_) descarta aleatoriamente os nodos e suas conexões no treinamento de uma RN para interromper co-adaptações frágeis, como na rede Multi-Layer Perceptron com algorítmo
de retropropagação (MLP-BP), que não generalizam para dados de testes. No caso mais simples, cada nodo é mantido com probabilidade fixa _p_, independente das outras unidades. É considerado
adequado a eliminação de 20% das unidades da camada de entrada e 50% das unidades da camada escondidas. Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/9ebe9735-b84a-4d5f-9226-4a67142c9821)

A tolerância a falhas nos pesos ou nodos consiste no no uso do ruído sináptico e na redução da magnitude do peso, sendo assim importante para uma Rede Neural, da mesma forma que o ruído na entrada melhora a capacidade de
generalização. Quanto menor a magnitude do peso, maior a tolerância a falhas.

A Esparsidade e estabilidade são duas propriedades conflitantes dos algoritmos de aprendizagem que colaboram na capacidade de generalização. A esparsidade aumenta a robustez da rede de 
aprendizado, introduzindo diferentes tensões com diferentes padrões de entrada. Um dado algoritmo precisa equilibrar esparsidade e estabilidade.

## **O uso da aprendizagem nas tarefas**

Entre os usos, incluem:

- Associação de padrões : Conchecimento por associação por meio da memória distribuíd ainspirada no cérebro humano. Entre a associação, temos a autoassociação e a heteroassociação.
- Reconhecimento de padrões : Um padrão ou sinal de entrada é incluído em uma entre possíveis categorias. Temos, como reconhecimento, a Classificação (Supervisionada) e o agrupamento
(Não-supervisionada).
- Determinação de funções : Produz uma rede neural que define uma função que replique um dado mapeamento entrada-saída. Temos, como determinação, a interpolação (Mapeamento que interpola
pontos aos existentes) e a aproximação (Mapeamento que aproxima a relação).
- Controle de processos : Rede neural para realizar identificação ou controle de um dado processo ou sistema. Como controle, temos a identificação de sistemas (Modela a operação de um
sistema) e o Sistema inverso (Modela o controlador do sistema). Segue a figura abaixo:

![image](https://github.com/user-attachments/assets/8ed6fdda-7dab-4766-b725-a82f2e0fa263)

- Filtragem de sinais : Separação de componentes de um sinal, eliminando partes indesejáveis de um sinal. Entre as filtragens, temos a suavisação (Retira variações bruscas de um sinal),
a Predição (Antevê o comportamento futuro de um dado sinal). Como exemplo, é possível remover ruídos de um áudio com as redes neurais profundas.

### Referências

- Disciplina UFPE IN0997 - Redes Neurais - Prof. Aluízio Araujo
- https://www.ibm.com/br-pt/think/topics/semi-supervised-learning
- https://aws.amazon.com/pt/what-is/transfer-learning/
- https://www.uema.br/2025/02/professor-da-uema-desenvolve-metodo-inovador-para-imputacao-de-dados-em-classificacao-multi-rotulo-2/
- https://medium.com/@minhkhangle.phd/multiple-instance-learning-mil-and-its-utility-in-whole-slide-image-wsi-analyses-3acb67f5434b
- https://pt.wikipedia.org/wiki/Estat%C3%ADstica_n%C3%A3o_param%C3%A9trica
- https://www-colorado-edu.translate.goog/lab/lisa/services/short-courses/parametric-versus-seminonparametric-regression-models?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=sge
- https://byjus-com.translate.goog/maths/difference-between-parametric-and-nonparametric/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=sge
- https://www.blog.trainindata.com/machine-learning-with-imbalanced-data/
- https://www-rudderstack-com.translate.goog/learn/machine-learning/generalization-in-machine-learning/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=sge&_x_tr_hist=true
- https://qohash-com.translate.goog/generalization-in-machine-learning/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=sge
- https://medium.com/@lg0702/overfitting-e-underfitting-6cba339aebfb
- https://pt.stackoverflow.com/questions/377643/o-que-%C3%A9-overfitting-e-underfitting-em-machine-learning
- https://glossario.maiconramos.com/glossario/o-que-e-erro-de-generalizacao-em-aprendizado-de-maquina/
- https://mlweb.loria.fr/book/en/estimationapproximationerrors.html
- https://www.quora.com/Where-is-Sparsity-important-in-Deep-Learning
  

