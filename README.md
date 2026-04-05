# Intelligence Newsletter — Sistema de Agregação de Notícias de IA

## Newsletter semanal automatizada com curadoria de notícias de Inteligência Artificial, gerada e enviada automaticamente toda segunda-feira e quinta-feira via n8n.


  **Sobre o Projeto**
  
O Intelligence Newsletter é um workflow automatizado desenvolvido no n8n para a Inteli Academy. Ele coleta, filtra, categoriza e resume as principais notícias de IA da semana, gerando uma newsletter HTML profissional enviada por e-mail e publicada automaticamente no LinkedIn.

O sistema resolve o problema da fragmentação de informações no universo da Inteligência Artificial, entregando um resumo semanal curado diretamente na caixa de entrada dos membros da comunidade.

<br>

 **Funcionalidades**

* Categorização inteligente via IA nas categorias: IA Generativa / Aprendizado de Máquina / Visão Computacional / Ética em IA / Aplicações em Setores
* Resumo em português com palavras-chave em negrito
* Título criativo gerado por IA para cada artigo
* Seção "Hypes do Momento" com os repositórios de IA mais populares do GitHub
* Newsletter HTML com design profissional em paleta bege/terracota
* Envio automático por e-mail toda segunda-feira e quinta-feira às 8h
* Post automático no LinkedIn com aprovação humana via e-mail

<br>

**Pré-requisitos**

* Docker instalado
  
* Conta no Groq
  
* Conta Gmail com Senha de App configurada
 
* Conta de desenvolvedor no LinkedIn
  
* Conta no GitHub (para a API pública)

<br>

**Configurar as Credenciais**

*1. Groq API*

Acesse console.groq.com

Crie uma API Key

No n8n, vá em Credentials → Add Credential → Groq

Cole sua API Key

<br>

*2. Gmail SMTP*

Ative a verificação em 2 etapas no Google

Crie uma Senha de App

No n8n, configure o nó Send Email com:

  Host: smtp.gmail.com, 
  Port: 465, 
  User: seu e-mail, 
  Password: senha de app gerada 

<br>

*3. LinkedIn API*

Acesse linkedin.com/developers

Crie um app e adicione o produto "Share on LinkedIn"

Configure o redirect URI: http://localhost:5678/rest/oauth2-credential/callback

Gere um Access Token seguindo o fluxo OAuth2

Configure o Header de autorização no nó HTTP Request do LinkedIn

<br>

**Número de Artigos**

Por padrão o workflow processa 8 artigos por execução. Para alterar, modifique o .slice(0, 8) no nó Filtrar Artigos da Semana.

**Licença**

Este projeto foi desenvolvido como trabalho acadêmico para a Inteli Academy.

**Autor**
Lucas Andrade Silva

LinkedIn: [lucasandrade](https://www.linkedin.com/in/lucas-andrade-sva/)

GitHub: [lucaskarter](https://github.com/lucaskarter)
