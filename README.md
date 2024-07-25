# 💻 Programação Orientada a Objetos com C#

Este artigo foi elaborado com o objetivo de compartilhar o conhecimento adquirido através das aulas e bootcamps oferecidos pela Digital Innovation One (DIO). A DIO é uma plataforma que se destaca por proporcionar uma ampla gama de cursos e treinamentos voltados ao desenvolvimento de habilidades técnicas e práticas em diversas áreas da tecnologia, incluindo a programação orientada a objetos (POO) com C#.



Ao longo deste artigo, abordaremos os conceitos fundamentais da POO, como objetos e classes, encapsulamento, herança, polimorfismo e abstração, e mostraremos como implementá-los na linguagem C#. Além disso, apresentaremos um exemplo prático de um sistema de gerenciamento de biblioteca para ilustrar a aplicação desses conceitos em um cenário real.



As boas práticas em POO, incluindo padrões de design e princípios SOLID, também serão discutidas, juntamente com a importância dos testes unitários para garantir a qualidade do código. Este artigo é uma fonte valiosa para desenvolvedores que desejam aprimorar suas habilidades e se aprofundar no desenvolvimento de software com C#.



Agradecemos à DIO pelo excelente conteúdo educacional e suporte, que foram fundamentais para a elaboração deste material. Esperamos que este artigo contribua para o seu crescimento profissional e o inspire a continuar explorando o fascinante mundo da programação orientada a objetos com C#.

<br>

 1 - Introdução

* Apresentação do tema
* Importância da Programação Orientada a Objetos (POO)
* Por que usar C# para POO

2 - Conceitos Básicos de POO

* Objetos e Classes
* Encapsulamento
* Herança
* Polimorfismo
* Abstração

3 - Introdução ao C#

* Visão geral da linguagem
* aracterísticas principais
* Ambiente de desenvolvimento (Visual Studio, .NET)

4 - Implementação de POO em C#

* Definição de Classes e Objetos
* Propriedades e Métodos
* Encapsulamento em C#
* Herança em C#
* Polimorfismo em C#
* Abstração em C#

5 - Exemplo Prático

* Descrição do problema a ser resolvido
* Implementação passo a passo
* Explicação do código

6 - Boas Práticas em POO com C#

* Design Patterns comuns
* Princípios SOLID
* Testes unitários

7 - Conclusão

* Recapitulação dos pontos principais
* Benefícios de usar POO com C#
* Considerações finais

## ❗ Vamos desenvolver cada seção com mais detalhes.


## 1 - Introdução

A Programação Orientada a Objetos (POO) é um paradigma de programação amplamente utilizado no desenvolvimento de software. Ela se baseia no conceito de "objetos", que podem conter dados e métodos. A POO facilita a organização e a modularização do código, tornando-o mais reutilizável e fácil de manter. O C# (C Sharp) é uma linguagem de programação moderna e orientada a objetos, desenvolvida pela Microsoft como parte da plataforma .NET. Utilizar C# para desenvolver aplicações orientadas a objetos oferece diversas vantagens, incluindo forte tipagem, gerenciamento automático de memória e uma ampla biblioteca de classes.

## 2 - Conceitos Básicos de POO

### Objetos e Classes

Classe: Uma classe é um molde ou modelo que define as características e comportamentos que os objetos criados a partir dela terão. Em C#, uma classe é definida usando a palavra-chave class.
Objeto: Um objeto é uma instância de uma classe. Ele representa uma entidade real com características e comportamentos definidos pela classe.

```
public class Pessoa
{
  public string Nome { get; set; }
  public int Idade { get; set; }

  public void Apresentar()
   {
      Console.WriteLine($"Olá, meu nome é {Nome} e eu tenho {Idade} anos.");
   }
}

Pessoa pessoa1 = new Pessoa();
pessoa1.Nome = "João"; 
pessoa1.Idade = 30; 
pessoa1.Apresentar();
```
### Encapsulamento


