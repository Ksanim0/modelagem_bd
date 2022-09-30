# provaDB

Integrantes do Grupo:

- Edmilson Júnior
- Ithala Kaynara

Professor: 

- Adeilson

## Modelo Conceitual:
<img src="Modelo_Conceitual.png">

## Modelo Lógico:
<img src="Modelo_Logico.png">


## Tabelas:

### Tabela _aluno_:
A tabela "aluno" é responsável por armazenar as informções de cada aluno, como: Matrícula, Nome do Aluno, Endereço, Cidade.
Nesta tabela, teremos como atributos/colunas:

- mat: matrícula do aluno (atributo identificador)
- nome: nome do aluno
- endereco: endereço do aluno
- cidade: cidade em que o aluno mora
- fk_historico_id_historico: chave estrangeira que faz referência a _historico_


### Tabela _possuir_:
A tabela "possuir" foi criada a partir do relacionamento entre as entidades "aluno" e "disciplinas".
Nesta tabela, teremos como atributos/colunas:

- fk_aluno_mat: chave estrangeira que faz referência a _aluno_
- fk_disciplinas_cod_disc: chave estrangeira que faz referência a _displinas_


### Tabela _disciplinas_:
A tabela "disciplinas" é destinada ao armazenamento de informações das discplinas, como: código da disciplinas, nome da discplina e carga horária.
Nesta tabela, teremos como atributos/colunas:

- cod_disc: chave primária da tabela
- nome_disc: nome da disciplina
- carga_hor: carga horária da disciplina
- fk_professores_cod_prof: chave estrangeira que faz referência a _professores_


### Tabela _professores_:
A tabela "professores" é responsável por armazenar os dados dos professores, como: código do professor, nome, endereço e cidade.
Nesta tabela, teremos como atributos/colunas:

- cod_prof: chave primária
- nome: nome do professor
- endereco_prof: endereço do professor
- cidade_prof: cidade do professor


### Tabela _ensinar_:
A tabela "ensinar" foi criada a partir do relacionamento entre _profesores_ e _turma_
Nesta tabela, teremos como atributos/colunas:

- fk_turma_cod_turma: chave estrangeira que faz referência a _turma_
- fk_professores_cod_prof: chave estrangeira que faz referência a _professires_


### Tabela _turma_:
A tabela "turma" é responsável por armazenar informações de cada turma em especifíco, como: código da turma, ano e horário.
Nesta tabela, teremos como atributos/colunas:

- cod_turma: chave primária
- ano: ano da turma
- horario: horário da turma
- fk_historico_id_historico: chave estrangeira que faz referência a _historico_


### Tabela _aula_:
A tabela "aula", surge a partir do relacionamento entre _turma_ e _disciplinas_.
Nesta tabela, teremos como atributos/colunas:

- fk_turma_cod_turma: chave estrangeira que faz referência a _turma_
- fk_disciplina_cod_disc: chave estrangeira que faz referência a _disciplinas_


### Tabela _historico_:
A tabela "historico" será responsável por armazenar os itens que compõem o histórico do aluno, como: a frequencia e as notas.
Nesta tabela, teremos como atributos/colunas:

- id_historico: chave primária
- frequencia: frequência do aluno
- nota: notas do aluno
