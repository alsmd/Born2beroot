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
</ul>