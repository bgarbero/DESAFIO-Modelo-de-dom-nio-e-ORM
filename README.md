
# Desafio: Modelo de Domínio e ORM

## 📚 Descrição do Desafio

Este repositório contém a solução para o desafio proposto no módulo **Back End** do curso **Java Spring Professional** da [DevSuperior](https://devsuperior.com.br). O objetivo é implementar um sistema que gerencie informações de **atividades acadêmicas** e **participantes** utilizando **Spring Boot**, **Java** e banco de dados **H2** em memória, com foco na criação do modelo de domínio e mapeamento ORM com JPA.

---

## 📝 Requisitos do Desafio

- Criar um projeto Spring Boot com Java e banco H2.
- Implementar o modelo de domínio conforme o diagrama conceitual fornecido.
- Realizar o seeding da base de dados conforme a instância de dados proposta.
- Assegurar que o sistema seja executável sem erros e que os dados possam ser visualizados no H2 Console.

---

## 📌 Especificação

O sistema é responsável por:

- Cadastrar **participantes** com nome e email.
- Cadastrar **atividades** com nome, descrição e preço.
- Associar cada atividade a uma **categoria** (curso, oficina, etc.).
- Associar cada atividade a um ou mais **blocos de horário** com data, início e fim.
- Registrar quais participantes estão inscritos em quais atividades (relação muitos-para-muitos).

---

## 📦 Estrutura do Domínio

- **Participante**: nome, email.
- **Atividade**: nome, descrição, preço, categoria.
- **Categoria**: descrição.
- **Bloco**: data, hora de início e fim.
- **Relacionamentos**:
  - Atividade ↔ Categoria: muitos-para-um.
  - Atividade ↔ Bloco: muitos-para-muitos.
  - Participante ↔ Atividade: muitos-para-muitos.

---

## 🧪 Dados de Seeding

Os dados iniciais são inseridos automaticamente ao executar a aplicação e incluem:

- 2 categorias: Curso, Oficina.
- 3 blocos de horário com datas e intervalos distintos.
- 2 atividades: Curso de HTML e Oficina de GitHub.
- 4 participantes com seus respectivos vínculos às atividades.

---

## ⚙️ Tecnologias Utilizadas

- Java 21
- Spring Boot 3.4.4
- Spring Data JPA
- Banco de Dados H2 (console ativo)
- Maven

---

## ▶️ Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/bgarbero/DESAFIO-Modelo-de-dom-nio-e-ORM.git
   ```

2. Importe o projeto em sua IDE (Eclipse, IntelliJ, VS Code).

3. Execute a aplicação pelo método `main()` da classe principal.

4. Acesse o H2 Console no navegador:
   ```
   http://localhost:8080/h2-console
   ```

   Use as configurações:
   - JDBC URL: `jdbc:h2:mem:testdb`
   - User: `sa`
   - Password: (em branco)

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais e de prática dos conceitos de **modelo de domínio e ORM com Spring Boot**.
