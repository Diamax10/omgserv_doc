---
description: >-
  There are plenty of tutorials on the Internet to install Java on a Linux
  system but here we gather them all.
---

# Install Java on your VPS

## Introduction

Java is not necessarily installed by default on Linux systems, to check this just run the command `java -version` if Java is not installed the system will tell you something like `java: command not found` otherwise it will show you the version installed and use by default. For example Java 8 will be noted `1.8.0`, Java 11 `1.11.0` or `11.0`, etc.

## Installation

### Java 8 \(up to Minecraft 1.16\)

{% tabs %}
{% tab title="Debian 9" %}
```bash
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}

{% tab title="Debian 10" %}
```bash
sudo apt update &&
sudo apt install -y apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common &&
wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | sudo apt-key add - &&
sudo add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/ &&
sudo apt update && sudo apt install adoptopenjdk-8-hotspot
```
{% endtab %}

{% tab title="Ubuntu 18.04 & 20.04" %}
```bash
sudo apt update && sudo apt install openjdk-8-jre
```
{% endtab %}
{% endtabs %}

### Java 11 \(since Minecraft 1.17\)

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