Encapsulamento é o conceito de esconder os detalhes internos de um objeto e expor apenas o que é necessário. Em C#, isso é feito usando modificadores de acesso como public, private, protected e etc.
```
public class ContaBancaria
{
    private double saldo;


    public void Depositar(double valor)
    {
        if (valor > 0)
        {
            saldo += valor;
        }
    }


    public double ObterSaldo()
    {
        return saldo;
    }
}
```
### Herança
Herança permite que uma classe (subclasse) herde as características e comportamentos de outra classe (superclasse). Em C#, usa-se o símbolo : para indicar herança.
```
public class Animal
{
    public void Comer()
    {
        Console.WriteLine("O animal está comendo.");
    }
}


public class Cachorro : Animal
{
    public void Latir()
    {
        Console.WriteLine("O cachorro está latindo.");
    }
}


Cachorro cachorro = new Cachorro();
cachorro.Comer();
cachorro.Latir();
```
### Polimorfismo
Polimorfismo é a capacidade de um objeto assumir diferentes formas. Em C#, isso é geralmente implementado através de métodos sobrecarregados ou métodos substituídos.
```
public class Forma
{
    public virtual void Desenhar()
    {
        Console.WriteLine("Desenhando uma forma.");
    }
}


public class Circulo : Forma
{
    public override void Desenhar()
    {
        Console.WriteLine("Desenhando um círculo.");
    }
}


Forma forma = new Circulo();
forma.Desenhar();  // Saída: Desenhando um círculo.

```
### Abstração
Abstração é o conceito de simplificar a complexidade do mundo real ao modelar classes em um nível de implementação elevado, focando apenas nos detalhes relevantes.
```
public abstract class Veiculo
{
    public abstract void Mover();
}


public class Carro : Veiculo
{
    public override void Mover()
    {
        Console.WriteLine("O carro está se movendo.");
    }
}


Veiculo veiculo = new Carro();
veiculo.Mover();
```
## 3 - Introdução ao C#
O C# é uma linguagem de programação orientada a objetos, desenvolvida pela Microsoft como parte da plataforma .NET. É amplamente utilizada para desenvolver aplicações desktop, web e móveis. Algumas das características principais do C# incluem:
* Sintaxe limpa e moderna: O C# foi projetado para ser fácil de ler e escrever, com uma sintaxe clara e concisa.
* Suporte a POO: O C# tem suporte completo a conceitos de POO, como classes, objetos, herança, polimorfismo, encapsulamento e abstração.
* Gerenciamento de memória: O C# utiliza coleta de lixo automática para gerenciar a memória, o que ajuda a evitar vazamentos de memória.
* Plataforma .NET: A plataforma .NET fornece uma ampla biblioteca de classes que pode ser usada para desenvolver aplicações robustas e eficientes.

### Ambiente de Desenvolvimento

O Visual Studio é o ambiente de desenvolvimento integrado (IDE) mais popular para o desenvolvimento em C#. Ele oferece diversas ferramentas e recursos que facilitam o desenvolvimento, depuração e manutenção de aplicações.

## 4 - Implementação de POO em C#

### Definição de Classes e Objetos


### Classes
Uma classe é uma estrutura que define um tipo de objeto. Ela serve como um molde ou template a partir do qual os objetos são criados. A classe define as propriedades e comportamentos que os objetos criados a partir dela terão.

Componentes de uma classe:
Atributos: Também chamados de variáveis de instância, são as características ou propriedades que os objetos da classe terão.
Métodos: São funções definidas dentro da classe que descrevem os comportamentos ou ações que os objetos podem executar.


### Objetos
Um objeto é uma instância de uma classe. Quando uma classe é definida, nenhum espaço na memória é alocado até que objetos dessa classe sejam criados. Cada objeto criado a partir da classe pode ter valores diferentes para os atributos definidos na classe.



### Resumo
Classe: Define um tipo de objeto, incluindo atributos e métodos.
Objeto: Uma instância de uma classe, com valores específicos para os atributos definidos na classe.


Essa abordagem permite organizar o código de maneira modular e facilita a reutilização e manutenção.
```
public class Carro
{
    public string Marca { get; set; }
    public string Modelo { get; set; }
    public int Ano { get; set; }


    public void ExibirInformacoes()
    {
        Console.WriteLine($"Marca: {Marca}, Modelo: {Modelo}, Ano: {Ano}");
    }
}


Carro carro = new Carro();
carro.Marca = "Toyota";
carro.Modelo = "Corolla";
carro.Ano = 2021;
carro.ExibirInformacoes();
```

### Propriedades e Métodos
As propriedades permitem que os atributos da classe sejam acessados e modificados, enquanto os métodos definem os comportamentos da classe.
```
public class Produto
{
    public string Nome { get; set; }
    public double Preco { get; set; }


    public double CalcularDesconto(double percentual)
    {
        return Preco - (Preco * percentual / 100);
    }
}
```
### Encapsulamento em C#
Em C#, o encapsulamento é implementado usando modificadores de acesso, como public, private, protected e internal.
```
public class Cliente
{
    private string nome;


    public string Nome
    {
        get { return nome; }
        set { nome = value; }
    }


    public void ExibirNome()
    {
        Console.WriteLine($"Nome do cliente: {Nome}");
    }
}
```
### Herança em C#
Em C#, uma classe pode herdar de outra classe usando o símbolo :. A classe base fornece a funcionalidade básica, enquanto a classe derivada pode adicionar ou modificar essa funcionalidade.
```
public class Veiculo
{
    public string Marca { get; set; }
    public string Modelo { get; set; }


    public void ExibirDetalhes()
    {
        Console.WriteLine($"Marca: {Marca}, Modelo: {Modelo}");
    }
}


public class Carro : Veiculo
{
    public int Ano { get; set; }


    public void ExibirDetalhesCompletos()
    {
        ExibirDetalhes();
        Console.WriteLine($"Ano: {Ano}");
    }
} 
```

