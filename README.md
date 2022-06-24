# TRABALHO DE PI:  YBY
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Larissa Kemile Pereira da Silva: larissakemile24@gmail.com<br>
Josias Neves Jardim Borba: jojarbor@gmail.com<br>
Vitória Isabel Lemos de Mattos: vitoriaisabel77351@gmail.com<br>

### 2.MINIMUNDO<br>
Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar)
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente real)
Descrição textual das regras de negócio definidas como um subconjunto do mundo real cujos elementos são propriedades que desejamos incluir, processar, armazenar, gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.
<br>

> O professor Carlinhos solicitou um sistema para o NEABI (Núcleo de Estudos Afro-Brasileiros). A principio, ele deseja armazenar informações a respeito de alunos sobre as seguintes informações: matrícula, nome, situação da matricula, nascimento, sexo, curso, telefone, email, cota, renda familiar percapita, nome do responsável cor/raça. A respeito dos professores, ele deseja registrar tais informações: sexo, curso que atua, cor/raça.

> Ao fim, os neabis conseguirão utilizar o sistema para obterem conclusões derivadas dos relatórios gerados. O conjunto de informações coletadas e armazenadas para fins de consulta a respeito dos NEABIS são:  qtd_integrantes, campus, data_origem, administradores, etnia.

> Um aluno pode pertencer a apenas uma turma e a turma pode conter diversos alunos. Um aluno pode ter vários professores e um professor pode ter vários alunos. Alunos e professores podem participar apenas do NEABI em que participam e um NEABI pode receber vários alunos e professores.

> Cada aluno pertence exclusivamente a uma única instituição de ensino médio, podendo ser cadastrada em conjunto, instituições extracurriculares.

> Os dados gerais a respeito da instituição consistem em: nome, data_origem e etnias. Para as organizações extracurriculares basta apenas o tipo (cursinhos pré enem, idiomas etc..).
 
 
### 3.PMC<br>
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/vitoria-F5/projeto_integrador_IFES/blob/main/arquivos/pmc(1).png "PMC")
a) inclusão do PMC desenvolvido pelo grupo

### 4.Personas e Histórias de usuário<br>
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/PMC.jpg?raw=true "PMC")
a) inclusão do PMC desenvolvido pelo grupo


### 5.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/EmpresaDevcom.pdf?raw=true "Empresa Devcom")


#### 5.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa DevCom precisa inicialmente dos seguintes relatórios:
* Relatório que informe quais são os gerentes de cada departamento incluindo as seguintes informações: número do departamento,  nome do departamento, e nome do gerente.
* Relatório de empregados por projeto incluindo as seguintes informações: número do projeto, nome do projeto, rg do empregado, nome do empregado e quantidade de horas de trabalho do empregado alocadas ao projeto.
* Relatório de empregados com dependentes incluindo as seguintes informações: rg do empregado, nome do empregado, nome do dependente, tipo de relação, data de nascimento do dependente e sexo do dependente.
* Relatório com a quantidade de empregados por cada departamento incluindo as seguintes informações: nome do departamento, supervisor e quantidade de empregados alocados no departamento.
* Relatório de supervisores e supervisionados incluindo as seguintes informações: nome do supervisor e nome do supervisionado.
 

### 6 TABELA DE DADOS DO SISTEMA:
    A) Esta tabela deve conter **todos os atributos do sistema** e um mínimo de 10 linhas/registros de dados.
    B) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
 <br> (veja o exemplo abaixo antes de criar a tabela para seu trabalho)
    C) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")

 
 

 
 
 ### 7.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento
 <br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/discproint/template_projeto_integrador/blob/main/arquivos/concept_sample.png?raw=true "Modelo Conceitual")
      
    
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
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 10	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
       
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
