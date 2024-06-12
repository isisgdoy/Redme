

- 👋 Olá mundo! Eu sou a Isis :)
- 👀 Estudante em Análise e desenvolvimento de sistemas
- 🌱 Iniciante na programação
##
<div> 
  
  <a href="https://www.instagram.com/isis_godoy/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:isisgodoi2@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/isis-valeria-godoy-bueno-33b979230/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
</div>

<!---
isisgdoy/isisgdoy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take fha look at your changes.

CALCULADORA

using System.ComponentModel.Design;
using System.Security.Cryptography.X509Certificates;


// minhas classe é Program
// Metodo é o Menu
namespace Calculadora
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Menu();
        }

        public static void Menu() 
        {
            Console.Clear();
            Console.WriteLine("Menu:");
            Console.WriteLine("1 - Somar");
            Console.WriteLine("2 - Subtrair");
            Console.WriteLine("3 - Dividir");
            Console.WriteLine("4 - Multiplicação"); 
            Console.WriteLine("5 - Resto da divisão");
            Console.WriteLine("6 - Potenciação");
            Console.WriteLine("0 - Sair"); 

            string opcao = Console.ReadLine();

            switch (opcao)
            {
                case "1":
                    Somar();
                    break;

                case "2":
                    Subtrair();
                    break;

                case "3":
                    Dividir();
                    break;

                case "4":
                    Multiplicacao();    
                    break;

                case "5":   
                    RestoDaDivisao();
                    break;

                case "6":   
                    CalcularPotenciacao();  
                    break;

                case "0":
                    break;

                default:
                    Menu();
                    break;

            }
                
        }

        
        public static void Somar()
        {
            double valor1, valor2;
            Console.WriteLine("Digite o primeiro valor:");
            valor1 = double.Parse(Console.ReadLine());
            Console.WriteLine("Digite o segundo valor:");
            valor2  = double.Parse(Console.ReadLine());

            Console.WriteLine($"{valor1} + {valor2} = {valor1 + valor2}");
            Console.ReadLine();

            Menu();
            
        }


        public static void Subtrair() 
        {
            double valor1, valor2;
            Console.WriteLine("Digite o primeiro valor:");
            valor1 = double.Parse(Console.ReadLine());
            Console.WriteLine("Digite o segundo valor:");
            valor2 = double.Parse(Console.ReadLine());

            Console.WriteLine($"{valor1} - {valor2} = {valor1 - valor2}");

            Console.ReadLine(); 
            Menu();
            
        }


        public static void Dividir()
        {
            double dividendo, divisor;

            Console.WriteLine("Informe o dividendo:");
            dividendo = double.Parse(Console.ReadLine());
            Console.WriteLine("Informe o divisor:");
            divisor = double.Parse(Console.ReadLine());

            if (divisor != 0)
                Console.WriteLine($"{dividendo} / {divisor} = {dividendo / divisor}");
            else
                Console.WriteLine("Não é possível dividir por zero.");

            Console.ReadLine();
            Menu();

        }

        public static void Multiplicacao()
        {
            double valor1, valor2;
            Console.WriteLine("Digite o primeiro valor:");
            valor1 = double.Parse(Console.ReadLine());
            Console.WriteLine("Digite o segundo valor:");
            valor2 = double.Parse(Console.ReadLine());

            Console.WriteLine($"{valor1} * {valor2} = {valor1 * valor2}");

            Console.ReadLine();
            Menu();

        }

        public static void RestoDaDivisao()
        {
            double dividendo, divisor;

            Console.WriteLine("Informe o dividendo:");
            dividendo = double.Parse(Console.ReadLine());
            Console.WriteLine("Informe o divisor:");
            divisor = double.Parse(Console.ReadLine());

            if (divisor != 0)
                Console.WriteLine($"Resto entre {dividendo} e {divisor} = {dividendo % divisor}");
            else
                Console.WriteLine("Não é possível dividir por zero.");

            Console.ReadLine();
            Menu();
        }

        public static void CalcularPotenciacao()
        {
            double basePotenciacao, expoente;

            Console.WriteLine("Informe a base:");
            basePotenciacao = double.Parse(Console.ReadLine());
            Console.WriteLine("Informe o expoente:");
            expoente = double.Parse(Console.ReadLine());

            Console.WriteLine($"{basePotenciacao} elevado a {expoente} = {Math.Pow(basePotenciacao, expoente)}");

            Console.ReadLine();
            Menu();

        }

    }
}



JOGAR DADOS


using System;
using System.Diagnostics.Metrics;

namespace JogarDados // modulo
{
    class Program //classe
    {
        // criação das variaveis para acessar os jogadores de qqlr metodo

