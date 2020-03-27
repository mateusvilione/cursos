# Testes unitários

##  que são testes unitários?

Teste unitários são uma maneira de o desenvolvedor garantir que o código escrito é funcional e que realmente funciona da maneira que deveria. Diferentemente do teste padrão, onde o desenvolvedor executa pequenos trechos de código e observa os valores obtidos, os testes unitários realizam testes em métodos específicos, fornecendo dados de teste no próprio código. Geralmente, são testes com caixa-branca ou caixa-cinza do tipo funcional em nível unitário.

Os testes unitários são uma importante ferramenta de garantia de qualidade quando fazem parte do seu processo de desenvolvimento de software. O ideal é que assim que você escreva um método, ou outro bloco de código (uma unidade de código, por isso esses testes possuem o nome de “testes unitários”), realize a criação de um teste unitário imediatamente para verificar o comportamento em diferentes situações, como por exemplo, uma entrada incorreta de dados. Dessa maneira, ao mesmo tempo que o software é escrito, ele é também testado, reduzindo-se a possibilidade de os testes serem desprezados pelo menos no nível unitário durante o desenvolvimento da aplicação. É obrigação do desenvolvedor escrever estes testes.

---

## Termos comuns quando utilizamos frameworks de testes unitários

Quando utilizamos frameworks de testes unitários, é normal existirem alguns termos que são comuns entre todos eles. Vamos verificar que termos são estes:

- Test Class: consiste em uma classe convencional, porém, decorada com alguns atributos que dependem do framework de teste unitário a ser utilizado. Esta classe conterá os métodos que definem os testes unitários que deverão ser executados. Geralmente, Test Classes contém somente os métodos que definem os testes unitários e métodos assessores que ajudam a configurar o ambiente de teste unitário. **Estas classes jamais devem conter métodos que serão utilizados pela sua aplicação real!** Elas servem somente para coordenar os testes unitários e nada mais. Na maioria das vezes, elas nem são compiladas e enviadas para um ambiente de produção, já que servem somente na etapa de testes funcionais unitários;
- Test Method: consiste em um método convencional, porém, assim como as Test Classes, contém algumas decorações que variam de acordo com o framework que definem que aquele método na verdade é um teste unitário. É dentro dos Test Methods que você escreverá seus testes que deverão testar as unidades da sua aplicação de maneira isolada umas das outras. Cada Test Method é, na verdade, um teste unitário a ser executado;
- Assert: o Assert consiste em verificar se a saída produzida pela unidade de código testada condiz com a saída de código que era esperada. A saída produzida não precisa ser necessariamente igual a saída esperada: você pode verificar se a saída está em um range esperado, por exemplo.

Podemos montar um diagrama de como ficariam nossas estruturas para testes unitários, independente do framework a ser utilizado:

![alt text](./img/aula4/1.png " ")

---

## Frameworks de teste unitário para a plataforma .NET

Existem algumas ferramentas que podemos utilizar para nos auxiliar na construção de códigos para realização de testes unitários. Estas ferramentas são conhecidas como “frameworks de testes unitários”. São considerados como frameworks porque geralmente eles definem um determinado workflow que deve ser seguido para que os testes sejam criados utilizando-se estas ferramentas. Vamos conhecer as três principais para o ecossistema do .NET: o Microsoft Visual Studio Test Tools (VS Test Tools), o nUnit e o xUnit.NET.

### Microsoft Visual Studio Test Tools

![alt text](./img/aula4/2.png " ")

O Microsoft Visual Studio Test Tools (VS Test Tools ou VS Tests) é um framework já integrado ao ecossistema do .NET que auxilia na criação de testes unitários, quer seja em Visual Basic ou C#.Suas classes ficam disponibilizadas no namespace Microsoft.VisualStudio.TestTools. Na verdade, o Visual Studio Test Tools contempla bem mais do que tests unitários: ele é uma ferramenta completa para realização de testes com todas as técnicas, de todos os tipos e em todos os níveis. Neste curso, em alguns capítulos adiante, voltaremos a falar e inclusive iremos utilizar algumas ferramentas de teste fornecidas pelo Microsoft Visual Studio Test Tools. Nós também utilizaremos, independente do framework utilizado, a aba “Test Explorer”, onde poderemos analisar e até mesmo estabelecer a ordem de nossos testes unitários. Essa aba, que age como se fosse um plugin do Visual Studio, também é provida pelo VS Test Tools.

