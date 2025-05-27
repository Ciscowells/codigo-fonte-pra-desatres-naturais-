Projeto Global Solution
O que o programa faz ?
O programa simula o cadastro de 2 desastres com dados fixos (baseado no seu exemplo) e exibe:

O total de desastres registrados

Um resumo das pessoas afetadas por categoria

A categoria mais afetada

O total geral de pessoas afetadas

O desastre com maior número de afetados

 Como usar o programa ?
1. Copie o código abaixo:
python
Copiar
Editar
# Simulação da entrada fixa com base no exemplo fornecido
quantidade = 2

# Listas com os dados dos 2 desastres
tipos = ["enchente", "tempestade"]
paises = ["Brasil", "Brasil"]
cidades = ["Porto Alegre", "Canoas"]
bairros = ["Centro", "São José"]
ruas = ["Av. Borges de Medeiros", "Rua das Palmeiras"]
total_afetados = [20, 15]
criancas = [5, 2]
adultos = [8, 6]
idosos = [3, 4]
mobilidade_reduzida = [2, 1]
feridos = [2, 2]

# Cálculo dos totais por categoria
soma_criancas = 0
soma_adultos = 0
soma_idosos = 0
soma_mob_reduzida = 0
soma_feridos = 0
soma_total_afetados = 0

for i in range(quantidade):
    soma_criancas += criancas[i]
    soma_adultos += adultos[i]
    soma_idosos += idosos[i]
    soma_mob_reduzida += mobilidade_reduzida[i]
    soma_feridos += feridos[i]
    soma_total_afetados += total_afetados[i]

# Encontrar a categoria mais afetada
categoria_mais_afetada = "Crianças"
maior_valor = soma_criancas

if soma_adultos > maior_valor:
    maior_valor = soma_adultos
    categoria_mais_afetada = "Adultos"
if soma_idosos > maior_valor:
    maior_valor = soma_idosos
    categoria_mais_afetada = "Idosos"
if soma_mob_reduzida > maior_valor:
    maior_valor = soma_mob_reduzida
    categoria_mais_afetada = "Mobilidade reduzida"
if soma_feridos > maior_valor:
    maior_valor = soma_feridos
    categoria_mais_afetada = "Feridos"

# Encontrar o desastre com maior número de afetados
indice_maior = 0
maior_afetados = total_afetados[0]

for i in range(1, quantidade):
    if total_afetados[i] > maior_afetados:
        maior_afetados = total_afetados[i]
        indice_maior = i

# Saída dos resultados
print(f"\nTotal de desastres registrados: {quantidade}\n")
print("Resumo de pessoas afetadas por categoria:")
print("Crianças:", soma_criancas, "| Adultos:", soma_adultos, "| Idosos:", soma_idosos,
      "| Mobilidade reduzida:", soma_mob_reduzida, "| Feridos:", soma_feridos)
print("\nCategoria mais afetada:", categoria_mais_afetada)
print("Total geral de pessoas afetadas:", soma_total_afetados)
print("\nDesastre com maior número de afetados:")
print("Tipo:", tipos[indice_maior])
print("Local:", ruas[indice_maior] + ", " + bairros[indice_maior] + ", " + cidades[indice_maior] + ", " + paises[indice_maior])
2. Abra um ambiente Python
Você pode usar:

Replit

VS Code ou outro editor com Python instalado

IDLE (instalado com o Python)

Terminal com comando python nome_do_arquivo.py se estiver salvo em um .py

3. Cole o código e execute
Cole o código completo

Execute o programa (pressione "Run" ou F5, dependendo do ambiente)

4. Veja o resultado:

yaml
Total de desastres registrados: 2

Resumo de pessoas afetadas por categoria:
Crianças: 7 | Adultos: 14 | Idosos: 7 | Mobilidade reduzida: 3 | Feridos: 4

Categoria mais afetada: Adultos
Total geral de pessoas afetadas: 35

Desastre com maior número de afetados:
Tipo: enchente
Local: Av. Borges de Medeiros, Centro, Porto Alegre, Brasil
