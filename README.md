# PHP Ubuntu

## Creazione di un nuovo progetto

Per avviare il progetto in locale, segui questi passaggi:

```bash
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/progetto1.conf
```

```bash
sudo nano /etc/apache2/sites-available/progetto1.conf
```

Scrivo dentro il file
```bash
<VirtualHost *:80>
    ServerName progetto1.local
    DocumentRoot /media/sf_Proverby/progetto1

    <Directory /media/sf_Proverby/progetto1>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

```bash
sudo a2ensite progetto1.conf
sudo systemctl reload apache2
sudo nano /etc/hosts
```

Aggiungo dentro il file
```bash
127.0.0.1 progetto1.local
```
