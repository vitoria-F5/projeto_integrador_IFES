# TRABALHO DE PI:  YBY
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Larissa Kemile Pereira da Silva: larissakemile24@gmail.com<br>
Josias Neves Jardim Borba: jojarbor@gmail.com<br>
Vitória Isabel Lemos de Mattos: vitoriaisabel77351@gmail.com<br>

### 2.MINIMUNDO<br>
Para que o sistema serve?

>O sistema servirá para gerir os dados do Campus IFES Serra, a fim de obter relatórios para o NEABI. Com tais relatórios, poderemos entender melhor o perfil de cada indivíduo dentro do Campus.
Digamos que em uma turma de 30 alunos, 21 sejam brancos. Ter esse dado em mãos de forma concreta, nos ajuda a embasar discussões acerca do racismo institucional dentro do Campus, assim como desmistificar a visão que temos dos indivíduos dentro da instituição, ajudando no seu crescimento tanto acadêmico, como humano. 
Informações como essas podem e vão fortalecer os debates dentro da instituição.

Qual o propósito?
>Contribuir para o debate a respeito de diversas questões como étnico-raciais, de gênero e socioêconomicas.

Qual problema deve resolver?
>Dentro do IFES, existem inúmeros dados sobre a situação socioeconômica de cada aluno, porém, tais  atualmente são utilizados, estáticos, e, mesmo com uma enorme oportunidade, a maior parte  deles não é aproveitado para que possamos realmente contribuir para a diversidade e inclusão da instituição. Junto disso, existe uma pobreza nas discussões  a respeito de temáticas sensíveis como gênero, raça, sexualidade, e classes sociais dentro do IFES. Muitas vezes o que ocorre é o imaginário que questões como essas estejam separadas dos assuntos acadêmicos, fazendo com que muitas vezes sejam esquecidos e/ou negligenciados.


O professor Carlinhos, solicitou um sistema para o NEABI (Núcleo de Estudos Afro-Brasileiros). A princípio, ele deseja armazenar as seguintes informações a respeito os alunos: matrícula, nome, situação da matricula, nascimento, sexo, curso, telefone, email, cota, renda familiar percapita, nome do responsável cor/raça.

Ao fim, os NEABIs conseguirão utilizar o sistema para obterem conclusões derivadas dos relatórios gerados. O conjunto de informações coletadas e armazenadas para fins de consulta a respeito dos NEABIS são:  id_Neabi, datOrig, administrador, id_Campus.

Um aluno pode pertencer a apenas uma turma, e a turma pode conter diversos alunos.Alunos e professores podem participar apenas do NEABI em que participam e um NEABI pode receber vários alunos e professores.

Cada aluno pertence exclusivamente a uma única instituição de ensino médio, podendo ser cadastrada em conjunto, instituições extracurriculares.
Os dados gerais a respeito da instituição consistem em: nome, 
data_origem e etnias. Para as organizações extracurriculares basta apenas o tipo (cursinhos pré enem, idiomas etc..).
 
### 3.PMC<br>
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/pmc(1).png "PMC")

### 4.Personas e Histórias de usuário<br>

