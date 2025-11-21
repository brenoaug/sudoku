# Sudoku

Projeto em Java para resolver / manipular tabuleiros de Sudoku. Este repositório contém a implementação de um resolvedor e utilitários para carregar, validar e imprimir tabuleiros Sudoku 9x9.

> Observação: ajuste os comandos de compilação/execução conforme a estrutura real do seu projeto (Maven/Gradle/nome do pacote e classe principal).

## Tabela de conteúdo
- [Sobre](#sobre)
- [Funcionalidades](#funcionalidades)
- [Pré-requisitos](#pré-requisitos)
- [Como compilar e executar](#como-compilar-e-executar)
  - [Usando javac/java (manual)](#usando-javacjava-manual)
  - [Usando Maven](#usando-maven)
  - [Usando Gradle](#usando-gradle)

## Sobre
Este projeto implementa lógica para:
- Resolver tabuleiros Sudoku 9x9 (backtracking, heurísticas, etc.),
- Validar a integridade de um tabuleiro,
- Ler e escrever tabuleiros em formato de texto,
- (Opcional) Gerar puzzles com níveis simples de dificuldade.

O objetivo é servir como material didático para aprendizado de algoritmos de busca e estruturas de dados em Java, além de ser uma base para desafios e extensões.

## Funcionalidades
- Leitura de tabuleiro em formato texto (linha por linha).
- Resolução do tabuleiro preenchendo células vazias.
- Verificação de validade (linhas, colunas, subblocos 3x3).
- Impressão do tabuleiro em formato legível.

## Pré-requisitos
- Java 8 ou superior
- (Opcional) Maven ou Gradle, se preferir usar um sistema de build

## Como compilar e executar

A seguir há opções genéricas — ajuste os nomes de pacotes e da classe principal conforme seu código.

### Usando javac/java (manual)
1. Compile:
   - Unix / macOS:
     javac -d out $(find src -name "*.java")
   - Windows (PowerShell):
     Get-ChildItem -Recurse -Filter *.java | ForEach-Object { & javac -d out $_.FullName }

2. Execute (substitua `com.example.Main` pela sua classe com método main):
   java -cp out com.example.Main

### Usando Maven
Se o projeto usa Maven (possui `pom.xml`):
- Compilar e empacotar:
  mvn clean package
- Executar JAR gerado (substitua o nome do JAR se diferente):
  java -jar target/dio-sudoku-1.0.jar

### Usando Gradle
Se o projeto usa Gradle (possui `build.gradle`):
- Compilar:
  ./gradlew build
- Executar (caso configure um jar executável) ou execute a classe principal via `run` se usar o plugin application:
  ./gradlew run

## Formato de entrada / exemplo de uso
Uma forma simples de representar um tabuleiro é usar 9 linhas com 9 caracteres cada, `0` ou `.` para células vazias. Exemplo:

```
530070000
600195000
098000060
800060003
400803001
700020006
060000280
000419005
000080079
```

Saída esperada (tabuleiro resolvido):

```
534678912
672195348
198342567
859761423
426853791
713924856
961537284
287419635
345286179
```


