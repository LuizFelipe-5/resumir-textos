# ✨ Resumidor Mágico de Texto e URL com Gemini Flash ✨

Cansado de textos longos e artigos intermináveis? Este Colab é a sua varinha mágica! Ele utiliza o poder do modelo Gemini 2.0 Flash da Google para transformar textos e conteúdos de URLs em resumos concisos e diretos. E a melhor parte? Ele ainda gera um PDF com o resumo para você salvar ou compartilhar!

## 🚀 Como Usar essa Magia

1.  **Obtenha sua Chave da API do Google GenAI:** Você precisa de uma chave para que o Gemini Flash funcione. Se ainda não tem, consiga uma [aqui](https://makersuite.google.com/app/apikey).
2.  **Salve sua Chave de API:** No Google Colab, vá em "Secrets" (geralmente no menu à esquerda, ícone de cadeado 🔒). Adicione um novo segredo com o nome `GOOGLE_API_KEY` e cole sua chave lá. O código já está configurado para ler essa variável de ambiente.
3.  **Escolha seu Modo:** Use o seletor mágica (`#@param`) para escolher entre "Texto" (se você quer colar um texto diretamente) ou "URL" (se você quer resumir o conteúdo de uma página da web).
4.  **Execute as Células:** Rode as células do Colab sequencialmente.
5.  **Insira o Texto ou URL:** Quando solicitado, insira o texto que deseja resumir ou a URL do artigo/página.
6.  **Veja a Magia Acontecer:** O Colab irá processar seu input, gerar um resumo e, em seguida, criar um arquivo PDF chamado `relatorio_resumo.pdf` com o resumo gerado.
7.  **Baixe seu PDF:** O arquivo PDF estará disponível no painel de arquivos do Colab (`/content/relatorio_resumo.pdf`).

## 🛠️ O que Acontece Por Trás dos Panos?

Este Colab faz o seguinte:

*   **Instala as bibliotecas necessárias:** `google-genai`, `requests`, `beautifulsoup4` e `fpdf`.
*   **Autentica com a API do Google GenAI:** Usando sua chave secreta.
*   **Define a função `resumir_texto`:** Que envia seu texto (ou o texto extraído de uma URL) para o modelo Gemini Flash para gerar o resumo.
*   **Define a função `extrair_texto_url`:** Se você escolher o modo "URL", esta função baixa o conteúdo da página, remove scripts e estilos, e extrai o texto puro.
*   **Define a função `gerar_pdf_relatorio`:** Pega o resumo gerado e cria um arquivo PDF formatado.
*   **Usa um seletor mágico:** Para permitir que você escolha facilmente entre resumir texto ou URL.

## 📚 Bibliotecas Utilizadas

*   `google-genai`: Para interagir com a API do Gemini Flash.
*   `requests`: Para fazer requisições HTTP e baixar o conteúdo de URLs.
*   `beautifulsoup4`: Para parsear o HTML das páginas web e extrair o texto.
*   `fpdf`: Para gerar o arquivo PDF com o resumo.

Divirta-se resumindo! ✨
