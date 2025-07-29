# [CTF] Level 8

*Requisito: Conhecimento de SSI (HTML dinâmico executado pelo servidor)*

URL: https://www.hackthissite.org/missions/basic/8/

![screenshot](/hackthissite/basic/8/img/challenge.png)

*Para resolver este desafio foi necessário entender como funciona SSI e Path Traversal. Abaixo seguem referências:*

- SSI: https://owasp.org/www-community/attacks/Server-Side_Includes_(SSI)_Injection <br>
- Path Traversal: https://owasp.org/www-community/attacks/Path_Traversal

*Após alguns momentos de estudos, partimos para testar a aplicação. Ressalto que foi necessário ter paciência, pois foram várias tentativas e erros até chegar no que realmente funcionava.*

*A porta de entrada é sem dúvida o input ```Enter your name:```*

![screenshot](/hackthissite/basic/8/img/challenge8.png)

*Ao injetar o comando ```<!--#exec cmd="ls" -->``` no campo de input, recebi a seguinte mensagem:*

![screenshot](/hackthissite/basic/8/img/message.png)


*São alguns possiveis arquivos com extensões .shtml, que não ajudou muito, porém uma observação importante, é que esses dados foram apresentados na URL ```hackthissite.org/missions/basic/8/tmp/```*

*Como o enunciado do desafio fala que o arquivo com a senha estaria no diretorio ```/var/www/hackthissite.org/html/missions/basic/8/``` testamos o seguinte comando ```<!--#exec cmd="cd /var/www/hackthissite.org/html/missions/basic/8/" -->``` para que liste os arquivos dentro desse diretório.*
*Com isso recebemos a seguinte mensagem abaixo, que foi primordial para entender algumas situações e, ver que estavamos no caminho certo.*

![screenshot](/hackthissite/basic/8/img/message1.png)

*A mensagem fala, dentre outras coisas, algo do tipo "manipule seu código para que ele seja um pouco mais pertinente". Com isso percebemos que além do conhecimento de SSI, precisavamos também utilizar técnicas de Path Traversal e, foi aí que o jogo evoluiu :-).*

*Lambra da URL com o diretorio ```/tmp```? Foi justamente aí que percebemos que precisavamos subir diretorio. Sendo assim, executamos o comando para listar arquivos com ```<!--#exec cmd="ls ../" -->``` e obtemos a mensagem abaixo:*

![screenshot](/hackthissite/basic/8/img/path_files.png)

*Encontramos os arquivos que queriamos, com estas informações em mãos, ficamos próximos de encontrar a senha e ao executarmos o comando ```<!--#exec cmd="cat ../au12ha39vc.php" -->``` para ler o conteúdo do arquivo ```au12ha39vc.php```*

*BigOooo, encontramos a senha!*

![screenshot](/hackthissite/basic/8/img/passwd.png)

*Usamos a mesma no input de ```Password:``` e finalizamos o desafio!*


![screenshot](/hackthissite/basic/8/img/congratz.png)





