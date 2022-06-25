# Overview

Este repositório tem como finalidade compartilhar os códigos utilizados na construção de um chatbot de whatsapp onde é possível consultar a definição de diversos termos relacionados à ciência de dados. A aplicação tem como inspiração este bot do [Me Bote na Conversa](https://www.hypeness.com.br/2021/11/me-bote-na-conversa-chatbot-inclusivo-traduz-termos-corporativos-em-ingles-no-whatsapp/), entretanto é voltada especificamente para a área de ciência de dados.

Basicamente, é um bot de whatsapp onde se pode enviar um termo (em português ou inglês) relacionado à área de ciência de dados, "one hot encode" por exemplo, e ele retorna o conceito/definição desse termo. Caso o termo não exista na base de dados, que está em constante construção, existe a possibilidade enviar sugestões de termos para adição futura. O conceito da aplicação é simples, mas acredito que pode ajudar principalmente quem está iniciando na área.

A aplicação ainda está na versão beta e para acessá-la basta adicionar este número ao whatsapp (https://wa.me/+14155238886), enviar o código **"join passage-grew"** e depois mandar um "olá", "alô", "alow", "boa tarde", etc.

Todo o projeto foi desenvolvido em Python, sendo que o formulário de sugestão de termos utiliza a biblioteca Streamilit. Para acessar a documentação, diversos exemplos, tutoriais e a comunidade da biblioteca basta clicar aqui. Ainda, atualmente o chatbot roda no Heroku e o formulário está rodando em uma instância EC2 da AWS sendo que as bases de dados estão disponíveis em um bucket S3 também da AWS. Também estou utilizando o serviço da Twilio para realizar a entrega das mensagens.

# Organização do repositório

Para uma melhor organização, o repositório está dividido em 2 pastas descritas abaixo:

**bot_whatsapp_termos_DS:** Esta pasta contém o código do bot bem como outros recursos necessário para realizar o deploy da aplicação do Heroku.

**sugestao_termos:** Esta pasta guarda todos os códigos necessários para gerar o formulário de sugestão de termos que utiliza a biblioteca Streamilit. A seguir, uma breve descrição do que cada código faz:

- **main.py:** gera o formulário de sugestão de termos;
- **resources.py:** arquivo que guarda funções auxiliares que foram apartadas do código principal para melhorar a manutenção e entendimento.

# Fluxo do chatbot

<p align="center"><img alt="fluxo_chatbot" width="90%" src="https://github.com/mvpalheta/bot_whatsapp_termos_DS/blob/main/fluxo1_chatbot.png"></p>

<br>

Espero que tanto a aplicação quanto os códigos disponibilizados aqui sejam úteis para alguém. Estou à disposição para esclarecer dúvidas, receber críticas construtivas e/ou sugestões através do e-mail mvpalheta@gmail.com. **Abraços**.
