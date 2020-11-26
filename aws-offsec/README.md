### AWS-Offsec

- Creating AWS IAM user for Cloud Goat
We go to IAM and users and setup profile for the cloudgoat user with programmatical access and administration access.

- Setting up cloudgoat and pip
We need pip to get done with the cloudgoat installation that manages and runs all the vulnerable aws seervices whch we will later try to privesc.
- Installing terraform
Installing terraform is easy all you need is to wget the latest version and move to /local/bin/
- Setting up AWS CLI
https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html
- Setting up cloud goat profile
```bash
#configure a profile to use cloud goat (user the profile name cloudgoat)
./cloudgoat.py config profile

#whitelist ip automatically
./cloudgoat.py config whitelist --auto


#config cloudgoat with creds
#download csv with creds of user and use here
aws configure --profile cloudgoat
```

### Exploitation

```bash

#auth user with creds
aws configure --profile cloudgoat

#create an aws service named the privesc_by_rollback
./cloudgoat.py create iam_privesc_by_roolback

# cat out the creds for aceess to the service deployed onto aws by cloudgoat

aws configure --profile  lab1
# enter the creds from the file generated when cloudgoat ran create.
````

For responses and aws CLI magic look at [commands.md](./commands.md)

### References
https://github.com/RhinoSecurityLabs/cloudgoat

https://askubuntu.com/questions/983351/how-to-install-terraform-in-ubuntu
