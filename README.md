# Codigo-Fila-Portugol
Código do Portugol feito durante aula de Lógica de programação, sobre o sistema de Fila (First In, First Out). 


[Uploading Fila d
programa {
  inclua biblioteca Util
  inclua biblioteca Texto --> T

  caracter opcao
  const inteiro total = 25
  cadeia nome[total], enter, resposta
  inteiro ponteiro = 0, n, x, idade[25], i=0

  funcao inicio() 
  {
    limpa()
		escreva("=================== MENU ==================\n")
		escreva("1 - Adicionar uma nova pessoa na fila\n")
		escreva("2 - Chamar próxima pessoa para ser atendida\n")
		escreva("3 - Listar todas as pessoas da fila\n")
		escreva("4 - Remover todas as pessoas da fila\n")
		escreva("5 - Conferir status da fila\n")
    		escreva("6 - Verificar quantidade de pessoas na fila\n")
    		escreva("7 - Sair do sistema\n")
		escreva("===========================================\n")
		escreva("Escolha uma das opções: ")
		leia(opcao)
		limpa()

    escolha(opcao)
		{
			caso '1':
			{
				adicionar()
				pare
			}

			caso '2':
			{
				remover()
				pare
			}

		
			caso '3':
			{
				listar()
				pare
			}

			caso '4':
			{
				limparFila()
				pare
			}

     		 caso '5':
			{
				status()
				pare
      		}

     		 caso '6':
     		 {
       		 quantidade()
       		 pare
   		      }

   		       caso '7':
     		 {
       		 sair()
       		 pare
   		      }

   		      caso contrario:
   		      {
   		      	escreva("Opção Inválida, por favor tente novamente!\n")
   		      	Util.aguarde(1500)
   		      	inicio()
   		      	pare
   		      }

    
		}
	}

  funcao adicionar()
  {
      se(ponteiro < 25)
		  {
		  escreva("========= ADICIONAR PESSOA NA FILA =========\n")
		  escreva("Qual o nome da pessoa que você deseja incluir na fila?\n")
		  leia(nome[ponteiro])
		  nome[ponteiro] = T.caixa_alta(nome[ponteiro])
		  limpa()
		  escreva("========= ADICIONAR PESSOA NA FILA =========\n")
		  escreva("Qual a idade do(a) ", nome[ponteiro] , "?\n")
		  leia(idade[i])
		  limpa()
		
			escreva("Pessoa adicionada com sucesso\n")
			ponteiro++
			i++
			Util.aguarde(1000)
			inicio()
		  }


		    senao
		    {
			  escreva("Desculpe, não há espaço livre na fila para uma nova pessoa\n")
			  retornar()
		    }
  }

  funcao remover()
  {
      para(n=0; n<ponteiro -1; n++)
		  {
			  nome[n] = nome[n+1]
			  idade[n] = idade[n+1]
		  }
		  ponteiro--
		  i--
      escreva("Realizando atendimento da primeira pessoa . . .\n")
      Util.aguarde(1500)
		  escreva("Primeira pessoa foi atendida!\n")
		  retornar()
  }


  funcao listar()
  {
    limpa()
		se(ponteiro==0)
		{
			escreva("AVISO: Não há nenhuma pessoa aguardando na fila\n")
			retornar()
		}
		senao 
		{
			para(n=0; n<ponteiro; n++)
			{
				escreva(n+1 , "- Pessoa: " , nome[n])
				escreva(" - Idade: " , idade[n] , "\n")
			}
			retornar()
  }
  }

  funcao status()
  {
  
		se(ponteiro==0)
		{
		escreva("===========================================\n")
		escreva("VERDADEIRO : Não há nenhuma pessoa na fila\n")
		escreva("===========================================\n")
		retornar()
		}

		senao
		{
		escreva("===========================================\n")
		escreva("    FALSO: Há pessoas aguardando na fila   \n")
		escreva("===========================================\n")
		retornar()
		}
	
	
  }

  funcao quantidade()
  {
        escreva("=========== QUANTIDADE DE PESSOAS NA FILA ===========\n\n")
        escreva("Tem:" , ponteiro , " pessoas aguardando na fila\n\n")
        escreva("Ainda há espaço disponível para mais:" ,total-ponteiro, " pessoas\n")
        escreva("======================================================\n\n\n")

        retornar()

  }

  funcao limparFila()
  {
  	escreva("=========== REMOÇÃO DE PESSOAS DA FILA ===========\n\n")
  	escreva("Deseja realmente remover todas as pessoas da fila? S/N \n")
		leia(resposta)
		resposta=T.caixa_alta(resposta)

		se(resposta=="S" ou resposta=="s")
		{
			limpa()
			escreva("Removendo todas as pessoas da fila . . .\n")
			Util.aguarde(1000)
			escreva("Todas as pessoas foram removidas\n")
			ponteiro=0
			i=0
			retornar()
		}

		senao
		{
			escreva("Nenhuma pessoa foi removida da fila\n")
			retornar()
		}

		
  }

  funcao retornar()
	{
		
		escreva("===========================================\n")
		escreva("Pressione a tecla [ENTER] para sair\n")
		escreva("===========================================\n")
		leia(enter)
		inicio()
		
	}

  funcao sair()
  {
    escreva("Finalizando o sistema . . .\n\n")
    Util.aguarde(1500)
    escreva("Sistema finalizado\n")
    
  }
  
}


/* $$$ Portugol Studio $$$ 
 * 
 * Esta seção do arquivo guarda informações do Portugol Studio.
 * Você pode apagá-la se estiver utilizando outro editor.
 * 
 * @POSICAO-CURSOR = 151; 
 * @PONTOS-DE-PARADA = ;
 * @SIMBOLOS-INSPECIONADOS = {nome, 8, 9, 4}-{idade, 9, 30, 5};
 * @FILTRO-ARVORE-TIPOS-DE-DADO = inteiro, real, logico, cadeia, caracter, vazio;
 * @FILTRO-ARVORE-TIPOS-DE-SIMBOLO = variavel, vetor, matriz, funcao;
 */e Pessoas.por…]()


