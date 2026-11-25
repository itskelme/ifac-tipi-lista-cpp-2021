# Lista 3 de C/C++

> Resoluções da lista 3 de exercícios de programação em C/C++ do curso técnico integrado em Informática para Internet do IFAC.

**Contexto:** IFAC · Técnico em Informática para Internet integrado ao ensino médio (TIPI) · Programação em C/C++, lista 3 · Prof. Breno · 2021

## Sobre

Resoluções feitas em dupla para a terceira lista de exercícios de programação. São programas de console curtos, cada um resolvendo um problema de matemática, física, química ou do dia a dia, para praticar entrada e saída, operadores, condicionais (`if`, `switch`) e laços (`for`, `while`, `do-while`).

Os arquivos têm extensão `.cpp`, mas o código usa o estilo de C (`stdio.h`, `printf`, `scanf`). Cada arquivo `questao-NN` resolve a questão de mesmo número; nem todas as questões da lista estão aqui.

## Conteúdo

| Questão | O que faz |
|---|---|
| [01](questao-01.cpp) | Calcula a área de um trapézio em cm² ou m², escolhendo a unidade por menu e validando que as medidas sejam positivas |
| [02 (C)](questao-02.c) / [02 (C++)](questao-02.cpp) | Calcula a área de um círculo a partir do raio; as duas versões fazem a mesma coisa |
| [03](questao-03.cpp) | Calcula a distância entre dois pontos no plano cartesiano |
| [04](questao-04.cpp) | Lê *n* números e mostra o maior, o menor, a quantidade de pares e de ímpares e a média |
| [05](questao-05.cpp) | Converte o peso da pessoa na Terra para o peso equivalente em cada planeta do Sistema Solar |
| [06](questao-06.cpp) | Imprime e soma os múltiplos de 7 entre 100 e 300 |
| [07](questao-07.cpp) | Converte um valor em km para m, cm e mm |
| [08](questao-08.cpp) | Imprime a sequência de Fibonacci até o *n*-ésimo termo |
| [09](questao-09.cpp) | Calcula o termo *aₙ* de uma progressão aritmética a partir de *a₁*, da razão e de *n* |
| [10](questao-10.cpp) | Calcula o termo *aₙ* de uma progressão geométrica a partir de *a₁*, da razão e de *n* |
| [11](questao-11.cpp) | Calcula H = 1 × 1/4 × 1/9 × ... × 1/n² |
| [12](questao-12.cpp) | Lê número atômico e número de massa de três elementos e diz quais são isótopos, isótonos ou isóbaros entre si |
| [13](questao-13.cpp) | Verifica se um número inteiro positivo é primo, contando seus divisores |
| [15](questao-15.cpp) | Calcula o tempo e a distância em que um carro (partindo do repouso, com aceleração constante) alcança um caminhão em velocidade constante |
| [18](questao-18.cpp) | Calcula a velocidade média de um móvel a partir das posições e dos tempos inicial e final |
| [20](questao-20.cpp) | Calcula uma potência com expoente natural usando laço, sem `pow` |
| [21](questao-21.cpp) | Converte uma temperatura de °C para °F e K |
| [22](questao-22.cpp) | Calcula a média geométrica de 4 números reais |
| [23](questao-23.cpp) | Calcula o capital final de uma poupança após um ano, com juros simples |
| [24](questao-24.cpp) | Diz se a acetona, numa temperatura informada, está abaixo do ponto de fusão (-94,6 °C), acima do ponto de ebulição (56,1 °C), entre os dois ou exatamente em um deles |
| [241](questao-241.cpp) | Calcula a distância entre duas pessoas nas extremidades de uma caverna pelo tempo do eco (som a 343 m/s) e quantos passos de 0,82 m isso dá. Apesar do nome, é um problema diferente da questão 24 |
| [25](questao-25.cpp) | Calcula, em litros, o volume de água de um reservatório cilíndrico cheio a 80% |
| [27](questao-27.cpp) | Diz se um país é da América do Sul pelo código telefônico internacional (DDI) |
| [29](questao-29.cpp) | Converte para reais os valores em dólar, euro e libra de *n* pessoas e mostra o total (cotações de 2021 fixas no código) |
| [31](questao-31.cpp) | Calcula em quantos dias se chega de Rio Branco a cada capital brasileira, dada uma velocidade constante (distâncias fixas no código, escolha por menu) |
| [34](questao-34.cpp) | Conta as vogais não acentuadas de uma frase lida caractere por caractere |
| [37](questao-37.cpp) | Soma os logaritmos de dois números inteiros positivos, cada um na base informada |

## Tecnologias / Formatos

- **C/C++**: código em estilo C (`stdio.h`, `stdlib.h`, `math.h`, `locale.h`), compilável com `g++`
- `setlocale(LC_ALL, "Portuguese")` para acentuação no console do Windows
- `system("cls")` e `system("pause")` para limpar e pausar a tela no Windows

## Estrutura do projeto

```
ifac-tipi-lista-cpp-2021/
├── questao-01.cpp ... questao-37.cpp   # uma resolução por arquivo
├── questao-02.c                        # versão em C da questão 2
├── LICENSE
└── README.md
```

## Como rodar

É preciso ter o GCC instalado (no Windows: [MSYS2](https://www.msys2.org/) ou MinGW; no Linux: pacote `build-essential` ou equivalente).

Uma questão:

```bash
g++ -o questao-01 questao-01.cpp
./questao-01
```

A versão em C da questão 2:

```bash
gcc -o questao-02-c questao-02.c
./questao-02-c
```

Todas de uma vez (bash):

```bash
for f in questao-*.cpp; do g++ -o "${f%.cpp}" "$f"; done
```

Observações:

- Os programas foram feitos para o console do Windows. No Linux eles rodam, mas `system("cls")` mostra um aviso de comando não encontrado e não limpa a tela.
- Os arquivos misturam as codificações ISO-8859-1 e UTF-8, e em alguns os acentos das mensagens se perderam. Dependendo do terminal, os textos podem aparecer com caracteres trocados; o cálculo não é afetado.
- O código foi mantido como foi entregue em 2021. A questão 01 tem falhas conhecidas: o `;` depois de `if (lowerBase == greaterBase)` faz o aviso de bases iguais aparecer sempre, e na opção 2 um `break` dentro do `do-while` impede a validação da altura.

## Referências

- Material e enunciados da lista: Prof. Breno (IFAC)
- Referência da linguagem C e da biblioteca padrão: <https://en.cppreference.com/w/c>
- MIZRAHI, V. V. *Treinamento em Linguagem C*. 2. ed. São Paulo: Pearson Prentice Hall, 2008.
- SCHILDT, H. *C Completo e Total*. 3. ed. São Paulo: Makron Books, 1997.

## Autores

- Diego Kelme Santos da Silva — [@itskelme](https://github.com/itskelme)
- Caio Pontes — dupla na resolução da lista
- Prof. Breno (IFAC) — enunciados da lista

## Licença

Este projeto está sob a licença [CC BY-NC 4.0](LICENSE): uso pessoal e modificação permitidos com atribuição; uso comercial proibido. Material de terceiros (slides, provas, enunciados) pertence aos respectivos autores e não é coberto por esta licença.
