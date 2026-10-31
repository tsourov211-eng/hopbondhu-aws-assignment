# Screenshot evidence

The PNG files in this folder were supplied as full-window AWS Console captures during the assignment. They are kept as evidence of the configuration visible at the time of capture.

Some screenshots show incomplete or time-sensitive state. In particular:

- `06-private-rt.png` shows only the local route; the NAT default route was not present in that capture.
- `06a-private-rt-subnet-associations.png` shows zero explicit associations, with the private subnet not yet associated with the private route table.
- `08a-web-sg-inbound.png` shows a My IP value from an earlier troubleshooting moment; public IP changes mean it must be refreshed before SSH access.

Do not treat these images as proof that the incomplete settings were later corrected. Replace or supplement them with fresh full-screen screenshots once the remaining configuration is completed.
