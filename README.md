# botzap
Create a bot to send massagers for my contacts.

from selenium import webdriver
import time

class WhatsAppBot:
    def __init__(self):
        self.mensagem = "teste"
        self.grupos = ["Lembrete e coisas"]
        options = webdriver.ChromeOptions()
        options.add_argument("lang=pt-br")
        self.driver = webdriver.Chrome(executable_path='/caminho/para/chromedriver.exe')

    def EnviarMensagens(self):
        self.driver.get('https://web.whatsapp.com')
        time.sleep(30)
        
        for grupo in self.grupos:
            grupo = self.driver.find_element_by_xpath(f"//span[@title='{grupo}']")
            time.sleep(3)
            grupo.click()
            
            chat_box = self.driver.find_element_by_class_name('_2xy_p _3XKXx')
            time.sleep(3)
            chat_box.click()
            chat_box.send_keys(self.mensagem)
            
            botao_enviar = self.driver.find_element_by_xpath("//span[@data-icon='send']")
            time.sleep(3)                                 
            botao_enviar.click()
            time.sleep(3)   

bot = WhatsAppBot()
bot.EnviarMensagens()
