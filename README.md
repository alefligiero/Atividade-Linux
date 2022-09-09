# Como Instalar o Oracle Linux 8.6 no VirtualBox

![img1](https://dibiei.files.wordpress.com/2020/03/oracle_linux.png)

Oracle Linux (OL, anteriormente conhecido como Oracle Enterprise Linux) é uma distribuição Linux empacotada e distribuída livremente pela Oracle, disponível parcialmente sob a Licença Pública Geral GNU desde o final de 2006.[3] É compilado a partir do código-fonte do Red Hat Enterprise Linux (RHEL), substituindo a marca da Red Hat pela da Oracle. Ele também é usado pelo Oracle Cloud e pelo Oracle Engineered Systems, como o Oracle Exadata e outros.

Usaremos o VirtualBox que é uma ferramenta de virtualização que visa criar ambientes para instalação de sistemas distintos para instalar este sistema. Para realizar a instalação é necessário baixar a iso do sistema operacional em que foi escolhido que estão explícitos na aba de Links para Download.

# Links para Download
Segue abaixo os links para os downlodas necessários para a instalação da máquina:
* Oracle Linux (iremos trabalhar com a versão 8.6): [Oracle Linux ISOs](https://yum.oracle.com/ISOS/OracleLinux/OL8/u6/x86_64/OracleLinux-R8-U6-x86_64-dvd.iso)
* VirtualBox (iremos trabalhar com a ultima release (VirtualBox 6.1.38): [Downloads - Oracle VM VirtualBox](https://www.virtualbox.org/wiki/Downloads)

# Processos de instalações e configurações

Agora vamos instalar e configurar o VirtualBox e, logo em seguida, o Oracle Linux para o uso.

## Instalando e configurando o VirtualBox

Após baixar os arquivos necessários, realize a instalação do VirtualBox. Basta ir clicando em Próximo, selecionando o local de instalação de preferência e recomendadas pelo próprio instalador.

## Criando e configurando a VM

Depois de realizar a instalação e configuração do VirtualBox, agora iremos configurar uma VM para que nela, rodemos o sistema operacional desejado.

Primeiramente, clique no botao de New para adicionar uma nova VM.

![img2](https://i.imgur.com/tTTMvOq.png)

Ira exibir outra janela, onde o usuário deverá preencher os campos de acordo com o que está sendo pedido.

![img3](https://i.imgur.com/km80AL6.png)

1. No campo name, insira o nome que você dará para a sua VM. 
2. Em seguida, no próximo campo você irá selecionar a pasta aonde ficará salvo todos os arquivos e pastas relacionados a sua VM.
3. Posteriormente, no campo Type e Version, é onde fica localizado o tipo do seu sistema operacional e a versão do mesmo, respectivamente. Normalmente, ao dar um nome relacionado a um sistema operacional existente, o próprio VirtualBox automaticamente seleciona automaticamente o tipo e a versão do sistema alvejado.
4. Após preencher todos os campos, clique em Next.

Após clicar em próximo, pedirá para o usuário definir a quantidade de memória RAM que será alocado para o uso da VM. Como padrão, ele já vem com 1024MB(1GB), mas o recomendado para o uso deste tipo de sistema operacional é de 2048MB(2GB).

![img3](https://i.imgur.com/HNGEng9.png)

Selecionado a quantidade desejada, que nesse caso, foi de 2048MB, clique em Next para avançar para o próximo passo da instalação.

Feito isso, chegou a hora de alocar um espaço no disco rígido para a VM. Sendo assim, criarei um disco virtual novo apenas clicando em Create com a opção que já vem pré-selecionada.

![img4](https://i.imgur.com/inx1p7u.png)

Logo após, o usuário deve escolher o tipo de disco rígido que vai ser criado. Neste caso, selecione a opção VHD(Virtual Hard Disk) pois é considerado um padrão universal de virtualização e clique em Próximo.

![img5](https://i.imgur.com/3ZZEFTT.png)

Em seguida, existem duas opções para o armazenamento do disco rígido. A opção que já vem selecionada, Dynamic Allocated, define que, o uso do espaço do disco rígido só será utilizado de acordo com o que for utilizado de memória física na VM. Já o Fixed size, o tamanho que for selecionado, já vai ser reservado e alocado fisicamente para a VM assim, deixando espaços na memória que não estão sendo utilizados, reservados somente pela VM. Deixe a opção Dynamic Allocated selecionado e clique em Next.

![img6](https://i.imgur.com/6U3SYPX.png)

Escolha o tamanho desejado e a pasta onde ficará salvo o seu disco virtual. Neste caso, foi escolhido 50GB e o caminho padrão, mas o usuário pode alterar de acordo com a suas necessidades.

![img7](https://i.imgur.com/OrICWti.png)

Agora sim, a VM está criada. Mas antes de inicia-la, iremos alterar algumas configurações para melhor desempenho.

Clique com o botão direito na VM criada e selecione a opção Settings...

![img8](https://i.imgur.com/NSQ1BIf.png)

Depois disso, vá na aba System e na subaba Processor e selecione a quantidade de CPUs que deseja utilizar na VM. Nesse caso, foi selecionado 4 CPUs que é o suficiente para o que será feito na VM.

![img9](https://i.imgur.com/L1zfsF1.png)

Logo em seguida, clique na aba de Storage, e selecione em Controller: IDE, o disco vazio (Empty) e em Optical Drive, clique no ícone do CD ao lado e Choose a disk file. Selecione então a ISO que foi baixada do OracleLinux.

![img10](https://i.imgur.com/1ymfebs.png)

Para terminar as configurações da VM, vá na Aba de Network e mude para Bridged Adapter onde está escrito "Attached to:" para alternar a conexão para modo Bridge e sua VM ter acesso a internet após ser instalada.

![img11](https://i.imgur.com/qlm7HsX.png)

Pronto, agora a configuração a da VM no VirtualBox está terminada, clique nela e um Start para inicia-la.

![img12](https://i.imgur.com/L80TDyy.png)

## Instalando e configurando o OracleLinux

Iniciando a VM, mostrará a tela de primeira inicialização com duas opções, sendo a primeira para instalar o OracleLinux 8.6 e a segunda para testar a mídia e logo em seguida realizar a instalação 

![img13](https://i.imgur.com/JfVDgMC.png)

Depois de carregar a instalação, selecione o idioma em que você deseja e clique em Continue. Nesse caso, o idioma foi mantido em inglês.

![img14](https://i.imgur.com/QXJAKFm.png)

Em seguida, irá entrar em uma janela com uma série de configurações.

![img15](https://i.imgur.com/1f2OuDT.png)

Primeiramente, realize a configuração do teclado, indo em Keyboard e adicionando um layout desejado de acordo com o teclado que está sendo utilizado. No meu caso, é um teclado americano, então não alterei nenhuma configuração.

![img16](https://i.imgur.com/DNeGLXe.png)

Segundamente, em Date & Time, selecione clicando no mapa ou através do menu na parte superior da tela e também se quiser, ative a opção Network Time que vai automaticamente estabelecer um horário de acordo com o fuso horário selecionado (Para alterar esta opção, necessita antes ativar a Network, que será vista em breve)

![img17](https://i.imgur.com/Znbrtti.png)

Logo após, clique na opção Software Selection e selecione a opção Minimal Install, onde só vai ser instalado as funcionalidades básicas do OracleLinux sem interface gráfica, que pode também ser instalada futuramente.

![img18](https://i.imgur.com/f68LNCP.png)

Selecione a opção Network & Host Name para ativar a conexão ethernet e sua VM ter acesso a internet e também alterar o nome da sua máquina. 

![img20](https://i.imgur.com/jqxbguL.png)

Selecione também a opção de Installation Destination que é usada para configurar o disco rígido aonde será instalado o seu sistema. Clicando nessa opção, a tela exibirá o disco rígido virtual que foi criado na configuração da VM no VirtualBox. Exibe também a opção de criar automaticamente as partições e de forma customizada. De primeiro momento, deixaremos de forma automática para que depois ,futuramente, possa configurar as partições direto no sistema. Clique em Done para finalizar a configuração.

![img19](https://i.imgur.com/yTscyC1.png)

Agora só falta apenas selecionar a senha para o usuário root, que é o administrador da rede Linux e criar também um usuário comum que irá ter acesso ao seu sistema. Para isso, basta selecionar a opção Root Password e inserir a senha em que deseja para o usuário administrador. E selecionando User Creation, você configura o login, nome e senha para o seu usuário comum.

Configurando a senha pro root

![img21](https://i.imgur.com/ON7l5Ja.png)

Criando um usuário comum

![img22](https://i.imgur.com/axP75HP.png)

Após realizar todas essas configurações, clique em Begin Installation para realizar a instalação do OracleLinux

Finalizando a instalação, clique no botão para reniciar o sistema. Após reniciar, ele pedira o login e senha. Sendo assim é recomendado primeiramente entrar com o root para poder realizar algumas configurações inicias.

![img23](https://i.imgur.com/ZcAqZe6.png)

Digite o comando dnf -y update para atualizar o Kernel e outros serviços e aplicações padrões do Sistema.

![img24](https://i.imgur.com/ixdeq39.png)

E enfim, o seu OracleLinux foi instalado com sucesso!
