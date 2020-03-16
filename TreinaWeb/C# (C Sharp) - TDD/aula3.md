# Conhecendo teste

## Afinal, pra que testar? O que são estes testes?

Como vimos, nós precisamos testar nossas aplicações para se atingir os seguintes objetivos:

- Qualidade do software;
- Estabilidade do software;
- Rentabilidade do software;
- Conclusão de maneira saudável de todo o ciclo de vida do software.

Quando os objetivos acima são atingidos, a probabilidade de se construir uma aplicação que “morra” prematuramente é extremamente baixa. Um software com qualidade e estável convence sua base de usuários de que realmente vale a pena utilizá-lo. Com isso, a tendência é que a base de usuários da aplicação se torne cada vez maior, pois os próprios usuários farão a “propaganda” do software para outras pessoas. Um software qualitativamente bom e com uma boa base de usuários se torna um software com alto poder de rentabilidade, pois raramente dará gastos que sejam imprevistos, além de que não será necessário perder tempo e mão-de-obra da equipe para corrigir problemas e bugs. Com a equipe desfocada de problemas e bugs do software, é possível canalizar toda a força da equipe para a expansão e melhoria das funcionalidades da aplicação. Tudo isso fará com que a aplicação tenha sucesso e complete todo o ciclo de vida de um software sem maiores problemas.

Há alguns anos a questão do “teste do software” está mais em evidência e a devida atenção vem sendo dada ao tema. Teste de software não é algo que é feito de qualquer maneira: existem algumas normas relacionadas ao tema, inclusive, há uma norma ISO (International Organization for Standarlization) que define o teste de software, a ISO 25010:2011 (ou ISO/IEC 9126 – no Brasil, NBR ISO/IEC 9126). Perceba o grau de seriedade com que teste de software deve ser tratado: há uma norma internacional para defini-lo.

A ISO 25010:2011 na verdade trata de todos os conceitos de qualidade de software, quesito onde o teste de software também se encaixa. Um software deve ser testado justamente para garantir sua qualidade. Ela é baseada nas seguintes características e métricas:

- Funcionalidade: a capacidade de um software prover características e funcionalidades que agreguem valor a seus usuários, ou seja: a capacidade de um software de atender às necessidades dos usuários;
- Confiabilidade: trata-se de quão confiável um software é, incluindo-se tolerância a eventuais falhas e capacidade de recuperar informações em um contexto de falha inesperada;
- Usabilidade: trata-se da capacidade da interface com o usuário que o software apresenta. Este quesito avalia quão atraente um software é para seus usuários, a facilidade de uso e clareza das informações que são apresentadas;
- Eficiência: trata do desempenho do software de maneira geral: tempo de resposta para as solicitações e consumo de recursos computacionais compatíveis com a operação solicitada;
- Manutenibilidade: trata de quão “fácil” é a manutenção de um software (seja do código propriamente dito ou da infraestrutura necessária para que ele seja executado);
- Portabilidade: trata a capacidade de um software de ser executado em diferentes plataformas ou transferido entre diferentes ambientes. Abrange, por exemplo, a capacidade de o software coexistir com outros softwares e o esforço necessário para instalá-lo em um novo ambiente.

Se a avaliação da qualidade de um software é pautada pela norma ISO 25010:2011, é necessário haver alguma maneira de avaliar e mensurar os pontos pautados acima (funcionalidade, confiabilidade, usabilidade, eficiência, manutenibilidade e portabilidade). Como mensurar, por exemplo, quanto um software é eficiente em números? Uma métrica é necessária para se avaliar cada um destes quesitos. E é exatamente neste ponto que entram as diferentes técnicas de teste de software. Cada técnica de teste de software, bem como as ferramentas envolvidas, visa justamente mensurar cada um destes tópicos.

---

## Técnicas de teste de software

Cada técnica de teste de software visa avaliar um determinado tipo de estrutura envolvida: uns avaliam cada funcionalidade do ponto de vista interno (código), outras avaliam a funcionalidade como um todo do ponto de vista externo...De maneira geral, temos as seguintes técnicas de teste de software:

- Caixa-branca: trata-se dos testes que avaliam o comportamento do código-fonte da aplicação, ou seja, avaliam as funcionalidades disponibilizadas do ponto de vista interno, fazendo uma avaliação diretamente do código-fonte. Geralmente, este tipo de teste visa assegurar que as lógicas, quer sejam de processamento ou de regras de negócio, foram implementadas corretamente. Tem esse nome justamente pelo fato de o acesso diretamente ao código-fonte ser necessário;
- Caixa-preta: trata-se dos testes que visam a avaliação do comportamento das funcionalidades do ponto de vista funcional e a integração desta com as demais funcionalidades em um nível externo. Geralmente, são testes baseados em entradas-saídas, onde a saída produzida pelo software é comparada com uma saída esperada para uma determinada entrada, porém, o comportamento interno do software não é levado em consideração neste tipo de teste. Tem esse nome justamente pelo fato de o acesso direto ao código-fonte não ser requerido, embora testes de caixa-preta podem ser realizados diretamente no código-fonte também;
- Caixa-cinza: é uma mistura das técnicas de caixa-preta e caixa-branca, onde a funcionalidade é avaliada ao mesmo tempo que o comportamento interno do software.

Testes com técnica caixa-cinza costumam ser mais utilizados, já que combinam justamente as técnicas de caixa-branca e caixa-preta.

---

## Tipos de teste de software

Podemos ter também diferentes tipos de testes de software, cada um deles visando determinar uma métrica e quantificar uma determinada característica. De maneira geral, temos os seguintes tipos de software:

