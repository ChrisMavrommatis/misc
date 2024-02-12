# Snippet to harvest all emails in a git repo

https://www.geeksforgeeks.org/how-to-protect-your-private-email-addresses-in-git-github/

## Bash
```bash
git log | grep Author | cut -d ":" -f2 | awk '{print $NF}' | sed -r 's/<// ; s/>//' | sort -u >> authorsEmails.txt
```

## Powershell
```powershell
(git log | Select-String -Pattern '[\w\-\.]+@([\w-]+\.)+[\w-]{2,}' -AllMatches).Matches.Value | Sort-Object | Unique

```