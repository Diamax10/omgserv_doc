---
description: >-
  In this tutorial we will see how to use Openmod to install a forge version
  superior to the 1.16 not available in auto install
---

# Installation of Forge 1.17+ via Openmod

{% hint style="info" %}
To install a Forge version inferior to 1.17 please follow [this tutorial](installation-de-forge-via-openmod.md)
{% endhint %}

{% hint style="danger" %}
**Do a server save before reading this tutorial** if you'd like to keep files from your actual server we made a tutorial [here.](../omgserv/sauvegarde-et-restauration.md#make-a-backup)
{% endhint %}

### **Installation (Starting from 1.17)**

* Download on [the Forge website](https://files.minecraftforge.net/net/minecraftforge/forge/) the Forge version needed (example: 1.18.2-40.1.60).
* Do a reinstallation of the server in the "Reinstallation" tab then select "Openmod Forge 1.17+".
* Drag the previously downloaded `.jar`.
* Then click on "install with Openmod".
* Select the previously downloaded `.jar` and click on "Continue".
* After a short installation, your server is installed.

### **Configuration**

* Verify the Java version in the **properties** tab of your panel.
  * For the 1.17 select **Java 16**.
  * For the 1.18+ select **Java 17**.
* Wait for the server to completelly start up (see console if needed) then shut it off.
* Connect to the FTP on the server using a FTP client like [FileZilla (tutorial)](../omgserv/connect-to-ftp.md) (or with the web ftp but it is unadvised due to many bugs).
* Drag your mods in the mods folder, including the configuration if there is one.
* Erase the wolrd folder to reset the map (⚠️ This will have the consequence to erase everything on your world, remember to keep a save of your world if you'd like to keep it).
* Finally, you can start your server and if everything was done correctly (mods compatibles between them, every files present and good Forge version) normally you should have your Minecraft server with your mods.
