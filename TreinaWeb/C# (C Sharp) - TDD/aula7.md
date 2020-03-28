# Testes na interface de usuário

## Testes na interface de usuário

Até este ponto do treinamento, aprendemos como realizar testes em nosso código visando sempre garantir uma maior qualidade no resultado final. No entanto, por mais que consigamos garantir que nossas classes de regra de negócio estejam devidamente testadas e funcionando conforme o esperado, existe outro fator que pode acabar sendo o grande vilão: a interface com o usuário. Não adianta se nossas unidades de software funcionam corretamente se sua integração não ocorre da maneira correta.

Em situações corriqueiras, esse teste da interface da aplicação é feito através de um usuário ou um grupo de usuários que avaliam a aplicação levantando cenários onde a interface não executa as operações como deveria (por exemplo, um botão que deveria executar alguma ação e não executa) ou até mesmo cenários onde a interface funciona da maneira correta, mas as informações não são apresentadas da melhor maneira (por exemplo, o tamanho da fonte de um determinado texto que dificulta sua leitura). Porém, estes testes demandam uma boa quantidade de tempo por parte dos testadores, além de serem extremamente dificultosos para serem executados em larga escala. Também contam com o fato de dependerem da atenção destes testadores: se a equipe que é encarregada de avaliar a interface não dá a devida atenção aos testes, o risco de passar algum problema é bem grande.

Para resolver este problema, podemos utilizar o conceito de testes automatizados que guiam sua aplicação por meio da interface de usuário. Este conceito é também conhecido como Coded UI Tests (CUITs). A utilização deste tipo de teste permite incluir testes funcionais dos controles da interface gráfica, além de verificar se a aplicação está funcionando de ponta a ponta, incluindo a interface gráfica.

---

## Frameworks de teste de interface para a plataforma .NET

Assim como nos testes unitários, existem frameworks que auxiliam na criação de testes automatizados da interface para a plataforma .NET Framework. A utilização de algum destes frameworks é essencial para a criação de testes de interface automatizados.

### Microsoft Visual Studio Test Tools

![alt text](./img/aula7/1.png " ")

O Visual Studio Test Tools também oferece ferramentas para criação de testes automatizados de interface. O VS Test Tools expõe algumas classes para criação e escrita destes testes através do namespace Microsoft.VisualStudio.TestTools.UITesting. Além disso, ao se criar um projeto de teste automatizado de interface, o Visual Studio oferece algumas ferramentas que permitem gravar e editar as operações na interface gráfica que deverão ser executadas nos testes automatizados, assim como também expõe ferramentas que possibilitem se fazer asserções de maneira facilitada.

Você pode criar testes de interface automatizados no Visual Studio criando um projeto do tipo Coded UI Test Project, na categoria Test, no wizard para criação de projetos no Visual Studio (File > New > Project...). Porém, este recurso só está presente nas versões pagas do Visual Studio.


### Selenium

![alt text](./img/aula7/2.png " ")

O Selenium é um framework de código aberto para criação de testes automatizados de interface em aplicações Web. Ele é composto por duas partes:

WebDriver: consiste em uma API exposta para interação com os diversos browsers. É através do WebDriver que podemos, por exemplo, verificar se após se clicar em um link, a página é redirecionada corretamente;
IDE: uma espécie de IDE integrada através de um plugin para escrita de scripts de testes de maneira mais rápida diretamente no browser. Esse plugin está disponível para o Mozilla Firefox.
A página do GitHub do Selenium está hospedada em https://github.com/SeleniumHQ, enquanto a página oficial está hospedada em http://docs.seleniumhq.org

---

## Testes de interface com MSTests - Parte 1

Criar projeto de interface Windows Form Application

---

## Testes de interface com MSTests - Parte 2

criar teste de interface

![alt text](./img/aula7/3.png " ")

Gravar a tela, executar o .exe no build, também é exibido no Test Explorer

![alt text](./img/aula7/4.png " ")

---

## Testes de interface com Selenium - Parte 1

Adicionar na solução um projeto Web

![alt text](./img/aula7/5.png " ")

![alt text](./img/aula7/6.png " ")

![alt text](./img/aula7/7.png " ")

Definir como projeto de inicialização


---

## Testes de interface com Selenium - Parte 2


---

## Exercícios