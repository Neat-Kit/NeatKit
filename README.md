# Neatkit local tunnel

Start the site and share it through a Cloudflare quick tunnel with one command:

```powershell
powershell -ExecutionPolicy Bypass -File .\start-local-tunnel.ps1
```

Dry run the launcher without starting anything:

```powershell
powershell -ExecutionPolicy Bypass -File .\start-local-tunnel.ps1 -DryRun
```

Stop the background processes later with the saved PID files:

```powershell
Stop-Process -Id (Get-Content .\python-server.pid) -Force
Stop-Process -Id (Get-Content .\cloudflared.pid) -Force
```

If you need to install `cloudflared` again on Windows, use:

```powershell
choco install cloudflared -y
```