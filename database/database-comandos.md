# 🗄️ Guia Básico de Comandos de Bancos de Dados

Este documento reúne os principais comandos utilizados em **bancos de dados relacionais e NoSQL**, servindo como referência rápida para desenvolvedores.

---

## ✍️ Autor

- **Matheus Rossetto**  
- Data: *01/10/2025*  

---

## 🚀 Comandos Essenciais – SQL Relacional

### 🔹 PostgreSQL

#### Conexão e Listagem
- `psql -h [host] -U [usuario] -d [database]` → Conecta ao servidor PostgreSQL.  
- `\l` → Lista todos os bancos de dados.  
- `\c [database]` → Conecta a um banco de dados específico.  
- `\dt` → Lista tabelas do banco atual.  
- `\d [tabela]` → Mostra estrutura de uma tabela.  
- `\q` → Sai do terminal PostgreSQL.  

#### Bancos de Dados
- `CREATE DATABASE [nome];` → Cria um novo banco de dados.  
- `DROP DATABASE [nome];` → Remove um banco de dados.  

#### Usuários e Permissões
- `CREATE USER [nome] WITH PASSWORD '[senha]';` → Cria um novo usuário.  
- `ALTER USER [nome] WITH PASSWORD '[nova_senha]';` → Altera senha do usuário.  
- `GRANT ALL PRIVILEGES ON DATABASE [database] TO [usuario];` → Concede permissões a um usuário.  
- `REVOKE ALL PRIVILEGES ON DATABASE [database] FROM [usuario];` → Revoga permissões.  

#### Tabelas
- `CREATE TABLE [tabela] (id SERIAL PRIMARY KEY, nome VARCHAR(50), idade INT);` → Cria uma tabela exemplo.  
- `DROP TABLE [tabela];` → Remove uma tabela.  
- `INSERT INTO [tabela] (nome, idade) VALUES ('Matheus', 25);` → Insere um registro.  
- `SELECT * FROM [tabela];` → Lista registros.  
- `UPDATE [tabela] SET idade=26 WHERE nome='Matheus';` → Atualiza registros.  
- `DELETE FROM [tabela] WHERE nome='Matheus';` → Remove registros.  

---

### 🔹 MySQL / MariaDB

#### Conexão e Listagem
- `mysql -h [host] -u [usuario] -p` → Conecta ao servidor MySQL.  
- `SHOW DATABASES;` → Lista bancos de dados.  
- `USE [database];` → Seleciona banco de dados.  
- `SHOW TABLES;` → Lista tabelas.  
- `DESCRIBE [tabela];` → Mostra estrutura da tabela.  

#### Bancos de Dados
- `CREATE DATABASE [nome];` → Cria banco de dados.  
- `DROP DATABASE [nome];` → Deleta banco de dados.  

#### Usuários e Permissões
- `CREATE USER '[usuario]'@'localhost' IDENTIFIED BY '[senha]';` → Cria usuário.  
- `ALTER USER '[usuario]'@'localhost' IDENTIFIED BY '[nova_senha]';` → Altera senha do usuário.  
- `GRANT ALL PRIVILEGES ON [database].* TO '[usuario]'@'localhost';` → Concede permissões.  
- `REVOKE ALL PRIVILEGES ON [database].* FROM '[usuario]'@'localhost';` → Revoga permissões.  
- `FLUSH PRIVILEGES;` → Aplica alterações de permissões.  

#### Tabelas
- `CREATE TABLE [tabela] (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(50), idade INT);` → Cria tabela exemplo.  
- `DROP TABLE [tabela];` → Deleta tabela.  
- `INSERT INTO [tabela] (nome, idade) VALUES ('Matheus', 25);` → Insere registro.  
- `SELECT * FROM [tabela];` → Lista registros.  
- `UPDATE [tabela] SET idade=26 WHERE nome='Matheus';` → Atualiza registros.  
- `DELETE FROM [tabela] WHERE nome='Matheus';` → Remove registros.  

---

## 🔹 Comandos Essenciais – NoSQL

### MongoDB
- `mongo` → Conecta ao servidor MongoDB.  
- `show dbs` → Lista todos os bancos.  
- `use [database]` → Seleciona banco de dados.  
- `db.createCollection("[nome_colecao]")` → Cria uma coleção.  
- `db.[colecao].insertOne({chave: valor})` → Insere documento.  
- `db.[colecao].find()` → Lista documentos.  
- `db.[colecao].updateOne({filtro}, {$set: {chave: valor}})` → Atualiza documento.  
- `db.[colecao].deleteOne({filtro})` → Remove documento.  

### Redis
- `redis-cli` → Conecta ao servidor Redis.  
- `PING` → Verifica conexão.  
- `SET chave valor` → Define valor.  
- `GET chave` → Recupera valor.  
- `DEL chave` → Remove chave.  
- `EXISTS chave` → Verifica se a chave existe.  
- `KEYS *` → Lista todas as chaves.  

---

## ⚡ Boas Práticas

- Sempre faça **backup antes de alterações em massa**.  
- Use transações (`BEGIN`, `COMMIT`, `ROLLBACK`) em operações críticas.  
- Nomeie bancos, tabelas, coleções e chaves de forma **consistente e clara**.  
- Para bancos NoSQL, entenda o modelo de dados antes de criar coleções ou índices.  

---

## 📚 Referências Oficiais

- [PostgreSQL Documentation](https://www.postgresql.org/docs/)  
- [MySQL Documentation](https://dev.mysql.com/doc/)  
- [MongoDB Manual](https://www.mongodb.com/docs/manual/)  
- [Redis Documentation](https://redis.io/documentation)  

---
