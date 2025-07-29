# [CTF] Level 7

URL: https://www.hackthissite.org/missions/basic/7/

![screenshot](/hackthissite/basic/7/img/challenge.png)
![screenshot](/hackthissite/basic/7/img/challenge7.png)

*O primeiro passo foi testar o input do view e ao digitar 2025, ele me retornou uma nova aba com todo o calendario deste mesmo ano com a uRL ```https://www.hackthissite.org/missions/basic/7/cal.pl ```*

![screenshot](/hackthissite/basic/7/img/calendar7.png)

*O desafio diz que existe um arquivo oculto, onde a senha (não encriptada) foi salva, então verifiquei o código fonte, mas nada foi encontrado.*
*Após um tempo analisando, resolvi fazer um brute-force para encontrar diretorios ou arquivos ocultos e, para isso utilizei a ferramenta gobuster, passando o seguinte comando: ```gobuster dir -u https://www.hackthissite.org/missions/basic/7/ -w /usr/share/seclists/Discovery/Web-Content/com
mon.txt -t 4 --delay 1s -o scan_directory.txt```*

*Mas o scan encontrou somente os arquivos que eu já tinha encontrado no recon manual, que foram o ```index.php``` e o ```cal.pl```*

*Note que o desafio cita que é necessário conhecimento básico de comandos UNIX, foi baseado nisto que resolvi realizar novamente, alguns testes no input view.*

*Pense bem! Se ao digitar um determinado ano, o campo me retornou um calendario, pensei, e se, passar no input um outro comando separado do qual me retornassem outras informações? foi aí que iniciei vários testes, como por exemplo:*


```
2025; ls
2025 && ls
cal 2025; ls 
cal 2025 && ls 
2025; ls -la (binGoOoo)
```
![screenshot](/hackthissite/basic/7/img/files7.png)

*Agora acho que estamos no caminho :-)* 

*Fui logo testando o ```level7.php``` e nada, recebi a seguinte mensagem:*

![screenshot](/hackthissite/basic/7/img/message7.png)

*Partir então para o ```k1kh31b1n55h.php``` e voilá, encontrei a senha!*

![screenshot](/hackthissite/basic/7/img/pass7.png)

*Com a senha não criptografada em mãos, finalizei o desafio!!*

![screenshot](/hackthissite/basic/7/img/win7.png)