### NUnit

![alt text](./img/aula4/3.png " ")

O NUnit é um framework muito popular na plataforma .NET específico para testes unitários. É um projeto de código aberto que, inicialmente, consistia na portabilidade para .NET de um framework também muito famoso na plataforma Java, o JUnit. Porém, com o passar do tempo e a evolução das linguagens da plataforma .NET, especialmente o C#, este deixou de ser uma simples portabilidade do código do JUnit para ganhar de fato “vida própria”. Hoje, seu código quase nada tem a ver mais com o código do JUnit e nem com suas versões iniciais, já que o código da versão mais nova (3.0) foi inteiramente reescrito.

O site oficial do NUnit está hospedado em http://nunit.org No site, você pode conferir a documentação, bem como fazer o download dos binários do NUnit. Porém, baixar os binários a partir do site não é necessário: o NUnit é entregável via pacote Nuget atualmente.

### xUnit.NET

![alt text](./img/aula4/4.png " ")

O xUnit.NET é uma outra opção de framework que pode ser utilizado para a escrita dos testes unitários nas linguagens que compõe o .NET Framework. Curiosamente, ele foi inicialmente escrito por um dos contribuidores do NUnit na versão 2.

O xUnit.NET é um framework que está crescendo com força total dentro da plataforma. Sua aceitação foi tão boa que ele agora faz parte da ASP.NET Open Source Gallery. Devido a isso, o xUnit.NET tende a ser o framework oficial para testes unitários especialmente no ASP.NET 5 que será lançado na segunda metade de 2015, substituindo a própria solução da Microsoft nesse âmbito (o Microsoft Test Tools).

O site oficial do xUnit.NET está hospedado em http://xunit.github.io Assim como o NUnit, é um projeto open source, hospedado no GitHub. O xUnit.NET também é entregável via pacote Nuget.

---

## Frameworks de testes unitários - MSTests

![alt text](./img/aula4/5.png " ")

Deletar a Class1.cs

![alt text](./img/aula4/6.png " ")

Criar classe publica Calculadora.cs

![alt text](./img/aula4/7.png " ")

Estabelecendo o limite mínimo através do construtor (ctor + tab + tab, cria o construtor)

![alt text](./img/aula4/8.png " ")

Criar todas as operações da Calculadora

![alt text](./img/aula4/9.png " ")

Criar uma pasta para os `Tests`

![alt text](./img/aula4/10.png " ")

Adicionar novo projeto na pasta `Tests`

![alt text](./img/aula4/11.png " ")

Especificando o projeto de `Tests`

![alt text](./img/aula4/12.png " ")

Nome do projeto de `Tests`

![alt text](./img/aula4/13.png " ")

Classe de `Tests`

![alt text](./img/aula4/14.png " ")

Adicionar as referências para o teste enxergar a classe

![alt text](./img/aula4/15.png " ")

Referência da solução

![alt text](./img/aula4/16.png " ")

- vermelho: janela de testes
- azul: código do teste
- verde: compilar a solução para reconhecer o teste

![alt text](./img/aula4/17.png " ")

A instancia da classe calculadora está repetindo muito, melhor criar um campo privado

```c#
namespace TreinaWeb.Calculadora.MSTests
{
	[TestClass] // Decoração q indica classe de testes
	public class CalculadoraTests
	{

		[TestMethod] // Decoração q indica método de teste
		public void TestSomar()
		{
			TwCalc.Calculadora calc = new TwCalc.Calculadora(); // repetição 
			Assert.AreEqual(4, calc.Somar(2, 2));
		}

		[TestMethod]
		public void TestSubtrair()
		{
			TwCalc.Calculadora calc = new TwCalc.Calculadora(); //repetição 
			Assert.AreEqual(0, calc.Subtrair(2,2));
		}
	}
}

```

Isso gera um erro, pois não foi chamado o new da classe

