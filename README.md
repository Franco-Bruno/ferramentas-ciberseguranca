# Utilizando KALI e MEDUSA em ambiente controlado

Neste laboratório, foram testados alguns conceitos de pentest e para isso foi usado a ferramenta medusa, 
vale salientar que ela é usada também pela equipe blue team para encontrar vulnerabilidades nos sistemas internos
da empresa.

Neste cenário, foram utilizadas duas máquinas virtuais sendo elas: Metasploitable2 e Kali.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/7a7de9bfab4630ba9869961550c503fa5567fe70/imagens/kali-meta.png)

Neste segundo momento, após a configuração foi testado o comando ping para a máquina que vamos aplicar os conceitos de brute force.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/ping%20kali1.png)

Com o ambiente configurado, iniciamos os primeiros testes de acesso para a nossa máquina virtual alvo, aqui fizemos um scan em portas específicas onde
é possível verificar o status dela e qual a versão do serviço utililzado, sabendo disso, podemos usar das vulnerabilidades de algumas versões.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/enumera%C3%A7%C3%A3o%20kali.png)

Uma vez encontrato a vulnerabilidade na máquina alvo, podemos testar o acesso ao serviço FTP, para isso iremos usar nossa ferramenta MEDUSA para forçar 
o acesso através de uma combinação entre usuários e senhas, então criamos uma lista de usuários e senhas possíveis para acessar o dispositivo.

![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/listas-usuario-senha.png)
![image alt](https://github.com/Franco-Bruno/ferramentas-ciberseguranca/blob/68090715780f09bec454aa003a86f6b05e3946a7/imagens/usando-medusa.png)
