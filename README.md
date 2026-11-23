# Secure CI/CD Demo (Python + Terraform + GitHub Actions)

A small personal project demonstrating a secure GitHub Actions pipeline for a tiny Python app and a Terraform-managed AWS S3 bucket.

## What this shows
- Automated checks on every push/PR
- Infrastructure as Code (Terraform)
- Security scanning (coming next)
- AWS access via OIDC (no stored keys) (coming next)
- Pinned actions and least-privilege tokens (coming next)

## Project structure
```
.
├── app/                  # Tiny Python app
│   ├── main.py
│   └── requirements.txt
├── terraform/            # S3 bucket definition
│   └── main.tf
├── .github/workflows/
│   └── ci.yml            # Pipeline
└── README.md
```

## Next steps we will add
1. gitleaks + Semgrep + Checkov (fail on high findings)
2. Pin every action to a commit SHA
3. AWS OIDC authentication (no long-lived keys)
4. Diagram + screenshot of a caught fake secret

## Local development
See `app/README.md` and run Terraform locally if you have AWS credentials configured.
