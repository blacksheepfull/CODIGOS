import unicodedata
import time

# Função para remover acentos
def remover_acentos(texto):
    nfkd = unicodedata.normalize('NFKD', texto)
    texto_sem_acento = "".join([c for c in nfkd if not unicodedata.combining(c)])
    return texto_sem_acento

print('''
      Bem vindo! 
      Vamos lá para nosso Quiz?!
      ''')

time.sleep(2)

quiz = [
    {"pergunta": "Qual é a capital da França?", "resposta": "Paris"},
    {"pergunta": "Qual é o maior oceano do mundo?", "resposta": "Pacífico"},
    {"pergunta": "Quem escreveu 'Dom Quixote'?", "resposta": "Miguel de Cervantes"},
    {"pergunta": "Em que ano o homem pisou na Lua pela primeira vez?", "resposta": "1969"},
    {"pergunta": "Qual é o planeta mais próximo do Sol?", "resposta": "Mercúrio"},
]
def executar_quiz():
    score = 0 
    
    try:
        for item in quiz:
            print(item["pergunta"])
            resposta_jogador = input("Sua resposta: ").strip()
            resposta_normalizada = remover_acentos(resposta_jogador).lower()
            resposta_correta_normalizada = remover_acentos(item["resposta"]).lower()

            if resposta_normalizada == resposta_correta_normalizada:
                print("Correto!")
                score += 1
            else:
                print(f"Errado! A resposta correta é: {item['resposta']}")
            
            print() 
        
        print(f"Fim do jogo! Você acertou {score} de {len(quiz)} perguntas.")
        
        print() 
    
    except Exception as e:
        print(f"Ocorreu um erro: {e}")

executar_quiz()
