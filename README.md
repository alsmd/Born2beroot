<h1>Born to be root!</h1>
<br>
<p>Esse é um projeto da 42 sp com o objetivo de nos introduzir ao mundo da virtualização.</p>
<p>Primeiramente teremos que instalar um linux (Debian/Centos) com a minima quantidade de sofwares, e baixar somente o necessario para o funcionamento de um servidor.</p>

<h2>Instalação</h2>
<ul>
    <li>Para o projeto eu optei pelo Debian por ser mais simples.</li>
    <li>Podemos fazer o download do nosso systema em <a target="_blank" href="https://www.debian.org/distrib/netinst">Debian</a>.</li>
    <li>Irei estar utilizar o <a target="_blank" href="https://www.virtualbox.org/">Virtual box</a> para instalar nosso systema.</li>
    <li>Agora basta <a href="https://tecnoblog.net/302459/como-criar-uma-maquina-virtual-virtualbox/" target="_blank" rel="noopener noreferrer">Criar</a> uma nova maquina virtual</li>
    <li>Antes de iniciar nossa nova maquina precisamos mudar a configuração de rede do virtual box para <strong>Placa em Modo Bridge</strong>.</li>
    <img src="conf.png" alt="">
    <li>Ao ligar nossa VM podemos selecionar nossa <strong>Debian Iso </strong> para instalação.</li>
    <li>É importante que selecionemos a instalação sem a interface grafica.</li>
    <li>A primeira parte da instalação é bastante simples, basta selecionar a linguagem e a localização,hostname (login da intra + 42), senha do root e usuario inicial.</li>
    <li>Depois das configurações basicas iremos definir como nossas partições serão organizadas.</li>
    <li>Basta selecionar a opção para setar o lvm encriptado automaticamente.</li>
    <li>Iremos criar algumas pastas em partições separadas.</li>
    <img src="part.png" alt="">
    <li>Agora basta esperar a instalação.</li>
    <li>Irei deixar apenas os sofwares padrões e o ssh como programas iniciais.</li>
    <img src="sof.png" alt="">
</ul>
<h2>Configurações</h2>
<ul>
    <li>Durante A instalação desse servidor estarei utilizando o gerenciador de pacote aptitude, por se tratar uma aplicação mais simples</li>
    <li><strong>apt install aptitude</strong></li>
    <li>Vim como editor de texto.</li>
    <li><strong>aptitude install vim</strong></li>
    <li>App Armor é um software sutilizado para limitar o acesso dos programas a certos recursos.</li>
    <li>Podemos visualizar o apparmor com <strong>aa-status</strong>.</li>
</ul>

<h2>SSH</h2>
<ul>
    <li>O <a href="https://www.weblink.com.br/blog/tecnologia/acesso-ssh-o-que-e/" target="_blank" rel="noopener noreferrer">SSH</a> é um protolo de rede utilizado para acessar, gerenciar e modificar um servidor remotamente. </li>
    <li>Esse acesso é realizado atraves da rede, onde dados e informações são transmitidos atraves de uma comunicação criptografada.</li>
    <li>A ferramenta utilizada sera o <a href="https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/" target="_blank" rel="noopener noreferrer"> Open SSH</a></li>
    <li>Podemos verificar sua execução com o systemctl status ssh</li>
    <li>Por padrão ele estara rodando na porta 22</li>
    <li>Estarei mudando a porta no arquivo /etc/ssh/sshd_config com o vim</li>
    <img src="port.png" alt="">
</ul>