# The DOD and what has been met:

- To be able to run the app without the port 3000

- To be able to implement this in automation, in a provisioning script, so every time the VM runs, there is a reverse proxy set up to ensure that the app is running without the port 3000.

This has been met and tested. In order to test it out, these are the following steps needed to be done:

Fork/clone this repo and download all the files.

Once this done, from the directory, run this command:

```
vagrant up
```
This will get the machine up and running.

The next command is the following:

```
vagrant provision
```

The bash will look for the "provision" script inside the VagrantFile and execute it. In this case, we have more than one "provision" script, so it runs the "db machine" first then the "app machine". 

Once the code has been fully executed, it should load the app successfully! 

To test this out, run the following addresses:

```
development.local
development.local/posts
```

Both of these addresses should separately open a post page and a app running testing page. 

This shows that I've successfully met the DOD and the acceptance criteria.  