---

title: "Week 7 Worklog"
date: 2026-06-08
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
----------------------

### Goals for Week 7

- Gain practical experience using the AWS Command Line Interface (AWS CLI) to inspect and manage AWS resources.
- Compare CLI-driven workflows with the graphical AWS Management Console and note pros/cons.
- Try cloud-hosted shells (CloudShell, Cloud9) as alternatives to a local terminal.
- Run basic AWS CLI commands to verify account identity, region settings, and common service states.

### Plan (daily breakdown)

| Day | Activities | Start | End | References |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- | ---- | ----------------------------------------------------------------------------- |
| Mon | Read introductory material on AWS CLI; outline typical use-cases and advantages over the console. | 08/06/2026 | 08/06/2026 | https://docs.aws.amazon.com/cli/ |
| Tue | Prepare local environment: check OS prerequisites, install or update AWS CLI, and verify the version. | 09/06/2026 | 09/06/2026 | https://docs.aws.amazon.com/cli/ |
| Wed | Configure the CLI: set up credentials, default region, output format, and experiment with named profiles. | 10/06/2026 | 10/06/2026 | https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html |
| Thu | Execute basic commands (STS get-caller-identity, describe-regions, list S3 buckets, describe EC2 instances) and take notes. | 11/06/2026 | 11/06/2026 | https://docs.aws.amazon.com/cli/latest/reference/ |
| Fri | Explore CloudShell/Cloud9, compare with local shell experience, summarize findings and update this worklog. | 12/06/2026 | 12/06/2026 | https://docs.aws.amazon.com/cloudshell/ |

### Key outcomes and lessons

- Established that the AWS CLI provides fast, scriptable access to AWS resources—especially useful for automation and repeatable checks.
- Noted differences between interfaces: the Console is better for visual exploration; CLI is faster for repetitive or automated tasks.
- Verified how to inspect the local environment and confirm a working AWS CLI installation.
- Completed configuration steps, including credential and profile management; emphasized keeping credentials secure.
- Ran a set of fundamental commands to confirm account identity and to query EC2 and S3 metadata.
- Tried CloudShell as an immediate, browser-accessible environment and compared its convenience to a configured local terminal.
- Reinforced the importance of protecting Access Key and Secret Access Key and using least-privilege credentials where possible.

This summary was posted to the site as the Week 7 entry after verifying commands and notes.
