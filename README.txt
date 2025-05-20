## Modelo de Classificação KNN - Elegibilidade de Crédito

modelo supervisionado capaz de prever o **resultado de uma solicitação de crédito** com base nas informações do solicitante.

**Variáveis Utilizadas no Modelo**

As seguintes **variáveis** foram utilizadas como **entrada** (X) no modelo, nesta ordem:

1. **divida_por_salario**: divisão entre total_dividas e salario_anual
2. **historico_pagamento_score**: percentual de contas pagas em dia (ex: 0.85 = 85%)
3. **idade**: idade do solicitante

**Variável de saída (categoria)**

- `1` → **Não Elegível** (Solicitação recusada)
- `2` → **Elegível com análise** (Necessita verificação adicional)
- `3` → **Elegível** (Aprovado imediatamente)


**Exemplo de Previsão Real**

Entrada (X) = `[0.35, 0.92, 45]`  
Saída (y) = `[3]` 
**Significado da saída:** Categoria `3` = Elegível


- As variáveis de entrada foram padronizadas com `StandardScaler` para melhor desempenho do KNN.
- O valor ideal de **K** foi escolhido com base na maior acurácia sobre o conjunto de teste.


## Arquivos Fornecidos

modelo salvo com `joblib` no arquivo:
- `modelo_knn_elegibilidade_de_credito.pkl`  
  Contém:
  - O modelo KNN pré-treinado (`modelo_elegibilidade`)
  - O normalizador `StandardScaler` utilizado (`padronizador`)




