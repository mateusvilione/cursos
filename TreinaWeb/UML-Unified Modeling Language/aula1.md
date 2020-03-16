# Introdução

## Fundamentos de UML
A Linguagem de Modelagem Unificada (UML - Unified Modeling Language) basicamente é uma linguagem visual para documentação de projetos e padrões de software. Aprofundando-se um pouco mais, no entanto, se descobre que UML pode ser aplicada em várias áreas diferentes e pode documentar e transmitir qualquer coisa: da organização da companhia aos processos de negócios para software empresarial. Ela pretende ser uma via comum para a documentação e expressão de relações, comportamentos e ideias de alto nível numa notação que é fácil de aprender e eficiente para escrever. UML é visual; nela, quase tudo tem representação gráfica. Ao longo do curso você aprenderá o significado por trás de vários elementos UML.

---

## Antecedentes
UML se tornou padrão para modelagem de aplicações de software e está crescendo em popularidade na modelagem de outros domínios. Suas raízes recaem em três métodos distintos: O Método Booch, por Grady Booch; a Técnica de Modelagem de Objeto, de coautoria de James Rumbaugh; e Objectory, de Ivar Jacobson. Conhecidos como Os Três Amigos, Booch, Rumbaugh e Jacobson produziram o que veio a ser a primeira versão de UML, em 1994. Em 1997, UML foi aceita pelo Object Management Group (OMG) e editado como UML v1.1.

Desde então, UML passou por diversas revisões e refinamentos, chegando à versão 2.5 atual. Cada revisão tenta atingir problemas e fraquezas identificadas nas versões anteriores, levando à interessante expansão e contração da linguagem. A UML 2.5 é, de longe, a maior especificação de UML em termos de páginas (somente a Superestrutura tem quase 800 páginas), mas representa a mais limpa e compacta versão de UML.

---

## O Básico de UML
Em primeiro lugar, e principalmente, é importante entender que UML é uma linguagem. Significa que ela tem tanto sintaxe como semântica. Quando se modela um conceito em UML, existem regras determinando como os elementos podem ser agrupados e o que isso significa quando eles são organizados em determinada forma.

UML não pretende ser apenas uma representação pictórica de um conceito, mas também informar alguma coisa sobre seu contexto: Como o dispositivo 1 se relaciona com o dispositivo 2? Quando um cliente faz um pedido, como a transação deverá ser manipulada? Como o sistema suporta tolerância a falhas e segurança?

Você pode aplicar UML em qualquer quantidade de formas, mas os usos comuns incluem:

- Projetos de software;
- Comunicação de processos de software ou negócios;
- Documentação de detalhes sobre um sistema, processo ou organização - existente.

UML tem sido aplicada a incontáveis domínios, incluindo:

- Setores bancários e de investimentos;
- Planos de saúde;
- Defesa;
- Computação distribuída;
- Sistemas embutidos;
- Vendas a varejo e suprimento.

O bloco básico de montagem de UML é um diagrama. Existem vários tipos, alguns com propósitos muito específicos (diagramas de tempo) e alguns com usos mais genéricos (diagrama de classe).

---

## Projetando Software
Como UML cresceu a partir do domínio de desenvolvimento de software, não é surpresa que esse seja o domínio em que ela tenha maior aplicação. Quando aplicada a software, UML procura fazer uma ponte sobre o vácuo entre a ideia original para uma parte de software e sua implementação. A UML produz uma via para documentar e discutir os requisitos no nível dos requisitos (diagrama de caso de uso), algumas vezes um novo conceito para projetistas. Existem diagramas para documentar as partes de software que produzem certos requisitos (diagramas de colaboração). Existem diagramas para documentar exatamente como aquelas partes do sistema produzem seus requisitos (diagramas de sequência e de gráfico de estado). Finalmente existem diagramas para mostrar como tudo se acopla e opera (digramas de desdobramento e de componentes).

