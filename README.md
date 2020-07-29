# Vydra-CI-CD-virtual-images

So far contains `Dockerfile` for building a docker image with QEMU, VBox, Packer, Vagrant, OpenStack-cli and Ansible.

## Example usage
```bash
# build
sudo docker build - < Dockerfile -t packer:latest

# run
sudo docker run --rm -it --privileged --network=host -w /opt -v `pwd`:/opt packer
```

For testing packer you can copy the included debian.json into [debian directory](https://gitlab.ics.muni.cz/CSIRT-MU/DEVOPS/debian-10-amd64) and run the container inside the debian directory.
For example (inside the docker container) `packer build -only=debian-vbox debian.json`
