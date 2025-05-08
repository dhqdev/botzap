🤖 WhatsAppBot com Selenium
Este projeto é um bot simples que automatiza o envio de mensagens em grupos do WhatsApp Web utilizando Python e Selenium. Ele é útil para lembretes, recados automáticos ou testes de automação com mensagens.

🚀 Funcionalidades
Acessa o WhatsApp Web automaticamente.

Aguarda o login manual via QR Code.

Procura grupos pelo nome.

Envia uma mensagem pré-definida para cada grupo listado.

🛠️ Como usar
1. Pré-requisitos
Python 3.x instalado

Google Chrome instalado

ChromeDriver compatível com sua versão do Chrome

Instale o Selenium:

bash
Copiar
Editar
pip install selenium
2. Configure o caminho do ChromeDriver
No código, atualize a linha abaixo com o caminho correto do seu chromedriver.exe:

python
Copiar
Editar
self.driver = webdriver.Chrome(executable_path='/caminho/para/chromedriver.exe')
3. Customize a mensagem e os grupos
Você pode mudar a mensagem e os grupos no __init__ da classe:

python
Copiar
Editar
self.mensagem = "teste"
self.grupos = ["Lembrete e coisas"]
4. Execute o bot
Depois de configurar, execute o script:

python
Copiar
Editar
python nome_do_arquivo.py
O bot abrirá o WhatsApp Web. Escaneie o QR Code com seu celular, e ele começará a enviar as mensagens automaticamente.

