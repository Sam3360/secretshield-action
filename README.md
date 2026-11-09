# SecretShield GitHub Actions Templates

Ready-to-use GitHub Actions workflows for [SecretShield](https://pypi.org/project/secretshield/), a secret detection and redaction tool for Python and other projects.

Use these templates to automatically scan your repository for secrets using GitHub Actions.

## Available Workflows

| Template | Description |
|---|---|
| [Default](templates/default.yml) | Scans on every push and pull request |
| [Daily](templates/daily.yml) | Scans once every day |
| [Weekly](templates/weekly.yml) | Scans once every week |
| [Monthly](templates/monthly.yml) | Scans once every month |

All scheduled workflows also support manual execution through GitHub Actions.

## Quick Start

1. Choose one of the workflow templates listed above.
2. Open the template file.
3. Copy its contents.
4. In your own repository, create the following directory if it doesn't already exist:

   ```text
   .github/workflows/
   ```

5. Create a file inside it named `secretshield.yml`.
6. Paste the copied workflow into that file.
7. Commit and push your changes.

That's it! GitHub Actions will automatically run SecretShield according to the selected workflow.

## Example

For the default workflow, your repository should contain:

```text
your-repository/
└── .github/
    └── workflows/
        └── secretshield.yml
```

The default workflow scans your repository whenever you push commits or open a pull request.

## Scheduled Scans

Scheduled workflows use GitHub Actions cron syntax and run in UTC.

| Schedule | Cron |
|---|---|
| Daily | `0 0 * * *` |
| Weekly (Monday) | `0 0 * * 1` |
| Monthly (first day) | `0 0 1 * *` |

GitHub may delay scheduled workflows during periods of high load.

## Manual Scans

The daily, weekly, and monthly templates include `workflow_dispatch`.

After adding one of these workflows:

1. Open your repository on GitHub.
2. Go to **Actions**.
3. Select the SecretShield workflow.
4. Click **Run workflow**.

## Requirements

- A GitHub repository with GitHub Actions enabled.
- No Python installation required on your local machine.
- SecretShield is automatically installed during the workflow.

## About SecretShield

SecretShield detects secrets in your code and helps prevent accidental exposure.

- GitHub: [Sam3360/secretshield](https://github.com/Sam3360/secretshield)
- PyPI: [secretshield](https://pypi.org/project/secretshield/)
- Website: [SecretShield](https://therealsecretshield.freebuff.app/)

## License

These workflow templates are provided under the [MIT License](LICENSE).
