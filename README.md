# bd-atv05-miguel

    DATABASE 01
    CREATE DATABASE ESCOLA;
	USE ESCOLA;
	CREATE TABLE ALUNOS (
    id_aluno INT AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    matricula VARCHAR(20) NOT NULL,
    PRIMARY KEY (id_aluno)
	);
    CREATE TABLE telefones (
    id_telefone INT AUTO_INCREMENT,
    numero VARCHAR(50),
    tipo VARCHAR(20),
    id_aluno INT AUTO_INCREMENT,
    PRIMARY KEY (id_telefone),
    FOREIGN KEY (id_aluno) REFERENCES ALUNOS (id_aluno)
    );
    INSERT INTO ALUNOS (nome,matricula) VALUES
    ('isabelly','109080'),
    ('joao','109081');
     INSERT INTO telefones (numero,tipo) VALUES
    ('2198765432','celular'),
    ('83987453901','celular');
    UPDATE ALUNOS
	SET matricula = '109079'
	WHERE ID = 1;

	DELETE FROM telefones
	WHERE tipo;
	
	SELECT * FROM telefones;
	DECR https://app.diagrams.net/
