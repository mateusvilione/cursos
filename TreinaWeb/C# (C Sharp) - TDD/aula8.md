# Testes de performance e carga em aplicações Web

## Testes de performance e carga em aplicações Web

Quando trabalhamos principalmente com aplicações Web, um dos grandes desafios é garantir sua performance principalmente em situações de alta carga e demanda. Mais complicado que isso é mensurar, por exemplo, quantas conexões simultâneas uma aplicação web desenvolvida suporta. E para mensurarmos o tempo de resposta de uma aplicação web, ainda mais com todas as variantes do processo (velocidade da conexão, browser utilizado etc.)?

Para se mensurar o comportamento em especial de aplicações web em situações extremas, como muitas requisições sendo feitas ao mesmo tempo, temos os testes de performance e carga. Cada um destes testes abordam o seguinte ponto:

- Performance: são testes que visam avaliar geralmente o tempo de carregamento de alguma página. Nesse tipo de teste, é levado em conta quanto tempo uma página demora para ser carregada completamente no browser cliente, ou seja, também é contabilizado o tempo de download de cada componente (imagem, script, CSS) da página;
- Carga: é um teste que visa descobrir quais são os limites de uma aplicação, quer seja com relação a hardware ou mesmo algum código que não apresenta uma performance satisfatória. Neste tipo de teste, a aplicação é submetida a uma determinada carga de dados. Essa carga de dados é aumentada com o passar do tempo, afim de que seja descoberto o momento exato onde a aplicação deixa de responder e funcionar, assim como também é investigado o fator que causa a falha da aplicação com um determinado volume de carga;

Testes de performance e carga são importantes justamente por mensurarem as limitações das aplicações, assim como também auxiliar a determinar os possíveis comportamentos que elas apresentarão em momentos de instabilidade e também mensurar a capacidade de resposta temporal de uma aplicação. Os resultados destes testes também servem para demonstrar para um determinado cliente que a aplicação suportará os possíveis cenários.

---

## Ferramentas de testes de carga e performance para a plataforma .NET

Assim como nos demais testes, existem frameworks para auxiliar na execução destes tipos de testes.

### Microsoft Visual Studio Test Tools

![alt text](./img/aula8/1.png " ")

Mais uma vez, o VS Test Tools também nos oferece a possibilidade de executar tanto testes de performance quanto testes de carga. Possui um editor para montar os testes muito similar ao editor para elaboração dos testes de interface. Oferece recursos como a definição de credenciais e de fontes de dados.

Apache JMeter

![alt text](./img/aula8/2.png " ")

Se tratando de testes de carga e performance, o Apache JMeter é a ferramenta mais popular. Escrito completamente em Java, é um projeto open source que está sob os cuidados da Fundação Apache. Permite a realização de testes de performance e carga não somente em aplicações web, mas também em FTPs, webservices (SOA e REST) e até em redes TCP. A página oficial do projeto está hospedada em http://jmeter.apache.org, enquanto o repositório no GitHub está em https://github.com/apache/jmeter

---


## Utilizando o MSTests para fazer testes de performance

---

## Utilizando o MSTests para fazer testes de carga

---

## Utilizando o JMeter para realizar testes de performance e carga

---

## Exercícios