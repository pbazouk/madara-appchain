
#ubuntu 20.04

#2cpu 4gb ram

sudo apt update

sudo apt upgrade



#install git

sudo add-apt-repository ppa:git-core/ppa

sudo apt update

sudo apt install git

sudo apt-get install build-essential libssl-dev libghc-zlib-dev libcurl4-gnutls-dev libexpat1-dev gettext unzip

wget https://github.com/git/git/archive/v2.34.1.zip -O git-2.34.1.zip

git clone --branch v2.34.1 https://github.com/git/git.git

git --version



#print

#"git version 2.43.0" is ok too.



#install rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

#proceed 1

source "$HOME/.cargo/env"

rustc --version

#print

#rustc 1.75.0 (82e1608df 2023-12-21)


#ubuntu

sudo apt install build-essential

sudo apt install pkg-config

sudo apt install libssl-dev

sudo apt install clang

sudo apt install protobuf-compiler



#clone repo

git clone https://github.com/karnotxyz/madara-cli


#build repo

cd madara-cli

cargo build --release

#initialize a new appchain

./target/release/madara init

#name: "your node name"

#mode: "sovereign"

#da layer: "avail"


#run your appchain

./target/release/madara run



