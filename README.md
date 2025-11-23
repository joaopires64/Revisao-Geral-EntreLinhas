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

Neste exercício, você deve escrever uma palavra ou nome, e dizer quantidade de vogais, consoantes, espaços, caracteres especiais, vogais acentuadas e vogais maiusculas e consoantes maiusculas.

Codigo:

    string entrada;

    // loop para sempre repetir o programa

    /*qual estrutura de repetição devemos usar, while, do-while, for, foreach?*/
    {
       Console.WriteLine("Escreva uma palavra ou frase:");
       entrada = Console.ReadLine();
       char[] dividir = entrada.ToCharArray();

       // Arrays declarados aqui, mas só serão criados depois de contarmos
       char[] vogais;
       char[] consoantes;
    
       int contadorvogais = 0, contadorconsoantes = 0, contadorespacos = 0, contadoroutroscaracteres = 0;
    
       // repetição para contar quantas vogais e consoantes existem na frase
    
       /*qual estrutura de repetição devemos usar, while, do-while, for, foreach?*/
       (int i = 0; i < dividir.Length; i++)
        {
          if (dividir[i] == 'a' || dividir[i] == 'e' || dividir[i] == 'i' || dividir[i] == 'o' || dividir[i] == 'u' ||
              dividir[i] == 'A' || dividir[i] == 'E' || dividir[i] == 'I' || dividir[i] == 'O' || dividir[i] == 'U' ||
              dividir[i] == 'á' || dividir[i] == 'é' || dividir[i] == 'í' || dividir[i] == 'ó' || dividir[i] == 'ú' ||
              dividir[i] == 'Á' || dividir[i] == 'É' || dividir[i] == 'Í' || dividir[i] == 'Ó' || dividir[i] == 'Ú' ||
              dividir[i] == 'à' || dividir[i] == 'è' || dividir[i] == 'ì' || dividir[i] == 'ò' || dividir[i] == 'ù' ||
              dividir[i] == 'À' || dividir[i] == 'È' || dividir[i] == 'Ì' || dividir[i] == 'Ò' || dividir[i] == 'Ù' ||
              dividir[i] == 'ã' || dividir[i] == 'õ' || dividir[i] == 'Ã' || dividir[i] == 'Õ' ||
              dividir[i] == 'â' || dividir[i] == 'ê' || dividir[i] == 'î' || dividir[i] == 'ô' || dividir[i] == 'û' ||
              dividir[i] == 'Â' || dividir[i] == 'Ê' || dividir[i] == 'Î' || dividir[i] == 'Ô' || dividir[i] == 'Û')
          {
             contadorvogais++;
          }
          else if (dividir[i] == ' ')
          {
             contadorespacos++;
          }
          else if ((dividir[i] >= 'b' && dividir[i] <= 'z') || (dividir[i] >= 'B' && dividir[i] <= 'Z'))
          {
             contadorconsoantes++;
          }
          else
          {
             contadoroutroscaracteres++;
          }
       }
    
       // criar os arrays com o tamanho exato
       vogais = new char[contadorvogais];
       consoantes = new char[contadorconsoantes];
    
       int indiceVogal = 0;
       int indiceConsoante = 0;
    
       // preencher novo array com vogais e consoantes
    
    
       /*qual estrutura de repetição devemos usar, while, do-while, for, foreach?*/
       (int i = 0; i < dividir.Length; i++)
        {
          if (dividir[i] == 'a' || dividir[i] == 'e' || dividir[i] == 'i' || dividir[i] == 'o' || dividir[i] == 'u' ||
              dividir[i] == 'A' || dividir[i] == 'E' || dividir[i] == 'I' || dividir[i] == 'O' || dividir[i] == 'U' ||
              dividir[i] == 'á' || dividir[i] == 'é' || dividir[i] == 'í' || dividir[i] == 'ó' || dividir[i] == 'ú' ||
              dividir[i] == 'Á' || dividir[i] == 'É' || dividir[i] == 'Í' || dividir[i] == 'Ó' || dividir[i] == 'Ú' ||
              dividir[i] == 'à' || dividir[i] == 'è' || dividir[i] == 'ì' || dividir[i] == 'ò' || dividir[i] == 'ù' ||
              dividir[i] == 'À' || dividir[i] == 'È' || dividir[i] == 'Ì' || dividir[i] == 'Ò' || dividir[i] == 'Ù' ||
              dividir[i] == 'ã' || dividir[i] == 'õ' || dividir[i] == 'Ã' || dividir[i] == 'Õ' ||
              dividir[i] == 'â' || dividir[i] == 'ê' || dividir[i] == 'î' || dividir[i] == 'ô' || dividir[i] == 'û' ||
              dividir[i] == 'Â' || dividir[i] == 'Ê' || dividir[i] == 'Î' || dividir[i] == 'Ô' || dividir[i] == 'Û')
          {
             vogais[indiceVogal] = dividir[i];
             indiceVogal++;
          }
          else if ((dividir[i] >= 'b' && dividir[i] <= 'z') || (dividir[i] >= 'B' && dividir[i] <= 'Z'))
          {
             if (dividir[i] != ' ')
             {
                consoantes[indiceConsoante] = dividir[i];
                indiceConsoante++;
             }
          }
       }

       // contar vogais acentuadas e maiúsculas
    
       int contadorvogaisacentudas = 0;
       int contadorvogaismaisculas = 0;
       int contadorconsoantesmaisculas = 0;
    
       /*qual estrutura de repetição devemos usar, while, do-while, for, foreach?*/
       (char vogal in vogais)
        {
          if (vogal == 'á' || vogal == 'é' || vogal == 'í' || vogal == 'ó' || vogal == 'ú' ||
              vogal == 'Á' || vogal == 'É' || vogal == 'Í' || vogal == 'Ó' || vogal == 'Ú' ||
              vogal == 'à' || vogal == 'è' || vogal == 'ì' || vogal == 'ò' || vogal == 'ù' ||
              vogal == 'À' || vogal == 'È' || vogal == 'Ì' || vogal == 'Ò' || vogal == 'Ù' ||
              vogal == 'ã' || vogal == 'õ' || vogal == 'Ã' || vogal == 'Õ' ||
              vogal == 'â' || vogal == 'ê' || vogal == 'î' || vogal == 'ô' || vogal == 'û' ||
              vogal == 'Â' || vogal == 'Ê' || vogal == 'Î' || vogal == 'Ô' || vogal == 'Û')
          {
             contadorvogaisacentudas++;
          }
    
    
          if (vogal == 'Á' || vogal == 'É' || vogal == 'Í' || vogal == 'Ó' || vogal == 'Ú' ||
              vogal == 'À' || vogal == 'È' || vogal == 'Ì' || vogal == 'Ò' || vogal == 'Ù' ||
              vogal == 'Â' || vogal == 'Ê' || vogal == 'Î' || vogal == 'Ô' || vogal == 'Û' ||
              vogal == 'Ã' || vogal == 'Õ' ||
              vogal == 'A' || vogal == 'E' || vogal == 'I' || vogal == 'O' || vogal == 'U')
          {
             contadorvogaismaisculas++;
          }
       }
    
    
       /*qual estrutura de repetição devemos usar, while, do-while, for, foreach?*/ (char consoante in consoantes)
        {
          if (consoante >= 'B' && consoante <= 'Z')
          {
             contadorconsoantesmaisculas++;
          }
       }
    
       Console.WriteLine($"\nNúmero de vogais: {contadorvogais}");
       Console.WriteLine($"Número de consoantes: {contadorconsoantes}");
       Console.WriteLine($"Número de espaços: {contadorespacos}");
       Console.WriteLine($"Número de outros caracteres: {contadoroutroscaracteres}");
       Console.WriteLine($"Número de vogais acentuadas: {contadorvogaisacentudas}");
       Console.WriteLine($"Número de vogais maiúsculas: {contadorvogaismaisculas}");
       Console.WriteLine($"Número de consoantes maiúsculas: {contadorconsoantesmaisculas}\n");
    
        } while (entrada != "0") ;



