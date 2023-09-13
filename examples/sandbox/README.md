# Sandbox CI example

This is an example how to use the CI for a KYPO sandbox, such as [junior-hacker](https://gitlab.ics.muni.cz/kypo-library/content/kypo-library-junior-hacker).

To use the CI:
- copy the files `.gitlab-ci.yml` and `terraform.tf`
- ensure the following CI/CD variables are set:
  - `TF_VAR_KYPO_ENDPOINT`
  - `KYPO_CLIENT_ID`
  - `KYPO_USERNAME`
  - `KYPO_PASSWORD`

If you want to use the CI to test the sandbox in Vagrant as well:
- ensure GitLab runner which has nested virtualization is available, and it has tag `image-builder` 
- add the following snippet to the `include` in `gitlab-ci.yml`:
```yaml
  - project: muni-kypo-images/ci-cd-virtual-images
    file: test-vagrant.yml
```
