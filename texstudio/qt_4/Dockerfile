FROM harshjv/texlive-2015
MAINTAINER Leandro Souza <leandrocsfrb@gmail.com>

ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  
ENV LC_ALL en_US.UTF-8 

RUN locale-gen "en_US.UTF-8"
RUN sudo dpkg-reconfigure locales

RUN apt-get update

RUN apt-get -f install -q -y ghostscript axel

RUN apt-get -f install -q -y axel libpoppler-qt4-4 libqt4-network libqt4-script libqt4-xml libqtcore4 libqtgui4 libqtwebkit4

WORKDIR $HOME

RUN axel http://download.opensuse.org/repositories/home:/jsundermeyer/xUbuntu_14.04/amd64/texstudio-qt4_2.10.10_amd64.deb

RUN dpkg -i texstudio-qt4_2.10.10_amd64.deb

RUN apt-get clean

CMD texstudio
