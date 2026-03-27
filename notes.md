## Prepare Environment
```
git init
- manage unsafe repositories
git config --global user.email "gianni.rubio@sapphirehealth.org"
git config --global user.name "sapphire-gio"

add .env to .gitignore

source ~/venv/azure/bin/activate
export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
```
## ansible env init
```
 . .env
 ```

## List Static Inventory
```
ansible-inventory -i inventory.yml --list --yaml
```


## Ping Linux Host
```
ansible -i inventory.yml -m ping all
```


