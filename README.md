## Operating System/Kernel

#### `uname -r ; uname -a` | Show OS/kernel information.
#### `free -m` | Show memory information.
#### `dmesg` | Show OS/kernel log.
#### `df -h` | Show information about your partitions/filesystems.
#### `ls /lib/modules/$(uname -r)` | Show the active modules on kernel.
#### `ls /lib/modules/$(uname -r)/kernel/drivers/` | Show all available modules for kernel.
#### `lsmod` | Show status of the modules on kernel.
#### `sudo modprobe module_name` | Load a module to the kernel (Linux).
#### `sudo modprobe -r module_name | Remove a module from the kernel.
#### `sudo rmmod module_name | Remove a module from the kernel.
#### `kldload module_name` | Load a module to the kernel (BSD).
#### `sudo umount /your/path` | Unmount one filesystem.
#### `sudo umount -a` | Unmount all filesystems except root filesystem.

## Hardware

#### `lscpu` | Show CPU information.
#### `cat /proc/meminfo` | Advanced memory information.
#### `ifconfig` | Show all active network interfaces.
#### `iwconfig` | Show all active wireless network interfaces.
#### `cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_available_governors` | Show available CPU governors.
#### `cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor` | Show current CPU governor.
#### `echo governor_name | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor` | Activate a CPU governor (most used are "powersave","performance" and "ondemand").

## Graphics

#### `startx` | Start X.Org from terminal (the command on .xinitrc will run).
#### `glxinfo | grep OpenGL` | Show your OpenGL driver name/version.
#### `vulkaninfo | grep Vulkan` | Show your Vulkan driver name/version.

## Networking

#### `hostname` | Show system DNS name.
#### `hostname -I` | Show all network addresses of your system.
#### `ping (website link or IP address)` | Ping any website or IP to see if it's online or measure your connection delay.
#### `whois https://websitename.com` | Show website registration information.

## User

#### `Ctrl+C` | This keyboard shortcut cancel any command process.
#### `clear` | Clean your terminal content/output.
#### `!!` | Run previous command.
#### `su -` | Ask root password to switch user for root with echo.
#### `sudo -i` | Ask current user password to become root.
#### `doas command` | Run as root per-command with root variables.
#### `sudo command` | Run any command with temporary root privileges and current user variables.
#### `sudo !!` | Run previous command as root temporarily.
#### `exit` | Exit root privileges or exit terminal session.
#### `whoami` | Current active user on terminal shell/$PATH.
#### `$HOME` | Environment variable for user folder.
#### `echo $SHELL` | Show your default terminal shell.
#### `echo $0` | Show your current terminal shell.
#### `cat /etc/shells` | Show your installed terminal shells (active on $PATH).
#### `chsh -s /pathof/yourshell` | Change your default terminal shell permanently (common path is /usr/bin).
#### `alias name='command'` | Add an alias/abbreviation for a command on your terminal shell (add this command on your shell configuration file to be permanent, generally a file named `.nameofyourshellrc` on your user folder).
#### `passwd nameoftheuser` | Change the user password.
#### `history` | Show the commands history.
#### `history name` | Show the commands with the name specified in history.

## Programs

#### `echo "text"` | Show the specified text on terminal.
#### `echo $PATH` | Show the directories in $PATH environment variable.
#### `ldd program_name` | Show the dependencies (shared libraries) used by a program.
#### `export PATH=$PATH:/your/directory` | Add a new PATH to your terminal shell.
#### `reset` | Restore the terminal variables to their default values.
#### `time command` | Count the time taken for a program to run the command.
#### `name*` | On some programs the * symbol apply an action to all files with that name.
#### `./` | This operator will launch any program from terminal.
#### `sh yourscriptname` | Run a non-executable sh script.
#### `bash yourscriptname` | Run a non-executable bash script.
#### `killall process_name` | Kill all instances of a running program.
#### `killall -u username` | Kill all processes of an user.
#### `>` | This operator store the output of a task on some file (example: `task > file.txt`).
#### `>>` | This operator store the output of a task on some file but don't overwrite it's contents (example: `task > file.txt`).
#### `|` | This operator apply a command above the output of other program (example: `glxinfo | grep OpenGL`, this command will search for "OpenGL" inside the output of "glxinfo").
#### `git clone https://github.com/nameoftheuser/nameoftherepository.git` | Download any GitHub repository to the active directory.
#### `git clone https://websitename.com/nameoftherepository.git` | Download any remote Git repository.
#### `git clone https://websitename.com/nameoftherepository.git /name/of/your/folder` | Download a Git repository to the specified directory.
#### `wget https://websitename.com/nameofthefile` | Download any file (as the HTTP protocol headers are flexible, it can download the wrong file, so try to specify the exact file without header problems, generally an exposed extension of the file in the URL "https://website.com/nameofthefile.extension").
#### `wget -c https://websitename.com/nameofthefile` | Resume an incomplete download.
#### `wget --tries=anynumber https://websitename.com/nameofthefile` | Download any file and try again from where it stopped if the connection failed (by default wget tries 20 times).
#### `wget -i file.txt` | Download from multiple links of a file.
#### `wget --recursive --page-requisites --html-extension --convert-links --no-parent https://websitename.com` | Download the entire website and convert it to work locally (offline).
#### `curl -O https://websitename.com` | Download any file.
#### `wget -C - -O https://websitename.com/nameofthefile` | Resume an incomplete download.
#### `curl -O https://websitename.com -O https://website2name.com` | Download files from multiple websites at once.
#### `WINEPREFIX=~/.yourprefixname ./wine` | Example command for custom Wine Prefixes.
#### `WINEPREFIX=~/.yourprefixname ./wine explorer` | Run Wine Explorer from the specified Wine Prefix.
#### `--appimage-extract` | Option to extract AppImage files.

