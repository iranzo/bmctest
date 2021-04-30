# BMC Testing

This repo aims to provide tooling to validate that BMC is able to load an ISO image from a remote server via http or via https and still be able to mount it within the OS.

- Requirements
  - Hardware
    - target host running RHEL and BMC credentials
  - Software
    - Remote http server containing the ISOs to load (small ISO and big ISO) with or without custom certificates
    - Ansible
      - inventory file which contains details for both BMC and target host as well as the data for the test

The output of the execution will summarize detected BIOS and BMC versions.

This playbook is based on the ones available at:

- https://github.com/openshift-kni/baremetal-deploy/tree/master/ansible-ipi-install
- https://github.com/openshift/assisted-test-infra/tree/master/ansible-bm-install

# Execution

Run `ansible-playbook -i inventory playbook.yml` to validate the server.
