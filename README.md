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

## Supported OS
Ubuntu is the only supported distro for now, however, its likely it works on Debian too.

Other distro will be supported in updates.

## Installation
Clone repository into your `/home` directory and add `$HOME/eknor/bin` to your PATH.

#### How to add to your PATH
Edit .bashrc in your home directory and add the following line:

`export PATH="$PATH:$HOME/eknor/bin"`

You will need to source your .bashrc or logout/login (or restart the terminal) for the changes to take effect. To source your .bashrc, simply type

`$ source ~/.bashrc`

**if you use zsh or any other shell, follow the same route**

## Usage
Run `eknor help` to get all use case, and run `eknor help COMMAND_NAME` for guidance on each of the command.

````
EKNOR 1.0.0

Usage:
  command [argument]

Available commands:
  domain	Displays/Sets domain tld
  help		Displays help for a given command [command optional]
  link		Virtualizes an existing project
  new		Creates new project (name required)
  park		Sets present directory as workspace/home for all projects
````

## License

Eknor is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)

## Contribution
For contribution and personal bug reporting, send a mail to the author <a href='mailto:tofex4eva@yahoo.com'>tofex4eva@yahoo.com</a>
