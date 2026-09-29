# Nicholas Johnson

Production support and automation engineer working with Linux, Ansible and Python.

Remote from Mexico (UTC-6) · US citizen · English (native), Spanish (advanced)

## What I do

- L3 production support and on-call for a global document-processing platform on AWS and GCP
- Lead developer of an internal Python automation tool
- Automate Linux and FreeBSD servers with Ansible, and manage DNS as code with OpenTofu (Terraform)

## Featured Projects

### Infrastructure and Automation

Together, these three repositories deploy a self-hosted site from start to finish: OpenTofu sets up the DNS, Ansible configures the server, and the Hugo theme builds the content that the server hosts.

- **[configuration-journal-server](https://github.com/njohnson-oss/configuration-journal-server)**: an Ansible playbook that sets up a Debian server to host a website, a Gemini capsule and a cgit Git server over the clearnet, Tor and I2P. Its nine roles set up a default-deny nftables firewall, SSH that allows only post-quantum key exchange, TLS through Caddy, and unattended upgrades. Custom Python filter plugins work out the Tor and I2P addresses from their keys. The playbook validates its inputs before it changes anything, so it will not fall back to a weaker SSH key exchange or mirror an empty directory over a live site. CI runs ansible-lint, ruff and a check of Jinja template syntax.
- **[provisioning-journal-server](https://github.com/njohnson-oss/provisioning-journal-server)**: OpenTofu configuration for the server's DNS records at Infomaniak. It manages address and alias records, a CAA record that allows only Let's Encrypt to issue certificates, and null MX, SPF and DMARC records so that nobody can send email that appears to come from the domain. CI checks formatting and runs `tofu validate` and TFLint.
- **[hugo-theme-journal](https://github.com/njohnson-oss/hugo-theme-journal)**: a Hugo theme that builds one site in two formats: HTML for the web and Gemtext for the Gemini protocol. Both have Atom feeds. The theme uses no JavaScript, has high-contrast pages, and supports English and Spanish. It comes with a reference guide that shows how each Markdown feature is converted to Gemtext.

### Software

- **[altspell](https://github.com/njohnson-oss/altspell)**: a Flask REST API that translates between traditional and reformed English spelling, live at [api.inglish.revlearn.org](https://api.inglish.revlearn.org). Each spelling system is a separate plugin package, built on a shared [plugin interface](https://github.com/njohnson-oss/altspell-plugins) and [NLP provider](https://github.com/njohnson-oss/nlp-provider). Plugins: [Lytspel](https://github.com/njohnson-oss/altspell-lytspel), [Portul](https://github.com/njohnson-oss/altspell-portul), [Soundspel](https://github.com/njohnson-oss/altspell-soundspel), [Refaurmd Lojikl Inglish](https://github.com/njohnson-oss/altspell-refaurmd-lojikl-inglish), [Universal Lojikl Inglish](https://github.com/njohnson-oss/altspell-universal-lojikl-inglish).
- **[gemini2html](https://github.com/njohnson-oss/gemini2html)**: a Gemtext-to-HTML converter written in C.
- **[hitomezashi](https://github.com/njohnson-oss/hitomezashi)** and **[hitomezashi-rs](https://github.com/njohnson-oss/hitomezashi-rs)**: a stitch-pattern generator written as a C library and CLI, then ported to Rust.

## Tools I use

Linux, FreeBSD, Ansible, OpenTofu (Terraform), Python, Flask, Hugo, Git, CI/CD, Caddy, Nginx, nftables

## Currently

- Studying for the CCNA
- Preparing to publish Ansible playbooks that deploy a Tor relay on FreeBSD

## Contact

njohnson@posteo.net · [linkedin.com/in/njohnson-oss](https://www.linkedin.com/in/njohnson-oss)