Os livros que descreveram as versões anteriores de UML fizeram questão de enfatizar que ela não era uma linguagem de programação visual. Entretanto, a UML 2.x altera um pouco essa regra. Uma das maiores motivações para passar da UML 1.5 para a UML 2.0 era a possibilidade de acrescentar a capacidade de os modeladores documentarem mais comportamentos do sistema e automação das ferramentas. Uma técnica relativamente nova, chamada Arquitetura Dirigida ao Modelo (MDA), oferece o poder de se desenvolver modelos executáveis em que as ferramentas podem se conectar e aumentar o nível de abstração acima do nível das linguagens de programação tradicionais. A UML 2.0 é central para a realização da MDA.

É importante entender que UML não é um processo de software. Ela foi projetada para ser utilizada dentro de um processo de software, além de possuir facetas determinadas a tomar parte numa passagem de desenvolvimento interativo.

A UML foi projetada para acomodar ferramentas automatizadas de projeto e esboços rápidos e documentação de projetos “elaborados no guardanapo”.

---

## Modelagem de processos de negócios
UML tem um vocabulário extensivo à documentação de comportamentos e fluxos de processos. Os diagramas de atividades e os gráficos de estado podem ser utilizados para documentação de processos de negócios envolvendo indivíduos, grupos internos ou mesmo organizações completas. A UML 2.5 tem notação que auxilia na modelagem de limites geográficos (partições de atividades), responsabilidades funcionais (pistas de natação) e transações complexas (diagramas de gráfico de estado).

---

## Especificações UML
Fisicamente, UML é um conjunto de especificações do OMG. A UML 2.5 é distribuída em quatro especificações: a Especificação de Intercâmbio de Diagrama, a Infraestrutura UML, a Superestrutura UML e a Linguagem de Restrição de Objetos (OCL). Todas estão disponíveis no site do OMG: http://www.omg.org

A Especificação de Intercâmbio de Diagramas foi escrita para fornecer uma maneira de compartilhar modelos UML entre diferentes ferramentas de modelagem. As versões anteriores de UML definiam um esquema XML para a documentação dos elementos utilizados num diagrama UML, mas não capturavam quaisquer informações sobre como o diagrama era montado. Para resolver esse problema, a Especificação de Intercâmbio de Diagramas foi desenvolvida juntamente com o mapeamento de outro esquema XML para uma representação Gráfica de Vetor Escalável (SVG). A Especificação de Intercâmbio de Diagramas tem sido usada somente por vendedores de ferramentas, embora o OMG faça um esforço para incluir “ferramentas para projetistas”. A Infraestrutura UML define os conceitos fundamentais, de baixo nível, centrais, de maior profundidade em UML; no geral, ela não é utilizada pelo usuário final, mas proporciona a base para Superestrutura UML.

A Superestrutura UML é a definição formal dos elementos de UML. Ela é a autoridade sobre a UML, pelo menos no que concerne ao OMG. A documentação da Superestrutura é tipicamente utilizada por vendedores de ferramentas e por aqueles que escrevem livros sobre UML, embora algumas tentativas tenham sido feitas para torná-la legível aos mais leigos.

A especificação OCL define uma linguagem simples para escrever restrições e expressões para elementos num modelo. A OCL é frequentemente colocada em jogo quando você especifica UML para um domínio em particular e precisa restringir os valores permissíveis para um parâmetro ou objeto.

É importante entender que, embora a especificação seja a fonte definitiva da definição formal de UML, ela não é o todo e o ponto final de UML. UML foi projetada para ser estendida e interpretada de acordo com o domínio, usuário e aplicação específica. Dependendo da especificação, é possível adaptar uma central de dados. Por exemplo, existem duas ou mais maneiras de se representar um conceito UML, dependendo do que aparece melhor no diagrama ou da parte do conceito que se deseja enfatizar. Você poderá representar um elemento em particular, utilizando uma notação caseira – o que é perfeitamente aceitável, você deve tomar cuidado ao utilizar notações não padronizadas, porque um dos motivos principais é justamente por ter uma representação padronizada.