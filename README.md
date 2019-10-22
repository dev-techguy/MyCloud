# <p align="center"><a href="#" target="_blank"><img src="https://github.com/dev-techguy/Point-Of-Sale/blob/master/img/logo.png"></a></p>

<p align="center">
  <b>Save Today,Save Tomorrow</b><br>
  <a href="https://github.com/dev-techguy/Point-Of-Sale/issues">
  <img src="https://img.shields.io/github/issues/dev-techguy/Point-Of-Sale">
  </a>
  <a href="https://github.com/dev-techguy/Point-Of-Sale/network/members">
  <img src="https://img.shields.io/github/forks/dev-techguy/Point-Of-Sale">
  </a>
  <a href="https://github.com/dev-techguy/Point-Of-Sale/stargazers">
  <img src="https://img.shields.io/github/stars/dev-techguy/Point-Of-Sale">
  </a>
  <br><br>
  <img src="https://github.com/dev-techguy/Point-Of-Sale/blob/master/img/banner.PNG">
</p>

Mycloud is a POS sofware that has the following features.

- Stock taking.
- Three Levels of users (Super admin, admin and users)
- Real time stock anaylsis.
- Receipt printing and invoicing.
- Supplier management and payment.
- Set-up and find more.

## Help and docs

- [Software Documentation](#)


## Software Requirements

Before installing the software you have to install the following.

- [Xampp Server](https://www.apachefriends.org/index.html)
- [Java Runtime Environment(JRE) 12.0.2](https://www.java.com/en/)


## Software Download

Here you can download the repository to get the .exe and database file.


## Installing Steps (For Windows Users)

### Step 1 (Database Set-up)

- Install xampp and start it.
- Go browser and enter http://localhost/.
- Create database named *mycloud*.

### Step 2 (SQL GRANT)

After creating database no its time to grant permissions. This are the steps.

- Run cmd as administrator.
- Navigate to cd xampp/mysql/bin.
- Copy and Paste the code below.

```php

CREATE USER 'mycloud'@'localhost' IDENTIFIED BY '12345678';
GRANT ALL PRIVILEGES ON mycloud.* TO 'mycloud'@'localhost';
FLUSH PRIVILEGES;

```
### Step 3 (Running set-up)

Run the mycloud.exe setup.

## Security Vulnerabilities
 For any security vulnerabilities, please email to [TechGuy](mailto:dev.techguy@mail.com).
 
## License
 This software licensed under the [EULA LICENSE](#).
