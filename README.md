[Lavalink]: https://github.com/freyacodes/Lavalink
[Lavaplayer]: https://github.com/sedmelluq/lavaplayer
[Documentation]: https://lavalink.readthedocs.io/en/master/
[Latest Docs]: https://lavalink.readthedocs.io/en/latest/

<img align="right" src="https://serux.pro/9e83af1581.png" height="150" width="150">

# Lavalink.py
[![Python](https://img.shields.io/badge/Python-3.5%20%7C%203.6%20%7C%203.7%20%7C%203.8%20%7C%203.9%20%7C%203.10-blue.svg)](https://www.python.org) [![Build Status](https://travis-ci.com/devoxin/Lavalink.py.svg?branch=master)](https://travis-ci.com/Devoxin/Lavalink.py) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/428eebed5a2e467fb038eacfa1d92e62)](https://www.codacy.com/gh/Devoxin/Lavalink.py/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Devoxin/Lavalink.py&amp;utm_campaign=Badge_Grade) [![License](https://img.shields.io/github/license/Devoxin/Lavalink.py.svg)](LICENSE) [![Documentation Status](https://readthedocs.org/projects/lavalink/badge/?version=latest)](https://lavalink.readthedocs.io/en/latest/?badge=latest)

Lavalink.py is a wrapper for [Lavalink] which abstracts away most of the code necessary to use Lavalink, allowing for easier integration into your projects, while still promising full API coverage and powerful tools to get the most out of it.

## Features
- Regions
- Multi-Node Support
- Load Balancing (this includes region-based load balancing)
- Audio Filters
- [Custom Sources](examples/custom_source.py)


# What is Lavalink?
Lavalink is standalone audio sending software capable of transmitting audio to Discord, utilising [Lavaplayer] for audio transcoding. It can be configured to work independently, or as part of a cluster depending on needs, which allows it to be highly scalable and performant. Head over to the [Lavalink] repository to find out more.


# Getting Started
First you need to run a command to install the library,
```shell
pip install lavalink
```

Then you need to setup the Lavalink server, you will need to install Java, and then download the latest [Lavalink.jar](https://github.com/freyacodes/Lavalink/releases/).
Then place an ``application.yml`` file in the same directory. The file should look like [this](https://github.com/freyacodes/Lavalink/blob/master/LavalinkServer/application.yml.example/). Finally run `java -jar Lavalink.jar` in the directory of the jar.

Additionally, there is an [example cog](examples). It should be noted that the example cog is oriented towards usage with Discord.py rewrite and Lavalink v3.1+, although backwards
compatibility may be possible, it's not encouraged nor is support guaranteed.

## Custom Sources
As of Lavalink.py 4.0, custom sources can be registered to a client instance to allow searching more audio sources. These aren't "true" sources in the sense that you can play from them (unless you support HTTP playback and are able to retrieve a playable HTTP URL).
This means you can build sources that allow retrieving track metadata from third party services, such as Spotify, whilst the underlying stream is played from elsewhere. This is a popular method for providing support for otherwise unsupported services. You can find an [example source here](examples/custom_source.py).

## Supported Platforms
While Lavalink.py supports any platform Python will run on, the same can not be said for the Lavalink server.
The Lavalink server requires an x86-64 (64-bit) machine running either Windows, or any Linux-based distro.
It is highly recommended that you invest in a dedicated server or a [VPS](https://en.wikipedia.org/wiki/Virtual_private_server). "Hosts" like Glitch, Heroku, etc... are not guaranteed to work with Lavalink, therefore you should try to avoid them. Support will not be offered should you choose to try and host Lavalink on these platforms.

### Exceptions
The exception to the "unsupported platforms" rule are ARM-based machines, for example; a Raspberry Pi. While official Lavalink builds do not support the ARM architecture, there are [custom builds by Cog-Creators](https://github.com/Cog-Creators/Lavalink-Jars/releases) that offer ARM support. These are the official builds, with additional native libraries for running on otherwise unsupported platforms.

## Need Further Help?
[Discord Server](https://discord.gg/SbJXU9s)

[Documentation] or [Latest Docs]
