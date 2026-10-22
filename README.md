# Screenmatch

Aplicação de console em Java com Spring Boot que consome a API pública do OMDb e converte a resposta JSON em objetos Java. Projeto desenvolvido durante a formação Java da Alura.

## O que a aplicação faz

1. Faz uma requisição HTTP à [OMDb API](https://www.omdbapi.com/) buscando os dados de uma série.
2. Converte o JSON recebido em um `record` Java com Jackson.
3. Exibe no console o título, o total de temporadas e a avaliação no IMDb.

## Conceitos praticados

- Consumo de API REST com `HttpClient` do Java
- Desserialização de JSON com Jackson (`@JsonAlias` e `@JsonIgnoreProperties`)
- Uso de `records` para representar dados imutáveis
- Interface genérica de conversão (`IConverteDados`), desacoplando a conversão do tipo de dado
- `CommandLineRunner` para executar código ao iniciar uma aplicação Spring Boot

## Tecnologias

- Java 17
- Spring Boot 3
- Jackson
- Maven

## Como rodar localmente

Pré-requisitos: Java 17+ e uma chave gratuita da [OMDb API](https://www.omdbapi.com/apikey.aspx).

```bash
git clone https://github.com/gustavoVitor504/screenmatch-sem-web.git
cd screenmatch-sem-web
```

Defina a chave da API:

```bash
# Linux/macOS
export OMDB_API_KEY=sua_chave
# Windows (PowerShell)
$env:OMDB_API_KEY="sua_chave"
```

Execute:

```bash
./mvnw spring-boot:run
```

## Autor

**Gustavo Vitor Ferreira Nunes** — [LinkedIn](https://www.linkedin.com/in/gustavovitorferreira/) · [GitHub](https://github.com/gustavoVitor504)
