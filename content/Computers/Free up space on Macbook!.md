Soon or later I see a "You're low on storage" message on my machine. I start by doing looking at these files:

### `/Library`
You can find 2 different libraries, I look at both ones:

- `~/Library/...`
- `/Users/<user-name>/Library/...`

To find the largest files, run:
```bash
du -sh ~/Library/* | sort -h
```
Then find the largest one and `rm -rf` if when you're sure it's safe to do so.