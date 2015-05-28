# Torne a mudança permanente

A simples alteração do arquivo /proc/sys/vm/swappiness, é inócua e não produz resultado algum.
Se você conseguir alterar este valor, o sistema o retornará ao padrão, assim que for reiniciado.
Você precisa alterar o arquivo /etc/sysctl.conf.
Abra-o com o seu editor de textos favorito (eu vou usar o nano):

sudo nano /etc/sysctl.conf
Agora, copie e cole o seguinte código ao final do arquivo:

#
## Reduz o uso de SWAP
vm.swappiness=10
## Melhora a gestão de cache
vm.vfs_cache_pressure=50
Em seguida, salve e saia do editor.
Reinicie a máquina e veja se houve melhora.
