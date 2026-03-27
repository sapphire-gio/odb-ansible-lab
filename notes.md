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

## List Dynamic Inventory
```
ansible-inventory -i inventory.azure_rm.yml --list --yaml
 
```
after adding inventory = inventory.azure_rm.yml to ansible.cfg simpler command can be used > ansible-inventory --list --yaml
basically no longer have to use -i for inventory command 

auth_source: msi in invebtory.azure_rm.yml means managed system identity to auth with api
idenitity is user assigned attached to container and has reader access on the subscription

## Ping Linux Host
```
ansible -i inventory.yml -m ping all
ansible -m ping all
```