## Package Management

#### `autoremove` | This common argument remove unused dependencies on some package managers.
#### `autoclean` | This common argument remove packages cache.
#### `package_name*` | This symbol applies an action to all packagess with that name.
#### `dpkg --configure -a` | Fix a incomplete package install on Debian systems.
#### `pkg delete -a` | Remove all packages on FreeBSD systems.

## Files/Folders

#### `pwd` | Show the current active directory.
#### `cd /nameof/yourfolder` | Change the active directory to the specified folder.
#### `cd -` | Change to the previous directory with echo.
#### `cd ..` | Change to the parent directory/folder.
#### `cd $HOME` | Change the active directory to your user folder.
#### `ls` | Show normal folders/files of the directory.
#### `ls -a` | Show all folders/files from a directory, including the hidden ones.
#### `ls -A` | Show almost all files/folders, excluding the hidden . and .. Unix tree files.
#### `ls *` | Show the files/folders inside all the folders of the directory.
#### `ls -a *` | Show all files/folders inside all the folders of the directory, inclusing hidden ones.
#### `ls -l` | Show advanced information about the files/folders of the directory.
#### `cat /directory/file` | Show the contents of any text file.
#### `mkdir nameofthefolder` | Create a new folder on the active directory.
#### `cp nameofyourfile /destination/folder` | Copy a file to other folder and overwrite on destination.
#### `cp -p nameofyourfile /destination/folder` | Copy a file to other folder, overwrite on destination and maintain the file permissions and timestamps.
#### `cp -v nameofyourfile /destination/folder` | Show the files that are being copied (verbose mode).
#### `cp -i nameofyourfile /destination/folder` | Ask if you want to overwrite the file.
#### `cp -pvib nameofyourfile /destination/folder` | Copy a file to other folder, maintain permissions/timestamps, show the file being copied, ask permission to overwrite and make a backup.
#### `cp -b nameofyourfile /destination/folder` | Copy/overwrite/backup a file to other folder with backup.
#### `cp file1 file2 /destination/folder` | Copy multiple files to other folder and overwrite on destination.
#### `cp -r /nameof/yourfolder /destination/folder` | Copy a folder to other folder and overwrite on destination.
#### `cp -r nameofyourfolder/. /destination/folder` | Copy only the things inside the folder and overwrite on destination.
#### `cp -rpvib nameofyourfolder /destination/folder` | Copy a folder to other folder, maintain permissions/timestamps, show the files being copied, ask permission to overwrite and make a backup.
#### `cp -r folder1 folder2 /destination/folder` | Copy multiple folders to other folder and overwrite on destination.
#### `mv /nameof/yourfolder /destination/folder` or `mv nameofyourfile /destination/folder` | Move a file/folder to other folder and overwrite on destination.
#### `mv -i nameofyourfile /destination/folder` | Ask if you want to overwrite the folder.
#### `mv *.extension /destination/folder` | Move all files with the specified extension to the destination folder.
#### `mv /nameof/yourfolder /newfolder/name` | Move/rename a folder.
#### `rm nameofthefile` | Remove/delete a file.
#### `rm -rf /nameof/thefolder` | Remove/delete any folder recursively without asking for permission (use with caution if you called the command with su/sudo/doas).
#### `rmdir /your/folder` | Remove an empty directory.
#### `echo "text" >> /directory/file` | Example command to add text on any file.
#### `.nameofthefile or .nameofthefolder` | A dot before the name of a file/folder make it hidden.
#### `find . -type f -name file_name` | Search for files on the directory/subdirectories (run with sudo/su if the directories are under root permissions).
#### `find . -type d -name folder_name` | Search for folders on the directory/subdirectories (run with sudo/su if the directories are under root permissions).
#### `tree /nameof/thefolder` | Show all folders/files/subfolders/subfiles in a tree.
