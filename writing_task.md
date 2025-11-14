# Task 1: How to install X program from GitHub Repository
After reading through this section, you'll be able to install X program from a GitHub repository
in a RPM-based linux system. Before you proceed, ensure you have `Git` installed on your local machine and Root user access.

Follow the outlined steps below to complete the program installation:

1. Clone the repository and navigate to it. 
Run the command below in your terminal:
```bash
git clone <repo-url>
cd <repo-name>
```
2. Run the installation script:
```bash
sudo sh install
```
3. Install the required package and specified version
```bash
sudo dnf install <package-name>-<version>
```
4. Confirm package was successfully installed:
```bash
dnf list installed <package-name>
```

### Questions for development team
Here are a few questions I will like to ask the development team as regards the installation of X program.
* Apart from using an RPM-based linux system and having `Git` installed, is there any other prerequisites required to successfully complete the installation of this program?
* What is the name of the exact package(s) and specific version to be installed?
* Does the installation script require certain environment variables? 
* What's a quick start or command to launch and use the installed program?
* What is a common issue encountered when installing this program?

# Task 2: Uninstalling the Package
At any point, if you wish to uninstall the Package, follow these steps:

1. Run the command in your terminal:
```bash
sudo yum remove <package-name>
```
2. (Optional) Remove orphaned packages:
```bash
sudo package-cleanup --leaves
```
> **_NOTE:_** package-cleanup is from _yum-utils_ package. New versions of `yum` can use `dnf autoremove`. 


3. (Optional) Remove configuration files and user data associated with the uninstalled package:
```bash
# remove any remaining configuration files
sudo rm -rf /etc/<package-name>

# remove user data 
sudo rm -rf /var/lib/<package-name>
```
 **_Warning:_** This will delete all package data permanently.