![As Personas](https://www.canva.com/design/DAE-DwsIPzM/UJqBI8FzzH_yFBft3-4QyQ/edit "PERSONAS")
<a href="https://www.canva.com/design/DAE-DwsIPzM/UJqBI8FzzH_yFBft3-4QyQ/edit">Personas</a>

> https://www.figma.com/proto/mwnCuYGBWkkDdcDCAj1x8h/Prot%C3%B3tipo?node-id=74%3A58&scaling=scale-down&page-id=0%3A1&starting-point-node-id=74%3A58

### 5.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
![Arquivo do protótipo do site YBY](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/home.png "YBY")
https://www.figma.com/proto/mwnCuYGBWkkDdcDCAj1x8h/Prot%C3%B3tipo?node-id=74%3A58&scaling=scale-down&page-id=0%3A1&starting-point-node-id=74%3A58

#### 5.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
Relatórios e informações a respeito do corpo docente e discente do IFES Campus Serra.

* Relatório que informe o perfil dos alunos de cada turma incluindo as seguintes informações: identificação padrão, matrícula, cota a qual pertence, etnia, curso e sexo.
* Relatório que informe o perfil dos professores de cada área incluindo identificação padrão, matrícula, etnia e sexo.
* Relatório que informe a quantidade de pessoas no NEABI.
* Relatório que informe a etnia dos alunos que pertencem a um pré-vestibular.
* Relatório que informe o perfil de renda de cada etnia dos alunos.

### 6 TABELA DE DADOS DO SISTEMA:

![Alt text](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/planilha.jpg "Tabela de dados")
 
 ### 7.MODELO CONCEITUAL<br>
![Alt text](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/Conceitual.jpg "Modelo Conceitual")

#### 7.1 Descrição dos dados 
PESSOA: Tabela que armazena as informações relativas a pessoa<br>
id_Pessoa: identificador da pessoa <br>
nome: nome da pessoa <br>
sexo: sexo da pessoa<br>	
id_Curso: identificador do curso da pessoa<br>
etnia: etnia da pessoa<br>
id_Renda: identificador de renda da pessoa<br>	
telefone: telefone da pessoa<br>	
email: email da pessoa<br>
nascimento: data de nascimento da pessoa<br>

ALUNO: Tabela que diferencia os alunos das outras pessoas<br>
id_Aluno: identificador da pessoa<br>	
id_Matricula: matrícula da pessoa<br>	

RENDA: <br>
id_Renda: identificador de renda <br>
descRend: descrição<br>

CURSO: <br>
id_Curso: identificador do curso <br>	
descCurs: descrição <br>

COTA: <br>
id_Cota: identificador da cota <br>
descCota: descrição <br>

STATUS_M: <br>
id_Status: identificador do status de matricula <br>	
descStat: descrição <br>

INSTITUICAO_EXTRAC: <br>
id_Extra: identificador da instituição extracurricular <br>
tipo: tipo da instituição <br>

NEABI: <br>
id_Neabi: identificador do NEABI <br>
datOrig: data de origem do NEABI <br>
administrador: administrador do NEABI<br>
id_Campus: identificador do campus <br>

CAMPUS: <br>
id_Campus: identificador do campus <br>
Nome:	nome do campus <br>
datOrigCampus: data origem do campus <br>


### 8	RASTREABILIDADE DOS ARTEFATOS<br>
        a) Historia de usuários vs protótipo (mockup)
(https://www.canva.com/design/DAFC0576NTA/U_6xr4kA3Gz6e-ZDcqEwJQ/view?utm_content=DAFC0576NTA&utm_campaign=designshare&utm_medium=link2 utm_source=sharebutton)
        
        b) Protótipo vs Modelo conceitual
        (não serão aceitos modelos que não estejam em conformidade)
        
        


### 9	MODELO LÓGICO<br>
![Alt text](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/Logico.jpg "Modelo Logico")

### 10	MODELO FÍSICO<br>

CREATE TABLE PESSOA (
    id_Pessoa INTEGER PRIMARY KEY,
    nome VARCHAR(100),
    sexo VARCHAR(100),
    telefone VARCHAR(100),
    email VARCHAR(100),
    nascimento DATE,
    FK_NEABI_id_Neabi INTEGER,
    FK_CURSO_id_Curso INTEGER,
    FK_RENDA_id_Renda INTEGER,
    FK_ETNIA_id_etnia INTEGER
);

CREATE TABLE ALUNO (
    id_Aluno INTEGER,
    FK_PESSOA_id_Pessoa INTEGER,
    FK_COTA_id_Cota INTEGER,
    FK_STATUS_M_id_Status INTEGER,
    FK_INSTITUICAO_EXTRAC_id_Extra INTEGER,
    PRIMARY KEY (id_Aluno, FK_PESSOA_id_Pessoa)
);

CREATE TABLE NEABI (
    id_Neabi INTEGER PRIMARY KEY,
    datOrig VARCHAR(100),
    administrador VARCHAR(100),
    FK_CAMPUS_id_Campus INTEGER
);

CREATE TABLE CURSO (
    id_Curso INTEGER PRIMARY KEY,
    descCurs VARCHAR(100)
);

CREATE TABLE RENDA (
    id_Renda INTEGER PRIMARY KEY,
    descRend VARCHAR(100)
);

CREATE TABLE CAMPUS (
    id_Campus INTEGER PRIMARY KEY,
    nome VARCHAR(100),
    datOrigCampus VARCHAR(100)
);

CREATE TABLE COTA (
    id_Cota INTEGER PRIMARY KEY,
    descCota VARCHAR(100)
);

CREATE TABLE STATUS_M (
    id_Status INTEGER PRIMARY KEY,
    descStat VARCHAR(100)
);

CREATE TABLE INSTITUICAO_EXTRAC (
    id_Extra INTEGER PRIMARY KEY,
    tipo VARCHAR(100)
);

