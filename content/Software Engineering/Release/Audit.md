\[Commands from [here](https://pnpm.io/cli/audit)\]

#### On going update:
1. You can always find the vulnerabilities using:`pnpm audit`
2. Then try `pnpm update`.
	1. If you see: `No known vulnerabilities found` Then you're good.
	2. If it doesn't fix all the issues, use `pnpm-worspace.yaml` or just run `pnpm audit --fix`.
#### Quick security patch
1. You can always find the vulnerabilities using:`pnpm audit`.
2. Then I make sure I've had all packages updated to the latest patch.


TODO: Add automated process