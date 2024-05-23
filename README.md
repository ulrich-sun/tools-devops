
## Tools DevOps

Dans ce depot Github Je rassemble l'ensemble des Tools que j'utilise au quotidien

NB: Je Travaille dans un environnement Linux et a cette date , je travaillais sur Ubuntu version 22.04 LTS

## 
---------------
**Prenom:** Ulrich Steve

**Nom**: NOUMSI

**Linkedin:** https://www.linkedin.com/in/ulrich-steve-noumsi/ 

---------------
## Kubens & Kubectl
```bash
curl -sS https://webi.sh/kubens | sh
curl -sS https://webi.sh/kubectx | sh
```

## Install Precommit tools
```bash
sudo apt update
sudo apt install python3 python3-pip
pip install pre-commit

```
## Packer
For Packer installation refers here: [Packer Website Installation](https://developer.hashicorp.com/packer/tutorials/docker-get-started/get-started-install-cli)
Choose your Os Distribution and Get Started the Installation 

if your OS it's Ubuntu don't forget to update the operating system
and add this : because we have some issues like this "sudo: apt-add-repository: command not found"
```bash
sudo apt-get install software-properties-common
```

## Docker
```bash
sudo apt update 
curl -fsSL https://get.docker.com -o install-docker.sh
 sudo sh install-docker.sh
```
## Terraform
J'installe la ligne de commande terraform
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update
sudo apt install terraform -y
terraform version
```
## Terrascan
```bash 
curl -L "$(curl -s https://api.github.com/repos/tenable/terrascan/releases/latest | grep -o -E "https://.+?_Darwin_x86_64.tar.gz")" > terrascan.tar.gz
tar -xf terrascan.tar.gz terrascan && rm terrascan.tar.gz
install terrascan /usr/local/bin && rm terrascan
```
Si cette option ne fonctionne pas vous pouvez utiliser pip
```bash 
pip install terrascan
```
## Install aws cli
```bash 
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
## TfSec

```bash 
curl -s https://raw.githubusercontent.com/aquasecurity/tfsec/master/scripts/install_linux.sh | bash
```

## Checkov
```bash 
pip3 install checkov
```

# Generer un graph

```bash
sudo apt install graphviz -y 
terraform graph > terraform.dot
dot -Tpng terraform.dot -o terraform.png
```