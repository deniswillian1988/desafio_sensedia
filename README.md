### Desafio Técnico - Vaga Cloud Operations

Para execução do desafio passado pela Sensedia para a vaga de Cloud Operations, optei por realizar local em meu notbook, Windows 7, utilizando:
  - Vagrant + VirtualBox
  - Puppet
  - Docker
  
Para inicializar a estrutura, é necessário instalar o Vagrant (2.0 ou superior) e o Virtual Box.
Utilizei o Chocolatey em meu Windows para instalar ambos.

Link com procedimento de instalação: https://chocolatey.org/install
Com o choco instalado, execute no prompt de comando:
  C:\> choco install virtualbox
  C:\> choco install vagrant

Faça download dos arquivos Vagrantfile e default.pp disponibilizando eles em um diretórico conforme estrutura:
  ..\Vagrant\Vagrantfile
  ..\Vagrant\manifests\default.pp
Obs: diretório "manifest" deve ser criado.

Via prompt de comando, acessando o diretório como os arquivos, execute:
  vagrant up
  
Sua VM está no ar. Para verificar a aplicação, no navegdor, entre com o endereço: http://127.0.0.1:5000
