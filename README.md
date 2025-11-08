# 🩺 Predição de Internação em UTI – Hospital Sírio-Libanês

Projeto desenvolvido na disciplina **Aprendizagem Estatística de Máquina II**, com o objetivo de aplicar técnicas de aprendizado supervisionado e não supervisionado para análise de dados clínicos e predição de internação em UTI.

---

## 🎯 Objetivo

- **Análise supervisionada:** prever a probabilidade de um paciente ser internado em UTI (`ICU = 1`), com base em variáveis demográficas, clínicas e laboratoriais.  
- **Análise não supervisionada:** identificar grupos de pacientes com perfis clínicos semelhantes, auxiliando na caracterização de grupos de risco.

Essas duas abordagens se complementam:  
enquanto a primeira busca prever **quem precisará de UTI**, a segunda busca entender **padrões e similaridades entre pacientes**.

---

## 🧩 Estrutura do repositório

📁 projeto_integrador_2tri_estatistica2/
- sirio_dados.xlsx # Base de dados original (Hospital Sírio-Libanês – Kaggle)
- dicionario_variaveis.xlsx # Dicionário de dados com descrição e relevância das variáveis
- analise_exploratoria.R # Scripts de exploração inicial e gráficos
- modelagem_supervisionada.R # Modelos: Regressão Logística, Random Forest e XGBoost
- modelagem_nao_supervisionada.R # Agrupamentos com K-Means e PCA
- README.md # Documento de apresentação do projeto


---

## ⚙️ Etapas de modelagem

1. **Tratamento de dados ausentes e padronização**  
   - Uso do pacote `recipes` (tidymodels) para normalização das variáveis.  
2. **Divisão treino/teste/validação**  
   - Garantia de validação justa dos modelos.  
3. **Ajuste e comparação de três modelos supervisionados:**  
   - Regressão Logística  
   - Random Forest  
   - XGBoost  
4. **Métricas de avaliação:**  
   - **AUC** – capacidade geral de discriminação  
   - **Acurácia** – proporção total de acertos  
   - **Sensibilidade** – acerto dos casos realmente graves (UTI)  
   - **Especificidade** – acerto dos casos não graves (evita falsos positivos)  

Essas métricas derivam da **matriz de confusão**, que resume o desempenho global do modelo.

---

## 🧠 Modelagem não supervisionada

- Seleção das variáveis contínuas (exames e sinais vitais)  
- Padronização dos dados  
- Agrupamento com **K-Means**  
- Determinação do número ótimo de clusters pelos métodos do **cotovelo** e **índice de silhueta**  
- Visualização dos grupos com **PCA** (redução de dimensionalidade)

---

## 🧾 Síntese

O projeto integra **estatística descritiva**, **aprendizado supervisionado** e **não supervisionado** para extrair conhecimento clínico relevante de uma base hospitalar real.  
Mostra como técnicas de *machine learning* podem apoiar o **diagnóstico precoce** e a **gestão hospitalar**, especialmente na priorização de pacientes com risco elevado.

---

## 📚 Fonte dos dados

Base pública disponibilizada no Kaggle:  
> [Hospital Sírio-Libanês – COVID-19 Dataset](https://www.kaggle.com/datasets/S%C3%ADrioLiban%C3%AAs/covid19)

---

## 👩‍💻 Autoria

Projeto desenvolvido no âmbito da disciplina *Aprendizagem Estatística de Máquina II*  
do Programa Avançado em Data Science e Decisão – **Insper**.

---
