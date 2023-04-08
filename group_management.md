Groups are a great thing when it comes to user management, because it helps you place users into categories. For example, you can have an accounting group, and all users in the accounting department will be a member of that group. You can give a user access to accounting files by simply adding them to the group.

But first, what groups am I a member of?

``` bash
groups
```
By executing the groups command, by itself, it will show you a list of groups you’re a member of.

You can also query the groups for a user other than yourself:

``` bash
groups <user>
```
Reading group memberships doesn’t require root privileges, so I didn’t even need to switch to root or use sudo in order to view that.

To view all groups.
``` bash
cat /etc/group
```

So, how do you create a new group? That’s simple, we can use the **groupadd** command:
``` bash
sudo groupadd <groupname>

```

You can use the **groupdel** command to delete group.
``` bash
sudo groupdel <groupname>
```

Add the new user to the group:
```bash
sudo usermod -aG <groupname> <username>
```
Remove the user from the group.
```bash
sudo gpasswd -d <username> <groupname>

```

