```    ____                    __  __           __      
   / __ \(⌐■_■)__________  / / / /___ ______/ /_ 
  / / / / / ___/ ___/ __ \/ /_/ / __ `/ ___/ __ \
 / /_/ / (__  ) /__/ /_/ / __  / /_/ (__  ) / / /
/_____/_/____/\___/\____/_/ /_/\__,_/____/_/ /_/  -v2 (Im too lazy to style the v2 prolerly
```
An updated and (hopefully) working version for jay's version of pwnagotchi.

### >: Wat it do (◕‿‿◕)??????????
It's made for [Pwnagotchi](https://pwnagotchi.ai/) (duh)
This is an updated version of [DiscoHash](https://github.com/flamebarke/DiscoHash)
It gets ur handshakes and when one is captured, it sends a message via a discord webhook.
It probably works with GPS but I dont have one yet so I cannot test it out.
Within the bot folder there is a Discord Bot that will scrape all captured hashes from the discord server and return them in a text file. This is not required for the plugin, but it makes it easier to pull large amounts of hashes quickly. You can modify the discord bot to only pull hashes from within a certain date range etc.


### >: Installation:
```
sudo su
apt-get update
apt-get install libcurl4-openssl-dev libssl-dev zlib1g-dev
```

- [X] Create a new Discord server and set up a new [web hook](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).
- [X] Copy discohashv2.py from this repo to /usr/local/share/pwnagotchi/custom-plugins/ (if the directory doesn't exist create it)

```
cd /usr/local/share/pwnagotchi/installed-plugins
sudo wget https://raw.githubusercontent.com/Rastizakia/discohash-v2/main/discohashv2.py
```

```
main.plugins.discohash.enabled = true
main.plugins.discohash.webhook_url = "YOUR WEB HOOK URL"
```

### >: Usage:
```
Reboot the pwnagotchi and it should work if you tether via bluetooth with your phone for internet access.
```

### >: Notes (◕‿‿◕):

This is not the original project as I have said. The original is at https://github.com/flamebarke/DiscoHash.
DiscoHash checks for new pcap files at the end of each epoch so they will come fairly frequently. To reduce this interval modify the code to use a different callback. 
To check out how to make plugins for Pwnagotchi check the docs [here](https://pwnagotchi.ai/plugins/#developing-your-own-plugin).

You can contact me by sending my Pwnagotchi some PwnMail at:

`fe15a54c000428cd8b88e4b689552379bbfb5b838caf52412690749cd2d105f0`
Or you can message me on Discord:
rashtiz
Please give info on whether this actually works lol, this is my first project intended for use of other people :3.
