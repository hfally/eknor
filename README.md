<p align="center">
    <strong>
        EKNOR - LINUX (UBUNTU)
    </strong>
</p>

<p align="center">
    <img src="https://img.shields.io/badge/Apache-Virtualhost-red.svg" alt="Apache virtualhost">
</p>


## Introduction
Eknor is an Apache virtual-host creator. It is a straight forward solution to creating a new web application 
environment or linking an existing one, thus, giving you a custom local domain.

It works for most PHP frameworks out there; Laravel, CodeIgniter, Yii, etc. It also works for your own 
vanilla project.

Furthermore, it gives you a customizable TLD and keeps a backup of your hosts file in case you wish to rollback.

Other distro will be supported in updates.

## Supported OS
Ubuntu and other Debian-based distros.

## Dependencies
The following applications are needed on your device for eknor to run successfully.

- Apache2: `$ sudo apt install apache2`
- OpenSSL: You most likely already have this installed. You can confirm by running `$ which openssl`. If it is not found, proceed with installation using `$ sudo apt install openssl` 
- Certutil: `$ sudo apt install libnss3-tools` - This is used to trust TLS certificates locally.

## Installation
Clone repository into your `~/` (your home directory) directory.

Go to your home directory on your terminal:

`$ cd ~`

Clone eknor into your home directory:

`$ git clone https://github.com/hfally/eknor.git`

Add `$HOME/eknor/bin` to your PATH.

#### How to add to your PATH
Edit .bashrc or .zshrc in your home directory and add the following line:
To edit, you can use terminal-based editors like *vi* or *nano*. I will use nano as an example.

`$ nano ~/.bashrc`

When the text editor comes up, scroll to the bottom and add this: 

`export PATH="$PATH:$HOME/eknor/bin"`

Press `ctrl + x` and `y` to save it.

You will need to source your .bashrc or logout/login (or restart the terminal) for the changes to take effect. To source your .bashrc, simply type:

`$ source ~/.bashrc`

**if you use zsh or any other shell, follow the same route**

## Basic Usage
Eknor can be used to initiate a new project; it creates a work director and an `index.php` file inside the `myapp.staging/public` directory (assuming myapp is the name of your new project). Eknor can also be used on an existing project, be it a vanilla PHP project or one built on a PHP framework (Yii, Laravel, Code-Igniter, etc).

* Go to your workspace on the terminal

    `$ cd ~/projects` (Assuming ~/projects is your workspace)

* To configure your workspace so eknor recognizes it, run

    `$ eknor park`

* To intiate a new project, lets assume the new project's name will be `myapp` run

    `$ eknor new myapp` (Make sure you are inside your workspace)

    A new directory will be created `mpapp.staging/public/index.php`

* To create virtual-host for an existing project run

    `$ eknor link` (Run this in the project's directory)

    Lets take a framework like Laravel for instance, assuming your Laravel projects name is `blog`

    `$ cd blog`

    `$ eknor link`

    Eknor automatically detects your `blog/public`

    Follow this same guide for a vanilla project or any other framework.

* To add HTTPS to an already linked project,

	`$ cd blog`
	
	`$ eknor secure` 

That's it!

You can always get help through `$ eknor help [command: eg. link]`

## Advanced Usage

Eknor's default TLD (.com, .org, .net, etc) is `.staging`, however in the spirit of freedom and open-source, you are at liberty to change it to whatever you want. Assuming you want to change it to `.local`


`$ eknor tld local`

To get current TLD, simply run

`$ eknor tld`

#### Pending ####
----
- [ ] Ability to revert creation 
- [ ] Ability to unlink
- [ ] Ability to revert TLS certificate generation 

## License

Eknor is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)

## Contribution
**Contributors**

- [Henry Falade](https://github.com/hfally)
- [Nana-Hauwa Adeku](https://github.com/nanahawau)

For contribution and personal bug reporting, send a mail to the author <a href='mailto:tofex4eva@yahoo.com'>tofex4eva@yahoo.com</a>