        public static string Jogador1;
        public static string Jogador2;

        // variavel para armazenar a pontuação dos jogos 

        public static byte PontosJogador1;
        public static byte PontosJogador2;

        // variavel para armazenar a rodada atual

        public static byte RodadaAtual;

        static void Main(string[] args) // metodos (funções) esse método deve receber como parâmetro um array de String (nomeado args)
        {
            Console.Clear();
            ConfigurarJogos();
            IniciarRodadas();
           
        }

        public static void ConfigurarJogos() 
        {
            RodadaAtual = 0; // campo/fields (variavel criada pra ser acessado em qqlr metodo)

            CriarJogadores(); //  metodos
            AtualizarPlacar();//  metodos

            Console.WriteLine($"\n Jogadores {Jogador1} e {Jogador2} criados. Pressione qulaquer tecla pra continuar.");
            Console.ReadKey(); // Obtém o próximo caractere ou tecla de função pressionada pelo usuário. // Console é a classe e ReadKey é o metodo

        }


        public static void CriarJogadores()
        {
            Console.WriteLine("Informe o nome do primeiro jogador:");
            Jogador1 = Console.ReadLine();
            PontosJogador1 = 0;

            Console.WriteLine("Informe o nome do segundo jogador:");
            Jogador2 = Console.ReadLine();
            PontosJogador2 = 0;

        }

        public static void AtualizarPlacar()
        {
            Console.Clear(); //é usado para limpar as mensagens do console
            Console.WriteLine($"Pontos do jogador {Jogador1}: {PontosJogador1}" );
            Console.WriteLine($"Ponstos do jogador {Jogador2}: {PontosJogador2}");
            Console.WriteLine();

            if (RodadaAtual == 0) 
            {

                Console.WriteLine("Jogo nao iniciado...");
            }

        }


        public static void IniciarRodadas()
        {
            AtualizarPlacar();
            if (RodadaAtual == 3) 
            {
                FinalizarJogo();
                    return;
            }

            RodadaAtual++; // incrementando no metodo RodadaAtual

            Console.WriteLine($"Rodada {RodadaAtual} iniciada!\n");
            Console.WriteLine($"Jogador {Jogador1} precisone enter para fazer sua jogada...");
            Console.ReadLine();
            byte ValorTiradoJogador1 = JogarDado();
            Console.WriteLine($"Valor do dado jogado pelo {Jogador1}: {ValorTiradoJogador1}");

            Console.WriteLine($"Rodada {RodadaAtual} iniciada!\n");
            Console.WriteLine($"Jogador {Jogador2} precisone enter para fazer sua jogada...");
            Console.ReadLine();
            byte ValorTiradoJogador2 = JogarDado();
            Console.WriteLine($"Valor do dado jogado pelo {Jogador2}: {ValorTiradoJogador2}");

            if (ValorTiradoJogador1 == ValorTiradoJogador2)
            {
                Console.WriteLine($"O jogador {Jogador1} tirou: {ValorTiradoJogador1} e o {Jogador2} tirou: {ValorTiradoJogador2}. Empate!");
                Console.WriteLine("Pressione ENTER para continuar com o jogo...");
                Console.ReadLine();
            }
            else 
            {
                string Vencedor;

                if (ValorTiradoJogador1 > ValorTiradoJogador2) 
                {
                    Vencedor = Jogador1;
                    PontosJogador1++;
                
                } else 
                {
                    Vencedor = Jogador2;
                    PontosJogador2++;
                    
                }

                Console.WriteLine($"{Jogador1} tirou o numero {ValorTiradoJogador1} e {Jogador2} tirou o numero {ValorTiradoJogador2}. O vencedor foi: {Vencedor}, da rodada {RodadaAtual}");
                Console.WriteLine("Pressione ENTER para continuar o jogo...");
                Console.ReadLine(); 

            }

            IniciarRodadas();

        }
        public static byte JogarDado()
        {
            Random gerador = new Random(); // gera numeros aleatórios 
            return Convert.ToByte(gerador.Next(1, 6)); //Converte um valor especificado em um inteiro sem sinal de 8 bits.

        }
        public static void FinalizarJogo()
        {

            AtualizarPlacar();
            Console.WriteLine("Jogo finalizado!!!");

            if (PontosJogador1 == PontosJogador2)
            {
                Console.WriteLine("Empate!");
            }
            else if (PontosJogador1 > PontosJogador2)
            {
                Console.WriteLine($"O jogador {Jogador1} venceu com {PontosJogador1} pontos!");
            }
            else
            {
                Console.WriteLine($"O jogador {Jogador2} venceu com {PontosJogador2} pontos!");
            }
        }

    }


}





--->
