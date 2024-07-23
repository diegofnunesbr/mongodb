# MongoDB

### Instalar o MongoDB no Kubernetes:

- `git clone git@github.com:diegofnunesbr/mongodb.git`
- `cd mongodb`
- `helm install --create-namespace mongodb -n mongodb .`

### Configurar o MongoDB no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') mongodb.local"`

### Remover o MongoDB no Kubernetes:

- `helm uninstall mongodb -n mongodb`
