# Comandos PostgreSQL ![Logo PostgreSQL](https://th.bing.com/th?id=ODLS.87970c9f-48f7-471f-84c4-39d53d664e49&w=32&h=32&qlt=90&pcl=fffffa&o=6&pid=1.2)
### CRIAR
#### Database
~~~sql
CREATE DATABASE 'nome do banco de dados';

~~~

#### Tabela
~~~sql
CREATE TABLE 'nome da tabela'();

~~~

#### Atributo
~~~sql
CREATE TABLE 'nome da tabela' (
  'nome do atributo' 'tipo' 'null ou not null',
   ...
)
~~~

#### Chave Primária
~~~sql
CONSTRAINT 'nome da chave primária' PRIMARY KEY ('atributo que receberá a chave primária')

~~~

#### Chave Estrangeira
~~~sql
CONSTRAINT 'nome da chave estrangeira' FOREIGN KEY ('atributo que se tornará a chave estrangeira') REFERENCES 'nome da tabela chave primária' ('atributo chave primária')

~~~
### Inserir Valores em um Atributo
~~~sql
INSERT INTO 'nome da tabela' ('atributo 1', 'atributo 2' ...) VALUES ('valor do atributo 1', 'valor do atributo 2' ...)

~~~


### Comandos para Manipulação de Atributos em uma Tabela
#### Adicionar Atributo
~~~sql
ALTER TABLE 'nome da tabela' ADD COLUMN 'nome do atributo' 'tipo';

~~~

#### Alterar Atributo
~~~sql
ALTER TABLE 'nome da tabela' ALTER COLUMN 'nome do atributo' 'novo tipo';

~~~

#### Deletar Atributo
~~~sql
ALTER TABLE 'nome da tabela' DROP COLUMN 'nome do atributo';

~~~

### Renomear
#### Database
~~~sql
ALTER DATABASE 'nome do banco de dados' RENAME TO 'nome novo';

~~~

#### Tabela
~~~sql
ALTER TABLE 'nome da tabela' RENAME TO 'nome novo';

~~~

#### Atributo
~~~sql
ALTER TABLE 'nome da tabela' RENAME COLUMN 'nome do atributo' TO 'nome novo';

~~~

### Atualizar
~~~sql
UPDATE 'nome da tabela' SET 'nome do atributo' 'operador' 'valor' WHERE 'nome do atributo' 'operador' 'valor';

~~~


### Deletar
#### Database
~~~sql
DROP DATABASE 'nome do banco de dados';

~~~

#### Tabela
~~~sql
DROP TABLE 'nome da tabela';

~~~

### Selecionar
#### Todos os atributos de uma tabela
~~~sql
SELECT * FROM 'nome da tabela';

~~~

#### Atributo específico de uma tabela
~~~sql
SELECT 'nome do atributo ou *' FROM 'nome da tabela';

~~~

#### Condição / Filtro
~~~sql
SELECT 'nome do atributo ou *' FROM 'nome da tabela' WHERE 'nome do atributo' 'operador' 'valor';

~~~

#### Expressões e Funções
~~~sql
SELECT 'atributo 1', 'atributo 2' ... 'operador' 'número' AS 'novo atributo' FROM 'nome da tabela';

~~~

#### Constantes e Literais
~~~sql
SELECT 'valor' AS 'atributo 1', 'atributo 2' ... FROM 'nome da tabela';

~~~

#### Ordenar dados
~~~sql
SELECT 'nome do atributo ou *' FROM 'nome da tabela' ORDER BY 'tipo' 'ASC ou DESC';

~~~
- ASC : ordenação crescente;
- DESC : ordenação decrescente;

OBS: Pode utilizar WHERE para condição de filtro.

## Comandos JOIN
#### INNER JOIN
- Retorna registros que têm valores correspondentes em ambas as tabelas.
~~~sql
SELECT 'nome da coluna ou *' FROM 'nome da tabela 1' INNER JOIN 'nome da tabela 2' ON 'condição de junção';

~~~
OBS: Pode utilizar WHERE para condições de filtro.

