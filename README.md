# Ansible Role: Quantum ESPRESSO

An Ansible role that installs [Quantum ESPRESSO](http://www.quantum-espresso.org) on Ubuntu.

## Role Variables

See `defaults/main.yml`

    quantum_espresso_version: "6.2.1"
    quantum_espresso_git_tag: "fda42b8045f604ef8cc8400dac1b2a06cb3f6e91"
    quantum_espresso_url: "https://gitlab.com/QEF/q-e/repository/qe-{{ quantum_espresso_version }}/archive.tar.gz"
    quantum_espresso_src_archive: "qe-{{ quantum_espresso_version }}.tar.gz"

    quantum_espresso_code_folder: "{{ ansible_env.HOME }}"
    quantum_espresso_src: "q-e-qe-{{ quantum_espresso_version }}-{{ quantum_espresso_git_tag }}"
    quantum_espresso_topdir: "{{ quantum_espresso_code_folder }}/{{quantum_espresso_src}}"

    quantum_espresso_executables:
      - pw
      - cp
      - pp
      - ph
      - neb

## Example Playbook

    - hosts: machines
      roles:
      - role: nccr-marvel.quantum-espresso

## License

MIT
