# Gentoo building instructions

## Install

1. sudo layman -o https://raw.github.com/ddorian1/gentoo-commentchain-overlay/master/gentoo-commentchain-overlay.xml -a commentchain
1. sudo emerge -av commentchain

## Configuration & web gui

1. mkdir ~/.commentchain
1. echo -e "rpcuser=user\nrpcpassword=pwd" > ~/.commentchain/commentchain.conf
1. chmod 600 ~/.commentchain/commentchain.conf
1. git clone https://github.com/miguelfreitas/commentchain-html.git ~/.commentchain/html

## Start

1. commentchaind -rpcuser=user -rpcpassword=pwd
1. Open http://127.0.0.1:28332/index.html and use the user/pwd credentials
1. Create your account !
