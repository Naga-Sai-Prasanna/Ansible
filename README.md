# Ansible Practice

A collection of Ansible playbooks covering core concepts, written as hands-on practice while learning Ansible — from basic playbook structure through variables, conditionals, loops, filters, error handling, and idempotency.

## What This Covers

Each playbook focuses on one specific concept, building up from the basics to more advanced Ansible features: playbook structure, variables and variable precedence, command-line arguments, conditionals, loops, filters, facts, registering output, idempotency, and error handling.

## Playbooks

| File | Topic |
|------|-------|
| `01-playbook.yaml` | Basic playbook structure |
| `02-playbook.yaml` | Playbook structure (continued) |
| `03-playbook.yaml` | Playbook structure (continued) |
| `04-var.yaml` | Defining and using variables |
| `05-arguments.yaml` | Passing arguments/extra-vars to a playbook |
| `06-var prefrence.yaml` | Variable precedence rules |
| `complte.yaml` | A more complete/combined example playbook |
| `conditions.yaml` | `when` conditionals |
| `conditions-2.yaml` | `when` conditionals (continued) |
| `course.yaml` | General course exercise playbook |
| `datatypes.yaml` | Ansible/YAML data types |
| `error.yaml` | Error handling (`failed_when`, `ignore_errors`, etc.) |
| `facts.yaml` | Gathering and using Ansible facts |
| `filelevel.yaml` | File-level tasks (creating/managing files) |
| `filters.yaml` | Jinja2 filters in Ansible |
| `idempotency.yaml` | Demonstrating idempotent task behavior |
| `inventory.ini` | Sample inventory file used by the playbooks |
| `loops.yaml` | Basic loops (`loop`) |
| `loops-2.yaml` | Loops (continued) |
| `loops-3.yaml` | Loops (continued) |
| `mongo.repo` | Sample yum repo file for MongoDB |
| `mongodb.sh` | Shell script for MongoDB setup (used alongside a playbook) |
| `playlevel.yaml` | Play-level settings and structure |
| `register.yaml` | Using `register` to capture task output |
| `set_facts.yaml` | Using `set_fact` to define custom facts/variables |
| `shell-command.yaml` | Running shell/command modules from a playbook |
| `students.json` / `students.xml` / `students.yaml` | Sample data files used for variable/lookup exercises |
| `task.yaml` | Task-level structure and examples |
| `username.yaml` | Example playbook working with user-related variables/tasks |

## Prerequisites

- Ansible installed locally (`pip install ansible` or `dnf install ansible`)
- A target host or local connection defined in `inventory.ini`

## Usage

Run any playbook directly with the included inventory:

```bash
ansible-playbook -i inventory.ini 04-var.yaml
```

Pass extra variables where a playbook expects them (see `05-arguments.yaml`):

```bash
ansible-playbook -i inventory.ini 05-arguments.yaml --extra-vars "key=value"
```

## Status

This is a personal learning/practice repo for Ansible fundamentals, building toward the structured deployments in the [`ansible-roboshop`](https://github.com/Naga-Sai-Prasanna/ansible-roboshop) and [`ansible-roboshop-roles`](https://github.com/Naga-Sai-Prasanna/ansible-roboshop-roles) projects.
