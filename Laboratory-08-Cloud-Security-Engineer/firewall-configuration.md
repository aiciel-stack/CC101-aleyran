# Firewall Configuration

## Command Used to Allow SSH
```bash
sudo ufw allow ssh
```

## Commands Used to Set the Default Deny Policy
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

## Command Used to Allow Port 8080
```bash
sudo ufw allow 8080/tcp
```

## What Would Happen if ufw enable Ran Before ufw allow ssh
If `sudo ufw enable` is run before allowing SSH, the Default Deny policy would immediately block incoming SSH traffic along with everything else, locking the administrator out of the server with no remote way back in.

## Evidence
# Firewall activated
<img width="493" height="372" alt="firewall-activated" src="https://github.com/user-attachments/assets/03d2dba6-c9ab-4e14-878e-fbcccb34dee5" />

# Firewall port allowed
<img width="445" height="590" alt="firewall-port-allowed" src="https://github.com/user-attachments/assets/ffcab203-a040-42fa-82ca-3858672e0b49" />


