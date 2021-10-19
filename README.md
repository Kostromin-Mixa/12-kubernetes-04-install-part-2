# Домашнее задание к занятию "12.4 Развертывание кластера на собственных серверах, лекция 2"   
Кластер запускался на Ubuntu с 3-мя нодами, 1-мастер и 2-рабочие ноды.   
hosts.yaml файл готовился с помощью билдера:  
__declare -a IPS=(192.168.1.120 192.168.1.121 192.168.1.122)__  
__CONFIG_FILE=inventory/mycluster/hosts.yaml python3 contrib/inventory_builder/inventory.py ${IPS[@]}__  
![2021-10-19_19-40-35](https://user-images.githubusercontent.com/78191008/137933392-a10b4144-e636-4bc7-ab5a-aa94dab3bc87.png)  
в качестве CRI — containerd : прописал "container_manager: containerd" в файле k8s-cluster.yml  
Проверка установки:  
![11](https://user-images.githubusercontent.com/78191008/137933917-68433ffb-c420-4d37-ae5a-10c457f4d9a7.png)  

![2021-10-19_20-11-52](https://user-images.githubusercontent.com/78191008/137939542-ee99c640-5f93-442a-a9ae-97d877be2cd3.png)

![2021-10-19_19-26-56](https://user-images.githubusercontent.com/78191008/137933806-09dc7a53-7571-468b-a39d-7f046fd3574c.png)  

![2021-10-19_20-14-13](https://user-images.githubusercontent.com/78191008/137939930-5fbcb164-b6f2-472d-b6bd-d859ea3c0990.png)

![33](https://user-images.githubusercontent.com/78191008/137940143-b49c68f5-6d8f-4d54-8bc1-2174a0c63d22.png)
