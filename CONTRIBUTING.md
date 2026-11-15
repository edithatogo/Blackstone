# Contributing to Blackstone

Contributions improve the Blackstone legal-language processing library while preserving its prototype limitations, source attribution, and reproducible model-dependent behavior.

## Before you start

Read the [README](README.md), [test workflow](.github/workflows/main.yml), and relevant spaCy component before changing an interface or extraction behavior. Explain which legal-text patterns and model assumptions are affected.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

The README's source-development setup is:

```sh
pip install --editable .
pip install -r dev-requirements.txt
```

The existing workflow checks include:

```sh
flake8 blackstone
pytest tests/
```

Check the workflow for its runtime and model prerequisites. It uses a historical Python/model combination; record the environment actually exercised, and do not claim support for newer versions without evidence. Keep dependency modernization separate from a focused bug fix.

Use public or synthetic legal-text fixtures with precise provenance. Add regression cases for changed entities, citations, or text transformations, including ambiguous and negative examples. Preserve the distinction between an extracted label and a verified legal conclusion. Avoid redistributing restricted judgments, confidential documents, or private model artifacts.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `master` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Respect the [existing license](LICENSE) and preserve third-party notices. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
