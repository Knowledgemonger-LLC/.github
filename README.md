# .github

Organization **default community-health files** for **Knowledgemonger-LLC**. This is the special
`.github` **repository** GitHub reads to provide fallback governance files to **every** repo in
the org that does not ship its own.

## What lives here

| File | Inherited as |
|---|---|
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contributing guide shown on issues/PRs |
| [`SECURITY.md`](SECURITY.md) | Security policy (Security tab) |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Code of conduct |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/) | Issue forms + chooser config |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Default PR template |

## How inheritance works

- GitHub applies these files to any org repo that **lacks its own** copy. A repo that ships its
  own `SECURITY.md` (etc.) overrides the org default for that file.
- Inheritance keys on **account ownership**, not repo visibility — **private** org repos inherit
  these too. Only *this* repo's visibility matters.
- Issue templates are **all-or-nothing per folder**: if a repo adds any file under its own
  `.github/ISSUE_TEMPLATE/`, it uses **none** of the org defaults for that folder.

## This repo must stay **public**

`ISSUE_TEMPLATE` and `PULL_REQUEST_TEMPLATE` inherit **only from a public `.github` repo** — an
internal/private one is insufficient. The other files are free to inherit either way. Since none
of this content is sensitive, this repo is **public**; keep it that way or Tier-2 inheritance
silently stops working in consuming repos.

## What is deliberately NOT here

- **`CODEOWNERS`** — GitHub reads CODEOWNERS **only from the repo itself**; it does **not**
  inherit from the org `.github` repo. It is therefore shipped **per-repo** by `template-base`
  (Tier-2 copy exception), not hosted here.

See [`template-base`](https://github.com/Knowledgemonger-LLC/template-base) for the full
four-tier baseline model; these files are its **Tier 2 (inherit)** delivery mechanism.
