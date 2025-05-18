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
aquela desejada para as amostras de treinamento.

![image](https://github.com/user-attachments/assets/93b0c912-3521-4b77-9a41-5387827aeef0)

A aprendizagem não-supervisionada (ANs) não usa saídas desejadas e se basea apenas nas correlações dos dados de entrada. Logo, determina
compartilhamento de características significativas sem a participação de um professor. A Aprendizagem Não-supervisionada comumente é do tipo
hebbiana, ou seja, usa relações locais envolvendo dois neurônios e uma sinapse, e a mudança de peso sináptico é proporcional à correlação entre
os sinais pré e pós-sinápticos.

![image](https://github.com/user-attachments/assets/ff1b0f8b-6876-4161-925d-6dc67252dd0f)




### Referências

Disciplina UFPE IN0997 - Redes Neurais - Prof. Aluízio Araujo



