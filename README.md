# TRABALHO DE PI:  YBY
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Larissa Kemile Pereira da Silva: larissakemile24@gmail.com<br>
Josias Neves Jardim Borba: jojarbor@gmail.com<br>
Vitória Isabel Lemos de Mattos: vitoriaisabel77351@gmail.com<br>

### 2.MINIMUNDO<br>

>O professor Carlinhos, solicitou um sistema para o NEABI (Núcleo de Estudos Afro-Brasileiros). A princípio, ele deseja armazenar as seguintes informações a respeito os alunos: matrícula, nome, situação da matricula, nascimento, sexo, curso, telefone, email, cota, renda familiar percapita, nome do responsável cor/raça.

>Ao fim, os NEABIs conseguirão utilizar o sistema para obterem conclusões derivadas dos relatórios gerados. O conjunto de informações coletadas e armazenadas para fins de consulta a respeito dos NEABIS são:  id_Neabi, datOrig, administrador, id_Campus.

>Um aluno pode pertencer a apenas uma turma, e a turma pode conter diversos alunos.Alunos e professores podem participar apenas do NEABI em que participam e um NEABI pode receber vários alunos e professores.

>Cada aluno pertence exclusivamente a uma única instituição de ensino médio, podendo ser cadastrada em conjunto, instituições extracurriculares.
Os dados gerais a respeito da instituição consistem em: nome, 
data_origem e etnias. Para as organizações extracurriculares basta apenas o tipo (cursinhos pré enem, idiomas etc..).
 
### 3.PMC<br>
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/pmc(1).png "PMC")

### 4.Personas e Histórias de usuário<br>
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/PMC.jpg?raw=true "PMC")

### 5.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
![Arquivo do protótipo do site YBY](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/home.png "YBY")

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
    A) Esta tabela deve conter **todos os atributos do sistema** e um mínimo de 10 linhas/registros de dados.
    B) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
 <br> (veja o exemplo abaixo antes de criar a tabela para seu trabalho)
    C) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")

 
 ### 7.MODELO CONCEITUAL<br>
![Alt text](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/conceitual.jpg "Modelo Conceitual")

#### 7.1 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>

### 8	RASTREABILIDADE DOS ARTEFATOS<br>
        a) Historia de usuários vs protótipo (mockup)
        b) Protótipo vs Modelo conceitual
        (não serão aceitos modelos que não estejam em conformidade)


### 9	MODELO LÓGICO<br>
![Alt text](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/conceitual.jpg "Modelo Conceitual")

### 10	MODELO FÍSICO<br>
CREATE TABLE PESSOA (
    id INTEGER PRIMARY KEY,
    nome VARCHAR(100),
    sexo VARCHAR(100),
    id_Renda INTEGER,
    telefone BIGINT,
    email VARCHAR(100),
    nascimento VARCHAR(100),
    etnia INTEGER,
    FK_NEABI_id_Neabi INTEGER,
    FK_CURSO_id_Curso INTEGER,
    FK_RENDA_id_Renda INTEGER
);

CREATE TABLE ALUNO (
    id_Aluno INTEGER,
    id_Cota VARCHAR(100),
    id_Matricula VARCHAR(100),
    FK_PESSOA_id INTEGER,
    FK_COTA_id_Cota INTEGER,
    FK_STATUS_M_id_Extra INTEGER,
    PRIMARY KEY (id_Aluno, FK_PESSOA_id)
);

CREATE TABLE NEABI (
    id_Neabi INTEGER PRIMARY KEY,
    campus VARCHAR(100),
    dataOrig DATE,
    administrador VARCHAR(100),
    FK_CAMPUS_id_Campus INTEGER
);

CREATE TABLE CURSO (
    id_Curso INTEGER PRIMARY KEY,
    descricao VARCHAR(100)
);

CREATE TABLE RENDA (
    id_Renda INTEGER PRIMARY KEY,
    descricao VARCHAR(100)
);

CREATE TABLE CAMPUS (
    id_Campus INTEGER PRIMARY KEY,
    nome VARCHAR(100),
    datOrigCampus DATE
);

CREATE TABLE COTA (
    id_Cota INTEGER PRIMARY KEY,
    descricao VARCHAR(100)
);

CREATE TABLE STATUS_M (
    id_Extra INTEGER PRIMARY KEY,
    tipo VARCHAR(100)
);

CREATE TABLE INSTITUICAO_EXTRAC (
    id_Status INTEGER PRIMARY KEY,
    descStatus VARCHAR(100)
);

CREATE TABLE Participa (
    fk_ALUNO_id_Aluno INTEGER,
    fk_ALUNO_FK_PESSOA_id INTEGER,
    fk_INSTITUICAO_EXTRAC_id_Status INTEGER
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
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_2
    FOREIGN KEY (FK_PESSOA_id)
    REFERENCES PESSOA (id)
    ON DELETE CASCADE;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_3
    FOREIGN KEY (FK_COTA_id_Cota)
    REFERENCES COTA (id_Cota)
    ON DELETE SET NULL;
 
ALTER TABLE ALUNO ADD CONSTRAINT FK_ALUNO_4
    FOREIGN KEY (FK_STATUS_M_id_Extra)
    REFERENCES STATUS_M (id_Extra)
    ON DELETE RESTRICT;
 
ALTER TABLE NEABI ADD CONSTRAINT FK_NEABI_2
    FOREIGN KEY (FK_CAMPUS_id_Campus)
    REFERENCES CAMPUS (id_Campus)
    ON DELETE CASCADE;
 
ALTER TABLE Participa ADD CONSTRAINT FK_Participa_1
    FOREIGN KEY (fk_ALUNO_id_Aluno, fk_ALUNO_FK_PESSOA_id)
    REFERENCES ALUNO (id_Aluno, FK_PESSOA_id)
    ON DELETE RESTRICT;
 
ALTER TABLE Participa ADD CONSTRAINT FK_Participa_2
    FOREIGN KEY (fk_INSTITUICAO_EXTRAC_id_Status)
    REFERENCES INSTITUICAO_EXTRAC (id_Status)
    ON DELETE SET NULL;
       
### 11	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados 
 <br> + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


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
