# Security policy

## Supported code

Security fixes target the current code on `main`. Older tags and downloadable
releases do not have a separate maintenance guarantee; use the latest fixed
revision when a security change is published. This is a personal project without
a guaranteed response time or paid security support.

## Report a vulnerability

Use GitHub's private
[Report a vulnerability](https://github.com/YouKnowJP/Personal-Project/security/advisories/new)
form if private vulnerability reporting is enabled for this repository.
If the form is unavailable, open an
[issue requesting a private security contact](https://github.com/YouKnowJP/Personal-Project/issues/new?title=Private%20security%20contact%20request)
without disclosing the vulnerability, affected secrets, or exploit details.
Wait for a private channel before sharing the report.

In the private report, include:

- The affected project, version or commit, browser/OS, and relevant configuration.
- A concise explanation of the impact and steps to reproduce it.
- A minimal proof of concept using synthetic data, if available.
- Any proposed fix or workaround.

Do not include real credentials, personal information, or other people's data.
Test against your own local copy and coordinate public disclosure with the
maintainer after a fix is available.

## Switchback's security boundary

The game runs in the browser and stores progress in `localStorage`. Local scores
and saves are editable by the browser owner and are not trusted competition
records. The bundled development server binds to `127.0.0.1` and serves an
allowlist of game files; use the static `dist/` package for deployment.

Report cases such as unintended file exposure by the development server,
script injection, or unexpected transmission of local data. Ordinary gameplay
bugs belong in the public bug-report template. Asset and dependency details are
listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
