# Nicholas Johnson

Production support and automation engineer working with Linux, Ansible and Python.

Remote from Mexico (UTC-6) · US citizen · English (native), Spanish (advanced)

## What I do

- L3 production support and on-call for a global document-processing platform on AWS and GCP, diagnosing issues from CloudWatch and Grafana logs
- Lead developer of an internal Python automation tool with GitLab CI; also write Python boto3 scripts for S3 document transfers and incident file pulls
- In my own projects, automate Linux servers with Ansible and manage DNS as code with OpenTofu (Terraform)

## Featured Projects

### Infrastructure and Automation

Together, these three repositories deploy a self-hosted site from start to finish: OpenTofu sets up the DNS, Ansible configures the server, and the Hugo theme builds the content that the server hosts.

- **[configuration-journal-server](https://github.com/njohnson-oss/configuration-journal-server)**: an Ansible playbook whose nine roles deploy a hardened Debian web and Git server, also reachable over Tor and I2P: default-deny nftables firewall, post-quantum-only SSH, automatic TLS through Caddy, and unattended upgrades. It checks every input before changing the host. CI runs ansible-lint, and ruff on its custom Python plugins.
- **[provisioning-journal-server](https://github.com/njohnson-oss/provisioning-journal-server)**: OpenTofu (Terraform) configuration for the server's DNS records, including CAA and email anti-spoofing (SPF, DMARC). CI checks formatting and runs `tofu validate` and TFLint.
- **[hugo-theme-journal](https://github.com/njohnson-oss/hugo-theme-journal)**: a Hugo theme that builds one site as both HTML and Gemtext, with no JavaScript, maintained since 2022 (370+ commits). CI builds it on two Hugo versions and tests the HTML, links and accessibility.

### Software

- **[altspell](https://github.com/njohnson-oss/altspell)**: a Flask REST API that translates between traditional and reformed English spelling, live at [api.inglish.revlearn.org](https://api.inglish.revlearn.org). Each spelling system is a separate plugin package, built on a shared [plugin interface](https://github.com/njohnson-oss/altspell-plugins) and [NLP provider](https://github.com/njohnson-oss/nlp-provider). Plugins: [Lytspel](https://github.com/njohnson-oss/altspell-lytspel), [Portul](https://github.com/njohnson-oss/altspell-portul), [Soundspel](https://github.com/njohnson-oss/altspell-soundspel), [Refaurmd Lojikl Inglish](https://github.com/njohnson-oss/altspell-refaurmd-lojikl-inglish), [Universal Lojikl Inglish](https://github.com/njohnson-oss/altspell-universal-lojikl-inglish).
- **[Spring-Social-Media-Blog-API](https://github.com/njohnson-oss/Spring-Social-Media-Blog-API)**: a Java REST API built with Spring MVC and Spring Data JPA during Revature training. It handles user registration, login, and creating, reading, updating and deleting messages, and passes all 37 of the project's tests.
- **[gemini2html](https://github.com/njohnson-oss/gemini2html)**: a Gemtext-to-HTML converter written in C.
- **[hitomezashi](https://github.com/njohnson-oss/hitomezashi)** and **[hitomezashi-rs](https://github.com/njohnson-oss/hitomezashi-rs)**: a stitch-pattern generator written as a C library and CLI, then ported to Rust.

## Tools I use

Linux, Ansible, OpenTofu (Terraform), AWS (CloudWatch, S3, boto3), Grafana, Python, Flask, Java (Spring), Hugo, Git, GitHub Actions, GitLab CI, Caddy, Nginx, nftables

## Currently

- Studying for the CCNA

## Contact

njohnson@posteo.net · [linkedin.com/in/njohnson-oss](https://www.linkedin.com/in/njohnson-oss)
