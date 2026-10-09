# python4..
entregael de pytho da semana 4
"""
programa
{
    funcao inicio()
    {
        // Declaração do vetor original de tamanho fixo
        real precos_originais[7] = {120.50, 45.00, 89.90, 45.00, 210.00, 15.20, 89.90}
        real precos_unicos[7]
        inteiro total_unicos = 0
        logico ja_existe

        // --- 1. SIMULAÇÃO DE CONJUNTO (Removendo duplicados manualmente) ---
        para (inteiro i = 0; i < 7; i++)
        {
            ja_existe = falso
            
            // Verifica se o preço já foi inserido no vetor de únicos
            para (inteiro j = 0; j < total_unicos; j++)
            {
                se (precos_originais[i] == precos_unicos[j])
                {
                    ja_existe = verdadeiro
                    pare
                }
            }

           # Se não for repetido, adiciona ao vetor de únicos
            se (nao ja_existe)
            {
                precos_unicos[total_unicos] = precos_originais[i]
                total_unicos++
            }
        }

        // --- 2. ORDENAÇÃO PELO MÉTODOS DA BOLHA (Bubble Sort) ---
        real auxiliar
        para (inteiro i = 0; i < total_unicos - 1; i++)
        {
            para (inteiro j = 0; j < total_unicos - 1 - i; j++)
            {
                se (precos_unicos[j] > precos_unicos[j + 1])
                {
                    auxiliar = precos_unicos[j]
                    precos_unicos[j] = precos_unicos[j + 1]
                    precos_unicos[j + 1] = auxiliar
                }
            }
        }

        // --- 3. CÁLCULO DE ESTATÍSTICAS E TUPLA (Estrutura/Registro) ---
        real menor_preco = precos_unicos[0]
        real maior_preco = precos_unicos[0]
        real soma_precos = 0.0

        para (inteiro i = 0; i < total_unicos; i++)
        {
            se (precos_unicos[i] < menor_preco)
            {
                menor_preco = precos_unicos[i]
            }
            se (precos_unicos[i] > maior_preco)
            {
                maior_preco = precos_unicos[i]
            }
            soma_precos = soma_precos + precos_unicos[i]
        }

        real media_precos = soma_precos / total_unicos

        // Exibição dos resultados
        escreva("--- RESULTADOS PORTUGOL ---\n")
        escreva("Preços únicos e ordenados: ")
        para (inteiro i = 0; i < total_unicos; i++)
        {
            escreva(precos_unicos[i], " ")
        }
        escreva("\nMenor Preço: ", menor_preco)
        escreva("\nMaior Preço: ", maior_preco)
        escreva("\nMédia dos Preços: ", media_precos)
    }
}
"""
