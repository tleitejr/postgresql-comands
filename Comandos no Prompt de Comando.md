# Comandos para usar o PostgreSQL no Terminal/Prompt de Comando ![Logo PostgreSQL](https://th.bing.com/th?id=ODLS.87970c9f-48f7-471f-84c4-39d53d664e49&w=32&h=32&qlt=90&pcl=fffffa&o=6&pid=1.2)
### Iniciar
#### Windows
1. Abra o Prompt de Comando;

    Digite esse comando:
`C:\Program Files\PostgreSQL\"versão"\bin`

    Substitua **"versão"** pela versão específica do PostgreSQl que você instalou.

#### Linux
1. Abra o Terminal;

    (Em distribuições baseadas em Debian). Digite esse comando: `/usr/bin/psql`

    (Em distribuições baseadas em Red Hat). Digite esse comando: `/usr/pgsql-"versao"/bin/psql`

- Substitua **"versão"** pela versão específica do PostgreSQl que você instalou.

#### macOS
   Se você instalou usando o HomeBrew, use esse comando: `/usr/local/bin/psql`
  
   Caso você instalou de outras maneiras, o local pode variar. Para saber, use esse comando: `which psql`

---

2. Digite esse comando:
~~~powershell
psql -U "seu usuario" -d "seu banco de dados" -h "seu servidor" -p "sua porta"
~~~

- **-U** : nome de usuário;
- **-d** : nome do banco de dados;
- **-h** : host(localhost se estiver na mesma máquina);
- **-p** : porta do servidor;
3. Insira a senha
  - O **psql** solicitará a senha do usuário especificado. Insira a senha e pressione Enter.

4. Sair
  - Digite **\q** e pressione Enter.

---
### Mostrar todas as tabelas do banco
~~~bash
\dt
~~~
---
### Limpar a tela
#### Windows (Prompt de Comando)
~~~bash
\! cls
~~~

#### Linux/macOS (Terminal)
~~~bash
\! clear
~~~

#### No console do PostgreSQL
~~~bash
\! clear
~~~
---
### Mostrar todos os atributos o tipo delas de uma tabela
~~~bash
\d 'nome da tabela'
~~~
