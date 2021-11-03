# Script de Instalaçaõ do Arch Linux
Antes de roda os script é necessario executar algum passos básicos
- 1º Crie uma partição de EFI com o cfdisk
- 2º Formate a partição com:
```sh
mkfs.fat /dev/sdxy
```
- 3º Após rodar o _pacstrap_, monte no diretorio /mnt/boot/efi simplesmente executando:
```sh
mkdir /mnt/boot/efi; mount /dev/sdxy /mnt/boot/efi
```
- 4º Crie um arquivo fstab com o comando:
```sh
genfstab -U /mnt >> /mnt/etc/fstab
```
- 5º Mude o root para o mnt
- 6º Clone esse repositorio e entre na pasta dele
- 7º rode o seguinte comando para dar a permisão e rodar o script:
```sh
chmod 775 arch.sh; ./arch.sh
```
