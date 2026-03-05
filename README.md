# MVP Análise de Dados e Boas Práticas - EmoPiano

**Autor:** Ricardo Fernandes de Almeida  
**Disciplina:** Sprint - Análise de Dados e Boas Práticas (MVP)  
**Data:** Abril 2026  
**Especialização em Ciência de Dados - PUC Rio**

**Dataset:** [EmoPiano: Dataset for Emotion Recognition in Piano](https://www.kaggle.com/datasets/ziya07/emopiano-dataset-for-emotion-recognition-in-piano)

---

## Descrição do Problema

O conjunto de dados EmoPiano foi projetado para o reconhecimento de emoções em composições de piano. Ele contém diversas características musicais e emocionais, tornando-o um recurso ideal para análise de sentimentos em musicologia computacional e tarefas de detecção de emoção assistida por IA. O objetivo principal é classificar a emoção de uma peça de piano (feliz, triste, com raiva, relaxada) com base em suas características extraídas.

Este é um problema de **classificação supervisionada**.

---

## Hipóteses do Problema

As hipóteses que guiaram esta análise foram:

1.  **As diferentes emoções podem ser distinguidas com base nas características musicais como tempo, `dynamic_range`, e `MFCCs`?**
2.  **Existe uma correlação entre as características de áudio (`MFCCs`, `Chroma`) e os indicadores de emoção `valence` e `arousal`?**
3.  **Composições com andamento (`tempo`) mais rápido tendem a ser classificadas como 'feliz' ou 'com raiva', enquanto as mais lentas são 'tristes' ou 'relaxadas'?**

---

## Análise Exploratória de Dados (EDA)

A análise exploratória do dataset EmoPiano revelou padrões importantes que conectam características musicais a emoções.

-   **Balanceamento do Dataset:** O dataset é perfeitamente balanceado, contendo 50 amostras para cada uma das quatro emoções (angry, happy, relaxed, sad).
-   **Distribuições:** A análise de histogramas para `tempo` e `dynamic_range` mostrou distribuições variadas que sugerem diferenças entre as classes.
-   **Relações entre Atributos:** Boxplots de `valence` (positividade) e `arousal` (intensidade) por emoção indicaram que essas características são discriminantes importantes. Por exemplo, músicas "felizes" e "com raiva" tendem a ter maior `arousal`.
-   **Matriz de Correlação:** A análise de correlação mostrou relações lineares entre as diversas características de áudio (`MFCCs`, `Chroma`) e os eixos emocionais de `valence` e `arousal`, reforçando seu potencial preditivo.

---

## Conclusões

A análise exploratória do dataset EmoPiano forneceu uma base sólida para a construção de um modelo de classificação de emoções musicais e permitiu validar as hipóteses iniciais:

1.  **Diferenças entre emoções:** Sim, características como `tempo` e `dynamic_range` mostram distribuições distintas para diferentes emoções, o que pode ser usado para a classificação.
2.  **Correlação com `valence` e `arousal`:** Sim, as características de áudio (`MFCCs` e `Chroma`) apresentam correlações com os eixos emocionais, indicando seu potencial preditivo.
3.  **Relação `tempo`-emoção:** Sim, músicas mais rápidas (`tempo` mais alto) tendem a ser associadas a emoções de alta energia como 'angry' e 'happy', enquanto as mais lentas estão associadas a emoções de baixa energia como 'sad' e 'relaxed'.

O dataset mostrou-se limpo (sem valores nulos) e bem estruturado, o que facilita as próximas etapas de modelagem.
