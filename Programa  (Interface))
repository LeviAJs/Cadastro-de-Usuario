namespace ProjetoCadastro
    {
    class Cadastro
        {
        static void Main(string[] args) {
            //criarcao de variaveis
            int EscolhaMenu;
            SalvarUsuario salvar = new SalvarUsuario();
            //criacao do loop 

            while(true) {
                Console.WriteLine("1 - Cadastro");
                Console.WriteLine("2 - Lista");
                Console.WriteLine("3 - Buscar");
                Console.WriteLine("4 - Sair");

                bool validacao = int.TryParse(Console.ReadLine(), out EscolhaMenu);
                if(validacao) {

                    if(EscolhaMenu == 4) {
                        break;
                        }
                    switch(EscolhaMenu) {
                        case 1:
                            Console.WriteLine("Cadastro de novo usuario");
                            Console.Write("Nome: ");
                            string nome = Console.ReadLine();
                            Console.WriteLine("Email: ");
                            string email = Console.ReadLine();
                            Console.Write("Idade: ");
                            if(!int.TryParse(Console.ReadLine(), out int idade)) {
                                Console.WriteLine("Idade inválida.");
                                break;
                                }
                            Usuario usuario = new(nome, email, idade);
                            salvar.Adicioanr(usuario);
                            break;

                        case 2:
                            Console.WriteLine("Lista:");

                            foreach(var item in salvar.Mostar()) {
                                Console.WriteLine($"Nome: {item.Nome} | Email: {item.Email} | Idade: {item.Idade}");
                                }

                            break;

                        case 3:
                            Console.Write("Nome a ser buscado: ");
                            nome = Console.ReadLine();
                            bool resultado = salvar.BuscarNome(nome);
                            if(resultado) {
                                Console.WriteLine("Nome encontrado");
                                }
                            else {
                                Console.WriteLine("Nome não encontrado");
                                }
                            break;
                        default:
                            Console.WriteLine("Numero invalido");
                            break;
                        }
                    }

                else {
                    Console.WriteLine("Precisa ser um numero");
                    continue;
                    }
               
                }
            }
        }
    }
