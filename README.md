# AWX Demo Playbooks

A small set of self-contained playbooks for the **AWX + Nautobot** lab tutorial.
Every playbook runs against `localhost` with `connection: local`, so you need
**no** real managed hosts, SSH keys, or credentials — they exist to let you focus
on AWX mechanics (projects, inventories, job templates, surveys) rather than on
writing Ansible.

You run these in **Part 1** of the tutorial, and the very same job templates are
then run *from Nautobot* in **Part 3**.

## What each playbook teaches

| Playbook | Job template | Use it to explore |
| --- | --- | --- |
| `ping.yml` | `01 - Hello` | Your first job. Confirms the whole chain works. |
| `survey.yml` | `02 - Survey` | **Surveys** and extra variables — its questions become native Nautobot form fields in Part 3. |
| `failtest.yml` | `03 - Fail Test` | **Job states** (success vs failed); set `should_fail=true` to make it fail. |

`inventory/hosts.ini` is a dummy inventory you can optionally import into an AWX
Inventory (the "Faster alternative" in Part 1 §8.3).
