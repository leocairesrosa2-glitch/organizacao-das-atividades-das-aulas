# Algoritmos e Pensamento Computacional

Exercícios em linguagem C desenvolvidos nas aulas da disciplina de **Algoritmos e Pensamento Computacional**. Cada arquivo resolve um problema simples e mostra um conceito novo de programação: entrada e saída, condições, laços, matrizes, arquivos e funções.

## Autor

- **Nome:** Leonardo Caires Rosa
- **RGM:** 48123676

## Conteúdo

| Aula | Arquivo | Problema resolvido | Conceitos |
|---|---|---|---|
| 3 | [`aula_03.c`](aulas/aula_03.c) | Perímetro da circunferência a partir do raio | variáveis, constantes, `scanf`, `printf` |
| 4 | [`aula_04.c`](aulas/aula_04.c) | Quantidade de caixas de revestimento e custo total | operadores, `math.h`, `ceil` |
| 5 | [`aula_05.c`](aulas/aula_05.c) | Valor da hospedagem por tipo de quarto e diárias | `switch`, `case`, `char` |
| 6 | [`aula_06.c`](aulas/aula_06.c) | Tabuada de um número | laço `for` |
| 7 | [`aula_07.c`](aulas/aula_07.c) | Média da turma com validação das notas (0 a 10) | `for`, `while`, validação de entrada |
| 8 | [`aula_08.c`](aulas/aula_08.c) | Matriz de vendas 3x4: leitura e exibição | matrizes, laços aninhados |
| 9 | [`aula_09.c`](aulas/aula_09.c) | Leitura de um arquivo texto linha por linha | `fopen`, `fgets`, `fclose` |
| 10 | [`aula_10.c`](aulas/aula_10.c) | Ordenação de um vetor de senhas | funções, vetores, Bubble Sort |

## Estrutura do repositório

```
projeto-4/
├── README.md
├── .gitignore
└── aulas/
    ├── aula_03.c
    ├── aula_04.c
    ├── ...
    ├── aula_10.c
    └── tabuada.txt     (arquivo lido pela aula 9)
```

## Pré-requisitos

- Um compilador C, como o **GCC**.
  - Linux e macOS: normalmente já vem instalado (`gcc --version` para conferir).
  - Windows: instale o MinGW ou use o WSL.
- Sem compilador instalado, dá para testar no navegador com o [GDB Online](https://www.onlinegdb.com/).

## Como compilar e executar

Entre na pasta das aulas:

```bash
cd aulas
```

Compile e execute uma aula (exemplo com a aula 3):

```bash
gcc aula_03.c -o aula_03.out
./aula_03.out
```

No Windows (PowerShell ou CMD):

```bash
gcc aula_03.c -o aula_03.exe
aula_03.exe
```

Para compilar todas de uma vez (Linux, macOS ou Git Bash):

```bash
for f in aula_*.c; do gcc "$f" -o "${f%.c}.out" -lm; done
```

## Exemplos de execução

**Aula 3: perímetro da circunferência**

```
Digite o raio da peça em centímetros: 10
Perímetro da circunferência: 62.83 cm
```

**Aula 4: revestimento (área de 4 m x 5 m, caixa a R$ 80,00)**

```
Qual e a largura da area (em metros)? 4
Qual e o comprimento da area (em metros)? 5
Qual e o valor de cada caixa? 80

Area total a ser revestida: 20.00 m^2
Quantidade de caixas necessarias: 8
Custo total da compra: R$ 640.00
```

**Aula 10: Bubble Sort**

```
Senhas antes da ordenação:
35 12 58 7 19 
Senhas depois da ordenação:
7 12 19 35 58 
```

## Observações

- A **aula 4** usa `math.h`, então precisa ser compilada com `-lm`: `gcc aula_04.c -o aula_04.out -lm`.
- A **aula 9** lê o arquivo `tabuada.txt`, que deve estar na mesma pasta de onde o programa é executado (a pasta `aulas`).
- No terminal do Windows, os acentos das mensagens podem aparecer errados. Isso não afeta o funcionamento dos programas.
- Os executáveis gerados (`*.out`, `*.exe`) são ignorados pelo Git por causa do `.gitignore`.
