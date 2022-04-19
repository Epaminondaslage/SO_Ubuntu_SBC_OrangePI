# Título: GPIO_em_SBC_Linux
Acesso à GPIO usando Single board computer com SO Linux 


# Índice deste Repositório

* [Descrição deste Projeto](#Descrição-deste-Projeto)
* [O que é o Orange Pi?](#O-que-é-o-Orange-Pi?)
* [Aplicações do Orange Pi](#Aplicações-do-Orange-Pi)
* [Recursos de hardware](#Recursos-de-hardware)
* [Introdução ao uso da placa de desenvolvimento](#Introdução-ao-uso-da-placa-de-desenvolvimento)
* [Instalação da Imagem no TF Card](#Instalação-da-Imagem-no-TF-Card)
* [Scripts em Shell](#Scripts-em-shell)
* [Status do Projeto](#Status-do-Projeto)
* [Bibliogafia](#Bibliogafia)


# Descrição deste Projeto
Computador de placa única (SBC) é um computador onde todos os componentes electrónicos necessários para o seu funcionamento estão situados numa única placa de circuito impresso. Estes computadores são geralmente usados em sistemas de controle, alarmes, sistemas de medidas, entre outros. Atualmente, a oferta de SBC (Single-Board Computers) é grande. Para citar somente alguns, temos acesso facilmente no mercado de sistemas embarcados a: Raspberry Pi, BeagleBone Black, BeagleBone Green, Linkit Smart 7688, Intel Edison, CubieBoard, Arduino Mega 2560, Odroid, Orange Pi, Asus Tinker Board, etc. 

Com esta oferta crescente, os fabricantes se diferenciam principalmente em dois aspectos: configurações de hardware cada vez mais robustas e preços cada vez menores. É justamente nestes dois pontos que a empresa Orange Pi focou para a fabricação da Orange Pi One. Esta placa possui características extremamente atraentes em hardware a um preço muito competitivo. Entre outras características, esta máquina também incorpora um conector de 40 pins, porta USB, uma porta Gigabit Ethernet e HDMI. 

Estas placas rodam o SO Linux  e possuem os pinos I/O  disponíveis para acesso através de Shell script, Pynton, etc. Uma vez configurados a direção do pino de I/O pode-se ler ou alterar o estado do pino de I/O resultado em leituras de sensores externos, atuação de relés, etc. 

Este Repositório visa disponibilizar aos alunos do Curso de Eletrotécnica do Departamento de Engenharia Elétrica do CEFET-MG um tutorial de uso e um repositório de programas para o acesso à GPIO do Orange Pi através de Shell Script


# O que é o Orange Pi?
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem1.jpg" alt="" width="200" /></td>
<td style="width: 50%;">Orange Pi &eacute; um computador de uma placa &uacute;nica e de c&oacute;digo aberto. Percence a uma nova gera&ccedil;&atilde;o de placa de desenvolvimento, pode executar o Android 4.4, Android 7.0, Ubuntu e Debian e outros sistemas operacionais. A placa de desenvolvimento Orange Pi One usa o sistema em chip Allwinner H3 e possui 512 MB de mem&oacute;ria DDR3.</td>
</tr>
</tbody>
</table>


# Aplicações do Orange Pi
Praticamente qualquer outra coisa, porque Orange Pi é de código aberto. Podemos usá-lo para construir:
<ul>
<li>Um computador</li>
<li>Um servidor sem fio</li>
<li>Jogos</li>
<li>Música e sons</li>
<li>Vídeo HD</li>
<li>Desenvolvimento de IoT</li>
<li>Firewall</li>
<li>Roteadores</li>
<li>Android</li>
</ul>


# Recursos de hardware 
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;">
<p><img src="/img/Imagem3.jpg" alt="" width="300" /></p>
</td>
<td style="width: 50%;"><img src="/img/hw orange pi.png" alt="" width="300" /></td>
</tr>
</tbody>
</table>


## As vistas superior e inferior do Orange Pi One
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem1.jpg" alt="" width="150" /></td>
<td style="width: 50%;"><img src="/img/Imagem2.jpg" alt="" width="150" /></td>
</tr>
</tbody>
</table>

## As conex&otilde;es externas do Orange Pi One
<p style="text-align: center;"><img src="/img/Imagem3.jpg" alt="" width="400" /></p>

# Introdução ao uso da placa de desenvolvimento

## Preparação dos acessórios   
1. Cart&atilde;o TF, um cart&atilde;o de alta velocidade de classe 10 ou superior com capacidade m&iacute;nima de 8GB.
<p style="text-align: center;"><img src="/img/Imagem4.jpg" alt="" width="80" /></p>
<p>2. Leitor de cart&atilde;o TF, usado para ler e escrever cart&atilde;o TF</p>
<p style="text-align: center;"><img src="/img/Imagem5.jpg" alt="" width="150" /></p>
<p>3. Cabo HDMI para HDMI padr&atilde;o, usado para conectar a placa de desenvolvimento a um monitor HDMI ou TV.</p>
<p style="text-align: center;"><img src="/img/Imagem6.jpg" alt="" width="150" /></p>
<p>4. Adaptador de energia, adaptador de energia de alta qualidade de pelo menos 5V/2A.</p>
<p style="text-align: center;"><img src="/img/Imagem7.jpg" alt="" width="150" /></p>
<p><strong><em><span style="background-color: #ffff00;">Observe que a interface OTG da placa de desenvolvimento n&atilde;o pode ser usada como entrada de energia.</span> </em></strong></p>
<p><strong>Download a&nbsp; imagem&nbsp; e informa&ccedil;&otilde;es relacionadas ao SW ou HW</strong></p>
<p><a href="http://www.orangepi.org/downloadresources/">http://www.orangepi.org/downloadresources/</a></p>
<p><a href="https://github.com/orangepi-xunlong">https://github.com/orangepi-xunlong</a></p>

# Instalação da Imagem no TF Card
<p>Inserir o cart&atilde;o TF em seu computador. O tamanho do TF deve ser maior que o tamanho da imagem do SO, geralmente 4 GB ou mais.</p>

## Formatar o cartão TF.
<p>1. Baixar a ferramenta de formato de cart&atilde;o TF, como TF Formatter, em <a href="https://www.sdcard.org/downloads/formatter_4/eula_windows/">https://www.sdcard.org/downloads/formatter_4/eula_windows/</a></p>
<p>2. Descompactar o arquivo de download e executar o setup.exe para instalar a ferramenta em sua m&aacute;quina.</p>
<p>3. No menu "Op&ccedil;&otilde;es", defina a op&ccedil;&atilde;o "FORMAT options" para R&Aacute;PIDO.</p>
<p style="text-align: center;"><img src="/img/Imagem8.png" alt="" width="300" /></p>
<p>4. Verificar se o cart&atilde;o TF inserido corresponde ao selecionado pela Ferramenta.</p>
<p>5. Clicar no bot&atilde;o "Format".</p>
<p style="text-align: center;"><img src="/img/Imagem9.png" alt="" width="300" /></p>
<p>&nbsp;</p>

## Baixar a imagem do SO na p&aacute;gina de downloads.
<p>1. Acessar o site: <a href="http://www.orangepi.org/downloadresources/">http://www.orangepi.org/downloadresources/</a>&nbsp;</p>
<p>2. Escolher a vers&atilde;o do hw adequado e vers&atilde;o do SO desejado No nosso caso Orange Pi One e Ubuntu.</p>
<p style="text-align: center;"><img src="/img/Imagem10.png" alt="" width="400" /></p>
<p>3. Salvar o arquivo em seu computador e descompacte o arquivo de download para obter a imagem do sistema operacional.</p>
<p style="text-align: center;"><img src="/img/Imagem11.png" alt="" width="400" /></p>
<p>4. Anotar o usu&aacute;rio e senha. Ser&aacute; necess&aacute;rio para acessar o OrangePi One : <strong>user(root)</strong>, <strong>password(orangepi)</strong></p>
<p>5. Escolher a vers&atilde;o desejada do SO Ubuntu (geralmente a vers&atilde;o servidor mais recente&nbsp; Orangepione_2.1.0_ubuntu_xenial_server_linux3.4.113.7z):</p>
<p style="text-align: center;"><img src="/img/Imagem11a.png" alt="" width="400" /></p>
<p>6. Utilizar um utilit&aacute;rio para descomprimir o arquivo e criar a vers&atilde;o ISO.</p>

## Gravar o arquivo de imagem no cart&atilde;o TF.
<p>1. Baixar uma ferramenta que pode gravar imagens em um cart&atilde;o TF, como o Balena Etcher no site:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <a href="https://www.balena.io/etcher/">https://www.balena.io/etcher/</a></p>
<p>2. Escolher a vers&atilde;o do SO que utiliza (MAC ou Windows. Baixar e instalar o software</p>
<p style="text-align: center;"><img src="/img/Imagem12.png" alt="" width="400" /></p>
<p>3. Abrir o arquivo de imagem descompactado.</p>
<p>4. Selecionar o Cart&atilde;o TF</p>
<p style="text-align: center;"><img src="/img/Imagem13.png" alt="" width="400" /></p>
<p>5. Clicar no bot&atilde;o Flash. Aguardar a conclus&atilde;o da escrita.&nbsp;</p>
<p style="text-align: center;"><img src="/img/Imagem14.png" alt="" width="400" /></p>

## Ligar o Orange Pi One e acessar seu SO
<ol>
<li>Insirir o cart&atilde;o TF com a imagem no slot de cart&atilde;o TF da placa de desenvolvimento Orange Pi.</li>
<li>Conectar um adaptador de energia de 5V e pelo menos 2A (3A tamb&eacute;m &eacute; poss&iacute;vel)</li>
</ol>
<p><span style="background-color: #ffff00;">Lembrar de n&atilde;o conectar o adaptador de energia de 12V, se voc&ecirc; conectar o adaptador de energia de 12V, a placa de desenvolvimento ser&aacute; queimada.</span></p>
<p>Muitos fen&ocirc;menos inst&aacute;veis ​​durante a inicializa&ccedil;&atilde;o e inicializa&ccedil;&atilde;o do sistema s&atilde;o basicamente causados ​​por problemas de fonte de alimenta&ccedil;&atilde;o, portanto, um adaptador de energia confi&aacute;vel &eacute; muito importante.</p>
<ol>
<li>A placa de desenvolvimento tem uma interface HDMI, voc&ecirc; pode conectar a placa de desenvolvimento a uma TV ou outros monitores HDMI atrav&eacute;s de um cabo HDMI. (opcional se o acesso ao mesmo for de forma SSH.</li>
<li>A placa de desenvolvimento possui uma porta Ethernet, que deve ser conectada a um cabo de rede para acesso &agrave; Internet e permitir seu acesso remoto.</li>
<li>Conecte o mouse e o teclado USB para controlar a placa de desenvolvimento Orange Pi. Iremos utilizar o acesso a placa atrav&eacute;s da rede local e acesso SSH.</li>
</ol>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; SSH &eacute; a sigla para Secure Socket Shell, sendo um dos protocolos &nbsp;&nbsp;&nbsp;&nbsp; espec&iacute;ficos de seguran&ccedil;a de troca de arquivos entre cliente e &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; servidor de internet, usando criptografia. O objetivo do SSH &eacute; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; permitir que desenvolvedores ou outros usu&aacute;rios realizem &nbsp; altera&ccedil;&otilde;es em sites e servidores utilizando uma conex&atilde;o simples &nbsp;&nbsp;&nbsp;&nbsp; e segura.</p>
<p>Se voc&ecirc; deseja visualizar as informa&ccedil;&otilde;es de sa&iacute;da do sistema atrav&eacute;s da porta serial de depura&ccedil;&atilde;o, use o cabo serial para conectar a placa de desenvolvimento ao computador.</p>

## Como descobrir qual &eacute; o meu IP?
I IP de seu computador pode ser descorberto através de comandos do próprio windows como o exemplo abaixo:
<ol>
<li>Abrir o CMD. Pressionar &ldquo;Win+R&rdquo; para abrir o Executar, digite cmd e clique em &ldquo;OK&rdquo; para abrir o Prompt de Comando.</li>
<li>Digitar o comando ipconfig, e teclar Enter.</li>
<li>Procurar por Endere&ccedil;o IPv4. Assim que o comando for executado, uma s&eacute;rie de informa&ccedil;&otilde;es ser&atilde;o exibidas na tela.</li>
</ol>
Pode-se usar aplicativos para o desktop ou para celular (desde que o Wi-Fi de seu celular esteja na mesma rede. O Fing (https://www.fing.com) permite aproveitar ao máximo sua rede. Ele premite ver todos os dispositivos conectados ao roteador WiFi, executa scanners de rede, monitora a velocidade da Internet e o nível de segurança. 
No exemplo abaixo está sendo utilizando o programa IP Scanner que possui mesma finalidade.
<p style="text-align: center;"><img src="/img/IP Scanner.png" alt="" width="300" /></p>

## Como descobrir o endere&ccedil;o IP do Orange Pi One?
<p>Para descobrir o IP de um dispositivo ligado a uma rede ser&aacute; necess&aacute;rio um programa para analisar a rede local que est&aacute; sendo utilizada. O IP Scanner ou outro analisador de redes.
<p style="text-align: center;"><img src="/img/IP Scanner1.png" alt="" width="300" /></p>

Uma vez identificado o Orange Pi pode-se exetutar comando Ping para verificar se é o Orange Pi One que está sendo utilizado. Certamente irá obter um tempo de resposta (ms).
<p style="text-align: center;"><img src="/img/ping.png" alt="" width="300" /></p>
Desligue o Orange Pi One durande a execução comando Ping e irá observar que não terá mais este “time”. Ligue novemante e ele voltará a ter o tempo de resposta. 

## Como acessar remotamente o Orange Pi?
O SSH é um protocolo de rede para o usuário internet acessar, administrar e modificar  remotamente computadores. Com o acesso SSH, o usuário pode fazer login em um outro computador por uma rede protegida por criptografia. Assim pode-se executar comandos, mover e editar arquivos de um local para outro sem riscos de interceptação por agentes maliciosos.
Essa tecnologia oferece uma interface baseada em texto para criar o acesso Shell remoto. Essa interface é o próprio terminal Shell, que executa os comandos digitados e faz a ponte entre a máquina do usuário e o servidor remoto. 
Shell, do inglês, significa concha, casca ou algo revestido. Neste contexto, o Shell é um interceptador de comandos que executa a ligação entre o usuário e o sistema operacional.

Para efetuar este comando a sintaxe do comando é a que segue. Vale lembrar que deverá ser digitado na linha de comando do teu terminal.

    ssh {user}@{host}

Onde:

    ssh – é a indicação do uso do comando SSH, que indica ao sistema que se quer abrir uma conexão criptografada e segura.
    {user} – é a conta a qual você deseja se conectar remotamente como usuário root (raiz), com direitos completos para mexer em qualquer coisa do sistema.
    {host} – é o computador que você quer acessar, inserindo um número de IP ou nome de domínio específico (o número do IP descoberto acima).

Assim que digitar as informações, basta pressionar ENTER. Será preciso inserir suas credenciais como nome de usuário e senha de acesso a sua conta. No caso o Orange Pi o User=root e a Senha=orangepi

    User=root
    Senha=orangepi
  
Novamente, confirme pressionando ENTER mais uma vez. Uma janela remota de acesso ao Orange Pi vai aparecer logo na sequência.Pronto você está acessando o Shell do Orange Pi. Pode assim transferir, editar, executar programas, comandos do SO ou outra atividade. 

<p style="text-align: center;"><img src="/img/ssh_orange.png" alt="" width="300" /></p>

O PuTTy é um cliente SSH para a plataforma Windows e Unix (Linux e suas distribuições). Ele é um software de código aberto desenvolvido e constantemente atualizado por um grupo de especialistas voluntários. O PuTTY é um dos mais populares clientes SSH. Ele cria uma espécie de túnel encriptado de comunicação entre servidores, garantindo a segurança e o anonimato das conexões.
Com o Putty, o  usuário pode acessar e gerenciar seu servidor ou hospedagem remotamente. Com isso, é possível instalar, editar ou remover aplicações de acordo com as preferências de uso. 

# Introdução ao Scripts em Shell

Podemos utilizar a criação de arquivos de scripts para tornar mais simples as execuções de tarefas repetitivas no dia a dia. Muito tempo do programador é empregado em ações desse tipo, como abrir os mesmos programas todos os dias; esvaziar a lixeira e diretórios temp para economizar espaço em disco; etc.
Um script nada mais é do que um algoritmo projetado para realizar uma determinada tarefa, utilizando os comandos específicos do bash e os executáveis do sistema operacional.

    Lembre-se de executar os comandos como usuário comum e não como root, visto que, como root tudo será aceito e, dependendo do que você fizer, isto pode gerar danos ao sistema operacional. Uma maneira fácil de verificar é abrir o terminal e se o símbolo antes do cursor é o $, você está como usuário comum, mas se é o #, você está como root. Para sair do modo root, digite exit
    
    Devemos portando criar um usuário para que possamos trabalhar com segurança. O comando "adduser" serve para adicionar um usuário ou um grupo ao sistema, onde será criado um diretório com o nome do usuário, com uma entrada para o usuário no arquivo /etc/passwd (senhas). A utilização do comando adduser necessita do uso do comando sudo (deve estar com previlégio de root).
Além disso, quando é adicionado um novo usuário, é criado, por padrão, um grupo com o nome do mesmo usuário. Caso seja criado um novo grupo, o comando adduser cria uma entrada para o grupo no arquivo /etc/group. 
    

    root@orangepione:/home# adduser epaminondas
    Adding user `epaminondas' ...
    Adding new group `epaminondas' (1001) ...
    Adding new user `epaminondas' (1001) with group `epaminondas' ...
    Creating home directory `/home/epaminondas' ...
    Copying files from `/etc/skel' ...
    Enter new UNIX password: 
    Retype new UNIX password: 
    passwd: password updated successfully
    Changing the user information for epaminondas
    Enter the new value, or press ENTER for the default
	Full Name []: Epaminondas Lage
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
    Is the information correct? [Y/n] Y
    root@orangepione:/home# 
Portanto pode-se sair da sessão e fazer ssh com o usuário recém criado.
<p style="text-align: center;"><img src="/img/epaminondaslage.png" alt="" width="300" /></p>
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 11.242%;"><img src="/img/manual.png" alt="" width="50" /></td>
<td style="width: 88.758%;"><br />Um arquivo PDF completo do manual de operação da SBC Orange Pi ode ser encontrado <a href="/docs/orangepi one_h3_user manual_v3.2.pdf">aqui</a></td>
</tr>
</tbody>
</table>

# Status do Projeto
![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# Bibliogafia

- `Orangepi one_h3_user manual_v3.2`: Manual de operação da Orange Pi One
- `Funcionalidade 2`: descrição da funcionalidade 2
- `Funcionalidade 3`: descrição da funcionalidade 3
- `Funcionalidade 4`: descrição da funcionalidade 4


