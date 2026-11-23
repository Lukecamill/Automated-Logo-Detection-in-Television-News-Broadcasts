# Working together

Use short-lived branches and pull requests so changes can be reviewed before entering `main`.

```sh
git clone https://github.com/Lukecamill/Automated-Logo-Detection-in-Television-News-Broadcasts.git
cd Automated-Logo-Detection-in-Television-News-Broadcasts
git switch -c person1/dataset-setup
# Edit your files.
git add <specific-files>
git commit -m "Describe the change"
git push -u origin person1/dataset-setup
```

Open a pull request on GitHub and ask another member to review it. This is the agreed workflow; branch protection has not been configured.

Before starting subsequent work:

```sh
git switch main
git pull --ff-only
git switch -c person1/next-task
```

Suggested prefixes: `person1/`, `person2/`, `person3/`, `person4/`, `person5/`.

Each member owns their detector notebook. Coordinate edits to shared EDA, evaluation, comparison and documentation files to avoid notebook merge conflicts. Commit useful plots and metrics; clear excessive notebook output. Never commit API keys, tokens, raw datasets, checkpoints or local environment folders. Use environment variables for credentials.

Use issues to describe tasks and record decisions. Include what changed and how it was checked in each pull request. Keep an honest record of AI assistance in your journal contribution.
