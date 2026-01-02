📧 Verificador de Spam – App em Python (Kivy)

Este projeto é um verificador básico de spam para textos de e-mail, desenvolvido em Python utilizando o framework Kivy.
Ele analisa o conteúdo do texto com base em palavras-chave e heurísticas simples para indicar se o e-mail provavelmente é spam ou não.

🧠 Como funciona

O app atribui uma pontuação de risco com base em:

Palavras comuns em spam (ex: “ganhe dinheiro”, “clique aqui”, “grátis”)

Quantidade de links no texto

Uso excessivo de exclamações (!!!)

Texto todo em letras maiúsculas

Com base nessa pontuação, o resultado é classificado como:

✅ Provavelmente não é spam

⚠️ Possível spam

🚨 Alto risco de spam

🖥️ Interface

O aplicativo possui:

Campo de texto para colar o e-mail

Botão Verificar

Resultado visual com emojis e cores

Compatível com desktop e mobile (Android, via Kivy).