### Polimorfismo em C#
O polimorfismo é implementado usando métodos virtuais e sobrecarregados.
```
public class Forma
{
    public virtual void Desenhar()
    {
        Console.WriteLine("Desenhando uma forma.");
    }
}


public class Quadrado : Forma
{
    public override void Desenhar()
    {
        Console.WriteLine("Desenhando um quadrado.");
    }
}
```

### Abstração em C#
A abstração é implementada usando classes e métodos abstratos.
```
public abstract class Animal
{
    public abstract void EmitirSom();
}


public class Gato : Animal
{
    public override void EmitirSom()
    {
        Console.WriteLine("O gato faz miau.");
    }
}
```

## 5 - Exemplo Prático

### Descrição do problema

Definição das Classes
Vamos definir as classes principais do sistema: Livro, Usuario, Emprestimo e Biblioteca.
```
// Classe Livro
public class Livro
{
    public string Titulo { get; set; }
    public string Autor { get; set; }
    public string ISBN { get; set; }
    public bool Disponivel { get; set; } = true;


    public void ExibirInformacoes()
    {
        Console.WriteLine($"Título: {Titulo}, Autor: {Autor}, ISBN: {ISBN}, Disponível: {Disponivel}");
    }
}


// Classe Usuario
public class Usuario
{
    public string Nome { get; set; }
    public string Email { get; set; }
    public List<Emprestimo> Emprestimos { get; set; } = new List<Emprestimo>();


    public void ExibirInformacoes()
    {
        Console.WriteLine($"Nome: {Nome}, Email: {Email}, Empréstimos: {Emprestimos.Count}");
    }
}


// Classe Emprestimo
public class Emprestimo
{
    public Livro Livro { get; set; }
    public Usuario Usuario { get; set; }
    public DateTime DataEmprestimo { get; set; }
    public DateTime? DataDevolucao { get; set; }


    public void ExibirInformacoes()
    {
        Console.WriteLine($"Livro: {Livro.Titulo}, Usuário: {Usuario.Nome}, Data de Empréstimo: {DataEmprestimo}, Data de Devolução: {(DataDevolucao.HasValue ? DataDevolucao.Value.ToString() : "Não devolvido")}");
    }
}


// Classe Biblioteca
public class Biblioteca
{
    public List<Livro> Livros { get; set; } = new List<Livro>();
    public List<Usuario> Usuarios { get; set; } = new List<Usuario>();


    public void AdicionarLivro(Livro livro)
    {
        Livros.Add(livro);
        Console.WriteLine("Livro adicionado com sucesso.");
    }


    public void CadastrarUsuario(Usuario usuario)
    {
        Usuarios.Add(usuario);
        Console.WriteLine("Usuário cadastrado com sucesso.");
    }


    public void RealizarEmprestimo(Livro livro, Usuario usuario)
    {
        if (livro.Disponivel)
        {
            Emprestimo emprestimo = new Emprestimo
            {
                Livro = livro,
                Usuario = usuario,
                DataEmprestimo = DateTime.Now
            };
            livro.Disponivel = false;
            usuario.Emprestimos.Add(emprestimo);
            Console.WriteLine("Empréstimo realizado com sucesso.");
        }
        else
        {
            Console.WriteLine("Livro indisponível.");
        }
    }


    public void RegistrarDevolucao(Livro livro)
    {
        Emprestimo emprestimo = livro.Emprestimos.FirstOrDefault(e => e.Livro == livro && !e.DataDevolucao.HasValue);
        if (emprestimo != null)
        {
            emprestimo.DataDevolucao = DateTime.Now;
            livro.Disponivel = true;
            Console.WriteLine("Devolução registrada com sucesso.");
        }
        else
        {
            Console.WriteLine("Este livro não está emprestado.");
        }
    }
}
```

### Explicação do Código
* Classe Livro: Representa um livro na biblioteca. Possui propriedades como Titulo, Autor, ISBN e Disponivel. O método ExibirInformacoes exibe os detalhes do livro.
* Classe Usuario: Representa um usuário da biblioteca. Possui propriedades como Nome, Email e uma lista de Emprestimos. O método ExibirInformacoes exibe os detalhes do usuário.
* Classe Emprestimo: Representa um empréstimo de um livro. Possui propriedades como Livro, Usuario, DataEmprestimo e DataDevolucao. O método ExibirInformacoes exibe os detalhes do empréstimo.
* Classe Biblioteca: Representa a biblioteca e contém listas de livros e usuários. Possui métodos para adicionar livros, cadastrar usuários, realizar empréstimos e registrar devoluções.

