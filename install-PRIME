#!/usr/lib/python3.7

# Descrição (PT-BR)

# Este script é uma automatização do HowTo criado pelo @jonathon (https://forum.manjaro.org/u/jonathon),
# um moderador do fórum oficial (https://forum.manjaro.org) da distribuição linux Manjaro. Me reservo o direito de ter 
# cometido erros durante a criação no script, que possam causar problemas em sua máquina, sejam de hardware ou de software. 
# Utilize-o por sua conta e risco próprios. Então, caso encontre erros, reporte-os. Toda e qualquer contribuição é sempre 
# bem vinda. Meu nickname no Telegram é @FVGuilherme.

# Description (EN-US)

# That script is an automatization of the HowTo created by @jonathon (https://forum.manjaro.org/u/jonathon),
# a moderator of the official forum (https://forum.manjaro.org) of the Manjaro Linux dsitribution. I reserve the right 
# to have made errors during script creation, which may cause problems on your machine, whether hardware or software. 
# Use it at your own risk. So, if you find errors, report them. Any and all contributions are always welcome. 
# My nickname on the Telegram is @FVGuilherme.


function espace {
    echo ''
    echo '============================================================'
    echo ''
}

function LightDM {
    espace
    echo 'LightDM é o DM escolhido. Iniciando as operações necessárias...'
    espace
    espace
    echo 'Setando a fonte de saída de acordo com o seu DM (gerenciador de login).'
    espace
    echo '#!/bin/sh
xrandr --setprovideroutputsource modesetting NVIDIA-0
xrandr --auto' > /usr/local/bin/optimus.sh
    chmod a+rx /usr/local/bin/optimus.sh
    echo ''
    echo '#
# General configuration
#
# start-default-seat = True to always start one seat if none are defined in the configuration
# greeter-user = User to run greeter as
# minimum-display-number = Minimum display number to use for X servers
# minimum-vt = First VT to run displays on
# lock-memory = True to prevent memory from being paged to disk
# user-authority-in-system-dir = True if session authority should be in the system location
# guest-account-script = Script to be run to setup guest account
# logind-check-graphical = True to on start seats that are marked as graphical by logind
# log-directory = Directory to log information to
# run-directory = Directory to put running state in
# cache-directory = Directory to cache to
# sessions-directory = Directory to find sessions
# remote-sessions-directory = Directory to find remote sessions
# greeters-directory = Directory to find greeters
# backup-logs = True to move add a .old suffix to old log files when opening new ones
# dbus-service = True if LightDM provides a D-Bus service to control it
#
[LightDM]
#start-default-seat=true
#greeter-user=lightdm
#minimum-display-number=0
#minimum-vt=7 # Setting this to a value < 7 implies security issues, see FS#46799
#lock-memory=true
#user-authority-in-system-dir=false
#guest-account-script=guest-account
#logind-check-graphical=false
#log-directory=/var/log/lightdm
run-directory=/run/lightdm
#cache-directory=/var/cache/lightdm
#sessions-directory=/usr/share/lightdm/sessions:/usr/share/xsessions:/usr/share/wayland-sessions
#remote-sessions-directory=/usr/share/lightdm/remote-sessions
#greeters-directory=$XDG_DATA_DIRS/lightdm/greeters:$XDG_DATA_DIRS/xgreeters
#backup-logs=true
#dbus-service=true

#
# Seat configuration
#
# Seat configuration is matched against the seat name glob in the section, for example:
# [Seat:*] matches all seats and is applied first.
# [Seat:seat0] matches the seat named "seat0".
# [Seat:seat-thin-client*] matches all seats that have names that start with "seat-thin-client".
#
# type = Seat type (local, xremote, unity)
# pam-service = PAM service to use for login
# pam-autologin-service = PAM service to use for autologin
# pam-greeter-service = PAM service to use for greeters
# xserver-backend = X backend to use (mir)
# xserver-command = X server command to run (can also contain arguments e.g. X -special-option)
# xmir-command = Xmir server command to run (can also contain arguments e.g. Xmir -special-option)
# xserver-config = Config file to pass to X server
# xserver-layout = Layout to pass to X server
# xserver-allow-tcp = True if TCP/IP connections are allowed to this X server
# xserver-share = True if the X server is shared for both greeter and session
# xserver-hostname = Hostname of X server (only for type=xremote)
# xserver-display-number = Display number of X server (only for type=xremote)
# xdmcp-manager = XDMCP manager to connect to (implies xserver-allow-tcp=true)
# xdmcp-port = XDMCP UDP/IP port to communicate on
# xdmcp-key = Authentication key to use for XDM-AUTHENTICATION-1 (stored in keys.conf)
# unity-compositor-command = Unity compositor command to run (can also contain arguments e.g. unity-system-compositor -special-option)
# unity-compositor-timeout = Number of seconds to wait for compositor to start
# greeter-session = Session to load for greeter
# greeter-hide-users = True to hide the user list
# greeter-allow-guest = True if the greeter should show a guest login option
# greeter-show-manual-login = True if the greeter should offer a manual login option
# greeter-show-remote-login = True if the greeter should offer a remote login option
# user-session = Session to load for users
# allow-user-switching = True if allowed to switch users
# allow-guest = True if guest login is allowed
# guest-session = Session to load for guests (overrides user-session)
# session-wrapper = Wrapper script to run session with
# greeter-wrapper = Wrapper script to run greeter with
# guest-wrapper = Wrapper script to run guest sessions with
# display-setup-script = Script to run when starting a greeter session (runs as root)
# display-stopped-script = Script to run after stopping the display server (runs as root)
# greeter-setup-script = Script to run when starting a greeter (runs as root)
# session-setup-script = Script to run when starting a user session (runs as root)
# session-cleanup-script = Script to run when quitting a user session (runs as root)
# autologin-guest = True to log in as guest by default
# autologin-user = User to log in with by default (overrides autologin-guest)
# autologin-user-timeout = Number of seconds to wait before loading default user
# autologin-session = Session to load for automatic login (overrides user-session)
# autologin-in-background = True if autologin session should not be immediately activated
# exit-on-failure = True if the daemon should exit if this seat fails
#
[Seat:*]
#type=local
#pam-service=lightdm
#pam-autologin-service=lightdm-autologin
#pam-greeter-service=lightdm-greeter
#xserver-backend=
#xserver-command=X
#xmir-command=Xmir
#xserver-config=
#xserver-layout=
#xserver-allow-tcp=false
#xserver-share=true
#xserver-hostname=
#xserver-display-number=
#xdmcp-manager=
#xdmcp-port=177
#xdmcp-key=
#unity-compositor-command=unity-system-compositor
#unity-compositor-timeout=60
greeter-session=lightdm-gtk-greeter
#greeter-hide-users=false
#greeter-allow-guest=true
#greeter-show-manual-login=false
#greeter-show-remote-login=true
user-session=xfce
#allow-user-switching=true
#allow-guest=true
#guest-session=
session-wrapper=/etc/lightdm/Xsession
#greeter-wrapper=
#guest-wrapper=
#display-setup-script=
#display-stopped-script=
#greeter-setup-script=
#session-setup-script=
#session-cleanup-script=
#autologin-guest=false
#autologin-user=
#autologin-user-timeout=0
#autologin-in-background=false
#autologin-session=
#exit-on-failure=false
display-setup-script=/usr/local/bin/optimus.sh

#
# XDMCP Server configuration
#
# enabled = True if XDMCP connections should be allowed
# port = UDP/IP port to listen for connections on
# listen-address = Host/address to listen for XDMCP connections (use all addresses if not present)
# key = Authentication key to use for XDM-AUTHENTICATION-1 or blank to not use authentication (stored in keys.conf)
# hostname = Hostname to report to XDMCP clients (defaults to system hostname if unset)
#
# The authentication key is a 56 bit DES key specified in hex as 0xnnnnnnnnnnnnnn.  Alternatively
# it can be a word and the first 7 characters are used as the key.
#
[XDMCPServer]
#enabled=false
#port=177
#listen-address=
#key=
#hostname=

#
# VNC Server configuration
#
# enabled = True if VNC connections should be allowed
# command = Command to run Xvnc server with
# port = TCP/IP port to listen for connections on
# listen-address = Host/address to listen for VNC connections (use all addresses if not present)
# width = Width of display to use
# height = Height of display to use
# depth = Color depth of display to use
#
[VNCServer]
#enabled=false
#command=Xvnc
#port=5900
#listen-address=
#width=1024
#height=768
#depth=8' > /etc/lightdm/lightdm.conf
    espace
    echo 'Instalação finalizada! Reinicie a máquina. =)'
    espace
}

