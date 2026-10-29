# Ansible Tutorial Reference

A personal, hands-on learning repository for following the Ansible tutorial below in order. Use the video as the source of truth for the lesson sequence and commands; keep your own notes and lab work here rather than copying the instructor's material.

## Learning resource and attribution

- **Video:** [Ansible In One Shot | Production Ready DevOps (Terraform Integration)](https://youtu.be/z0BZDAtQa6E)
- **Original author/channel:** [TrainWithShubham](https://www.youtube.com/@TrainWithShubham)

All lesson explanations and demonstrations belong to the original creator. This repository is an independent study companion and is not affiliated with or endorsed by the channel.

## How to follow the tutorial

1. Watch from the beginning and follow the demonstrated sequence without skipping ahead.
2. Before each new section, note the video timestamp and the goal demonstrated there.
3. Reproduce the steps in your own disposable lab, then record what worked, what changed in your environment, and any questions.
4. Keep secrets, private keys, inventory credentials, and generated state out of Git. Use placeholders in committed examples and store real values in an untracked vault or environment-specific secret store.
5. At the end of a section, verify the result yourself before moving on. If a command or version differs from the video, document the difference rather than silently changing the lesson.

## Suggested study milestones

Use these as a progress checklist, not as claims about the video's exact chapter names. Add the corresponding video timestamp and the instructor's demonstrated steps as you reach each topic.

- [ ] **Lab preparation:** identify the operating system, controller/managed-node setup, required tools, and safe test environment used in the lesson.
- [ ] **Ansible fundamentals:** follow the lesson's explanation of its architecture, configuration, inventory, and ad-hoc execution; verify each example in the lab.
- [ ] **Playbooks and automation:** reproduce the playbook examples in the order shown; record variables, handlers, roles, or other constructs only as they appear in the video.
- [ ] **Production-readiness practices:** capture the practices demonstrated for repeatability, security, organization, and safe execution; test changes on disposable resources first.
- [ ] **Terraform integration:** follow the demonstrated handoff between Terraform and Ansible, note prerequisites and inputs, then verify the complete workflow end to end.
- [ ] **Review and cleanup:** rerun the finished workflow from a clean state, summarize what it provisions/configures, and remove disposable resources safely.

## Repository workflow

Create a directory per lesson or topic and keep examples small and easy to rerun. A starting layout:

```text
.
├── README.md
├── notes/
│   └── lesson-log.md
├── inventory/
│   └── README.md
├── playbooks/
│   └── README.md
└── terraform/
    └── README.md
```

Only add these directories when you begin the corresponding lesson. Store timestamps, commands (without secrets), expected results, and troubleshooting notes in `notes/lesson-log.md`.

## Prerequisites

The exact versions and setup should follow the tutorial and your lab environment. Before running commands, check the video for required operating-system, Ansible, Terraform, provider, and cloud/local-lab prerequisites. Use an isolated test environment and least-privilege credentials. Do not run infrastructure-changing examples against production accounts.

## Useful official references

Use official documentation to clarify behavior while keeping the video as the learning sequence:

- [Ansible documentation](https://docs.ansible.com/)
- [Terraform documentation](https://developer.hashicorp.com/terraform/docs)
- [Ansible and Terraform overview](https://developer.hashicorp.com/terraform/tutorials/configuration-language/ansible)

## Safety and version notes

Tutorials can use versions or provider behavior that later change. Record the version you used and any necessary adaptation in your notes. Review infrastructure plans and playbook targets before applying changes, avoid committing secrets or state files, and only use resources you own or are authorized to manage.
