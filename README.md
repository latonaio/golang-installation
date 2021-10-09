## golang-installation
LatonaおよびAIONでは、より先進的で安定的なエッジコンピューティング環境を管理維持するために、コアのランタイム環境として、Golangを採用しています。    
ここでは、Golangのエッジ環境へのインストール手順を説明します。

## 前提条件
・ARM / AMD / Intel  
・LinuxOS  
・AION / Kubernetes    
   
## Golangをインストールする   
以下の手順でGolangをインストールします。   


##### サンプルのAnsible / go-install.yaml(jetson-aion-ansible-unification/roles/common/tasks/go-install.yaml、jetson-aion-ansible-unification/roles/common/vars/go-install.yaml)
```
- name: go-install vars
  include_vars: go-install.yaml
  
- name: git clone goenv
  git:
    repo: https://github.com/syndbg/goenv.git
    dest: "/home/{{ user_name }}/{{ goenv_path }}"  
```

##### サンプルのAnsible(main.yaml内)記述(jetson-aion-ansible-unification/roles/common/tasks/main.yaml内)
```
- include: go-install.yaml
```

#### Golangとは
Googleによって開発されたオープンソースのプログラミング言語です。