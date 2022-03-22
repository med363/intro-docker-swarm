### nb:conteneur appeler service dans docker swarm
### 1.change le nom de votre machine entre dans le fichier etc/hosts et dans le fichier /etc/hostname 
```bash
sudo nano /etc/hosts
```
```bash
sudo /etc/hostname
```
### 2.installer le git
```bash
sudo apt install git
```
### 3.il faut docker est installer
```bash
sudo apt  install docker.io
```
### 4.ajouter l'utilisateur courant au group docker pour n'utilise pas toujours sudo
```bash
sudo usermod -aG docker $USER
```
### 5.Initialiser cluster dockerSwarm dans le master-node et verifier leur output
```bash
docker swar init
```
### 6.visualise les nodes votre cluster 
```bash
docker node ls
```
### 7.clone repo git contant docker compose oriente swarm
```bash
sudo git clone https://github.com/med363/example-voting-app.git
cd example-voting-app
```

### 8.Maintenant on va deploye mon stack
### la commande se compose ->docker deploy -c [fichier de deployement] [nom de mon pile]
```bash
docker stack deploy -c docker-stack.yml monstack
```
### 9.voir mon stack et le service visulizer permet de visualizer mon cluster UI
```bash
docker stack ls
```
### pour bien visualiser chaque sur quellee node s'exxecuter
```bash
docker stack ps monstack
```
