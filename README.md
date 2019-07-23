# Ansible Role: Quantum ESPRESSO

An Ansible role that installs [Quantum ESPRESSO](http://www.quantum-espresso.org) on Ubuntu.

## Role Variables

See `defaults/main.yml`

## Example Playbook

```yaml
- hosts: machines
  roles:
  - role: nccr-marvel.quantum_espresso
```

## Tests

This role uses [Molecule](https://molecule.readthedocs.io/en/latest/#) and Docker for tests.

## License

MIT
