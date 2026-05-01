# Utilizando KALI e MEDUSA em ambiente controlado

Neste laboratório, foram testados alguns conceitos de pentest e para isso foi usado a ferramenta 
medusa, vale salientar que ela é usada também pela equipe blue team para encontrar vulnerabilidades 
nos sistemas internos da empresa.

Neste cenário, foram utilizadas duas máquinas virtuais sendo elas: Metasploitable2 e Kali.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/7a7de9bfab4630ba9869961550c503fa5567fe70/imagens/kali-meta.png)

Neste segundo momento, após a configuração foi testado o comando ping para a máquina que vamos aplicar 
os conceitos de brute force.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/ping%20kali1.png)

Com o ambiente configurado, iniciamos os primeiros testes de acesso para a nossa máquina virtual alvo, aqui
fizemos um scan em portas específicas onde é possível verificar o status dela e qual a versão do serviço utililzado, 
sabendo disso, podemos usar das vulnerabilidades de algumas versões.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/enumera%C3%A7%C3%A3o%20kali.png)

Uma vez encontrato a vulnerabilidade na máquina alvo, podemos testar o acesso ao serviço FTP, para isso iremos usar 
nossa ferramenta MEDUSA para forçar o acesso através de uma combinação entre usuários e senhas, então criamos uma lista 
de usuários e senhas possíveis para acessar o dispositivo.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/listas-usuario-senha.png)

Após criarmos as listas, vamos utilizar a MEDUSA para que faça os testes de combinação e nos retorne uma resposta onde encontra 
o nome de usuário e senha para que possamos ter acesso ao sistema.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/usando-medusa.png)

Uma vez encontrado o nome de usuário e senha, vamos utilizá-lo. No terminal digitamos o nome do serviço, nesse caso o FTP e o IP do alvo.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/75bb123e0e9ff436ece07e86227533de88ee8d97/imagens/testandoconex%C3%A3oftp.png)

Quando digitado o nome de usuário e senha corretos, temos acesso ao dispositivo, por isso é importante atualizar para versões mais recentes as quais
contam com mais segurança ao protocolo.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/75bb123e0e9ff436ece07e86227533de88ee8d97/imagens/ataque-bem-sucedido.png)

Vimos que com ferramentas gratuitas e um pouco de dedicação é possível aplicar técnicas de extração de dados em dispositivos mal configurados e
dependendo do alvo pode trazer um grande prejuízo se for uma corporação ou órgão governamental, por isso é essencial que os protocolos de serviços estejam
sempre atualizados, assim como um firewall bem configurado para bloquear as tentativas de acesso mal sucedidas e também, orientar aos usuários
que criem senhas fortes com isso a segurança na rede aumenta.

Nesse mesmo projeto foram feitos laboratórios com testes a ataque para a web utilizando o DVWA e também técnicas de password sprayng em SMB. Os testes podem ser 
visto na pasta imagens.
