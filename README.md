# Sistema de Notas e Frequência Escolares

Este projeto é um teste prático do processe seletivo da Dti Digital. A aplicação é full-stack e tem como objetivo auxiliar professores na organização das notas e da frequência de seus alunos.

## Descrição

O sistema permite que o professor registre as notas (0a 10) dos alunos em cinco diciplinas diferentes, além de monitorar a presença dos alunos em cada aula. Automaticamente, o sistema calcula: 

1. A média das notas de cada aluno;
2. A média da turma em cada disciplina;
3. A frequência geral de cada aluno.

Além disso, o sistema identifica e destaca:

1. Alunos com média de notas superior à média da turma;
2. Alunos com frequência inferior a 75%, que precisam de atenção especial.

Caso não haja alunos com média superior à média da turma ou com frequência abaixo de 75%, o sistema exibirá uma linha vazia. 

## Tecnologias e Ferramentas

- **Spring Boot**
- **Spring Data JPA**
- **MySQL**
- **Maven**

## Pré-requisitos

- JDK 17
- Maven
- MySQL

## Premissas Assumidas

Para garantir o funcionamento correto do projeto, as seguintes premissas foram consideradas: 

1. **Ambiente de Desenvolvimento**:
   - Java JDK 17 ou superior instalado.
   - Maven 3.8.1 ou superior instalado.
   - IDE compatível, como IntelliJ IDEA ou VS Code.

2. **Banco de Dados**:
   - MySQL instalado e rodando na máquina de desenvolvimento. O banco de dados deve estar configurado com as credenciais corretas no arquivo `application.properties`.

3. **Conhecimento Prévio**: 
   - É assumido que o usuário possui conhecimentos básicos de Java, Spring Boot e conceitos de API RESTful.

## Estrutura do Projeto

### Backend
- Java 17
- Maven
- MySQL

### Frontend
- Node.js
- npm (ou Yarn)

## Dependências

- `spring-boot-starter-web`: inclui os recursos essenciais para o desenvolvimento de aplicações web.
- `spring-boot-devtools`: ferramenta de desenvolvimento que facilita o processo de codificação, permitindo o reinínio automático da aplicação durante o desenvolvimento.
- `mysql-connector-j`:driver JDBC necessário para conectar a aplicação ao banco de dados MySQL.
- `spring-boot-starter-test`: essencial para garantir a qualidade do código durante o desenvolvimento.

## Configuração do Backend

1. **Instale o Java 17**

   Certifique-se de que o Java 17 está instalado em sua máquina. Você pode verificar a versão do Java instalada executando:

   ```bash
   java -version
   ```

   Se não estiver instalado, baixe o Java 17 [aqui](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html).

2. **Instale o Maven**

   O Maven é usado para gerenciar dependências e construir o projeto. Verifique se o Maven está instalado executando:

   ```bash
   mvn -version
   ```

   Se não estiver instalado, você pode seguir as instruções [aqui](https://maven.apache.org/install.html).

3. **Configuração do Banco de Dados**

   O projeto utiliza MySQL. Certifique-se de que o MySQL está instalado e em execução.

   - Crie um banco de dados chamado `sne` (ou qualquer outro nome de sua preferência).
   - Configure o arquivo `application.properties` para se conectar ao seu banco de dados. Exemplo:
   
   ```properties
      spring.datasource.url=jdbc:mysql://localhost:3306/sne
      spring.datasource.username=seu_usuario
      spring.datasource.password=sua_senha
      spring.jpa.hibernate.ddl-auto=update
   ``` 


4. **Compilar e Executar o Backend**

   Navegue até o diretório raiz do backend e execute o Maven para compilar e rodar o projeto:

   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

   O backend estará rodando em `http://localhost:3030`.

## Configuração do Frontend

1. **Instale o Node.js**

   O frontend requer Node.js. Verifique se está instalado executando:

   ```bash
   node -v
   ```

   Se não estiver instalado, baixe e instale o Node.js [aqui](https://nodejs.org/).

2. **Instale as Dependências do Projeto**

   Navegue até o diretório do frontend e instale as dependências com npm ou Yarn:

   Usando npm:

   ```bash
   npm install
   ```

   Usando Yarn:

   ```bash
   yarn install
   ```

3. **Configurar o Endpoint da API**

   Certifique-se de que o frontend está configurado para apontar para o backend correto:

   ```javascript
   const API_BASE_URL = 'http://localhost:3030/api/alunos';
   ```

4. **Executar o Frontend**

   Execute o seguinte comando para iniciar o servidor de desenvolvimento:

   Usando npm:

   ```bash
   npm start
   ```

   Usando Yarn:

   ```bash
   yarn start
   ```

   O frontend estará rodando em `http://localhost:3000`.

## Rodando o Projeto

1. **Inicie o backend**:

   ```bash
   mvn spring-boot:run
   ```

   Verifique se o backend está funcionando acessando `http://localhost:3030/api/alunos`.

2. **Inicie o frontend**:

   ```bash
   npm start
   ```

   Verifique se o frontend está funcionando acessando `http://localhost:3000`.

## Estrutura do Projeto

- **Backend**: Pasta com o código Spring Boot e a API REST.
- **Frontend**: Pasta com o código React.

## Considerações Finais

- Certifique-se de que o MySQL está rodando antes de iniciar o backend.
- Configure o arquivo `application.properties` corretamente para refletir as configurações do seu ambiente de desenvolvimento.