function GDM {
    espace
    echo 'GDM é o DM escolhido. Iniciando as operações necessárias...'
    espace
    espace
    echo ' Setando a fonte de saída de acordo com o seu DM (gerenciador de login).'
    espace
    echo '[Desktop Entry]
    Type=Application
    Name=Optimus
    Exec=/usr/local/bin/optimus.sh
    NoDisplay=true
    X-GNOME-Autostart-Phase=DisplayServer' > /usr/local/share/optimus.desktop
    echo ''
    echo 'Linkando o arquivo criado (/usr/local/share/optimus.desktop) para iniciar com o GDM.'
    echo ''
    sudo ln -s /usr/local/share/optimus.desktop /usr/share/gdm/greeter/autostart/optimus.desktop
    sudo ln -s /usr/local/share/optimus.desktop /etc/xdg/autostart/optimus.desktop
    echo ''
    espace
    echo 'Instalação finalizada! Reinicie a máquina. =)'
    espace
}
    
function SDDM {
    espace
    echo 'SDDM é o DM escolhido. Iniciando as operações necessárias...'
    espace
    espace
    echo ' Setando a fonte de saída de acordo com o seu DM (gerenciador de login).'
    espace
    echo 'xrandr --setprovideroutputsource modesetting NVIDIA-0
    xrandr --auto' >> /usr/share/sddm/scripts/Xsetup
    echo ''
    espace
    echo 'Instalação finalizada! Reinicie a máquina. =)'
    espace
}    

