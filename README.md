# CI-CD-virtual-images

This repository contains definitions of pipelines for images in [MUNI-KYPO-IMAGES](https://gitlab.ics.muni.cz/muni-kypo-images) group.

- Import `vbox.yml` for testing VirtualBox images for Vagrant.
- Import `qemu.yml` for testing QEMU images for KYPO CRP, tested with Terraform
- `qemu-old.yml` is an old version of `qemu.yml` and can be imported instead of `qemu.yml`

This repository also contains definitions of pipelines for sandboxes in KYPO.

- Import `test-kypo.yml` for testing in KYPO CRP.
- Import `test-vagrant.yml` for testing in Vagrant.

See [examples](./examples) for more information.

## License

This project is licensed under the [MIT License](LICENSE).
