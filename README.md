# bd-atv05-miguel
DATABASE 01
CREATE DATABASE bd_festa;
	USE bd_festa;

	CREATE TABLE convidados (
	nome VARCHAR(50),
    idade INT,
    endereco VARCHAR(50)
);
	CREATE TABLE comidas (
	bebida VARCHAR(30),
    salgado VARCHAR(30),
    enfeites VARCHAR(50)
);
    CREATE TABLE organizadores (
	nome VARCHAR(100),
    gastos FLOAT
);

	INSERT INTO convidados (nome,idade,endereco) VALUES
    ('CLAUDIO','18','RUA JOAQUIM 189'),
	('MARIA','21','RUA CASTRO 141'),
	('JOAO','27','RUA MANESTRO 207');
    
	SELECT * FROM convidados;
    
    INSERT INTO comidas (bebida,salgado,enfeites) VALUES
    ('REFRIGERANTE','PIZZA','BALOES'),
	('WHISKY','COXINHAS','FOGOS DE ARTIFICIO'),
	('ENERGETICO','SALGADINHOS','CONFETES');
    
    ALTER TABLE convidados
    ADD id_convidado INT PRIMARY KEY AUTO_INCREMENT;
    
     ALTER TABLE comidas
    ADD id_comidas INT PRIMARY KEY AUTO_INCREMENT;
    
     ALTER TABLE organizadores
    ADD id_organizadores INT PRIMARY KEY AUTO_INCREMENT;
    
    SELECT * FROM organizadores;

    DATABASE02
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
    SELECT * FROM telefones;
