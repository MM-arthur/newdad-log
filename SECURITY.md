# Security Policy / Medical content issues

## Reporting medical-content issues

If you find a medical error in any decision tree (incorrect red flag, wrong
threshold, outdated guideline), please open an **Issue** with:

- File path and line number
- The incorrect claim (quote it)
- The authoritative source you're citing (WHO / AAP / UpToDate guideline name + year + URL)
- Your suggested correction

We prioritize medical accuracy above all other contributions. Maintainers
will review and respond within 7 days.

## Reporting privacy violations

If you find content that violates the privacy iron rule (real names, dates,
hospital names, numeric values for any specific case), please open a
**private** issue or contact the maintainers directly:

- **GitHub Issue** (label `privacy`): https://github.com/MM-arthur/newdad-log/issues
- **Email**: (see repository About section for maintainer contact)

We will:

1. Remove the violating content within 24 hours of confirmation
2. Audit related content for similar patterns
3. Add detection rules to prevent recurrence

## Scope of this policy

This covers:

- **Privacy**: personal data, real names, real dates, real locations
- **Medical accuracy**: incorrect clinical claims, wrong thresholds, outdated guidelines
- **Security**: code execution issues, malicious content injection (currently N/A — content-only repo)

This does NOT cover:

- General parenting disagreements (use Discussions)
- Feature requests (use Issues with `enhancement` label)
- Translations quality disputes (use Issues with `i18n` label)

## What we will NOT do

We will not request, store, or process any personal health information in
this repository. All content is generic and desensitized. Do not submit PRs
containing personal case data.
