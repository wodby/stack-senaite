# SENAITE LIMS application stack for Kubernetes on Wodby

Deploy SENAITE LIMS applications on Kubernetes with Wodby.

This repository defines the Wodby stack manifests and default service
composition for SENAITE LIMS.

<!-- wodby:generated:start -->

## Stack contract

- [SENAITE LIMS stack on Wodby](https://wodby.com/stacks/senaite)
- [Browse Wodby application stacks](https://wodby.com/stacks)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## Service definitions

- [SENAITE LIMS service](https://github.com/wodby/service-senaite)
- [SENAITE database (ZEO) service](https://github.com/wodby/service-senaite-zeo)
- [OpenSMTPD service](https://github.com/wodby/service-opensmtpd)

## What's included

| Component / service | Default configuration |
| --- | --- |
| SENAITE LIMS<br>`senaite` | required; enabled by default; links: `zeo` → `zeo`, `sendmail` → `opensmtpd` |
| SENAITE database (ZEO)<br>`zeo` | required; enabled by default; volumes: `data` 20 GB |
| OpenSMTPD<br>`opensmtpd` | optional; disabled by default |

Enabled optional services are selected by default but can be excluded when an
app is created. Disabled optional services are available but not selected by
default. Required services cannot be excluded.

## Validate the stack manifest

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

<!-- wodby:generated:end -->
