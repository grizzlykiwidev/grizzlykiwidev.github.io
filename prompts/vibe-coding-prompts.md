# 10 Reusable Vibe-Coding Prompts

Paste into Cursor, Claude Code, Codex or similar. Replace `<...>`.

## 1. Debug from an error
```
Here is the error and how to reproduce it: <error + steps>.
Before changing code: list the 3 most likely causes, ranked, with the evidence for each from the code.
Then confirm the top cause (add a log or a failing test), fix it with the smallest change, and show the test passing.
```

## 2. "It used to work"
```
<Feature> worked before and is now broken. Look at recent changes (git diff / git log -p for <files>) and identify which change caused it. Explain why, then fix without reverting unrelated work.
```

## 3. Plan before building
```
I want <feature>. Don't write code yet. Read the relevant files and give me: the files you'll touch, the approach, edge cases, and how you'll verify it. Wait for my OK.
```

## 4. Safe refactor
```
Refactor <file/function> to <goal: smaller functions / remove duplication / clearer names>. Behaviour must not change. First make sure tests cover the current behaviour (add them if missing), then refactor, then run them.
```

## 5. Write tests
```
Write tests for <file/function> using <test framework> in the style of <existing test file>. Cover the happy path, edge cases (empty, null, max, invalid input) and one failure path. Run them and fix only the tests, not the code, unless you've found a real bug; if so, tell me.
```

## 6. Code review
```
Review the current diff like a strict senior engineer. List issues by severity: bugs, security, performance, readability. Be specific with file:line. Don't change anything yet.
```

## 7. Security pass
```
Audit <area/app> for: exposed secrets, missing auth checks on server routes/actions, missing input validation, SQL/command injection, and data that leaks to the client. Report findings with fixes, most severe first.
```

## 8. Deploy readiness check
```
I'm about to deploy to <Vercel/Netlify/Fly/etc.>. Check: production build passes, all required env vars are listed in .env.example and none are hardcoded, no secrets in client bundles, DB migrations are committed, error/404 pages exist, no console.logs of sensitive data, and the README has run/deploy steps. Give me a pass/fail checklist and fix the fails.
```

## 9. Explain this code
```
Explain <file/folder> to me like I'm a capable beginner: what it does, how data flows through it, and the 3 things most likely to break if I change it.
```

## 10. Update outdated code
```
Check this project's real dependency versions in <package.json/etc.> and find code using deprecated or outdated APIs for those versions. List each with the modern replacement, then update them one at a time, running checks after each.
```
