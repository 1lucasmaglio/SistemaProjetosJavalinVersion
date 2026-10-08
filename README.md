# Sistema de Gerenciamento de Projetos — Javalin

Sistema desenvolvido em **Java** para cadastro e gerenciamento de projetos.

O projeto foi desenvolvido durante as aulas com o objetivo de aplicar na prática conceitos de **orientação a objetos, organização em camadas, persistência de dados, interface gráfica e API REST**.

Esta versão utiliza o framework **Javalin** para implementar a API HTTP. O projeto também possui uma versão com **HttpServer**, disponível no [repositório principal](https://github.com/1lucasmaglio/SistemaProjetos).

---

## Como funciona?

O sistema é dividido em diferentes partes, cada uma com sua responsabilidade:

- `model` — representa os objetos do sistema.
- `service` — concentra as operações e regras relacionadas aos projetos.
- `dao` — realiza a leitura e escrita dos dados.
- `view` — contém a interface gráfica.
- `api` — disponibiliza a comunicação HTTP utilizando Javalin.

Os projetos são armazenados em um arquivo CSV, permitindo que os dados permaneçam salvos mesmo depois que o programa é encerrado.

---

## Arquitetura

```text
        VIEW
          │
          ▼
       SERVICE
          │
          ▼
         DAO
          │
          ▼
  dados/projetos.csv

API (Javalin) ─────► SERVICE
```

---

## Tecnologias utilizadas

- **Java**
- **Java Swing** — interface gráfica
- **Javalin** — API HTTP
- **Maven** — gerenciamento de dependências
- **CSV** — persistência dos dados

---

## Estrutura do projeto

```text
SistemaProjetos/
├── dados/
│   └── projetos.csv
│
├── src/main/java/
│   ├── api/
│   ├── dao/
│   ├── model/
│   ├── service/
│   ├── view/
│   └── Main.java
│
├── pom.xml
└── README.md
```

---

## Executando o projeto

### Interface gráfica

Para utilizar a interface gráfica, execute a classe responsável pela interface dentro do pacote:

```text
view/
```

### API HTTP

Para iniciar a API, execute a classe responsável pelo servidor Javalin dentro do pacote:

```text
api/
```

---

## Outras versões

O sistema possui duas implementações de servidor HTTP:

- **Javalin (este repositório):** utiliza um framework Java para implementar a API.
- **HttpServer:** utiliza o servidor HTTP disponível no JDK, sem a necessidade de frameworks externos.

A versão com HttpServer está disponível em:

[github.com/1lucasmaglio/SistemaProjetos](https://github.com/1lucasmaglio/SistemaProjetos)

---

## Status

🚧 **Em desenvolvimento**

Projeto desenvolvido e atualizado durante as aulas, acompanhando a implementação de novos conceitos e funcionalidades.
