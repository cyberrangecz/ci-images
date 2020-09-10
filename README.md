# Vydra-CI-CD-virtual-images

So far contains `Dockerfile` based on [johannthorir/packer-vbox](https://hub.docker.com/r/johannthorir/packer-vbox) for building a docker image with QEMU, VBox, Packer, Vagrant, OpenStack-cli and Ansible.

## Example usage
```bash
# build
sudo docker build - < Dockerfile -t packer:latest

# run
sudo docker run --rm -it --privileged --network=host -w /opt -v `pwd`:/opt packer
```
