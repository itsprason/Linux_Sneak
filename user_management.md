To add a user, we can use the command **useradd** command.
```bash
sudo useradd larry
```

To create a user along a home directory, add -m flag.

``` bash
sudo useradd -m larry
```

To delete(remove) the user, we can use the **userdel** command.

```bash
sudo userdel larry
```

By default, the **userde** command doesn't delete the user's home directory unless you explicitly tell it that you want it to do so. If we add -r flag to the **userdel** command, the home directory of the user will also get deleted along with the user.

``` bash
sudo userdel -r larry
```

To change user's password:
```bash
sudo passwd larry 
```

System users are useful for automation, and running processes. To create a System user, you can add the -r flag to the **useradd** command.

```bash
sudo useradd -r systemuser
```

Check /etc/passwd or /etc/shadow for user details.