### Exercício n° 4

Vamos a um exercício bem simples de modularização, nesse progarma vamos escrever uma frasem e temos a opção de adicionar mais uma frase a ela ou simplesmente repeti-la quanata vezes solicitadas

Código:


    using System;
    
    class Program
    {
        /*Essa função foi declarada no Main, qual o nome que foi declarado lá?*/(string fraseOriginal, int vezes)
        {
    
            string resultado = fraseOriginal;
    
    
            for (int i = 1; i < vezes; i++)
            {
    
                resultado += " " + fraseOriginal;
            }
    
            return resultado;
        }
    
        static void AdicionarFrase(string frase1, string frase2)
        {
            Console.WriteLine(frase1 + " " + frase2);
        }
    
        static void Main(string[] args)
        {
            Console.WriteLine("Escreva uma frase qualquer: ");
            string frase = Console.ReadLine();
    
            Console.WriteLine("Você quer multiplicar a frase ou adicionar mais frases? (M/A)");
            string escolha = Console.ReadLine().ToUpper(); 
    
            if (escolha == "M")
            {
                Console.WriteLine("Escreva quantas repetições você quer:"); 
                
    
                int multiplicador = int.Parse(Console.ReadLine());
                
                Console.WriteLine(MultiplicarFrase(frase, multiplicador));
            }
            else if (escolha == "A")
            {
                Console.WriteLine("Escreva uma outra frase:");
                string novaFrase = Console.ReadLine();
                /*qual metodo deve ser inserido aqui?*/(frase, novaFrase);
            }
            else
            {
                Console.WriteLine("Opção inválida.");
            }
        }
    }


