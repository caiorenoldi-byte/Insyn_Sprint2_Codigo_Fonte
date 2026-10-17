# Insyn — código-fonte do protótipo da Sprint 2

Este pacote contém o mesmo código da versão demonstrativa criada nesta conversa.
Os quatro arquivos do site foram colocados na raiz da pasta para facilitar a publicação no GitHub Pages. Não há etapa de instalação de dependências ou de build.

## 1. Entender os arquivos

- index.html: estrutura da página, menu e diálogo sobre a demonstração.
- style.css: cores, fontes, espaçamento e adaptações para telas menores.
- data.js: oito máquinas fictícias, filtros e validação dos registros.
- app.js: navegação entre as telas, renderização, gráfico e avaliações.
- .nojekyll: indica ao GitHub Pages que os arquivos podem ser servidos diretamente.

O HTML aponta para app.js, que importa data.js. Os nomes e caminhos relativos devem ser preservados.
O código foi gerado por IA com assistência do Codex; revisem e entendam as mudanças antes de adotá-las como trabalho do grupo.

## 2. Abrir no VS Code

1. Extraia o ZIP para uma pasta, por exemplo Documentos/Insyn.
2. Abra o VS Code.
3. Use File > Open Folder (Arquivo > Abrir Pasta) e selecione a pasta Insyn que contém index.html.
4. Veja os arquivos no Explorer, na lateral esquerda.
5. Para melhorar a apresentação do código ao estudar, use Format Document (Formatar Documento), normalmente Shift+Alt+F no Windows. Salve com Ctrl+S.

## 3. Ver o site no computador

O site usa módulos JavaScript e deve ser aberto por um servidor local. Dar dois cliques no index.html pode impedir o carregamento dos módulos.

Se Python estiver instalado:

1. No VS Code, abra Terminal > New Terminal (Novo Terminal).
2. Confirme que o terminal está na pasta que contém index.html.
3. Execute:

    python -m http.server 5500 --bind 127.0.0.1

No Windows, se o comando python não funcionar e o iniciador py estiver instalado, tente:

    py -m http.server 5500 --bind 127.0.0.1

4. No navegador, abra http://127.0.0.1:5500
5. Para encerrar, pressione Ctrl+C no terminal.

Isso serve apenas para visualizar o projeto no seu computador. O Python não faz parte da lógica deste protótipo; ele apenas entrega os arquivos ao navegador.

## 4. Guardar versões no GitHub pelo VS Code

Requisitos: Git instalado no computador e uma conta GitHub.

1. Abra Source Control (Controle do Código-Fonte), normalmente Ctrl+Shift+G.
2. Escolha Initialize Repository (Inicializar Repositório).
3. Selecione os arquivos para Stage Changes (Preparar Alterações).
4. Escreva uma mensagem, como Versão inicial do protótipo Insyn, e faça Commit.
5. Abra a paleta de comandos com Ctrl+Shift+P e procure Publish to GitHub.
6. Entre na sua conta quando solicitado, escolha um nome e a visibilidade do repositório.
7. Abra o repositório no GitHub para conferir os arquivos.

Um commit é uma versão registrada localmente. Push envia os commits ao GitHub. Pull traz alterações dos colegas. No trabalho em grupo, cada pessoa pode clonar o repositório e propor mudanças por branches e pull requests.

## 5. Publicar o protótipo pelo GitHub Pages

Para o caminho gratuito mais simples, use um repositório público que contenha somente este código e os dados fictícios da demonstração.

1. No GitHub, abra o repositório e vá a Settings > Pages.
2. Em Build and deployment, escolha Deploy from a branch.
3. Selecione o branch que contém o código (geralmente main) e a pasta /(root).
4. Salve e aguarde a publicação.
5. Use o endereço mostrado pelo próprio GitHub. Não é necessário contratar um domínio.

O arquivo index.html deve ficar na raiz do repositório, ao lado de app.js, data.js e style.css. Não envie apenas a pasta externa do ZIP deixando os arquivos um nível abaixo.
Depois de configurar o Pages, novos pushes para o branch escolhido atualizam a publicação.
O endereço do GitHub Pages será uma publicação independente do endereço criado nesta conversa; alterações em um não se propagam automaticamente para o outro.

## 6. O que a demonstração faz

Visão geral > diário da máquina > consultar evidência > avaliação técnica > novo evento no diário.
As máquinas, curvas e prioridades são fictícias. Não há modelo preditivo treinado nem conexão com a operação da Motiva.
As avaliações são guardadas apenas no armazenamento local do navegador (localStorage). Publicar o site não cria um banco compartilhado: cada visitante continua com os próprios registros. O botão de restauração limpa somente os registros desta aplicação.
A previsão e o banco central fazem parte de uma evolução futura que depende de dados e validação.

## 7. Usar Codex no editor

É possível instalar a extensão oficial Codex no VS Code, entrar na conta e pedir explicações ou alterações usando os arquivos abertos como contexto. A disponibilidade depende da conta e das configurações do serviço.
Exemplos: Explique o arquivo data.js em linguagem de iniciante; mostre como a avaliação entra no diário; altere a cor principal e explique quais linhas mudaram.
O histórico desta conversa não deve ser presumido como automaticamente transferido para uma nova sessão: forneça o README e o contexto necessário.

## Documentação oficial

- VS Code e Git: https://code.visualstudio.com/docs/sourcecontrol/quickstart
- GitHub Pages: https://docs.github.com/pt/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- Codex no editor: https://learn.chatgpt.com/docs/codex/ide
