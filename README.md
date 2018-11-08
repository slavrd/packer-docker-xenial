## Packer docker
A packer template that builds a basic xenial docker image and a vagrant file for a docker machine.

#### Prerequisites:
* Install Vagrant - [installation instructions](https://www.vagrantup.com/downloads.html)

#### Setting up Vagrant environment:
* Build the VM - run: `vagrant up`
* Login to VM - run: `vagrant ssh -c "sudo su -"`
* Get the git repo - run: `git clone https://github.com/slavrd/packer-docker-xenial.git` and `cd packer-docker-xenial`

#### Building the Docker image and pushing it ot Docker Hub with Packer:
* Run: `packer build -var 'dhub_user=<username>' -var 'dhub_pwd=<password>' template.json`<br>
This will push the image to the Docker Hub registry under repository `ubuntu` and tag `xenial`
