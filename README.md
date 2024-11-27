# FlagExplorer

Prequisites:
- NodeJs: 20.17
- DotNet 8 sdk

------------- Running the application on a workstation ------------

1. Clone repo: git clone --recurse-submodules -j8 https://github.com/TimNape/FlagExplorer.git

2. Build frontend 
2.1 cd frontend
2.2. Install packages: npm i
2.3. Make a build: npm run build-dev   # for Prod: npm run build-prod, files published to: dist/development/frontend
2.4. To make a Prod build: npm run build-dev   # for Prod: npm run build-prod, files published to: dist/prod/frontend

3. Build and Run the backend
3.1. cd backend
3.2. dotnet publish -p:PublishProfile=Dev    # to publish files to: dist/development/backend
3.2. dotnet publish -p:PublishProfile=Dev    # to publish files to: dist/development/backend
3.2. Run the application: dotnet run
3.3. Run the backend   #The back end needs the frontend build to be in adjacent folder named frontend
 
4. Run the application (navigate the the Backend URL without the 'Swagger' suffix




Build locations (build files should be in adjacent folders named):
backend: /backend
frontend: /frontend
------------------ Running CI/CD pipelines ------------



5. Install Docker for Windows

5. Install Choco:
- Instructions here: https://chocolatey.org/install

5.2. Instalation using PowerShell (admin mode)
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

5. Install act-cli
> choco install act-cli

5.1. Manual Act Install:

- Download the Act binary for Windows from the Releases page (https://github.com/nektos/act/releases).
- Place it in a directory like C:\Program Files\Act.
- Add this directory to your system PATH under Environment Variables.

5.2. If ascked for size of act to install while installing act - choose Medium.

5. Run Act
Run Act:
act -j test
act -j build

