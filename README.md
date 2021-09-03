# tps_09_21

> For this competition, you will predict whether a customer made a claim upon an insurance policy. The ground truth claim is binary valued, but a prediction may be any number from 0.0 to 1.0, representing the probability of a claim. The features in this dataset have been anonymized and may contain missing values.

<details><summary> DADOS VIZ </summary>
<p>
  
![](https://github.com/Alexandre-Caldeira/tps_09_21/blob/main/todos.png)

  </p>
</details>

[Fonte](https://www.kaggle.com/azzamradman/catboost-baseline-with-simple-eda) da visualização.
 
<details><summary>Lista dos dias</summary>
<p>

- [a-Dia 1](https://github.com/Alexandre-Caldeira/tps_09_21#a-dia-1)
- [g-Dia 1](https://github.com/Alexandre-Caldeira/tps_09_21#g-dia-1)
- [a-Dia 1](https://github.com/Alexandre-Caldeira/tps_09_21#a-dia-1)
- [a-Dia 1](https://github.com/Alexandre-Caldeira/tps_09_21#a-dia-1)
- [a-Dia n](https://github.com/Alexandre-Caldeira/tps_09_21#a-dia-n)
- [g-Dia n](https://github.com/Alexandre-Caldeira/tps_09_21#a-dia-n)
  
</p>
</details>

# Resumo do que fomos fazendo / aprendendo 

## a-Dia 1:
  - <details><summary>Eu fiz:</summary>
      <p>
      
      - Remover colunas que fossem de baixa "utilidade", baseando nesse [link]() para métodos de se fazer isso e aplicando em uma rede neural densa profunda simples tipo do cap 10 do treinamento. Não foi a pior solução possível (foi literalmente a 2ª pior), mas atibuo isso ao uso da rede neural desregrado.
      - Apenas após primeira submissão percebi que estava treinando "errado", o score usado na competição é [Área sob a ROC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic). Percebi que praticamente não sabia usar k-fold / cross_validation e é essencial aqui.
      - Usando essa mesma técnica de cleaning, empreguei um modelo XGBoost similar ao que vi em algumas soluções bem rankeadas. Automaticamente subi umas 20 posições.
      - Ainda, removi meu data cleaning inicial (dropador de colunas doidasso) e treinei novos modelos, subindo um pouco mais, usando XGBoost. A solução com rede neural continua com performance muito ruim (porque? talvez pela complexidade do modelo). 
      - Por fim, tentei usar a saída de um modelo XGBoost como parte das entradas de um modelo de rede neural densa e também de uma rede neural com Embedding baseada numa solução [bem rankeada](https://www.kaggle.com/lukaszborecki/tps-09-nn).
        
      </p>
     </details>
  - Muita gente gera notebooks "Benchmark" de alguns modelos, nos quais um modelo é aplicado com todos os dados após data cleaning "básico"
  - Chutes dos "high scorers" são benchmarks de data cleaning sem muita lógica por trás (drop ou imputes/encodes) aplicados em  AutoML e XGBoost 
  - <details><summary>Aprender/reler/entender melhor:</summary>
      <p>
        
      - [x] K-Fold!!!! [notebook que usa, por exemplo](https://www.kaggle.com/jarupula/tps-sep-getting-started)
      - [x] [XGBoost](https://xgboost.readthedocs.io/en/latest/tutorials/model.html)
        - Marreta:
      - [ ] [keras.layers.Embedding](https://www.kaggle.com/rajmehra03/a-detailed-explanation-of-keras-embedding-layer)
        - Marreta:
      - [ ] Revisar regressões: [the 5-day regression challenge](https://www.kaggle.com/rtatman/the-5-day-regression-challenge)
        - Marreta:
      - [x] Estudar mais qual accuracy metric usar [?](http://gim.unmc.edu/dxtests/roc3.htm)
        - Marreta:
      - [ ] [Solução 1](https://www.kaggle.com/antonellomartiello/tps09-autogluon), [Solução 2](https://www.kaggle.com/alexryzhkov/sep21-lightautoml-starter) com AutoML, ver mais sobre? Largar pra lá?
        - Decisão:
        
      </p>
     </details>
  - Por fim, pra lembrar amanhã: **FAÇA O SIMPLES PRIMEIRO, COMPLEXO = AJUSTE FINO**.

## g-Dia 1:
  - ...
  - ...

## a-Dia 2:
  - Li sobre XGBoost, algumas outras soluções e tentei aplicar metodos mais simples de regressão por DNN mas não tive bons resultados (não submeti nada)
  - Postei nova visualização em alta resolução pra facilitar propostas de novos modelos, talvez 

## g-Dia 2:
  - ...
  - ...

## a-Dia 3:
  - Aprendendo sobre [Elastic Net](https://www.kaggle.com/rtatman/regression-challenge-day-5), [AutoGluon](https://auto.gluon.ai/stable/tutorials/tabular_prediction/tabular-quickstart.html) e [NNI](https://github.com/microsoft/nni)