CREATE TABLE ETNIA (
    descEtnia VARCHAR(100),
    id_etnia INTEGER PRIMARY KEY
);
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_2
    FOREIGN KEY (FK_NEABI_id_Neabi)
    REFERENCES NEABI (id_Neabi)
    ON DELETE RESTRICT;
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_3
    FOREIGN KEY (FK_CURSO_id_Curso)
    REFERENCES CURSO (id_Curso)
    ON DELETE CASCADE;
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_4
    FOREIGN KEY (FK_RENDA_id_Renda)
    REFERENCES RENDA (id_Renda)
    ON DELETE SET NULL;
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_5
    FOREIGN KEY (FK_ETNIA_id_etnia)
    REFERENCES ETNIA (id_etnia)
    ON DELETE CASCADE;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_2
    FOREIGN KEY (FK_PESSOA_id_Pessoa)
    REFERENCES PESSOA (id_Pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_3
    FOREIGN KEY (FK_COTA_id_Cota)
    REFERENCES COTA (id_Cota)
    ON DELETE SET NULL;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_4
    FOREIGN KEY (FK_STATUS_M_id_Status)
    REFERENCES STATUS_M (id_Status)
    ON DELETE RESTRICT;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_5
    FOREIGN KEY (FK_INSTITUICAO_EXTRAC_id_Extra)
    REFERENCES INSTITUICAO_EXTRAC (id_Extra)
    ON DELETE CASCADE;
 
ALTER TABLE NEABI ADD CONSTRAINT FK_NEABI_2
    FOREIGN KEY (FK_CAMPUS_id_Campus)
    REFERENCES CAMPUS (id_Campus)
    ON DELETE CASCADE;
       
### 11	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

INSERT INTO CAMPUS(id_Campus, nome, datOrigCampus) VALUES(1, 'Serra','2001');
INSERT INTO CAMPUS(id_Campus, nome, datOrigCampus) VALUES(2, 'Vitoria','1909');
INSERT INTO CAMPUS(id_Campus, nome, datOrigCampus) VALUES(3, 'Linhares','2008');
INSERT INTO CAMPUS(id_Campus, nome, datOrigCampus) VALUES(4, 'Vila Velha','2010');


INSERT INTO NEABI(id_Neabi, datOrig, administrador, FK_CAMPUS_id_Campus) VALUES(1, '2007','ana', 1);
INSERT INTO NEABI(id_Neabi, datOrig, administrador, FK_CAMPUS_id_Campus) VALUES(2, '2004','diego', 2);
INSERT INTO NEABI(id_Neabi, datOrig, administrador, FK_CAMPUS_id_Campus) VALUES(3, '2010','edilson', 3);
INSERT INTO NEABI(id_Neabi, datOrig, administrador, FK_CAMPUS_id_Campus) VALUES(4, '2012','moises', 4);


INSERT INTO RENDA(id_Renda, descRend) VALUES(1, 'Até um salario');
INSERT INTO RENDA(id_Renda, descRend) VALUES(2, 'De um a dois salários');
INSERT INTO RENDA(id_Renda, descRend) VALUES(3, 'De dois a tres salários');

INSERT INTO ETNIA(id_Etnia, descEtnia) VALUES(1, 'Preto');
INSERT INTO ETNIA(id_Etnia, descEtnia) VALUES(2, 'Pardo');
INSERT INTO ETNIA(id_Etnia, descEtnia) VALUES(3, 'Branco');
INSERT INTO ETNIA(id_Etnia, descEtnia) VALUES(4, 'Indigena');
INSERT INTO ETNIA(id_Etnia, descEtnia) VALUES(5, 'Amarela');

INSERT INTO CURSO(id_Curso, descCurs) VALUES(1, 'Informatica');
INSERT INTO CURSO(id_Curso, descCurs) VALUES(2, 'Mecatronica');
INSERT INTO CURSO(id_Curso, descCurs) VALUES(3, 'Automacao');
INSERT INTO CURSO(id_Curso, descCurs) VALUES(4, 'IOT');

INSERT INTO COTA(id_Cota, descCota) VALUES(1, 'Racial');
INSERT INTO COTA(id_Cota, descCota) VALUES(2, 'Economica');
INSERT INTO COTA(id_Cota, descCota) VALUES(3, 'Necessidade Especial');
INSERT INTO COTA(id_Cota, descCota) VALUES(4, 'Escolaridade');
INSERT INTO COTA(id_Cota, descCota) VALUES(5, 'Ampla concorrencia');

INSERT INTO STATUS_M(id_Status, descStat) VALUES(1, 'Trancado');
INSERT INTO STATUS_M(id_Status, descStat) VALUES(2, 'Cursando');
INSERT INTO STATUS_M(id_Status, descStat) VALUES(3, 'Desistente');

INSERT INTO INSTITUICAO_EXTRAC(id_Extra, tipo) VALUES(1, 'Linguas');
INSERT INTO INSTITUICAO_EXTRAC(id_Extra, tipo) VALUES(2, 'pre-vest');
INSERT INTO INSTITUICAO_EXTRAC(id_Extra, tipo) VALUES(3, 'instrumentos');
INSERT INTO INSTITUICAO_EXTRAC(id_Extra, tipo) VALUES(4, 'esportes');


INSERT INTO PESSOA(id_Pessoa, nome, sexo, FK_CURSO_id_Curso, FK_ETNIA_id_Etnia, FK_RENDA_id_Renda, FK_NEABI_id_Neabi, telefone, email, nascimento) VALUES(1, 'julia', 'f', 1, 2, 1, 4,  '5584551', 'ju@gmail.com', '1992-08-23');
INSERT INTO ALUNO(id_Aluno, FK_PESSOA_id_pessoa, FK_STATUS_M_id_Status, FK_COTA_id_Cota, FK_INSTITUICAO_EXTRAC_id_Extra) VALUES(1, 1, 1, 1, 1);

INSERT INTO PESSOA(id_Pessoa, nome, sexo, FK_CURSO_id_Curso, FK_ETNIA_id_Etnia, FK_RENDA_id_Renda, FK_NEABI_id_Neabi, telefone, email, nascimento) VALUES(2, 'matheus', 'm', 2, 1, 2, 3, '51651651', 'mateuzin57@gmail.com', '2006-02-17');
INSERT INTO ALUNO(id_Aluno, FK_PESSOA_id_pessoa, FK_STATUS_M_id_Status, FK_COTA_id_Cota, FK_INSTITUICAO_EXTRAC_id_Extra) VALUES(2, 2, 2, 2, 2);

INSERT INTO PESSOA(id_Pessoa, nome, sexo, FK_CURSO_id_Curso, FK_ETNIA_id_Etnia, FK_RENDA_id_Renda, FK_NEABI_id_Neabi, telefone, email, nascimento) VALUES(3, 'joao', 'm', 3, 4, 1, 2, '616165', 'joaaaao@gmail.com', '2000-02-19');
INSERT INTO ALUNO(id_Aluno, FK_PESSOA_id_pessoa, FK_STATUS_M_id_Status, FK_COTA_id_Cota, FK_INSTITUICAO_EXTRAC_id_Extra) VALUES(3, 3, 3, 3, 3);

INSERT INTO PESSOA(id_Pessoa, nome, sexo, FK_CURSO_id_Curso, FK_ETNIA_id_Etnia, FK_RENDA_id_Renda, FK_NEABI_id_Neabi, telefone, email, nascimento) VALUES(4, 'ana', 'f', 4, 3, 3, 1, '8484854', 'ana@gmail.com', '2007-03-23');
INSERT INTO ALUNO(id_Aluno, FK_PESSOA_id_pessoa, FK_STATUS_M_id_Status, FK_COTA_id_Cota, FK_INSTITUICAO_EXTRAC_id_Extra) VALUES(4, 4, 2, 4, 4);

### 12	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 12.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
#### 12.2 PRINCIPAIS CONSULTAS DO SISTEMA 
 Inserir as principais consultas (relativas aos 5 principais relatórios) definidas previamente no iten 3.1 deste template.
 <br>
  a) Você deve apresentar as consultas em formato SQL para cad um dos relatórios.
 <br>
  b) Além da consulta deve ser apresentada uma imagem com o resultado obtido para cada consulta.<br>
 #### 12.3 ANTEPROJETO VERSÃO 1
 ![Modelo de Anteprojeto](https://docs.google.com/document/d/1nGgzfSoPeej1z7zsuWkrFLMlNeRunrtw/edit?usp=sharing&ouid=104104747195236161434&rtpof=true&sd=true "Anteprojeto")
 <br>
 https://docs.google.com/document/d/1_9PeBBs8see21dz_RfKniQmSsvZXPxrzDNPQvWyhmKw/edit?usp=sharing


 <br>
 <br>
 
 
 
 
 ### 13 Gráficos, relatórios, integração com Linguagem de programação e outras solicitações.<br>
     OBS: Observe as instruções relacionadas a cada uma das atividades abaixo.<br>
 #### 13.1	Integração com Linguagem de programação; <br>
 #### 13.2	Desenvolvimento de gráficos/relatórios pertinentes, juntamente com demais <br>
 #### solicitações feitas pelo professor. <br>
 #### 13.3 ANTEPROJETO VERSÃO 2
 <br>
 <br>
 
 
 ### 14 Slides e Apresentação em vídeo. <br>
     OBS: Observe as instruções relacionadas a cada uma das atividades abaixo.<br>
 #### 14.1 Slides; <br>
 #### 14.2 Apresentação em vídeo <br>
 #### 14.3 ANTEPROJETO VERSÃO FINAL
 <br>
 <br>   


    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")