function commom {
    espace
    echo 'Iniciando a instalação do PRIME.'
    espace

    espace
    echo 'Removendo o Bumbleblee.'
    espace
    sudo mhwd -f -r pci video-hybrid-intel-nvidia-bumblebee
    sudo mhwd -f -r pci video-linux 
    sudo mhwd -f -r pci video-vesa
    echo ''

    espace
    echo 'Instalando o driver da NVidia.'
    espace
    sudo mhwd -i pci video-nvidia
    echo ''

    espace
    echo 'Setando uma nova configuração do mhwd para o Xorg.'
    espace

    sudo rm -f /etc/X11/xorg.conf.d/90-mhwd.conf
    echo 'Section "Module"
    Load "modesetting"
EndSection
      
Section "Device"
    Identifier "nvidia"
    Driver "nvidia"
    BusID "PCI:1:0:0"
    Option "AllowEmptyInitialConfiguration"
EndSection' > /etc/X11/xorg.conf.d/optimus.conf
    echo ''

    espace
    echo ' Redefinindo a blacklist.'
    espace
    sudo rm /etc/modprobe.d/mhwd*
    echo ''

    echo 'blacklist nouveau
blacklist nvidiafb
blacklist rivafb' > /etc/modprobe.d/nvidia.conf
    echo ''

    espace
    echo ' Criando o nvidia-drm.modeset.'
    espace
    sudo echo 'options nvidia_drm modeset=1' > /etc/modprobe.d/nvidia-drm.conf
    echo ''

    espace
    echo ' Hora de escolher qual é o seu Display Manager (DM). PRESTE MUITA ATENÇÃO. Escolher o DM errado provavelmente implicará em tela preta.'
    espace

}

function DM_choice {
    espace
    echo 'Escolha o seu DM:
          1 - LightDM;
          2 - GDM;
          3 - SDDM.'
    espace
    read OPT
    case $OPT in
        1) LightDM
        ;;
        2) GDM
        ;;
        3) SDDM
        ;;
        *) echo "Era para escolher 1, 2 ou 3. Saindo..." && exit
    esac
}

function inicio {
    espace
    echo 'ATENÇÃO! Antes de prosseguir, verifique o BusID da sua placa dedicada (3D controller) com o comando ***lspci | grep -E "VGA|3D"***. Se a saída for algo como 01:00.0, prossiga. Caso contrário, modifique o script com o valor do BusID correspodente a sua placa.'
    echo ''
    echo 'Além disso, certifique-se que seu sistema está atualizado executando o comando abaixo, de preferência pelo TTY.

    sudo pacman-mirrors -g && sudo pacman -Syyuu'
    espace
    echo 'Você verificou aquilo descrito acima?

    1 - Sim, quero prosseguir.
    2 - Não, vou fazê-lo.'

    echo ''
        read inicio
        case $inicio in
            1) commom && DM_choice
            ;;
            2) exit
            ;;
            *) echo 'As opções são apenas 1 ou 2. Saindo...' && exit
        esac
}

inicio



