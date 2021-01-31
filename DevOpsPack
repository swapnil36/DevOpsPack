#!/bin/bash

RED='\033[0;31m'
BLUE='\033[40;38;5;82m'
PURPLE='\033[0;35m'

echo "
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
||D||E||V||O||P||S||P||A||C||K||
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
"
checkOS () {
    unameOut="$(uname -s)"
    case "${unameOut}" in
        Linux*)     machine=Linux;;
        Darwin*)    machine=Mac;;
        *)          machine="UNKNOWN:${unameOut}"
    esac
}
checkOS
if [ ! -x "$(command -v vagrant)" ]; then
    
    if [ "$machine" == "Mac" ]; then
        echo -e "${PURPLE} Installing Vagrant Please Wait ..."
        sleep 1
        brew cask install vagrant
        echo -e " ${PURPLE} Vagrant Has Been Installed Successfully !"
        elif [ "$machine" == "Linux" ]; then
        echo -e "${PURPLE} Installing Vagrant... \e[0m "
        sleep 1
        sudo apt-get update -y
        sudo apt-get install vagrant -y
        echo -e " ${PURPLE} Vagrant Has Been installed! \e[0m "
        
    else
        echo -e " ${PURPLE} Vagrant Has Been Already Installed."
    fi
fi

if [ ! -x "$(command -v virtualbox)" ];
then
    
    if [ "$machine" == "Mac" ]; then
        echo -e "${PURPLE} Installing VirtualBox..."
        sleep 1
        brew cask install virtualbox
        echo -e " ${PURPLE} Virtualbox Has Been Installed!"
        elif [ "$machine" == "Linux" ]; then
        echo -e "${PURPLE} Installing VirtualBox... \e[0m"
        sleep 1
        sudo apt-get update -y
        sudo apt-get install virtualbox -y
        echo -e " ${PURPLE} Virtualbox Has Been Installed Successfully ! \e[0m "
    else
        echo -e " ${PURPLE} Vagrant Has Been Already Installed!"
    fi
fi

if [ -x "$(command -v vagrant)" ] && [ -x "$(command -v virtualbox)" ]; then
    if [ "$machine" == "Mac" ]; then
        echo -e " ${BLUE} Your machine has meets all the requirements to install DEVOPS-PACK. Run *bash devpack.sh* "
    elif [ "$machine" == "Linux" ];
    then
        echo -e " ${BLUE} Your machine has meets all the requirements to install DEVOPS-PACK. Run *bash devpack.sh*  \e[0m "
    fi
    
fi
