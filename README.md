# Extrator-de-contato-em-email
Extrator de contato em email

- Criando um código que consiga extrair um endereço de e-mail de um texto.
- Vamos considerar que apenas 1 email será incluída no texto e o @ não será usado em outros locais.

- texto_email = """Prezados,
Favor encaminhar documentação para o email qualquercoisa@gmail.com
Obrigado"""

# Existem diferentes formas de fazer esse exercício, faremos considerando que o email sempre tem ou espaço ou quebra de linha antes ou depois dele, o que é bem provável
linhas = texto_email.split("\n")
for linha in linhas:
    if "@" in linha:
        palavras = linha.split(" ")
        for palavra in palavras:
            if "@" in palavra:
                email = palavra

print(email)
