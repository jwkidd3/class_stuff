sudo apt-get update  
sudo apt-get -y upgrade

sudo rm /usr/bin/go

wget https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz

sudo tar -xvf go1.20.5.linux-amd64.tar.gz   

sudo mv go /usr/local  

cd ~

vi .profile

#add the following

GOROOT=/usr/local/go

PATH=$GOPATH/bin:$GOROOT/bin:/home/ubuntu/go/bin:$PATH


****Close and save the .profile file and then execute

go install sigs.k8s.io/kind@v0.20.0

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
