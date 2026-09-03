Steps for setup:
1. Install WSL in your windows powershell:
```powershell
wsl --install
```

2. Install DDEV in your WSL
```powershell
wsl --install Ubuntu --name DDEV
```
or download the installer in the official website
```browser
https://ddev.com/get-started/
```

3. clone the project and go to the file
```ubuntu
git clone https://github.com/M1cko25/jobhuntAI.git
cd jobhuntAI
```

4. start DDEV
```ubuntu
ddev start
```

5. install composer dependencies
```ubuntu
ddev composer install
```

6. install Node dependencies
```ubuntu
ddev npm install
ddev npm run dev
```

7. open new ubuntu terminal & setup the environment
```ubuntu
cp .env.example .env
ddev artisan key:generate
```

8. migrate
```ubuntu
ddev artisan migrate
```

9. access the site
```browser
https://jobhuntai.ddev.site
```

10. access the database
```browser
  https://jobhuntau.ddev.site:8037/
```


Debugging Tips
1. Restart Docker
2. Ensure you have php installed in your WSL
3. try restarting DDEV
```bash
ddev poweroff
ddev start
```
4. try clean DDEV
```bash
ddev clean --all
ddev hostname --remove-inactive
rm -r ~/.ddev
