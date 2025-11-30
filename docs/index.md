# Mythbound Foundations

This is the official documentation for Mythbound’s organisation platforming. Application and service repositories consume these foundations. They do not modify them.

It defines:

- GCP organisation level layout and environment projects
- shared Terraform state backend and encryption
- CI service accounts and Workload Identity Federation for GitHub Actions
- GitHub organisation settings, core repositories, teams and branch protections

For the full rationale behind these patterns, the pitfalls of the old “bare metal and XAMPP” model, and how application repositories are expected to consume this platform, see the [`Golden path`](golden-path.md) write-up.

## Scope

This documentation is about platforming only.

It discusses the management of:

- GCP organisation level resources
- environment projects such as dev and prod
- shared Terraform state storage and encryption
- CI identities and their permissions
- GitHub organisation settings, core repositories, teams and branch protections

It does not manage:

- individual game or web workloads
- application specific infrastructure inside environment projects
- per project CI pipelines beyond what is needed for platform itself

Those concerns live in separate application or infrastructure repositories that consume the foundations defined here.

## How to use these docs

If you are new to this platform start here.

1. Read the [`Golden path`](golden-path.md)

   Understand why this platform exists and what problems it is solving for Mythbound and similar Open Tibia services.

2. Read the architecture section

   Get a high level view of how GCP, GitHub, Terraform, Ansible and the various repositories fit together.

3. Use the runbooks when you make changes

   Follow the step by step guides when bootstrapping the organisation, adding environments or onboarding new repositories.

4. Refer to contributing when you change the platform itself

   Platform changes are slower and more controlled than application changes. The contributing guide sets expectations.

## Sections

- [Golden path](golden-path.md)  
  Rationale for the platform, how it differs from legacy hosting patterns, and the core principles that guide everything else.

- [Architecture](architecture/index.md)

  High level view of the platform layout including GCP organisation structure, environment projects, Terraform backends and GitHub organisation wiring.

- [Runbooks](runbooks/index.md)

  Task oriented guides for common workflows such as bootstrapping the platform, adding a new environment or onboarding a new infra repository.

- [Contributing](contributing/index.md)

  Expectations and workflow for making changes to the platform foundations, including review requirements and testing strategy.
