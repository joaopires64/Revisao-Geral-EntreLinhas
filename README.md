# Revisao-Geral-EntreLinhas



## Na aula de hoje, vamso fazer uma revisão de toda a matéria estudada até o momento, com foco em revisar tudo o que foi visto anteriormente para a prova da semana que vem.





### Exercício n° 1



Vamos relembrar alguns dos principais tipos de variaveis, abaixo você devera alocar o tipo da variavel correto de acordo com o dado que ela representa



Código:



     Console.WriteLine("Escreva seu nome:");

     /*Qual o tipo mais adequado para nome*/ nome = Console.ReadLine();

     

     Console.WriteLine("Escreva sua idade:");

     /*Qual o tipo mais adequado para idade*/ idade = /*tipo*/.Parse(Console.ReadLine());

     

     Console.WriteLine($"Escreva sua altura em metros");

     /*Qual o tipo mais adequado para altura*/ altura = /*tipo*/.Parse(Console.ReadLine());

     

     Console.WriteLine("Escreva se você é do sexo feminino 'm' = masculino, 'f' = feminino");

     /*Qual o tipo mais adequado para sexo*/ sexo = /*tipo*/.Parse(Console.ReadLine());

     

     do{

     if (sexo == 'm' || sexo == 'f')

     {

         Console.Write("");

     }

     else

     {

         Console.WriteLine("Sexo inválido. Por favor, insira 'm' para masculino ou 'f' para feminino.");

     }

     }while (sexo != 'm' && sexo != 'f');

     

     Console.WriteLine("Você é um estudante de nivel basico ou superior? 's' = sim, 'n' = não");

     string estudantestring = Console.ReadLine();

     

     /*Qual o tipo de variavel estudante, pode ser verdadeiro ou falso*/

     /*tipo*/ estudantestring = true;

     

     if (estudantestring == 'n')

     {

        estudante == false;

     }

     

     

     if (estudante == true)

     {

         Console.WriteLine("Seu nome é " + nome + ", você tem " + idade + " anos, sua altura é " + altura + " metros, você é do sexo " + sexo + " e você é um estudante.");

     }

     else

     {

         Console.WriteLine("Seu nome é " + nome + ", você tem " + idade + " anos, sua altura é " + altura + " metros, você é do sexo " + sexo + " e você não é um estudante.");

     }



### Exercício n° 2



Neste exercício, vamos verificar as informações sobre um determinado numero, se ele é inteiro ou não, se é um numero positivo ou negativo (zero conta como um número positivo), se o numero é pár ou impar, e por fim se o número é primo ou não.

Código:

    // pedir e receber um número do usuário
    using System.Reflection.Metadata;
    
    Console.WriteLine("Escreva um número qualquer:");
    double numero = double.Parse(Console.ReadLine());
    
    // boleanos verificadores, no caso se é inteiro, positivo, par ou primo
    bool inteiro = false, positivo = false, par = false, primo = false;
    
    
    // primeiro verificar se é inteiro
    
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/
    (numero % 1 == 0)
    {
        inteiro = true;
    }
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/
    {
        inteiro = false;
    }
    
    
    // agora verificar se é positivo ou negativo
    
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/ (numero > 0)
    {
        positivo = true;
    }
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/ (numero == 0)
    {
        positivo = true;
    }
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/
    {
        positivo = false;
    }


    // agora verificar se é par ou ímpar


    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/ (numero % 2 == 0)
    {
        case true:
            par = true;
            break;
        case false:
            par = false;
            break;
    }


    // agora vamos verificar se é primo ou não


    int contador = 0;
    for (int i = 1; i <= numero; i++)
    {
       /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/ (numero % i == 0)
        {
            contador++;
        }
    }
    
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/
     (contador == 2)
    {
        primo = true;
    }
    /*qual estrutura deve ser escrita aqui? (if, else, if-else ou switch ?)*/
    {
        primo = false;
    }

    // agora vamos mostrar os resultados para o usuário
    Console.WriteLine($"O número {numero} é inteiro? {inteiro}");
    Console.WriteLine($"O número {numero} é positivo? {positivo}");
    Console.WriteLine($"O número {numero} é par? {par}");
    Console.WriteLine($"O número {numero} é primo? {primo}");




### Exercício n° 3



repetição



### Exercício n° 4



modularização (metodos, função  e procedimento)



### Exercício n° 5



vetor 



### Exercício n° 6 - Faça o seu proprio programa.



Por fim, o no ultimo exercício, você deverá criar um programa do zero, mais especificamente uma calculadora.



Não haverá exigencias em especifico, apenas que os requisitos do exercício sejam atendidos. 



Requisitos:



* O programa deve fazer as seguintes operações : Adição(A + B), Subtração(A - B), Multiplicação(A * B), Divisão(A / B) , Potenciação (A ^ B) E Radiciação (B √ A).



* O programa deve aceitar entradas e saídas corretamente.



* O programa deve ter uma variavel que salva o resultado do ultimo calculo.   Exemplo: 2 + 5 = 7 (resultado do ultimo calculo) , depois 4 * ultimo calculo = 28.



* O programa deve fazer as operações repetidas vezes.
