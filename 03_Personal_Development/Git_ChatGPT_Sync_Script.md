# Git & ChatGPT Sync Script (design)

```bash
#!/usr/bin/env bash
# cron: every 30 min
curl -H "Authorization: Bearer $TOKEN" \
  "https://chat.openai.com/api/export?since=$(date -d '-30 minutes' +%s)" \
  | jq -r '.messages[] | .timestamp + "
" + .content' \
  >> "$VAULT/Inbox/chatgpt_$(date +%F).md"
git -C "$VAULT" add .
git -C "$VAULT" commit -m "Auto‑import ChatGPT $(date)"
git -C "$VAULT" push
```

*Requires ChatGPT export API or scrape workaround.*
