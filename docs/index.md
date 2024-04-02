<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/ciencia-da-computacao">Ciência da Computação</a></h3>


<font size="+12"><center>
*&lt;Sistema de Presença para a Escola Aprendizado Infinito&gt;*
</center></font>

**Conteúdo**
- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores
* Laura C. Balbachan dos Santos
* Vinicius S. Pansan

# Descrição do Projeto
*&lt;A Escola Aprendizado Infinito está em busca de uma forma mais eficiente de registrar a presença de seus alunos do Ensino Fundamental I, visto que ainda fazem esse processo de forma manual. 
O corpo docente dispõe um professor para cada turma, geralmente entre 20 e 30 alunos, para o lecionam as matérias de Matemática, Português, Artes, Ciências, História e Geografia. Para  Inglês e Educação Física, são dois outros professores.
A chamada é realizada duas vezes por dia, a primeira pela manhã e a segunda após o intervalo e para a formação do aluno, ele necessita de pelo menos 75% de presença em todas as aulas.&gt;*

# Análise de Requisitos Funcionais e Não-Funcionais

| RF | RNF |  
| --- | --- | 
| RF01: O sistema deve permitir que cada professor entre no sistema. | RNF01: O sistema deve ser fácil de usar para permitir que os professores registrem rapidamente a presença dos alunos. |  
| RF02: O sistema deve permitir o registro de presença dos alunos duas vezes por dia. | RNF02: O sistema deve ser seguro e proteger as informações dos alunos. |  
| RF03: O sistema deve permitir a atribuição de um professor para cada turma. | RNF03: O sistema deve ser rápido e responsivo para evitar atrasos na aula. |  
| RF04: O sistema deve permitir a atribuição de matérias específicas para cada professor. | RNF04: O sistema deve ser acessível para que diferentes pessoas consigam usar sem dificuldades. |  
| RF05: O sistema deve ser capaz de calcular a porcentagem de presença de cada aluno. | RNF05: O sistema deve estar disponível e ser responsivo aos navegadores. |  
| RF06: O sistema deve notificar a diretoria caso o aluno esteja próximo do número de faltas limite. |  |  
| RF07: O sistema deve permitir o registro de atraso dos alunos. |  |  
| RF08: O sistema deve permitir que a diretoria altere a presença dentro do prazo de uma semana, para que erros na chamada possam ser corrigidos. |  |  
| RF09: O sistema deve permitir que o aluno ou seus responsáveis tenham acesso as faltas. |  |  
| RF10: O sistema deve permitir que os professores de Inglês e Ed. Física escolham a turma que irão registrar a presença. |  |  


# Diagrama de Atividades
![image](https://github.com/Balbachan/UML-Classroom-FCI/assets/84653771/cb0a364d-a6fc-40a7-9eb4-790c4e0395f5)

# Diagrama de Casos de Uso
![image](https://github.com/Balbachan/UML-Classroom-FCI/assets/84653771/b6b32110-8136-477f-bd66-198dbb11a64a)


# Descrição dos Casos de Uso
## Especificações para Registrar a Presença dos Alunos ##
| Nome do Caso de Uso | Registrar a Presença dos Alunos |
| --- | --- |
| Ator Principal | Professor  |
| Atores Secundários  | Alunos, Diretores |
| Resumo | O professor entra no sistema, seleciona a turma que esta dando aula, a data e o horário e computa os alunos que estão faltando |
| Pré Condições | O professor precisa ter cadastro no sistema  |
| Pós Condições | O professor deve confirmar o relatório de faltas |

| Cliente  | Sistema |
| --- | --- |
| Professor Entra no Sistema |  |
|  | Sistema apresenta seleção de Turma |
| Professor seleciona a turma |  |
|  | Sistema apresenta seleção de data |
| Professor seleciona a data |  |
| Professor realiza a chamada na Sala |  |
|  | Sistema apresenta tabela com opções de marcar presença ou falta de cada aluno |
| Professor marca a presença dos alunos |  |
|  | Sistema salva os dados das falta e presenças |
|  | Em casos de falta superior a 75%, sistema informa os pais do aluno |


## Especificações para Alterar o Registro de Faltas  ##
| Nome do Caso de Uso | Alterar o Registro de Faltas  |
| --- | --- |
| Ator Principal | Diretor |
| Atores Secundários  | Aluno |
| Resumo | O diretor diretor é notificado sobre os requerimentos dos alunos sobre reavaliação de faltas e caso seja necessário uma alteração, o diretor realiza a ação. |
| Pré Condições | O aluno precisa abrir um requerimento. |
| Pós Condições | O diretor notifica o aluno sobre a alteração. |

| Cliente | Sistema |
| --- | --- |
| Diretor acessa o sistema  |  |
|  | O sistema notifica o diretor sobre a recorrência |
| Caso necessário, o diretor altera a falta do aluno |  |
|  | O sistema atualiza os dados  |
|  | O sistema notifica o aluno da ação do diretor  |


## Especificações para Gerar Relatório ##
| Nome do Caso de Uso | Gerar Relatório |
| --- | --- |
| Ator Principal | Diretor |
| Atores Secundários  | Alunos |
| Resumo | O diretor pede ao sistema gerar o relatório de presença.  |
| Pré Condições | O diretor precisa selecionar a turma da qual ele deseja gerar o relatório |
| Pós Condições | O diretor deve entrar em contato com os alunos e pais dos alunos caso o aluno não tenha comparecido em muitas aulas. |

| Cliente | Sistema |
| --- | --- |
| Diretor entra no sistema |  |
|  | Sistema apresenta Seleção da Turma |
| Diretor seleciona turma |  |
|  | Sistema apresenta opção de gerar relatório  |
| Diretor seleciona gerar relatório |  |
|  | Sistema gera relatório de presença da turma |


## Especificações para Acessar o Registro de Faltas ##
| Nome do Caso de Uso | Acessar o Registro de Faltas |
| --- | --- |
| Ator Principal | Aluno |
| Resumo | O aluno entra no sistema para consultar o número de faltas. |
| Pré Condições | O aluno precisa estar cadastrado em alguma turma. |
| Pós Condições | O aluno precisa ter sido informado sobre sua condição de faltas. |

| Cliente | Sistema |
| --- | --- |
| O aluno entra no sistema  |  |
|  | Sistema apresenta as informações relacionadas as faltas |


## Especificações para Pedir Reavaliação de Faltas ##
| Nome do Caso de Uso | Pedir Reavaliação de Faltas |
| --- | --- |
| Ator Principal | Aluno |
| Atores Secundários  | Diretor |
| Resumo | O aluno abre um requerimento pedindo a reavaliação da falta. |
| Pré Condições | O aluno precisa ter tido uma falta concedida. |
| Pós Condições | Com base na decisão do diretor, o aluno tem ou não a falta alterada. |

| Cliente | Sistema |
| --- | --- |
| O aluno recorre ao recurso de reavaliar a falta |  |
|  | O sistema notifica o diretor sobre a recorrência |



# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
