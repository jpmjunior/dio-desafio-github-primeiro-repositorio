# Servidor de arquivos com Linux

Instalação e configuração do servidor de arquivos SAMBA no Ubuntu

## Instalação
Comando para instalar o pacote samba:
```bash
sudo apt install samba -y
```

## Configuração
Editar arquivo de configuração:
```bash
sudo nano /etc/samba/smb.conf
```
Habilita a inicialização automática:
```bash
sudo systemctl enable smbd
```
Reinicia o SAMBA
```bash
sudo systemctl restart smbd
```
Retorna status do servidor SAMBA
```bash
sudo systemctl status smbd
```
## Exemplo
Adicione estas linhas ao final no arquivo de configuração para configurar uma pasta de acesso público.  
Obs.: A pasta deve existir no path indicado.  

> [publica]  
>   
> path = /publica  
> writable = yes  
> guest ok = yes  
> guest only = yes  

Para que as alterações sejam efetivadas é necessário reiniciar o SAMBA com o seguinte comando:  
```bash
sudo systemctl restart smbd
```