```c#
namespace TreinaWeb.Calculadora.MSTests
{
	[TestClass] // Decoração q indica classe de testes
	public class CalculadoraTests
	{
		private TwCalc.Calculadora calc;

		[TestMethod] // Decoração q indica método de teste
		public void TestSomar()
		{
			Assert.AreEqual(4, calc.Somar(2, 2));
		}

		[TestMethod]
		public void TestSubtrair()
		{
			Assert.AreEqual(0, calc.Subtrair(2,2));
		}
	}
}
```

- Branco: variável privada da classe Calculadora
- Vermelho: Inicialização do SetUp antes de rodar os testes
- Amarelo: Instância da Calculadora;
- verde: Área de teste
- Rosa: Resultado dos testes
- Azul: CleanUp, limpa a instância da classe

![alt text](./img/aula4/18.png " ")

- Vermelho: Um teste de insucesso que gera uma Exception
- Laranja: É esperado um erro do tipo ArgumentOutOfRangeException

![alt text](./img/aula4/19.png " ")

- Amarelo: A função do teste foi criado, mas não está rodando por causa da decoração `[Ignore]`

![alt text](./img/aula4/20.png " ")

- Vermelho: Remover a referência do projeto de Teste

![alt text](./img/aula4/21.png " ")


---

## Frameworks de testes unitários - NUnit

Criando projeto NUnit

![alt text](./img/aula4/22.png " ")

![alt text](./img/aula4/23.png " ")

![alt text](./img/aula4/24.png " ")

O NUnit é adquirido via pacote nuget

![alt text](./img/aula4/25.png " ")

![alt text](./img/aula4/26.png " ")

Criar classe de teste

![alt text](./img/aula4/27.png " ")

Referência

![alt text](./img/aula4/28.png " ")

Referência da Classe 

![alt text](./img/aula4/29.png " ")

Utilizar o NUnit Test Adapter para o Visual Studio reconhcer os testes

![alt text](./img/aula4/30.png " ")

Testes completo

![alt text](./img/aula4/31.png " ")

---

## Frameworks de testes unitários - xUnit.NET

Seguir os mesmos passos para criação, novo projeto, class Library (.dll)

Adicionar via pacote Nuget os dois pacotes

![alt text](./img/aula4/32.png " ")

Criar a classe, o xUnit não usa as anotações

Adicionar a referência ao projeto

![alt text](./img/aula4/33.png " ")

---

## Exercícios

Questão 1 de 4
Complete o código abaixo, de forma que ele defina uma classe de teste do xUnit.NET corretamente.
```c#
public class ContaTests
{
     
	[Fact]
    public void DebitoComSaldoValido()
    {
        // arrange
        double saldoInicial = 11.99;
        double debito = 4.55;
        double esperado = 7.44;
        
        Conta conta = new Conta("Carlos Silva", saldoInicial);
        
        // act
        conta.Debito(debito);
        
        // assert
        double atual = conta.Saldo;
        Assert.Equal(esperado, atual, 0.001);
    }
} 
```

Questão 2 de 4 errado
Complete corretamente a afirmação abaixo:
É dentro das `test class` que se define os `métodos` que contém os testes unitários que deverão ser executados .

Questão 3 de 4
Complete o código abaixo, de forma que ele defina uma classe de teste do NUnit corretamente.
```c#
[TestFixture]
public class ContaTests
{
    [Test] 
    public void DebitoComSaldoValido()
    {
        // arrange
        double saldoInicial = 11.99;
        double debito = 4.55;
        double esperado = 7.44;
        
        Conta conta = new Conta("Carlos Silva", saldoInicial);
        
        // act
        conta.Debito(debito);
        
        // assert
        double atual = conta.Saldo;
        Assert.AreEqual(esperado, atual, 0.001, "Conta não debitada corretamente");
    }
} 
```

Questão 4 de 4
Complete o código abaixo, de forma que ele defina uma classe de teste corretamente.
```c#
[TestClass]
public class ContaTests
{
	[TestMethod]
    public void DebitoComSaldoValido()
    {
        // arrange
        double saldoInicial = 11.99;
        double debito = 4.55;
        double esperado = 7.44;
        
        Conta conta = new Conta("Carlos Silva", saldoInicial);
        
        // act
        conta.Debito(debito);
        
        // assert
        double atual = conta.Saldo;
        Assert.AreEqual(esperado, atual, 0.001, "Conta não debitada corretamente");
    }
} 
```