#### LEFT JOIN (ou LEFT OUTER JOIN)
- Retorna todos os registros da tabela à esquerda e os registros correspondentes da tabela à direita. Se não houver correspondência, os resultados da tabela à direita serão nulos.
~~~sql
SELECT 'nome da coluna ou *' FROM 'nome da tabela 1' LEFT JOIN 'nome da tabela 2' ON 'condição de junção';

~~~

#### RIGHT JOIN (ou RIGHT OUTER JOIN)
- Retorna todos os registros da tabela à direita e os registros correspondentes da tabela à esquerda. Se não houver correspondência, os resultados da tabela à esquerda serão nulos.
~~~sql
SELECT 'nome da coluna ou *' FROM 'nome da tabela 1' RIGHT JOIN 'nome da tabela 2' ON 'condição de junção';

~~~

#### FULL JOIN (OU FULL OUTER JOIN)
- Retorna todos os registros quando há uma correspondência em uma das tabelas. Se não houver correspondência, os resultados da tabela sem correspondência serão nulos.
~~~sql
SELECT 'nome da coluna ou *' FROM 'nome da tabela 1' FULL JOIN 'nome da tabela 2' ON 'condição de junção';

~~~

## Tipos de Valores
#### Tipos Numéricos:
- __integer__ - Números inteiros.
- __bigint__ - Inteiros de precisão estendida.
- __decimal__ ou __numeric__ - Números decimais com precisão arbitrária.
- __real__ - Números de ponto flutuante de precisão simples.
- __double__ - Números de ponto flutuante de dupla precisão.

#### Tipos de Texto:
- __character varying(n)__ ou __varchar(n)__ - Strings de caracteres com comprimento variável.
- __character(n)__ ou __char(n)__ - Strings de caracteres com comprimento fixo.

#### Tipos de Data e Hora:
- __date__ - Data (ano, mês, dia).
- __time__ - Hora do dia.
- __timestamp__ - Data e hora combinadas.
- __interval__ - Intervalo de tempo.

#### Tipos Booleanos:
- __boolean__ - Valores verdadeiro ou falso.

#### Tipos Binários:
- __bytea__ - Sequência de bytes.

#### Tipos de Enumeração:
- __enum__ - Enumerações (conjunto de rótulos nomeados).

#### Tipos de Array:
- __integer[]__ - Arrays de inteiros.
- __text[]__ - Arrays de texto.

#### Tipos Geoespaciais:
- __point__ - Ponto em um plano.
- __polygon__ - Polígono.

#### Tipos de Rede:
- __inet__ - Endereço IP.
- __macaddr__ - Endereço MAC.

#### Tipos de UUID:
- __uuid__ - Identificador único universal.

#### Tipos de JSON:
- __json__ - Dados JSON.
- __jsonb__ - Dados JSON binários.

#### Tipos de HSTORE:
- __hstore__ - Armazena um conjunto de pares chave-valor.

## Tipos de Operadores
#### Operadores Aritméticos
- __+__ (adição)
- __-__ (subtração)
- __*__ (multiplicação)
- __/__ (divisão)
- __%__ (módulo)

#### Operadores de Comparação
- __=__ (igual)
- __<>__ ou __!=__ (diferente)
- __<__ (menor que)
- __>__ (maior que)
- __<=__ (menor ou igual a)
- __>=__ (maior ou igual a)

#### Operadores Lógicos
- __AND__ (E lógico)
- __OR__ (OU lógico)
- __NOT__ (NÃO lógico)

#### Operadores de Concatenação
- __||__ (concatenação de strings)

#### Operadores de Texto
- __LIKE__ (comparação de padrões)
- __ILIKE__ (LIKE case-insensitive)

#### Operadores de Conjunto
- __IN__ (pertence a um conjunto)
- __NOT IN__ (não pertence a um conjunto)

#### Operadores de Intervalo
- __BETWEEN__ (dentro de um intervalo)
- __NOT BETWEEN__ (fora de um intervalo)

#### Operadores de Bitwise
- __&__ (AND bitwise)
- __|__ (OR bitwise)
- __#__ (XOR bitwise)
- __~__ (NOT bitwise)

#### Operadores de Array
- __@>__ (contém elemento)
- __<@__ (é contido por)
- __=__ (igualdade de arrays)
- __<>__ ou __!=__ (desigualdade de arrays)
