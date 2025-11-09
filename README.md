# README — Modelo de Otimização de Habilidades (MOH)

## Visão Geral

O MOH (Modelo de Otimização de Habilidades) é uma ferramenta que auxilia o Profissional do Futuro a planejar a aquisição de habilidades estratégicas, considerando valor profissional, adaptabilidade, tempo disponível e complexidade das competências. O sistema inclui simulação de incertezas, análise de desempenho e recomendações personalizadas.

## Estrutura do Projeto

- `bloco1_imports_config.py` — Configuração inicial, carregamento das habilidades e imports.
- `bloco2_funcoes_auxiliares.py` — Funções de métricas, verificação de grafo e pré-requisitos.
- `bloco3_desafio1.py` — Caminho de Valor Máximo (determinístico e Monte Carlo).
- `bloco4_desafio2.py` — Verificação Crítica de habilidades.
- `bloco5_desafio3.py` — Seleção gulosa de habilidades básicas (V/T).
- `bloco6_desafio4.py` — Ordenação das habilidades (Merge Sort e Sort nativo) e sprints.
- `bloco7_desafio5.py` — Recomendações de próximas habilidades com probabilidades simuladas.
- `ConjuntoDeDadosMestre.csv` — Arquivo CSV com a base de habilidades, incluindo colunas: `ID`, `Nome`, `Tempo`, `Valor`, `Complexidade`, `Pre_Reqs`.

## Requisitos

- Python 3.8+

### Bibliotecas

- `numpy`
- `matplotlib`
- `psutil`
- `pandas`

Instale as dependências com:

```bash
pip install numpy matplotlib psutil pandas

```

### Imports usados no projeto

```python
import itertools           # Para combinações e permutações de habilidades
import random              # Para simulação Monte Carlo e embaralhamento
import time                # Para medir tempo de execução
import psutil              # Para medir uso de memória
import numpy as np         # Para cálculos numéricos e estatísticos
import matplotlib.pyplot as plt  # Para gráficos de visualização
import pandas as pd        # Para manipulação de dados tabulares (CSV)

```

## Como Executar

Clone ou baixe o repositório.

Crie e ative o ambiente virtual:

```bash
py -m venv .venv
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.venv\Scripts\activate

```

Instale as dependências:

```bash
pip install numpy pandas matplotlib psutil

```

O script principal carregará automaticamente as habilidades do CSV `ConjuntoDeDadosMestre.csv` e executará todos os desafios, exibindo os resultados, métricas de tempo e memória, e gráficos de visualização.

## Saídas Esperadas

- Listas de habilidades recomendadas ou ordenadas.
- Métricas de desempenho: tempo de execução e memória utilizada.
- Gráficos comparativos:
    - Valor total vs Tempo vs Memória (Desafio 1)
    - Custo total das sequências críticas (Desafio 2)
    - Eficiência (V/T) das habilidades básicas (Desafio 3)
    - Complexidade das habilidades por Sprint (Desafio 4)
    - Probabilidade de próximas habilidades (Desafio 5)

## Personalização

- Alterar ou adicionar novas habilidades no arquivo CSV `ConjuntoDeDadosMestre.csv`.
- Modificar tempos (`Tempo`), valores (`Valor`) e complexidade (`Complexidade`) para testar cenários distintos.
- Ajustar número de simulações Monte Carlo (`N_SIM`) no Desafio 1.

## Observações Técnicas

- Todos os grafos de habilidades são validados antes da execução para evitar ciclos ou pré-requisitos inexistentes.
- Seleção gulosa e heurísticas são comparadas com soluções ótimas ou determinísticas quando aplicável.
- Métricas de tempo e memória são calculadas usando `psutil` para controle de desempenho do sistema.

## Autor
- Autor: Gustavo Viega
- Autor: Kaio Drago
