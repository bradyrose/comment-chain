# Ubuntu / Debian building instructions

Tested on a pristine:
 - Ubuntu 13.10 amd64

## Install

1. sudo apt-get update
1. sudo apt-get install git autoconf libtool build-essential libboost-all-dev libssl-dev libdb++-dev libminiupnpc-dev
1. git clone https://github.com/miguelfreitas/commentchain-core.git
1. cd commentchain-core
1. ./autotool.sh
1. ./configure
1. make

## Configuration & web gui

1. mkdir ~/.commentchain
1. echo -e "rpcuser=user\nrpcpassword=pwd" > ~/.commentchain/commentchain.conf
1. chmod 600 ~/.commentchain/commentchain.conf
1. git clone https://github.com/miguelfreitas/commentchain-html.git ~/.commentchain/html

## Start

1. cd commentchain-core
1. ./commentchaind -rpcuser=user -rpcpassword=pwd -rpcallowip=127.0.0.1
1. Open http://127.0.0.1:28332/index.html and use the user/pwd credentials
1. Create your account !
