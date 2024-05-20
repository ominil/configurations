# Configuration for developement environment

- OS: Ubuntu 24.04


## BeforeAll

Run the following command to update the store:

```shell
sudo apt update
```


## Editors

Install vim:
```shell
sudo apt update && sudo apt install -y vim
```

## Bash Completition

Install bash completition:
```shell
sudo apt update && sudo apt install -y bash-completion
```

In the next sections are present the commands to activate the competion.


## Git

Install git:
```shell
sudo apt update && sudo apt install -y git-all
```

Activate bash-completion:

```shell
echo "source /usr/share/bash-completion/completions/git" >> ~/.bashrc
source ~/.bashrc
```


Create an ssh key to connect with GIT:

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"

eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519
```

Copy the public key and add it to the git client you are using, i.e. Github.


## Java

To install the default version of Java:
```shell
sudo apt update && sudo apt-get install default-jdk
```

Verify the installation:
```shell
java -version
```

Activate bash-completion:
```shell
echo "source /usr/share/bash-completion/completions/javac" >> ~/.bashrc
echo "source /usr/share/bash-completion/completions/java" >> ~/.bashrc

source ~/.bashrc
```


## Maven

Install maven:
```shell
sudo apt update && sudo apt-get -y install maven
```

Verify the installation:
```shell
mvn -version
```

Activate bash-completion:
```shell
echo "source /usr/share/bash-completion/completions/mvn" >> ~/.bashrc
source ~/.bashrc
```


## Docker

To install docker with apt you need to set up the docker repositoty:
```shell
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

Install Docker:
```shell
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Verify docker installation:
```shell
sudo docker run hello-world
```

Activate bash-completion:
```shell
echo "source /usr/share/bash-completion/completions/docker" >> ~/.bashrc
source ~/.bashrc
```



## Kubernetes




