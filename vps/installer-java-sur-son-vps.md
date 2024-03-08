---
description: >-
  Il existe pleins de tutoriels sur Internet pour installer Java sur un système
  Linux mais ici nous les rassemblons tous.
---

# Installer Java sur son VPS

### Introduction

Java n'est pas forcément installé par défaut sur les système Linux, pour vérifier cela il suffit d'exécuter la commande `java -version` si Java n'est installé le système vous dira quelque chose du style `java: command not found` sinon il vous affichera la version installée et utilisée par défaut. Par exemple Java 8 sera noté `1.8.0`, Java 11 `1.11.0` ou `11.0`, etc.

## Installation

### Java 8 (jusqu'à Minecraft 1.16)

{% tabs %}
{% tab title="Debian 9" %}
```bash
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}

{% tab title="Debian 10 & 11" %}
```bash
apt install -y wget apt-transport-https gpg

wget -qO - https://packages.adoptium.net/artifactory/api/gpg/key/public | gpg --dearmor | tee /etc/apt/trusted.gpg.d/adoptium.gpg > /dev/null

echo "deb https://packages.adoptium.net/artifactory/deb $(awk -F= '/^VERSION_CODENAME/{print$2}' /etc/os-release) main" | tee /etc/apt/sources.list.d/adoptium.list

apt update

apt install temurin-8-jre
```
{% endtab %}

{% tab title="Ubuntu 18.04 & 20.04" %}
```bash
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}
{% endtabs %}

### Java 11

{% tabs %}
{% tab title="Debian 9 & 10" %}
```bash
sudo apt update && sudo apt install openjdk-11-jre
```
{% endtab %}

{% tab title="Ubuntu 18.04 & 20.04" %}
```bash
sudo apt update && sudo apt install openjdk-11-jre
```
{% endtab %}
{% endtabs %}

### Java 16 (à partir de Minecraft 1.17)

{% tabs %}
{% tab title="Debian 9" %}
```bash
sudo apt install -y wget apt-transport-https gnupg && 
curl https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public --output adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --import adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --export --output adoptopenjdk-archive-keyring.gpg && 
rm adoptopenjdk-keyring.gpg adoptopenjdk.gpg &&
sudo mv adoptopenjdk-archive-keyring.gpg /usr/share/keyrings &&
echo "deb [signed-by=/usr/share/keyrings/adoptopenjdk-archive-keyring.gpg] https://adoptopenjdk.jfrog.io/adoptopenjdk/deb stretch main" | sudo tee /etc/apt/sources.list.d/adoptopenjdk.list &&
sudo apt update &&
sudo apt install adoptopenjdk-16-openj9-jre
```
{% endtab %}

{% tab title="Debian 10" %}
```bash
sudo apt install -y wget apt-transport-https gnupg && 
curl https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public --output adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --import adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --export --output adoptopenjdk-archive-keyring.gpg && 
rm adoptopenjdk-keyring.gpg adoptopenjdk.gpg &&
sudo mv adoptopenjdk-archive-keyring.gpg /usr/share/keyrings &&
echo "deb [signed-by=/usr/share/keyrings/adoptopenjdk-archive-keyring.gpg] https://adoptopenjdk.jfrog.io/adoptopenjdk/deb buster main" | sudo tee /etc/apt/sources.list.d/adoptopenjdk.list &&
sudo apt update &&
sudo apt install adoptopenjdk-16-openj9-jre
```
{% endtab %}

{% tab title="Ubuntu 18.04" %}
```bash
sudo apt install -y wget apt-transport-https gnupg && 
curl https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public --output adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --import adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --export --output adoptopenjdk-archive-keyring.gpg && 
rm adoptopenjdk-keyring.gpg adoptopenjdk.gpg &&
sudo mv adoptopenjdk-archive-keyring.gpg /usr/share/keyrings &&
echo "deb [signed-by=/usr/share/keyrings/adoptopenjdk-archive-keyring.gpg] https://adoptopenjdk.jfrog.io/adoptopenjdk/deb bionic main" | sudo tee /etc/apt/sources.list.d/adoptopenjdk.list &&
sudo apt update &&
sudo apt install adoptopenjdk-16-openj9-jre
```
{% endtab %}

{% tab title="Ubuntu 20.04" %}
```bash
sudo apt install -y wget apt-transport-https gnupg && 
curl https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public --output adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --import adoptopenjdk.gpg &&
gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --export --output adoptopenjdk-archive-keyring.gpg && 
rm adoptopenjdk-keyring.gpg adoptopenjdk.gpg &&
sudo mv adoptopenjdk-archive-keyring.gpg /usr/share/keyrings &&
echo "deb [signed-by=/usr/share/keyrings/adoptopenjdk-archive-keyring.gpg] https://adoptopenjdk.jfrog.io/adoptopenjdk/deb focal main" | sudo tee /etc/apt/sources.list.d/adoptopenjdk.list &&
sudo apt update &&
sudo apt install adoptopenjdk-16-openj9-jre
```
{% endtab %}
{% endtabs %}

### Java 17 (à partir de Minecraft 1.18)

{% tabs %}
{% tab title="Debian 9 & 10" %}
```bash
sudo apt update &&
sudo apt install -y apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common &&
sudo add-apt-repository --yes ppa:linuxuprising/java &&
sudo apt update && 
sudo echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/linuxuprising-java.list &&
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A &&
sudo apt-get update &&
sudo apt install oracle-java17-installer --install-recommends
```
{% endtab %}

{% tab title="Debian 11" %}
```bash
sudo apt update && sudo apt install openjdk-17-jre
```
{% endtab %}

{% tab title="Ubuntu" %}
```bash
sudo apt update &&
sudo apt install -y apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common &&
sudo add-apt-repository --yes ppa:linuxuprising/java &&
sudo apt update && 
sudo echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/linuxuprising-java.list &&
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A &&
sudo apt-get update &&
sudo apt install oracle-java17-installer --install-recommends
```
{% endtab %}
{% endtabs %}

