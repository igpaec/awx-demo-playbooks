# AWX Demo Playbooks

A small set of self-contained playbooks for learning Ansible AWX. Every
playbook runs against `localhost` with `connection: local`, so you need **no** real managed hosts, SSH keys, or credentials to use them. They exist to let you focus on AWX mechanics (projects, inventories, job templates, surveys,
workflows, schedules) rather than on writing Ansible.

## Push this to a git repo

AWX pulls playbooks from source control. Create an empty repo (GitHub, GitLab, or anywhere AWX can reach) and push this folder:

```bash
cd awx-demo-playbooks
git init
git add .
git commit -m "AWX demo playbooks"
git branch -M main
git remote add origin <YOUR_REPO_URL>
git push -u origin main
```

Then point an AWX **Project** at that repo URL.

## What each playbook teaches

| Playbook | Use it to explore |
| --- | --- |
| `ping.yml` | Your first job. Confirms the whole chain works. |
| `facts.yml` | Fact gathering and Job Template **verbosity** levels. |
| `survey.yml` | **Surveys** and extra variables (prompt-at-launch input). |
| `watch.yml` | Live streaming output; test the **Cancel** button (~30s run). |
| `failtest.yml` | **Job states** (success vs failed); set `should_fail=true` to fail it. |
| `inventory_demo.yml` | **Inventories**, groups, and host **limits** (no real hosts needed). |

`inventory/hosts.ini` is a dummy inventory for `inventory_demo.yml`.
