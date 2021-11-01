# Git Commands Cheat Sheet
Here in this repository you will find the basic to advannced command related to git,
with the help of these commands you can easily get hands on git.

####  what is git?
> Git is an Open Source Distributed Version Control System.

OR

> Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
for more details, Please checkout these resources:
[git Documentation](https://www.git-scm.com/doc)
[freecodecamp](https://www.freecodecamp.org/news/what-is-git-and-how-to-use-it-c341b049ae61/)

## Let's set up git
configure user information for all local repositories

```git config --global user.name "<your first name and last name>"```
>    set a name that is identifiable when review version history (git logs)

```git config --global user.email "<valid Email>"```
>    set an email address that wll be associated with each history maker

## Setup and Init the Repositories (GIT BASICS)
configuring user information, initializing and cloning the repositories

```git init <directory>```
> Create empty Git repo in specified directory. Run with no 
arguments to initialize the current directory as a git repository.

``` git clone <url>```
> clone an repository from a hosted loacation via URL

``` git add <directory> ```
> stage all changes in ```directory``` for the next commit.
replace ```directory``` with a ```file``` to change a specific file.

``` git commit -m "message" ```
> commit sthe stage snapshot, but instead of launching a text editor, use ```message``` 
as the commut message.

```git status```
> list which files are staged, unstaged, and untracked.

```git log```
> Display the entire commit history using the default format.

```git diff```
> show unstaged changes between your index and working directory

## How to setup ssh keys

```ls ~/.ssh```
on executing the above command if you see something like this
![sshcommand output](https://github.com/Angryl/git-demo/blob/master/assets/ssh%20command%201.PNG)

this means you havent setup any ssh keys yet.

###### Now run these commnad

![ssh keygen](https://github.com/Angryl/git-demo/blob/master/assets/sshkeygen.PNG)

and then it will ask for keys file location just press ```Enter``` for the default location

![ssh keygen location](https://github.com/Angryl/git-demo/blob/master/assets/ssh%20confirmation.PNG)

and then it will ask to enter a passhrase , Do nothing just pres ```Enter```
![asking for passphrase ](https://github.com/Angryl/git-demo/blob/master/assets/ssh%20confirmation%20again.PNG)

and then again it will ask to retype the passphrase, just press the ```Enter ``` again
![again asking for passphrase](https://github.com/Angryl/git-demo/blob/master/assets/ssh%20confirmation%20passphrse.PNG)

and finally your keys generated
![ssh keys generated](https://github.com/Angryl/git-demo/blob/master/assets/final%20keygen.PNG)

To check the keys type

![sshkeys](https://github.com/Angryl/git-demo/blob/master/assets/ssh%20keys.PNG)

there you will find the two pair of keys names ```id_rsa``` and ```id_rsa.pub``` private and public keys respectively.

###### Its time to add the keys
go to the repository for which you want to use.
and Before adding the keys we have to start the ```ssh -agent```
for that use command:

![eval()](https://github.com/Angryl/git-demo/blob/master/assets/evalcommand.PNG)

and the add private keys to repository

![ssh-add..](https://github.com/Angryl/git-demo/blob/master/assets/affkeys%20privte.PNG)
now you private keys added Successfully.

##### now its time to add the public key 
> Add the ```GitHub ``` account in which you want to upload the files using git.
for that:

> login into ```Github``` account
> and the goto settings of the account
> and then click on ```SSH and GPG keys```
> and there you will see something like this.

![SSH and GPG keys](https://github.com/Angryl/git-demo/blob/master/assets/sshand%20gpg%20keys.PNG)

> then click on button ```New SSH keys```

![NEw sshkeys](https://github.com/Angryl/git-demo/blob/master/assets/adding%20pub%20lic%20keyts.PNG)

> and then add the title in the __Title__ section and then paste the public keys in __Key__ section
> click on ```Add SSH Keys```
> Now your public keys addes Successfully

### Set the Origin path 

- Now you have to set the *Origin* path of your ```Github``` Repository to ```Git```
- then push your code to ```Github```




