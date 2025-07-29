# [CTF] meta

URL: https://capturetheflag.com.br/challenge/meta

![screenshot](/hackersec/challenges/beginner/meta/img/challenge.png)

*Hello my friends! Mais um desafio de nível básico e, como sempre aquela verificada basica no código fonte da página,
mas desta vez nada de interessante. Bem, no próprio enunciado do desafio já fica bem claro o caminho, pois fala sobre
metadados e logo abaixo mostra um base64.*

*Ao realizar o decode do code ```bWVOYS5wbmc=``` encontramos o seguinte resultado:*

![screenshot](/hackersec/challenges/beginner/meta/img/base64.png)

*Fica bem claro que temos uma imagem, mas onde está essa imagem? É simples, utilizando o próprio browser a URL do desafio
acrescentando ao final ```.png``` exatamente assim https://capturetheflag.com.br/challenge/meta.png e olha só caros
padawans o que encontramos!*

![screenshot](/hackersec/challenges/beginner/meta/img/meta.png)

*E agora? Partindo do princípio que o desafio é sobre metadados, fica claro que na própria imagem está escondido a nossa 
flag. Com isso iniciou a minha saga para descobrir esses dados. Confesso que logo de inicio utilizei umas formas que 
não deram nada certo, até as cores da imagem alterei para ver se encontrava algo, mas nada. Daí utilizei uma 
ferramenta OSINT bem legal, segue link https://29a.ch/photo-forensics/#forensic-magnifier* 

*E olha só o que encontramos em String Extraction, simplesmente A NOSSA FLAG !!!*

![screenshot](/hackersec/challenges/beginner/meta/img/data.png)

*Novamente fiz o decode, (tudo isso utilizando a própria ferramenta da HackerSec) e BINGoO. Flag!!* 

![screenshot](/hackersec/challenges/beginner/meta/img/flag.png)

*E com a flag ```flagmetahs``` finalizamos o desafio com sucesso.*

![screenshot](/hackersec/challenges/beginner/meta/img/win.png)





