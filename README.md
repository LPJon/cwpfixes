# Support Me:
<p><a href="https://github.com/sponsors/LPJon"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="LPJon" /></a></p><br><br>


# CWP Fixes - Fixes for CentOS 7 versions of CentOS Web Panel
Used for correcting CWP (CentOS Web Panel) install script code errors
- # Installation
  - # Netdata - Live Server Metrics and Statistics
    
  To install the "install_netdata" script into your CWP server run the following command in an ssh terminal.

  This is meant to be a drop in replacement for the current script supplied by CWP and will make a backup of the original for you.
  
    ```
    cd /root && wget https://raw.githubusercontent.com/LPJon/cwpfixes/main/install_netdata && chmod +x install_netdata && mv -f /scripts/install_netdata /scripts/install_netdata.orig && mv -f install_netdata /scripts/
    ```
  After installation just go to the Admin Web UI Dashboard and select "Graphs" from the panel on the left and install Netdata as usual. The installation can take some time so be paitent and wait for the page to refresh.

  Optionally you can run the "NVM" version installation by editing the "install_netdata" script with your favorite editor and changing the  ```usenvm=n``` variable at the top of the script to ```usenvm=y```.

  NOTE: If you have already installed Netdata you will have to re-run the script manually with the following command in an ssh terminal ```/scripts/./install_netdata```. This will make the changes needed for NVM.
  If you would like to switch back just switch the ```usenvm=y``` back to ```usenvm=n``` and re-run the script again and it will be changed back to the original NodeJS RPM.

  - # CWP Pro Terminal - A Browser Based Terminal Console for CWP Admins

  To install the "install_terminal" script into your CWP server run the following command in an ssh terminal.

  This is meant to be a drop in replacement for the current script supplied by CWP and will make a backup of the original for you.
  
    ```
    cd /root && wget https://raw.githubusercontent.com/LPJon/cwpfixes/main/install_terminal && chmod +x install_terminal && mv -f /scripts/install_terminal /scripts/install_terminal.orig && mv -f install_terminal /scripts/
    ```
  After installation just go to the Admin Web UI Dashboard and select "Terminal" from the top and install CWP Pro Terminal as usual. The installation can take some time so be paitent and wait for the page to refresh with a prompt.

  Optionally you can run the "NVM" version installation by editing the "install_terminal" script with your favorite editor and changing the  ```usenvm=n``` variable at the top of the script to ```usenvm=y```.

  NOTE: If you have already installed CWP Pro Terminal you will have to re-run the script manually with the following command in an ssh terminal ```cd /root && rm -rf node_modules server.js package.json packge-lock.json terminal.sock && /scripts/./install_terminal```. This will make the changes needed for NVM.
  If you would like to switch back just switch the ```usenvm=y``` back to ```usenvm=n``` and re-run the script again and it will be changed back to the original NodeJS RPM.
