# Titulo: GPIO_em_SBC_Linux
Acesso à GPIO usando Single board computer com SO Linux 


# Índice 

* [Título e Imagem de capa](#Título-e-Imagem-de-capa)
* [Índice](#índice)
* [O que é o Orange Pi?](#O-que-é-o-Orange-Pi?)
* [Status do Projeto](#status-do-Projeto)
* [Funcionalidades](#funcionalidades)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Autor](#autores)
* [Licença](#licença)
* [Conclusão](#conclusão)


# Descrição do Projeto

Atualmente, a oferta de SBC (Single-Board Computers) é grande. Para citar somente alguns, temos acesso facilmente no mercado de sistemas embarcados a: Raspberry Pi, BeagleBone Black, BeagleBone Green, Linkit Smart 7688, Intel Edison, CubieBoard, etc. 

Com esta oferta crescente, os fabricantes se diferenciam principalmente em dois aspectos: configurações de hardware cada vez mais robustas e preços cada vez menores. É justamente nestes dois pontos que a empresa Orange Pi focou para a fabricação da Orange Pi One. Esta placa possui características extremamente atraentes em hardware a um preço muito competitivo.

# O que é o Orange Pi?

Orange Pi é um computador de uma placa única e de código aberto. Percence a uma nova geração de placa de desenvolvimento, pode executar o Android 4.4, Android 7.0, Ubuntu e Debian e outros sistemas operacionais. A placa de desenvolvimento Orange Pi One usa o sistema em chip Allwinner H3 e possui 512 MB de memória DDR3.

## Aplicaçoes do Orange Pi

Podemos usá-lo para construir:
<ul>
<li>Um computador</li>
<li>Um servidor sem fio</li>
<li>Jogos</li>
<li>M&uacute;sica e sons</li>
<li>V&iacute;deo HD</li>
<li>Desenvolvimento de IoT</li>
<li>Firewall</li>
<li>Roteadores</li>
<li>Android</li>
</ul>
Praticamente qualquer outra coisa, porque Orange Pi é de código aberto.

## Recursos de hardware 


## As vistas superior e inferior do Orange Pi One
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 50%;"><img src="/img/Imagem1.jpg" alt="" width="300" /></td>
<td style="width: 50%;"><img src="/img/Imagem2.jpg" alt="" width="300" /></td>
</tr>
</tbody>
</table>

## As conex&otilde;es externas do Orange Pi One
<p style="text-align: center;"><img src="/img/Imagem3.jpg" alt="" width="300" /></p>

## Introdu&ccedil;&atilde;o ao uso da placa de desenvolvimento

## Prepara&ccedil;&atilde;o dos acess&oacute;rios
          
1. Cart&atilde;o TF, um cart&atilde;o de alta velocidade de classe 10 ou superior com capacidade m&iacute;nima de 8GB.
<p style="text-align: center;"><img src="/img/Imagem4.jpg" alt="" width="300" /></p>
<p>2. Leitor de cart&atilde;o TF, usado para ler e escrever cart&atilde;o TF</p>
<p style="text-align: center;"><img src="/img/Imagem5.jpg" alt="" width="300" /></p>
<p>3. Cabo HDMI para HDMI padr&atilde;o, usado para conectar a placa de desenvolvimento a um monitor HDMI ou TV.</p>
<p style="text-align: center;"><img src="/img/Imagem6.jpg" alt="" width="300" /></p>
<p>4. Adaptador de energia, adaptador de energia de alta qualidade de pelo menos 5V/2A.</p>
<p style="text-align: center;"><img src="/img/Imagem7.jpg" alt="" width="300" /></p>
<p><strong><em><span style="background-color: #ffff00;">Observe que a interface OTG da placa de desenvolvimento n&atilde;o pode ser usada como entrada de energia.</span> </em></strong></p>
<p><strong>Download a&nbsp; imagem&nbsp; e informa&ccedil;&otilde;es relacionadas ao SW ou HW</strong></p>
<p><a href="http://www.orangepi.org/downloadresources/">http://www.orangepi.org/downloadresources/</a></p>
<p><a href="https://github.com/orangepi-xunlong">https://github.com/orangepi-xunlong</a></p>
<p><strong>Instala&ccedil;&atilde;o do TF Card</strong></p>
<p>Inserir o cart&atilde;o TF em seu computador. O tamanho do TF deve ser maior que o tamanho da imagem do SO, geralmente 4 GB ou mais.</p>

## Formatar o cart&atilde;o TF.
<p>1. Baixar a ferramenta de formato de cart&atilde;o TF, como TF Formatter, em <a href="https://www.sdcard.org/downloads/formatter_4/eula_windows/">https://www.sdcard.org/downloads/formatter_4/eula_windows/</a></p>
<p>2. Descompactar o arquivo de download e executar o setup.exe para instalar a ferramenta em sua m&aacute;quina.</p>
<p>3. No menu "Op&ccedil;&otilde;es", defina a op&ccedil;&atilde;o "FORMAT options" para R&Aacute;PIDO.</p>
<p><img src="img1" alt="" width="300" /></p>
<p>4. Verificar se o cart&atilde;o TF inserido corresponde ao selecionado pela Ferramenta.</p>
<p>5. Clicar no bot&atilde;o "Format".</p>
<p><img src="img1" alt="" width="300" /></p>
<p>&nbsp;</p>

## Baixar a imagem do SO na p&aacute;gina de downloads.
<p>1. Acessar o site: <a href="http://www.orangepi.org/downloadresources/">http://www.orangepi.org/downloadresources/</a>&nbsp;</p>
<p>2. Escolher a vers&atilde;o do hw adequado e vers&atilde;o do SO desejado No nosso caso Orange Pi One e Ubuntu.</p>
<p><img src="img1" alt="" width="300" /></p>
<p>3. Salvar o arquivo em seu computador e descompacte o arquivo de download para obter a imagem do sistema operacional.</p>
<p><img src="img1" alt="" width="300" /></p>
<p>4. Anotar o usu&aacute;rio e senha. Ser&aacute; necess&aacute;rio para acessar o OrangePi One : <strong>user(root)</strong>, <strong>password(orangepi)</strong></p>
<p>5. Escolher a vers&atilde;o desejada do SO Ubuntu (geralmente a vers&atilde;o servidor mais recente&nbsp; Orangepione_2.1.0_ubuntu_xenial_server_linux3.4.113.7z):</p>
<p><img src="img1" alt="" width="300" /></p>
<p>6. Utilizar um utilit&aacute;rio para descomprimir o arquivo e criar a vers&atilde;o ISO.</p>

## Gravar o arquivo de imagem no cart&atilde;o TF.
<p>1. Baixar uma ferramenta que pode gravar imagens em um cart&atilde;o TF, como o Balena Etcher no site:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <a href="https://www.balena.io/etcher/">https://www.balena.io/etcher/</a></p>
<p>2. Escolher a vers&atilde;o do SO que utiliza (MAC ou Windows. Baixar e instalar o software</p>
<p><img src="img1" alt="" width="300" /></p>
<p>3. Abrir o arquivo de imagem descompactado.</p>
<p>4. Selecionar o Cart&atilde;o TF</p>
<p><img src="img1" alt="" width="300" /></p>
<p>5. Clicar no bot&atilde;o Flash. Aguardar a conclus&atilde;o da escrita.&nbsp;</p>
<p><img src="img1" alt="" width="300" /></p>

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
<ol>
<li>Abrir o CMD. Pressionar &ldquo;Win+R&rdquo; para abrir o Executar, digite cmd e clique em &ldquo;OK&rdquo; para abrir o Prompt de Comando.</li>
<li>Digitar o comando ipconfig, e teclar Enter.</li>
<li>Procurar por Endere&ccedil;o IPv4. Assim que o comando for executado, uma s&eacute;rie de informa&ccedil;&otilde;es ser&atilde;o exibidas na tela.</li>
</ol>

## Como descobrir o endere&ccedil;o IP do Orange Pi One?
<p>Para descobrir o IP de um dispositivo ligado a uma rede ser&aacute; necess&aacute;rio um programa para analisar a rede local que est&aacute; sendo utilizada. O Wireshark &eacute; o analisador de protocolo de rede amplamente utilizado do mundo. Ele permite que voc&ecirc; veja o que est&aacute; acontecendo em sua rede. Ele pode ser baixado em <a href="https://www.wireshark.org/">https://www.wireshark.org/</a> &nbsp;</p>
<p><img src="img1" alt="" width="300" /></p>
<p>Usar o comando Ping para verificar se &eacute; o Orange Pi One que est&aacute; sendo utilizado. Certamente ir&aacute; obter um tempo de resposta (ms).</p>

# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# :hammer: Funcionalidades 

- `Funcionalidade 1`: descrição da funcionalidade 1
- `Funcionalidade 2`: descrição da funcionalidade 2
- `Funcionalidade 3`: descrição da funcionalidade 3
- `Funcionalidade 4`: descrição da funcionalidade 4


# Tecnologias utilizadas 💻

<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" /> | `https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white`
          
# Autor

| [<img src="https://github.com/account" width=115><br><sub>Epaminondas Lage</sub>](https://github.com/epaminondaslage) | 

# Conclusão
