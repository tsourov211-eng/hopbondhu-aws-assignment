# Commands Used — ShopBondhu AWS Assignment

This file separates commands that were actually run from commands that are still planned. Replace example paths or IP addresses only when executing them in the actual environment.

## Windows PowerShell — public IP and SSH diagnostics

Commands used during troubleshooting:

```powershell
(Invoke-RestMethod https://checkip.amazonaws.com).Trim()
Test-NetConnection 13.206.195.203 -Port 22
ssh -i ".\\shopbondhu-key.pem" ubuntu@13.206.195.203
```

The SSH attempts returned `Connection timed out`, and `Test-NetConnection` returned `TcpTestSucceeded : False`. The public IP changed during troubleshooting, so the `My IP` source in `shopbondhu-web-sg` must match the current public IP (`/32`) at the time of connection.

## Ubuntu — web EC2 (planned; not yet confirmed executed)

The following commands are for Task 7. They should only be marked as executed after successful SSH access to `shopbondhu-web`.

```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx --no-pager
sudo systemctl is-enabled nginx
curl -I http://localhost
```

## Ubuntu — private backend (planned; Task 9)

Run these only after the private route table has an active default route to the available NAT Gateway and the private subnet is associated with that route table.

```bash
sudo apt update
curl -I https://google.com
```

## Frontend deployment (planned; Task 8)

No frontend upload command has been confirmed as executed yet. Add the exact `scp`, file-copy, ownership, and Nginx reload commands here after performing the deployment.