- Funcional: são testes que visam quantificar quanto um software apresenta como funcionalidades em relação ao que é esperado. Este tipo de teste é focado nas funcionalidades como um todo, verificando se, após uma determinada entrada, a saída esperada é produzida, além de verificar se determinada funcionalidade que era esperada de fato existe no software;
- Regressão: na verdade, testes de regressão consistem na repetição de um determinado conjunto de testes que já foram aplicados quando uma nova versão do software é lançada. Este tipo de teste visa garantir que as alterações que foram realizadas não interferiram nas funcionalidades pré-existentes e que, mesmo após as alterações e atualizações, o software continua funcionando de maneira plena;
- Performance: são testes que visam mensurar a performance do software, ou seja: o tempo que o software demora para retornar uma resposta após a entrada de alguma informação. Por exemplo, um teste de performance em uma funcionalidade de cadastro de usuários visa verificar quanto tempo o software leva para inserir o novo usuário na base de dados e devolver uma resposta para a interface do usuário;
- Stress: são testes que visam verificar qual comportamento o software irá apresentar em cenários extremos. Por exemplo, um teste de stress em uma aplicação web poderia ser a simulação de acesso simultâneo de 10000 usuários ao mesmo tempo. Dependendo do negócio, essa situação é atípica, porém, mesmo assim pode acontecer. Se pode acontecer, o teste de software deve avaliar esta situação. Testes de stress também costumam ser utilizados para se definir os limites técnicos e requisitos mínimos de um software;
- Carga: é um tipo de teste bem similar ao teste de stress, porém, visa a verificação da quantidade de dados que um software pode processar ao mesmo tempo. Por exemplo, a solicitação de inserção de vários usuários em uma base de dados ao mesmo tempo para se verificar quantos usuários podem ser inseridos ao mesmo tempo caracteriza um teste de carga. Geralmente, testes de carga acompanham testes de stress e vice-versa.

---

## Níveis de teste de software

Variando-se o ponto de avaliação de um teste de software, podemos ter vários níveis de teste de software:

- Unitário: consiste nos testes nas menores unidades de seu software, que são avaliadas de maneira separada e independente umas das outras. Como “menor unidade de um software”, você pode entender como sendo os métodos de suas classes ou mesmo métodos que coordenam o funcionamento de alguns outros métodos. Este teste é aplicado geralmente diretamente sob o código-fonte;
- Integração: são testes que visam mensurar a qualidade da integração das unidades do software do ponto de vista interno. Por exemplo: é possível aplicar um teste de integração em um trecho de código que faz a invocação de um webservice por exemplo, visando avaliar a qualidade da integração de se software e este webservice;
- Sistêmico: os testes sistêmicos são feitos sob a perspectiva dos usuários finais visando avaliar se as funcionalidades expostas pelo software realmente atendem aos requisitos que motivaram a construção do software;
- Aceitação: os testes de aceitação geralmente são realizados por um grupo de futuros usuários da aplicação. Estes usuários utilizam a aplicação em condições normais que enfrentarão no dia-a-dia, a fim de verificar se as funcionalidades expostas pelo software atendem aos requisitos no dia-a-dia de utilização do software. Também acabam sendo avaliados itens como a usabilidade do software;
- Operação: geralmente são testes realizados quando a aplicação é colocada em ambiente de produção para verificação de seu comportamento em um ambiente real.

Quando traçamos uma estratégia de teste de software, é necessário combinar-se a técnica com o tipo e o teste adequados para a situação. Por exemplo, podemos ter um teste funcional em nível unitário utilizando-se técnicas de caixa-branca. Isso quer dizer que este teste irá verificar uma determinada funcionalidade (teste funcional) mensurando a qualidade de cada unidade de software (teste unitário) e de maneira direta ao código (teste caixa-branca). Poderíamos representar estes três conceitos no seguinte diagrama:

![alt text](./img/aula3/1.png " ")

A maneira como os testes deverão ser realizados, bem como as técnicas, tipos e níveis que deverão ser aplicados em cada uma das etapas de teste deve ser planejada antecipadamente. A este planejamento inicial, damos o nome de **plano de teste**. É este documento que estabelece quais técnicas, tipos e níveis devem ser aplicados, bem como os determinados momentos em que cada teste deverá ser aplicado. Ele também especifica as condições de teste, como o ambiente onde o teste deve ser realizado ou mesmo a enumeração das entradas e as respectivas saídas que deverão ser produzidas.

Perceba então que todos estes conceitos nos auxiliam a mensurar as características previstas pela ISO 25010:2011. Mais importante ainda: testar um software significa garantir e assegurar que este possui qualidade e pode ser utilizado “sem medo”, sem apresentar comportamentos inesperados ou erros de execução. Por isso é importantíssimo testar de maneira correta um software.

---

## Exercícios

Questão 1 de 3
O que avaliam os testes caixa-branca?

Avaliam os relatórios da aplicação.

✔ O comportamento do código fonte da aplicação.

O comportamento das funcionalidades da aplicação.

Avaliam o comportamento do código fonte em conjunto com as funcionalidades da aplicação.

Avaliam o banco de dados da aplicação.


Questão 2 de 3
Dentre as opções abaixo, qual não é um tipo de teste?

Stress.

Performance.

✔ Refatoração.

Funcional.

Carga.

Questão 3 de 3
Dentre as opções abaixo, qual não é um objetivo que o teste da aplicação procura atingir?

Conclusão de maneira saudável de todo o ciclo de vida do software.

Qualidade do software.

✔ Diminuir o tempo de desenvolvimento.

Estabilidade do software.

Rentabilidade do software.