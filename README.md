# 🛡️ Spam Checker App

O **Spam Checker** é uma aplicação moderna e leve projetada para verificar a segurança de e-mails suspeitos em tempo real. Com uma interface elegante inspirada em aplicativos nativos, o app analisa textos utilizando heurísticas avançadas de palavras-chave, quantidade de links, excesso de letras maiúsculas e pontuação para detectar fraudes, golpes e phishing.

---

## ✨ Funcionalidades Principais

* **Detecção Inteligente de Spam:** Sistema de pontuação baseado em critérios de risco (palavras-chave suspeitas, múltiplos links, letras maiúsculas e exclamações excessivas).
* **Histórico de Análises:** Salve e consulte suas verificações anteriores diretamente no armazenamento local do dispositivo.
* **Estatísticas Rápidas:** Acompanhe quantos e-mails foram analisados e classificados como seguros, suspeitos ou de alto risco.
* **Dicas de Segurança Práticas:** Guia integrado para ajudar usuários a identificar golpes comuns de e-mail.
* **Design Multiplataforma Responsivo:** Layout otimizado para simular a experiência de apps nativos em **Android**, **iOS** e **Windows**.

---

## 🚀 Tecnologias Utilizadas

* **HTML5 & JavaScript (Vanilla):** Lógica limpa e sem dependências de frameworks pesados.
* **Tailwind CSS (CDN):** Estilização moderna com suporte a modo escuro (`dark mode`).
* **LocalStorage:** Persistência local para salvar o histórico de verificações e contadores.
* **SVG Icons:** Ícones vetoriais leves e escaláveis.

---

## 📦 Como Usar

Como o projeto é desenvolvido em tecnologias web modernas, você pode executá-lo de duas formas:

### 1. Uso Direto no Navegador (Web / PWA)
1. Baixe ou copie o código fonte (`index.html`).
2. Abra o arquivo em qualquer navegador moderno (Chrome, Edge, Safari, Firefox).

### 2. Executando como Aplicativo (Android, iOS e Windows)
Você pode empacotar este código HTML/JS usando ferramentas de conversão para aplicativos nativos ou híbridos:
* **Android / iOS:** Utilize o **Capacitor** ou **Cordova** para gerar os arquivos `.apk` (Android) ou `.ipa` (iOS).
* **Windows:** Utilize o **Electron** ou abra o app diretamente via navegador web no modo tela cheia (F11).

---

## 📱 Guia de Telas do Aplicativo

1. **Capa / Início (`view-capa`):** Tela de boas-vindas com acesso rápido para iniciar a verificação, ver estatísticas ou acessar as configurações.
2. **Verificador (`view-app`):** Campo de texto onde você cola o conteúdo do e-mail suspeito para receber o veredito instantâneo.
3. **Histórico & Dicas (`view-history` / `view-tips`):** Registros salvos das análises anteriores e dicas de prevenção contra phishing.
4. **Configurações (`view-config`):** Informações sobre os critérios ativos, sensibilidade e versão do app.

---

## 🛠️ Exemplo de Código (Estrutura Básica)

```javascript
// Exemplo da função de verificação de spam
function verificarSpam() {
    const texto = document.getElementById("emailTexto").value;
    const textoLower = texto.toLowerCase();
    
    const palavrasSpam = ["ganhe", "dinheiro", "promoção", "oferta", "clique aqui", "grátis", "urgente"];
    let score = 0;

    palavrasSpam.forEach(palavra => {
        if (textoLower.includes(palavra)) score += 2;
    });

    if ((texto.match(/https?:\/\//g) || []).length > 2) score += 3;
    if ((texto.match(/!/g) || []).length > 3) score += 2;

    // Retorna o resultado com base na pontuação...
}
