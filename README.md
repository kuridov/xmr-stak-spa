# Guia en español para minar con xmr-stak

```
sudo su
echo '* soft memlock 262144' >> /etc/security/limits.conf
echo '* hard memlock 262144' >> /etc/security/limits.conf
echo 'vm.nr_hugepages=128' >> /etc/sysctl.conf
sudo sysctl -p /etc/sysctl.conf
sudo apt-get update
sudo apt-get install -y libmicrohttpd-dev libssl-dev libhwloc-dev git
git clone https://github.com/kuridov/xmr-stak-spa.git && cd xmr-stak-spa && chmod 755 xmr-stak
(cerrar sesion - 'cerrar todas las consolas', no es necesario hacer reboot)
	
sudo su
cd xmr-stak-spa
tmux new -s XMRSTAKSPA //Crear una sesion para mantener el minero encendido a pesar de cerrar las consolas
./xmr-stak
    0 [ENTER]
    cryptonight_lite_v7 [ENTER]
    aqui pones la url de una pool [ENTER]
    aqui pones tu wallet [ENTER]
    x [ENTER]
    [ENTER]
    n [ENTER]
    n [ENTER]
    n [ENTER]
	
//Para cerrar sin parar el minero
(abrir otro terminal/consola)
sudo su
tmux detach
	
//Para ver el minero
sudo su
tmux attach -t XMRSTAKSPA
	
//Para matar el minero
sudo su
tmux kill-session -t XMRSTAKSPA
```

## Donaciones
BITCOIN:
```
1588JY8nzjyXBgECbSSkmyfXkRSNMMckh9
```

TURTLECOIN:
```
TRTLv2EiqzvELTNvJmf5asJ4w2jEgHiuqY38fkigHtHKddnwzBbQiDg1B7ssz5wWnrJzKJwA5pFqJCnSZF2di2cBNpqAsjVjAuj
```

WORKTIPS:
```
WtipUwCGMLSKMDqGrGPu4zHWnycn71vCm3rV3YReLT2QK77cKu97T3f9FkS2dNL4Lsh7M6ZptT1iHauM7Fxt9SfC7mWh5SdzeH
```

DOGECOIN:
```
DEeQNjZgCV2tpKJGFvDJSTZ7xRhYUqc4uB
```
