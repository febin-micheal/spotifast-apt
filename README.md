# spotifast-apt

Unofficial apt repository for [Spotifast](https://github.com/crmne/spotifast) on Ubuntu 22.04 and newer (amd64).

Upstream's packages need Ubuntu 24.04. This repo builds the same release tags from source on Ubuntu 22.04 every week and publishes a signed apt repository. Not affiliated with Spotify or the Spotifast author. Spotifast is MIT licensed.

## Install

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://febin-micheal.github.io/spotifast-apt/key.gpg -o /etc/apt/keyrings/spotifast-apt.gpg
echo "deb [signed-by=/etc/apt/keyrings/spotifast-apt.gpg] https://febin-micheal.github.io/spotifast-apt stable main" | sudo tee /etc/apt/sources.list.d/spotifast-apt.list
sudo apt update && sudo apt install spotifast
```

Updates arrive through the normal `sudo apt upgrade`.
