
## Tools DevOps

Dans ce depot Github Je rassemble l'ensemble des Tools que j'utilise au quotidien

NB: Je Travaille dans un environnement Linux et a cette date , je travaillais sur Ubuntu version 22.04 LTS

## 
---------------
****Prenom:**** Ulrich

****Nom***: NOUMSI

****Linkedin:**** https://www.linkedin.com/in/ulrich-steve-noumsi/ 
---------------

## Terraform
J'installe la ligne de commande terraform
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
$ echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
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

## TfSec

```bash 
curl -s https://raw.githubusercontent.com/aquasecurity/tfsec/master/scripts/install_linux.sh | bash
```

## Checkov
```bash 
pip3 install checkov
```
