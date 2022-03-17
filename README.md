# WhaTicket NINJA 🥷
📝 O backend usa [whatsapp-web.js](https://github.com/pedroslopez/whatsapp-web.js) para receber e enviar mensagens do WhatsApp, criar tickets a partir deles e armazenar tudo em um banco de dados MySQL.

📝 _Frontend é um aplicativo de bate-papo_ multiusuário com recursos completos, inicializado com react-create-app e Material UI, que se comunica com o **backend** usando API REST e Websockets. Permite interagir com contatos, tickets, enviar e receber mensagens do WhatsApp.

🚨⚠️ *Não é garantido garantir que você não será bloqueado usando este método, embora tenha funcionado para várias pessoas. O WhatsApp não permite bots ou clientes não oficiais em sua plataforma, portanto, isso não deve ser considerado totalmente seguro.* (*Não somos responsáveis por qualquer tipo de punição ou bloqueio.*)

## 💻 Como funciona?
A cada nova mensagem recebida em um WhatsApp associado, um novo Ticket é criado. Então, esse ticket pode ser acessado em uma _fila_ na página _Tickets_ , onde você pode atribuir o ticket a você mesmo, _aceitando-o, respondendo a mensagem do ticket e, eventualmente, _resolvendo_-o.

🚀 As mensagens subsequentes do mesmo contato serão relacionadas ao primeiro ticket **aberto/pendente encontrado.**

🚀 Se um contato enviar uma nova mensagem em menos de **10s** (*pode ser alterado nas configurações*) de intervalo e não houver nenhum ticket desse contato com status **pendente/aberto , o ticket** **fechado** mais recente será reaberto, em vez de criar um novo.

## 🚀 Recursos 

-   Tenha vários usuários conversando no mesmo número do WhatsApp ✅
-   Conecte-se a várias contas do WhatsApp e receba todas as mensagens em um só lugar ✅ 
-   Crie e converse com novos contatos sem tocar no celular ✅
-   Enviar e receber mensagem ✅
-   Enviar mídia (imagens/áudio/documentos) ✅
-   Receber mídia (imagens/áudio/vídeo/documentos) ✅

### 🥷 Extras:
- Ignore mensagens de grupos ✅🆕
- Altere tempo para criação de um novo ticket ✅🆕
- Ignore chamadas de áudio/vídeo ✅🆕
- Associe uma conexão padrão ao usuário ✅🆕
- Transferência de tickets para outra conexão ✅🆕
- Mais em [ Grupo Whaticket NINJA 🥷](https://telinkei.com/whaticket-zap) 🥷 | [whaticket.online](https://whaticket.online/) | [ZAP das Galáxias](https://www.youtube.com/channel/UCrPbAoQKz42Gm0mLdWatAEA)
***Todos os direitos reservados a seus respectivos criadores.*** ❤️ - GP Whaticket NINJA DEVS 🥷

## 💯 Instalação e Configuração (Ubuntu)

###  🔥 Instale as dependências:

    sudo apt-get install -y libxshmfence-dev libgbm-dev wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2 0,0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc ++ 6 libx11-6 libx11-6 libx11-6 libxcb1 libxComposite1 libxCursor1 libxDamage1 libxext6 libxfixes3 libxi6 libxRandr2 libxrender1 libxss1 libxxrender1 CA-Certificados fontes-Libertação -release xdg-utils

###  💣 Clonar este repositório
    git clone https://github.com/whaticket/whaticketvip whaticketvip 

Vá para a pasta ***backend*** e edite o arquivo `.env`:

    NODE_ENV=
    BACKEND_URL=http://localhost
    FRONTEND_URL=http://localhost:3000
    PROXY_PORT=8080
    PORT=8080
    
    DB_DIALECT=mysql
    DB_HOST=localhost
    DB_USER=root
    DB_PASS=
    DB_NAME=wpp
    
    JWT_SECRET=3123123213123
    JWT_REFRESH_SECRET=75756756756

Instale dependências de ***backend***, *build o app, execute as migrações e seeds* do banco de dados:

    npm install
    npm run build
    npx sequelize db:migrate
    npx sequelize db:seed:all

🚀 Iniciando o ***backend***:

    npm start

---

Vá para a pasta ***frontend*** e edite o arquivo `.env`:

    REACT_APP_BACKEND_URL = http://localhost:8080/
    REACT_APP_HOURS_CLOSE_TICKETS_AUTO = 24

Instale as dependências do ***frontend***:

    npm install 
    npm run build
    npm install -g serve

🚀 Iniciando o ***backend***:

    serve -s build

-   Vá para `http://localhost_ou_ip:3000/signup`
-   Crie um usuário e faça login com ele.
-   Na barra lateral, acesse a página _Conexões_ e crie sua primeira conexão do WhatsApp.
-   Aguarde o botão QR CODE aparecer, clique nele e leia o código qr.
-   Feito. Todas as mensagens recebidas pelo seu número do WhatsApp sincronizado aparecerão na Lista Tickets.


##  🚀 Produção

A instalação e configuração dos recursos PM2, NGINX e outros, podem se encontradas no diretório [canove/whaticket](https://github.com/canove/whaticket#:~:text=Start%20frontend%20with%20pm2,%20and%20save%20pm2%20process%20list%20to%20start%20automatically%20after%20reboot:). ❤️


### 📃 Isenção de responsabilidade
 This project is not affiliated, associated, authorized, endorsed by, or in any way officially connected with WhatsApp or any of its subsidiaries or its affiliates. The official WhatsApp website can be found at  [https://whatsapp.com](https://whatsapp.com/). "WhatsApp" as well as related names, marks, emblems and images are registered trademarks of their respective owners.

### 📃  Legal 
This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by WhatsApp or any of its affiliates or subsidiaries. This is an independent and unofficial software. Use at your own risk. Commercial use of this code/repo is strictly prohibited.

### 🔗Links Úteis

### GitHub

-   [Repositório Oficial de Cassio Santos no GitHub](https://github.com/canove/whaticket)
-   [Repositório Oficial da WhatsApp Web JS API, de Pedro Lopez no GitHub](https://github.com/pedroslopez/whatsapp-web.js/)

### Discord

-   [Whaticket - Grupo de Estudos](https://discord.gg/9Nw2ssrX)
-   [Whaticket - Comunidade Oficial](https://discord.gg/Dp2tTZRYHg)

### WhatsApp

-   [Grupo Whaticket NINJA 🥷  ](https://telinkei.com/whaticket-zap) 

### Telegram

-   [Grupo Whaticket NINJA 🥷 ](https://telinkei.com/whaticket-tg)


### *Todos os direitos reservados aos seus respectivos autores* ❤️