### Demonstração do Sistema
Vamos criar um pequeno programa para demonstrar o funcionamento do sistema de gerenciamento de biblioteca.
```
class Program
{
    static void Main(string[] args)
    {
        Biblioteca biblioteca = new Biblioteca();


        // Adicionando livros
        Livro livro1 = new Livro { Titulo = "O Senhor dos Anéis", Autor = "J.R.R. Tolkien", ISBN = "123456789" };
        Livro livro2 = new Livro { Titulo = "Harry Potter", Autor = "J.K. Rowling", ISBN = "987654321" };
        biblioteca.AdicionarLivro(livro1);
        biblioteca.AdicionarLivro(livro2);


        // Cadastrando usuários
        Usuario usuario1 = new Usuario { Nome = "João Silva", Email = "joao@example.com" };
        Usuario usuario2 = new Usuario { Nome = "Maria Oliveira", Email = "maria@example.com" };
        biblioteca.CadastrarUsuario(usuario1);
        biblioteca.CadastrarUsuario(usuario2);


        // Realizando empréstimo
        biblioteca.RealizarEmprestimo(livro1, usuario1);


        // Exibindo informações
        livro1.ExibirInformacoes();
        usuario1.ExibirInformacoes();


        // Registrando devolução
        biblioteca.RegistrarDevolucao(livro1);


        // Exibindo informações após devolução
        livro1.ExibirInformacoes();
        usuario1.ExibirInformacoes();
    }
}
```
## 6 - Boas Práticas em POO com C#


### Design Patterns Comuns
* Singleton: Garante que uma classe tenha apenas uma instância e fornece um ponto global de acesso a ela.
* Factory Method: Define uma interface para criar objetos, mas permite que subclasses alterem o tipo de objetos que serão criados.
* Observer: Define uma dependência um-para-muitos entre objetos, onde quando um objeto muda de estado, todos os seus dependentes são notificados e atualizados automaticamente.


### Princípios SOLID
* S: Princípio da Responsabilidade Única (Single Responsibility Principle)
* O: Princípio do Aberto-Fechado (Open/Closed Principle)
* L: Princípio da Substituição de Liskov (Liskov Substitution Principle)
* I: Princípio da Segregação de Interfaces (Interface Segregation Principle)
* D: Princípio da Inversão de Dependência (Dependency Inversion Principle)

### Testes Unitários
Escrever testes unitários é uma prática essencial para garantir que o código funcione conforme o esperado e para facilitar a manutenção e refatoração do código.
```
using NUnit.Framework;


[TestFixture]
public class BibliotecaTests
{
    [Test]
    public void AdicionarLivro_DeveAdicionarLivroNaLista()
    {
        Biblioteca biblioteca = new Biblioteca();
        Livro livro = new Livro { Titulo = "Teste", Autor = "Autor Teste", ISBN = "123" };
        
        biblioteca.AdicionarLivro(livro);


        Assert.Contains(livro, biblioteca.Livros);
    }


    [Test]
    public void RealizarEmprestimo_DeveMarcarLivroComoIndisponivel()
    {
        Biblioteca biblioteca = new Biblioteca();
        Livro livro = new Livro { Titulo = "Teste", Autor = "Autor Teste", ISBN = "123" };
        Usuario usuario = new Usuario { Nome = "Usuario Teste", Email = "teste@example.com" };


        biblioteca.AdicionarLivro(livro);
        biblioteca.CadastrarUsuario(usuario);
        biblioteca.RealizarEmprestimo(livro, usuario);

        Assert.IsFalse(livro.Disponivel);
    }
}
```

## 7. Conclusão


A Programação Orientada a Objetos com C# oferece uma maneira eficiente e organizada de desenvolver software. Utilizando os conceitos de POO, como encapsulamento, herança, polimorfismo e abstração, é possível criar sistemas robustos e fáceis de manter. Além disso, seguindo boas práticas e princípios de design, como os padrões de projeto e os princípios SOLID, os desenvolvedores podem garantir que seus códigos sejam mais reutilizáveis, escaláveis e de fácil manutenção.

Se você deseja desenvolver aplicações com qualidade e eficiência, aprender e aplicar POO com C# é um passo fundamental na sua jornada como desenvolvedor de software.


# OBRIGADO POR LER!


### Escrito por LeoMarxs

https://github.com/LeoMarxs

https://www.linkedin.com/in/leonardohmarques/

https://www.instagram.com/leo.marxs/?next=%2F

https://www.dio.me/users/leonardomarquesj2004

