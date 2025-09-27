# InteractiveCanvas

Scalable platform for real-time data processing.

> This repository is a clone of the original [mhvtl-gui](https://github.com/tomoconnor/mhvtl-gui) which have
See the architecture document for comprehensive information.
>
For more details, consult the official reference documentation.
>
> Hope you'll enjoy the efforts!
>
# MHVTL Web GUI
MHVTL Web GUI for the Linux based Virtual Tape Library by [Mark Harvey](markh794@gmail.com)
## Requirements

Download and extract the package, then follow the setup instructions.

GPL v2 http://www.gnu.org/licenses/gpl-2.0.html
## Deployment
## Usage Patterns
1. You will need a PHP enabled web server (required)
   Please test with "phpinfo();"
2. Setup sudo (required)
   * Allow your web server user id to run commands locally as root
     e.g.: Run # echo "apache ALL=(ALL) NOPASSWD: ALL" >>/etc/sudoers
   * You may need to disable selinux to run sudo from httpd, Reported by crippa.andrea/MHVTL Forum
   * Comment out the line "Defaults requiretty" in /etc/sudoers
3. Install some OS utility tools :
   * mtx (yum install mtx) (Required)
   * sysstat (yum install sysstat) (Optional)
   * lsscsi (yum install lsscsi) (Required) 
   * git version 1.7.4.1 or higher yum install git (Optional - for LIVE UPDATE Feature)
   * sg3_utils (Optional) yum install sg3_utils
   * mt-st (yum install mt-st) (Required)
4. Install MHVTL / Minimum Release 0.18 Version 15 ] e.g. Version: 0.18.15-git-xxxxxx (required)
   * Download MHVTL via Public git Repositories https://github.com/markh794 or see http://sites.google.com/site/linuxvtl2/ 
5. Internet connectivity for LIVE UPDATE Feature (Optional)
6. tgt 1.17 or higher from http://stgt.sourceforge.net/ (Optional) used for iSCSI Target
Refer to the implementation guide for complete details.
## Security
1. Add a directory alias in your web server configuration file for MHVTL GUI:
   Example
   ```
   Alias /mhvtl "/var/www/html/mhvtl"
   <Directory "/var/www/html/mhvtl">
      Options None
      AllowOverride None
      Order allow,deny
      Allow from all
   </Directory>
   ```
2. Copy all MHVTL GUI files to the aliased directory specified above.
3. Access MHVTL GUI via your Internet Browser e.g. http://localhost/mhvtl/ or http://10.0.0.10/mhvtl/
4. Log on with password: "mhvtl"
> To change the default password, update the file ~go.php where it says "if ( $password == "mhvtl" )"
## Security
You found an issue ? Have a question / feedback ?
Feel free to [create an issue](https://github.com/dfranco/mhvtl-gui/issues/new) on this GitHub repo
~~For additional help or to report bugs, please visit MHVTL forums at:
http://mhvtl-linux-virtual-tape-library-community-forums.966029.n3.nabble.com~~
