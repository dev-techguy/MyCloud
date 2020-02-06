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

Mycloud is a POS software that has the following features.

- Stock taking.
- Three Levels of users (Super admin, admin and users)
- Real time stock analysis.
- Receipt, printing and invoicing.
- Supplier management and payment.
- Set-up and find more.

## Help and docs

- [Software Documentation](#)


## Software Requirements

Before installing the software you have to install the following.

- [Xampp Server](https://www.apachefriends.org/xampp-files/7.3.14/xampp-windows-x64-7.3.14-0-VC15-installer.exe)
- [Java Development Kit(JDK) 13.0.2](https://www.oracle.com/java/)

## Software Architecture

The software currently performance well on windows 7, 8 and 10 only.


## Software Download

Here you can download the repository to get the .exe and database file.


## Software Installation

### Step 1 (Database Set-up)

- Install xampp and start it.
- Go browser and enter *http://localhost/phpmyadmin*.
- Create database named *mycloud*.

### Step 2 (SQL GRANT)

After creating database, next is to grant permissions. This are the steps.

- Run cmd as administrator.
- Navigate to *cd xampp/mysql/bin*.
- Type in the terminal *mysql -u root*. Remember no password will be required just hit return key.
- Copy and Paste the code below.

```php

CREATE USER 'mycloud'@'localhost' IDENTIFIED BY '12345678';
GRANT ALL PRIVILEGES ON mycloud.* TO 'mycloud'@'localhost';
FLUSH PRIVILEGES;

```
### Step 3 (Running set-up)

- Through your browser *http://localhost/phpmyadmin* import *mycloud.sql* to the database you created earlier.
- Then run the *mycloud.exe* setup.

### Step 4 (Credentials)

After successful installation, you will be redirect to login page.

- Login as admin | username = *mycloud* | password = *12345678*. 

- Login *GUI*

 <img src="https://github.com/dev-techguy/Point-Of-Sale/blob/master/img/login.PNG">

## Security Vulnerabilities
 For any security vulnerabilities, please email to [TechGuy](mailto:dev.techguy@mail.com).


## TroubleShooting

On system crash or had shutdown the application and when trying to start can't seem to start. Kindly follow this:-

- Check if xampp server *(Apache & MySQL)* are running.

- Stop both *(Apache & MySQL)*

- Try starting the application.
 
## License
 This software licensed under the [EULA LICENSE](https://github.com/dev-techguy/Point-Of-Sale/blob/master/license.txt).
