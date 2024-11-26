# FlagExplorer

1. Clone source code
- git clone https://github.com/TimNape/FlagExplorer.git
-  cd FlagExplorer
- git clone https://github.com/TimNape/flag-explorer-backend.git
- git clone https://github.com/TimNape/flag-explorer-frontend.git


2. Install Docker for Windows

2. Install Choco:
- Instructions here: https://chocolatey.org/install

2.2. Instalation using PowerShell (admin mode)
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

3. Install act-cli
> choco install act-cli

3.1. Manual Act Install:

- Download the Act binary for Windows from the Releases page (https://github.com/nektos/act/releases).
- Place it in a directory like C:\Program Files\Act.
- Add this directory to your system PATH under Environment Variables.

3.2. If ascked for size of act to install while installing act - choose Medium.

4. Run Act
Run Act:
act -j test
act -j build