### Exercício n° 5

Mais um exercício simples, porem com vetores, neste exercício, você criará um array, e escreverá os 5 primeiros numeros e o vetor invertido

Código:

    int tamanhoArray = 10;
    /*como declaramos um vetor?*/ numeros = new double[tamanhoArray];
    
    // primeira repetição para preencher os vetor
    for (int i = e; i < tamanhoArray; i++)
    {
        Console.WriteLine($"Digite o {i + 1}º número:");
        numeros[/*Qual deve ser o indice?*/] = Convert.ToDouble(Console.ReadLine());
    }
    
    // vetor que vai receber o numero na ordem invertida
    
    /*como declaramos um vetor?*/ numerosinvertidos = new double[tamanhoArray];
    
    for (int i = 0; i < tamanhoArray; i++)
    {
        // preenchendo o vetor na ordem invertida
        numerosinvertidos[i] = numeros[/*Qual deve ser o indice?*/];
    }
    
    // vetor que vai receber a metade dos números
    
    /*como declaramos um vetor?*/ metadenumeros = new double[/*Qual deve ser o indice?*/];
    
    for (int i = 0; i < tamanhoArray / 2; i++)
    {
        
        metadenumeros[/*Qual deve ser o indice?*/] = numeros[/*Qual deve ser o indice?*/];
    }
    
    // exibindo os números na ordem invertida
    Console.WriteLine("Números na ordem invertida:");
    for (int i = 0; i < tamanhoArray; i++)
    {
        Console.WriteLine(numerosinvertidos[i]);
    }
    
    // exibindo a metade dos números
    Console.WriteLine("Metade dos números:");
    for (int i = 0; i < tamanhoArray / 2; i++)
    {
        Console.WriteLine(metadenumeros[i]);
    }




### Exercício n° 6 - Faça o seu proprio programa.



Por fim, o no ultimo exercício, você deverá criar um programa do zero, mais especificamente uma calculadora.



Não haverá exigencias em especifico, apenas que os requisitos do exercício sejam atendidos. 



Requisitos:



* O programa deve fazer as seguintes operações : Adição(A + B), Subtração(A - B), Multiplicação(A * B), Divisão(A / B) , Potenciação (A ^ B) E Radiciação (B √ A).



* O programa deve aceitar entradas e saídas corretamente.



* O programa deve ter uma variavel que salva o resultado do ultimo calculo.   Exemplo: 2 + 5 = 7 (resultado do ultimo calculo) , depois 4 * ultimo calculo = 28.



* O programa deve fazer as operações repetidas vezes.
