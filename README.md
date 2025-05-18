# MACHINE_LEARNING
Repositório de algoritmos de aprendizagem de máquina supervisionada e não supervisionada.

## Sobre a Aprendizagem de Máquina

Machine Learning (ML), ou aprendizagem de máquina, é o campo de estudo que dá aos computadores a capacidade de aprender sem serem 
explicitamente programados com o conhecimento. Tem como objetivo a construpção de sistemas para computadores que possam se adaptar e
aprender com sua experiência.

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

Como Raciocínio Científico, temos o Dedutivo e o Indutivo.

O raciocínio indutivo é o ato de usar fatos específicos e tirar conclusões generalizadas deles..Consiste em obter uma 
conclusão de forma redutiva por meio da aplicação de regras gerais válidas para a totalidade de um domínio fechado,
estreitando seguidamente o intervalo em consideração até que restem apenas as conclusões. Também é conhecido como raciocínio
_top-down_. A primeira forma de raciocínio dedutivo é a lei do desapego, também conhecido como eliminação de implicações.
Consiste em uma regra de inferência em que, se P implica Q (P -> Q) e P for verdadeiro (V), então Q deve ser verdadeiro (Q).
Para chegar a uma conclusão, esse tipo de raciocínio parte do específico para o geral. Assim, de uma premissa particular há uma
generalização até chegar no universal. Note que ele pode criar conhecimentos novos.

Exemplo:
- Todo gato é mortal.
- Todo cão é mortal.
- Todo pássaro é mortal.
- Todo peixe é mortal.
- Logo, todo animal é mortal.

Já o Raciocínio DEdutivo consiste em ob



## Referências

Disciplina UFPE IN0997 - Redes Neurais - Prof. Aluízio Araujo



