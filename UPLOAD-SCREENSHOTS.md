# Add the full-screen screenshot evidence

The AWS screenshots were captured as full-screen PNG files and packaged separately as `shopbondhu-screenshots-evidence.zip`.

The archive contains a `screenshots/` folder with the following files:

- `01-vpc.png`
- `02-subnets.png`
- `02a-public-subnet-settings.png`
- `02b-private-subnet-settings.png`
- `05a-public-rt-subnet-associations.png`
- `06-private-rt.png`
- `06a-private-rt-subnet-associations.png`
- `07-ec2-instances.png`
- `07b-backend-instance-details.png`
- `08b-backend-sg-inbound.png`
- `08a-web-sg-inbound.png`
- `14-backend-instance-launch.png`

## Add them to this repository

1. Download `shopbondhu-screenshots-evidence.zip` from the ChatGPT conversation.
2. Extract the archive into the local root of this repository. It will add the PNG files into the existing `screenshots/` folder; keep the existing `screenshots/README.md`.
3. Review the files and confirm that no private key or credentials are present.
4. From the repository folder, run:

```powershell
git status
git add screenshots/*.png
git commit -m "docs: add full-screen AWS evidence through Task 6"
git push origin main
```

5. Open the GitHub README and confirm the embedded screenshots render.

## Evidence gaps that still need fresh screenshots

The archive does not contain a compliant full-screen capture for every assignment requirement. In particular, still capture the following after the corresponding settings are correct:

- Internet Gateway details showing `shopbondhu-igw` attached to `shopbondhu-vpc`.
- NAT Gateway details showing the final Zonal gateway as `Available` with its Elastic IP associated.
- Public route table **Routes** tab.
- Private route table after adding `0.0.0.0/0 → shopbondhu-nat` and associating `shopbondhu-private-subnet`.
- Current Web Security Group inbound rule with the then-current public IP `/32`.
- Task 7 Nginx status and browser page, after SSH access is working.

Do not rename an older screenshot to imply that it proves a later configuration. Retake it when the AWS console shows the final state.
