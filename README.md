# How To Use  

#### On Local Machine  

* First, install Vagrant and VirtualBox on your machine  

    git clone https://github.com/varmil/vagrant.git
    cd vagrant
    vagrant up
    vagrant ssh-config node1 > ssh_config
    vagrant ssh-config node2 >> ssh_config
    scp -F ssh_config ~/.vagrant.d/insecure_private_key node1:.ssh/id_rsa
> 起動後、Ansible で node1 から node2 へ ssh するため、Vagrant 用の秘密鍵をコピーする


#### On Remote Machine(192.168.33.11)
    ssh vagrant@192.168.33.11
    yum install ansible
    git clone https://github.com/varmil/ansible.git
    cd ansible
    ansible-playbook -i test-servers site.yml


#### On Remote Machine(192.168.33.12)

* This is for development. You use this.
