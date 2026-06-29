# 📊 Algoritmos de Ordenação em C++

Trabalho de implementação e comparação de três algoritmos clássicos de ordenação aplicados sobre um arquivo de registros importado em tempo de execução.

---

## 📁 Estrutura do Projeto

```
.
├── Trab.cpp                        # Código-fonte principal
├── ARQIMPORT.txt                   # Arquivo de entrada com os registros
├── resultado_ordenacao.txt         # Gerado ao executar — contém os resultados
└── Algoritmos_de_Ordenacao.docx    # Documentação técnica dos algoritmos
```

---

## ⚙️ Como Compilar e Executar

### Pré-requisitos
- Compilador C++ com suporte a C++11 ou superior (g++, clang++)

### Compilar
```bash
g++ -O2 -o Trab Trab.cpp
```

### Executar
```bash
./Trab
```

> **Atenção:** o arquivo `ARQIMPORT.txt` deve estar na **mesma pasta** do executável.

---

## 📋 Formato do Arquivo de Entrada

Cada linha do `ARQIMPORT.txt` deve conter um código numérico de 3 dígitos seguido de palavras-chave separadas por espaço:

```
001 FINANCEIRO INVESTIMENTO RENDA GASTOS DESPESAS LUCRO
002 CONTABILIDADE BALANÇO BALANCETE RAZÃO ENTRADA SAÍDA
...
```

---

## 🔀 Algoritmos Implementados

### 1. Shell Sort
Extensão do Insertion Sort que compara elementos distantes usando intervalos (gaps) decrescentes. Utiliza a sequência de gaps de Knuth (`1, 4, 13, 40, ...`).

| Complexidade | Valor |
|---|---|
| Melhor caso | O(n log n) |
| Caso médio | O(n log² n) |
| Pior caso | O(n²) |
| Espaço extra | O(1) |

---

### 2. Heap Sort
Constrói um max-heap a partir do vetor e extrai o maior elemento repetidamente para obter a ordenação. In-place e com complexidade garantida.

| Complexidade | Valor |
|---|---|
| Melhor caso | O(n log n) |
| Caso médio | O(n log n) |
| Pior caso | O(n log n) |
| Espaço extra | O(1) |

---

### 3. Merge Sort
Divide o vetor recursivamente ao meio e mescla as metades ordenadas. Algoritmo estável baseado em dividir e conquistar.

| Complexidade | Valor |
|---|---|
| Melhor caso | O(n log n) |
| Caso médio | O(n log n) |
| Pior caso | O(n log n) |
| Espaço extra | O(n) |

---

## 📤 Saída Esperada

O programa exibe no terminal e salva em `resultado_ordenacao.txt` os registros ordenados por cada algoritmo, além do tempo de execução de cada um:

```
==========================================
  SHELL SORT
==========================================
001 FINANCEIRO INVESTIMENTO RENDA GASTOS DESPESAS LUCRO
002 CONTABILIDADE BALANÇO ...
...
Tempo Shell Sort: 0.012 ms

==========================================
  HEAP SORT
==========================================
...

==========================================
  MERGE SORT
==========================================
...
```

---

## 🚀 Como enviar para o GitHub

### Primeira vez (criar repositório)

1. Acesse [github.com](https://github.com) e crie um repositório novo (ex: `algoritmos-ordenacao`)
2. No terminal, dentro da pasta do projeto:

```bash
git init
git add .
git commit -m "primeiro commit - algoritmos de ordenacao"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/algoritmos-ordenacao.git
git push -u origin main
```

### Atualizações futuras

```bash
git add .
git commit -m "descricao da mudanca"
git push
```

---

## 👨‍💻 Autor

André Luiz Faria Vitor
