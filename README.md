# Análise de Algoritmos Aproximativos: Problema da Mochila (Knapsack Problem)

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Status](https://img.shields.io/badge/Status-Concluído-success)
![Subject](https://img.shields.io/badge/Disciplina-Análise_de_Algoritmos-orange)

Este repositório contém a implementação e análise comparativa de meta-heurísticas para a resolução do **Problema da Mochila 0/1** (*Knapsack Problem*), desenvolvido como parte da avaliação da disciplina de **Análise e Projeto de Algoritmos**.

## 👥 Equipe

* **Antonio Heitor Gomes Azevedo**
* **Deivison Ryan Brito Tavares**
* **Gustavo Yuji Virgolino Nishimura**
* **Heitor Yasuo Yamamoto**

---

## 📝 Sobre o Projeto

O **Problema da Mochila** é um clássico da otimização combinatória, classificado como **NP-Difícil** (*NP-Hard*). Devido à sua complexidade exponencial O(2^n), encontrar a solução exata via força bruta torna-se inviável para grandes conjuntos de dados.

Este projeto explora duas abordagens aproximativas para encontrar soluções sub-ótimas de alta qualidade em tempo polinomial:

1.  **Particle Swarm Optimization (PSO):** Algoritmo baseado em inteligência de enxame.
2.  **Simulated Annealing (SA):** Algoritmo probabilístico baseado no processo de recozimento de metais.

### Objetivos
* Implementar algoritmos bio-inspirados em Python.
* Comparar desempenho (Tempo de CPU vs. Qualidade da Solução).
* Analisar a estabilidade (Desvio Padrão) em diferentes tamanhos de instância.

---

## ⚙️ Tecnologias e Configurações

O projeto foi desenvolvido em **Python 3**, utilizando apenas bibliotecas nativas para garantir facilidade de execução.

### Algoritmos Implementados

| Algoritmo | Complexidade Big-O | Parâmetros Principais |
| :--- | :--- | :--- |
| **PSO** | $O(I \cdot P \cdot n)$ | População: 30 \| Iterações: 200 \| $w$: 0.7 \| $c1, c2$: 1.5 |
| **Simulated Annealing** | $O(I \cdot n)$ | $T_0$: 100 \| Resfriamento: 0.99 \| Iterações: 3000 |

*Onde I = iterações, P = partículas, n = número de itens.*

---

## 🚀 Como Executar

1. **Pré-requisitos:** Certifique-se de ter o [Python 3.x](https://www.python.org/) instalado.
2. **Clonar o repositório:**
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
   cd nome-do-repositorio

3.   Executar:
   
   `python main.py`

📊 Resultados ObtidosOs testes foram realizados com 100 execuções independentes para cada instância (n=10, 30, 100). Abaixo, o resumo dos resultados para a instância grande (N=100):

Métrica,PSO,Simulated Annealing,Análise
Melhor Valor,3174,3170,Empate Técnico
Média,2928.32,2459.50,PSO +19% Superior
Estabilidade,Alta (σ≈67),Baixa (σ≈271),PSO mais confiável
Tempo Médio,0.525s,0.048s,SA 10x Mais Rápido


Conclusão dos Experimentos
Qualidade: O PSO mostrou-se superior para encontrar soluções de maior valor consistentemente, evitando ótimos locais graças à sua abordagem populacional.

Velocidade: O Simulated Annealing confirmou sua eficiência teórica, sendo ideal para cenários onde o tempo de resposta é crítico, mesmo sacrificando a precisão média.

📚 Estrutura do Repositório
├── main.py          # Código fonte contendo PSO, SA e gerador de instâncias
├── Relatorio.pdf    # Relatório técnico detalhado (Teoria e Resultados)
├── README.md        # Documentação do projeto
└── slides/          # Apresentação do projeto
