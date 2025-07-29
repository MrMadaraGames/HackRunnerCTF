# [CTF] StartTech

URL: https://capturetheflag.com.br/challenge/StartTech


![screenshot](/hackersec/challenges/beginner/startech/img/challenge.png)

*Mais um desafio de nível básico, que logo de cara já notamos um código que me parece um hash seguido de um encode. Vamos analisá-lo!*

*Como sempre, faço a leitura do código fonte e, observe a imagem abaixo, temos um base64 aqui.*

![screenshot](/hackersec/challenges/beginner/startech/img/code_review.png)

*Pensei rapidamente que já tinha em mãos o que precisava para resolver este desafio e encontrar a flag, mas não foi bem assim...*

*Utilizando a propria ferramenta da plataforma hackersec, fiz o decode e como pensei, realmente tinhamos um MD5 e dois base64.*

![screenshot](/hackersec/challenges/beginner/startech/img/md5.png)

![screenshot](/hackersec/challenges/beginner/startech/img/base64.png)

![screenshot](/hackersec/challenges/beginner/startech/img/base64_2.png)

*Com essas informações em mãos, logo pensei, pronto, já consegui a flag, mas entrei em um dilema de como organizar as informações
para tornar isso a flag. Tentei várias vezes submeter mas sempre recebia ACESSO NEGADO!*

*Por mais que simples, confesso que não resolvi este desafio no mesmo dia. Ao voltar, logo percebi que na verdade um dos
códigos era apenas para atrapalhar e assim dificultar um pouco mais a resolução do desafio e, foi aí que ao usar somente
as palavras ```hackersec-edtech```, exatamente neste formato, cheguei a flag.*

![screenshot](/hackersec/challenges/beginner/startech/img/flag.png)

No final, fica a mensagem, persistência e resiliencia, SEMPRE!

