# prompt: Gere um readme para esse meu colab

# Resumo de Texto e URL com Gemini e Geração de PDF

Este Colab permite gerar resumos concisos de textos ou conteúdos de URLs utilizando o modelo Gemini 2.0 Flash da Google AI e, opcionalmente, gerar um relatório em PDF com o resumo gerado.

## Funcionalidades

- Resumo de texto inserido diretamente pelo usuário.
- Resumo do conteúdo de uma URL, extraindo o texto principal da página.
- Geração de um arquivo PDF contendo o resumo.

## Configuração

1. **Obtenha uma chave de API da Google AI:** Você precisará de uma chave de API para usar o modelo Gemini. Siga as instruções na documentação da Google AI para obter uma chave.
2. **Configure a chave de API no Google Colab:**
   - No menu lateral, clique no ícone de chave (Secrets).
   - Clique em "+ New secret".
   - No campo "Name", digite `GOOGLE_API_KEY`.
   - No campo "Value", cole sua chave de API da Google AI.
   - Certifique-se de que a caixa de seleção "Notebook access" esteja marcada para este Colab.

## Como usar

1. **Execute as células de instalação de bibliotecas:** As primeiras células instalam as bibliotecas necessárias (`google-genai`, `requests`, `beautifulsoup4`, `fpdf`).
2. **Execute a célula de configuração da API:** Esta célula configura sua chave de API.
3. **Escolha o modo de geração:** Utilize a variável de formulário (`modo_geracao`) para selecionar entre "Texto" ou "URL".
4. **Execute a célula principal:** Dependendo do modo selecionado:
   - Se for "Texto", você será solicitado a inserir o texto a ser resumido.
   - Se for "URL", você será solicitado a inserir a URL do artigo a ser resumido.
5. **Visualize o resumo:** O resumo gerado será exibido na saída da célula.
6. **PDF do relatório:** Um arquivo PDF chamado `relatorio_resumo.pdf` será gerado no ambiente do Colab, contendo o resumo. Você pode baixá-lo na seção de arquivos do Colab.

## Bibliotecas utilizadas

- `google-genai`: Para interagir com os modelos da Google AI.
- `requests`: Para fazer requisições HTTP e obter o conteúdo de URLs.
- `beautifulsoup4`: Para parsear HTML e extrair texto de páginas web.
- `fpdf`: Para gerar arquivos PDF.

## Observações

- A qualidade do resumo depende da complexidade do texto/URL e do modelo Gemini.
- A extração de texto de URLs pode variar dependendo da estrutura do site.
- O arquivo PDF será gerado no diretório `/content/`.
