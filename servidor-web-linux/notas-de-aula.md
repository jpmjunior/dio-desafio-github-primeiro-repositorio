# Servidor Web no Linux
Instalação do servidor web Apache no Ubuntu.  

## Instação
```bash
sudo apt install apache2
```
## Configuração
Editar arquivo da página inicial:
```bash
sudo nano /var/www/html/index.html
```
Exibe status do servidor.
```bash
sudo systemctl status apache2
```
Obs. 1: O parâmetro `status` do comando `systemctl` pode ser substituído por `[start|stop|restart]`, consulte o `--help` para mais detalhes.

Obs. 2: Para acessar a página inicial digite o ip do servidor em seu browser, você pode verificar o ip com o comando `ip a` ou `ifconfig`.
Caso esteja usando o browser do próprio servidor acesso com `localhost` ou `127.0.0.1`. Lembrando que para acessar de outra máquina, esta 
deve estar na mesma rede do servidor.
