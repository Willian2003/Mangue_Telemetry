IMPORTANTE PARA O FUNCIONAMENTO: (O codigo so ira funcionar se essa lista for feita)
PARA MELHOR FUNCIONAMENTO USE O PYCHARM
Instale todas as bibliotecas

Como instalar bibliotecas no pycharm:
Canto inferior esquerdo procure por Python Packages
Clicando nela coloque o nome da biblioteca que você quer instalar
Selecione a biblioteca e pressione Install package.


Para não dar erro de serial port quando der start em "radio" PRECISA SER
LIGADO NO SEU PC O MÓDULO DA TELEMETRIA!!

Para o mapa inclua OBRIGATORIAMENTE A BIBLIOTECA FOLIUM E O MOZILLA FIREFOX
( o navegador pode ser baixado por fora mesmo (link para instalar no site: https://www.mozilla.org/pt-BR/firefox/new/ ))
E INSTALE A BIBLIOTECA SELENIUM

Em def update_map procure por _to_png e aperte ctrl+click para ir diretamente para 
sua definação. Desça um pouco e quando avistar: 
	if self._png_image is None:
            if driver is None:
                from selenium import webdriver
procure por: driver = webdriver.Firefox(options=options), você irá precisar modifica-la para:
driver = webdriver.Firefox(options=options, firefox_binary=r"C:\Program Files\Mozilla Firefox\firefox.exe")
Assim ele vai prourar diramente na pasta padrão onde é baixado o firefox.

Vale ressaltar que C:\Program Files\Mozilla Firefox é o caminho padrão, porém, dependendo onde e como você
instalou pode mudar. Então tenha certeza que o caminho está correto.