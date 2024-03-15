# vendas-com-intelig-ncia-incorporada
Que utiliza Técnicas de Aprendizado de Máquina para Personalizar a Abordagem de Vendas com Base no Comportamento do Cliente:

# Importar bibliotecas necessárias
import random

# Dados do cliente (simulados para fins de exemplo)
idade = 30
interesse = 'tecnologia'
ultima_compra = 15  # Dias desde a última compra

# Função para gerar uma resposta personalizada com base nos dados do cliente
def gerar_resposta_personalizada(idade, interesse, ultima_compra):
    resposta_padrao = "Olá! Como posso ajudá-lo hoje?"

    # Verificar a idade do cliente
    if idade < 25:
        resposta_idade = "Olá, jovem! Está procurando por algo específico?"
    elif idade >= 25 and idade <= 40:
        resposta_idade = "Bom dia! Temos ótimas opções para pessoas da sua faixa etária."
    else:
        resposta_idade = "Boa tarde! Temos produtos que podem interessar a todas as idades."

    # Verificar o interesse do cliente
    if interesse == 'tecnologia':
        resposta_interesse = "Vejo que você está interessado em tecnologia. Temos os últimos lançamentos disponíveis!"
    elif interesse == 'moda':
        resposta_interesse = "Seu interesse em moda é muito bem-vindo. Temos uma grande variedade de roupas e acessórios."
    else:
        resposta_interesse = "Não tem problema! Estou aqui para ajudar com qualquer coisa que você precise."

    # Verificar a última compra do cliente
    if ultima_compra < 7:
        resposta_ultima_compra = "Vejo que você fez uma compra recente. Precisa de algo mais?"
    elif ultima_compra >= 7 and ultima_compra <= 30:
        resposta_ultima_compra = "Já faz um tempo desde a sua última compra. Talvez haja algo novo que você gostaria de conferir!"
    else:
        resposta_ultima_compra = "Faz um tempo desde a sua última compra. Estou aqui para ajudar se precisar de algo novo."

    # Gerar a resposta final combinando todas as informações
    resposta_final = f"{resposta_padrao}\n{resposta_idade}\n{resposta_interesse}\n{resposta_ultima_compra}"

    return resposta_final

# Exemplo de dados do cliente
print("Exemplo de Resposta Personalizada:")
print(gerar_resposta_personalizada(idade, interesse, ultima_compra))
