## Localhost Setup Guide

1. Download the Setup package from GitHub

2. Verify Package Hash

Open PowerShell in the folder containing the downloaded ZIP file.

Run:

Get-FileHash .\setup.zip -Algorithm SHA256

Output:

Algorithm : SHA256
Hash      : 2A4D85014296F990FD8ED0FF3B480A107430C87DE7A07694EC3FA2590903631B
Path      : C:\Users\Administrator\Downloads\setup.zip

Compare the Hash value against the published SHA256 hash from GitHub.

If the hashes match, package integrity is verified.

3. Extract the setup package

Recommended location:

C:\Apps

4. Open PowerShell as Administrator

5. Navigate to the setup folder

Example:

cd C:\Apps\ChristChurchGeelong-Setup\setup

6. Run scripts in numbered order

.\00-install-dotnet.ps1
.\01-install-git.ps1
.\02-install-python.ps1
.\03-install-sql.ps1
.\04-install-cloudflared.ps1
.\05-environment-check.ps1
.\06-backup-local-state.ps1
.\07-reset-local-app.ps1
.\08-bootstrap-localhost.ps1

Note:

08-bootstrap-localhost.ps1 requires prior access to the private Anglican_Church_Australia repository.

Clone operations will fail without an institutional GitHub invite.
