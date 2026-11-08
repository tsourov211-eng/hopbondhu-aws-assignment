# Upload the supplied AWS screenshots

The companion archive is named `ostad-3tier-assignment-evidence.zip`.

1. Download the archive from this conversation.
2. Place it in a local clone of this repository's root folder.
3. Extract it at the repository root. It creates `ostad-3tier-assignment/screenshots/`.
4. Open a terminal in the repository root and run:

```bash
git add ostad-3tier-assignment/screenshots/
git commit -m "docs: add Ostad three-tier AWS assignment screenshots"
git push origin main
```

After pushing, open `ostad-3tier-assignment/README.md` on GitHub. Its screenshot embeds should render.

## Screenshot files

- `00-aws-console-home.png`
- `01-vpc-created.png`
- `02-subnets-created.png`
- `03-public-subnet-settings.png`
- `04-private-route-via-nat.png`
- `05-working-todo-app.png`
- `06-cloudformation-output.png`
- `07-ec2-instances.png`
- `08-security-groups.png`

Do not commit SSH private keys, passwords, database credentials, AWS access keys, or secret environment files. Review the screenshots for identifiers before keeping the repository public.
