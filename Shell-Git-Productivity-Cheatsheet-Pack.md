# Shell & Git Productivity Cheatsheet Pack
**$5 · Personal-use digital product · A4 PDF also produced on box**

## 1. Everyday Shell Power Moves
| Command | What it does |
|---------|----------------|
| `!!` | Re-run last command |
| `!$` | Last argument of previous command |
| `cd -` | Jump back to previous directory |
| `pushd /path && popd` | Stack directories; pop returns |
| `mkdir -p a/b/c` | Create nested dirs safely |
| `ls -lah` | Human-readable listing with hidden |
| `du -sh * \| sort -h` | Size of each item, sorted |
| `df -h` | Disk free space |
| `find . -name '*.py'` | Find files by name |
| `rg 'TODO' -n` | Ripgrep search (fast) |
| `history \| rg ssh` | Search command history |
| `ctrl-r` | Interactive history search |
| `alias gs='git status'` | Save keystrokes forever |
| `export PATH="$HOME/bin:$PATH"` | Put personal bins first |
| `chmod +x script.sh` | Make script executable |
| `xargs -P4 -I{} cmd {}` | Parallelize simple loops |

## 2. Git Workflow That Ships
| Command | What it does |
|---------|----------------|
| `git status -sb` | Short status with branch |
| `git add -p` | Stage hunks interactively |
| `git commit -m 'msg'` | Commit with message |
| `git commit --amend --no-edit` | Fix last commit (unpushed) |
| `git pull --rebase` | Update branch cleanly |
| `git push -u origin HEAD` | Push + set upstream |
| `git switch -c feature/x` | Create and switch branch |
| `git switch main` | Switch to main |
| `git restore --staged FILE` | Unstage without losing edits |
| `git restore FILE` | Discard working-tree changes |
| `git stash -u && git stash pop` | Park / restore WIP |
| `git log --oneline --graph -20` | Pretty recent history |
| `git diff main...HEAD` | What this branch changed |
| `git rebase -i HEAD~5` | Clean up last 5 commits |
| `git cherry-pick <sha>` | Apply one commit elsewhere |
| `git bisect start` | Binary-search a regression |

## 3. Debugging & Inspection
| Command | What it does |
|---------|----------------|
| `ps aux \| rg node` | Find a running process |
| `lsof -i :3000` | Who owns a port |
| `curl -I https://example.com` | HTTP headers only |
| `ss -tlnp` | Listening TCP sockets |
| `tail -f /var/log/syslog` | Follow a log live |
| `strace -e openat cmd` | See files a process opens |
| `env \| sort` | Inspect environment |
| `stat FILE` | Detailed file metadata |

## 4. Safety Nets
| Command | What it does |
|---------|----------------|
| `cp -a src dst` | Archive copy (perms + times) |
| `rsync -av --dry-run src/ dst/` | Preview sync before writing |
| `git reflog` | Recover lost commits |
| `git reset --soft HEAD~1` | Undo commit, keep changes |
| `trash FILE` | Soft-delete habit |
| `set -euo pipefail` | Bash: fail fast in scripts |
| `command -v tool` | Check if a binary exists |
| `umask 022` | Sensible default file perms |

## 5. Bonus: 1-Week Practice Checklist
- [ ] Day 1: Alias your top 5 commands; restart shell; use them all day.
- [ ] Day 2: Use `git add -p` on a real change; write a clear commit message.
- [ ] Day 3: Practice ctrl-r / history search instead of retyping.
- [ ] Day 4: Run `du -sh` and clean one directory that surprised you.
- [ ] Day 5: Use `git stash` around an interrupt; pop cleanly later.
- [ ] Day 6: Read `git reflog` once so recovery feels familiar.
- [ ] Day 7: Write a 10-line script with `set -euo pipefail` and `chmod +x`.

## License
Personal use license. You may print and use this pack yourself. Do not redistribute commercially. No warranty - commands can be destructive; understand them before running.
