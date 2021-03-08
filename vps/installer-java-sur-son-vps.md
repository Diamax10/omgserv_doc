---
description: >-
  Il existe pleins de tutoriels sur Internet pour installer Java sur un système
  Linux mais ici nous les rassemblons tous.
---

# Installer Java sur son VPS

### Introduction

Java n'est pas forcément installé par défaut sur les système Linux, pour vérifier cela il suffit d'exécuter la commande `java -version` si Java n'est installé le système vous dira quelque chose du style `java: command not found` sinon il vous affichera la version installée et utiliser par défaut. Par exemple Java 8 sera noté `1.8.0`, Java 11 `1.11.0` ou `11.0`, etc.

## Installation

### Java 8 \(jusqu'à Minecraft 1.16\)

{% tabs %}
{% tab title="Debian 9" %}
```text
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}

{% tab title="Debian 10" %}
```text
sudo apt update &&
sudo apt install -y apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common &&
wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | sudo apt-key add - &&
sudo add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/ &&
sudo apt update && sudo apt install adoptopenjdk-8-hotspot
```
{% endtab %}

{% tab title="Ubuntu 18.04 & 20.04" %}
```text
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}
{% endtabs %}

### Java 11 \(à partir de Minecraft 1.17\)

{% tabs %}
{% tab title="Debian 9 & 10" %}
```
sudo apt update && sudo apt install openjdk-11-jre
```
{% endtab %}

{% tab title="Ubuntu 18.04 & 20.04" %}
```
sudo apt update && sudo apt install openjdk-11-jre
```
{% endtab %}
{% endtabs %}

