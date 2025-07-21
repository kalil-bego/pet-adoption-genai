# 🧬 Matching Inteligente entre Pets e Adotantes usando Algoritmo Genético

## 📌 Definição do Problema

A adoção de pets envolve diversos fatores subjetivos e logísticos: porte do animal, tipo de moradia do adotante, tempo disponível, presença de crianças, entre outros. Fazer o "match ideal" entre pet e adotante não é trivial e exige múltiplos critérios simultâneos.

Este projeto utiliza **Algoritmo Genético (AG)** para otimizar a atribuição entre um conjunto de pets disponíveis para adoção e um conjunto de adotantes cadastrados. O objetivo é maximizar a **compatibilidade entre pares**, levando em conta preferências e restrições de ambos os lados.

---

## 🎯 Objetivo

Criar um sistema baseado em Algoritmo Genético que:

- Receba dados de pets e adotantes;
- Avalie a compatibilidade entre cada par;
- Encontre a melhor combinação global (máximo de compatibilidade total);
- Visualize o progresso em tempo real durante a evolução do AG.

---

## ✅ Critérios de compatibilidade considerados na função de fitness:

- Preferência do adotante por tipo e porte do pet;
- Porte grande com moradia em apartamento;
- Pelagem longa com presença de alergia;
- Tempo disponível x energia/idade do pet;
- Vacinação, vermifugação e esterilização;
- Condição de saúde do pet;
- Presença de crianças na casa do adotante.

Cada par recebe um **score entre 0 e 100**, e o algoritmo busca maximizar a soma total desses scores.

---

## ⚙️ Implementação

O projeto foi implementado em Python utilizando Jupyter Notebook e as bibliotecas:

- `pandas`: manipulação dos dados;
- `matplotlib`: visualização e animação;
- `IPython.display`: renderização em tempo real;
- `random`: evolução da população.

O cromossomo do AG representa um vetor onde cada gene indica qual adotante foi atribuído a qual pet.

A função de fitness avalia cada match (pet ↔ adotante) individualmente, e soma os scores para calcular a aptidão total do indivíduo.

### 🔄 Operações do AG:
- **Seleção elitista** (top 20%);
- **Crossover** por ponto único;
- **Mutação aleatória** com taxa de 10%;
- **População inicial** aleatória.

---

## 📊 Visualização

Durante a execução do algoritmo, o sistema exibe:

- Um gráfico **em tempo real** com a evolução da fitness por geração;
- Uma visualização interativa do matching:
  - Pets distribuídos em colunas (🐶),
  - Adotantes alinhados à direita (🧍),
  - Conexões coloridas (vermelho → verde) e top 3 destacadas em azul;
  - Score exibido sobre cada linha de match.

---

## 🧪 Testes e Resultados

Testes realizados com:
- 100 pets simulados com características variadas;
- 20 adotantes gerados com preferências realistas.

**Resultado esperado**: a partir de uma população aleatória, o algoritmo converge para combinações mais compatíveis em poucas gerações (em média < 40), elevando o score médio de ~40 para ~90+.

### Comparação com abordagem aleatória:
- Versão aleatória: fitness média < 60;
- Com AG: fitness média final > 90 (com top 3 matches ideais).

---

## 🧾 Arquivos entregues

- `pet-adoption-genai.ipynb` — código completo da solução com visualização integrada;
- `README.md` — este documento;
- `raw-data/adotantes.csv` e `raw-data/pets.csv` — dados simulados;
- `analytical-base-table.csv` — base combinada pet × adotante com features normalizadas.

---

## 🧠 Conclusão

O projeto demonstra a eficácia do Algoritmo Genético para resolver um problema real e multidimensional de otimização, que envolve preferências, condições físicas e comportamentais.

A metodologia é aplicável a outros contextos de matching com múltiplos critérios — como alocação de recursos, formação de equipes e sistemas de recomendação.

---

## 👨‍💻 Desenvolvedores

- Kalil Bego Rocha
- José Paulo Marinho da Silva