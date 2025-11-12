
![gradinet first](https://github.com/user-attachments/assets/390670b5-12e9-416f-a421-ee85e32be013)



first you need gpu you can get [vast.ai] (https://cloud.vast.ai/?ref_id=345155)

===========================================================================

## 💻 System Requirements

 | Requirement                        | Details                                                                                      |
 |-------------------------------------|---------------------------------------------------------------------------------------------|
 | **CUDA Devices (Recommended)**      | `RTX 3090`, `RTX 4090`, `A100`, `H100`                                                      |
 | **minimum**                         | + 8 GB                                                                                      |

===========================================================================


1 - open powershell on windows

2 -  

```bash
ssh-keygen -t rsa 
```

3 - press enter to save the file 

4 - copy your public key ( SSH )

Replace Your Address
```bash
Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub" | Set-Clipboard
```

5 - go back to the website and define ssh key for your servers

6 - get your private key on your windows powershell 

Replace Your Address
```bash
Get-Content "$env:USERPROFILE\.ssh\id_rsa" | Set-Clipboard
```

7 - go to termius and set a keychain with your private and public key

8 - right now add a new host with ip and port ( your provider will give you )

Done 


===========================================================================


# 2) Install Dependencies :

```
 sudo apt update && sudo apt upgrade -y
```

```
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

```
sudo apt install python3.11 python3.11-venv python3.11-dev -y
```

```
sudo apt update
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo bash -
sudo apt install -y nodejs
node -v
npm install -g yarn
yarn -v
```


```
curl -o- -L https://yarnpkg.com/install.sh | bash
```

```
export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"
```

```
source ~/.bashrc
```

 install docker [docker](https://github.com/0xmoei/Linux_Node_Guide/blob/main/linux-config.md#docker-docker-compose)

===========================================================================

# 3) install & run  parallax :

```sh
git clone https://github.com/GradientHQ/parallax.git
cd parallax
```


```
docker pull gradientservice/parallax:latest-hopper
```

```
screen -S run
```
```
docker run -it --gpus all --network host gradientservice/parallax:latest-hopper bash
```

```
parallax run
```
wiat for show open `localhost:3000` 

after see this open powershell on windows and use this command:

`use your ip and port `

```
 ssh -i "$env:USERPROFILE\.ssh\id_rsa.pub" -N -L 3000:localhost:3000 -p <port> root@<ipserver>
```

creat seconde screen :

```
screen -S join
```
```
parallax join
```



