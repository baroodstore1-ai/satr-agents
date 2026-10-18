# Duo Agent Platform evidence: first run of all 5 flows (Oct 18, 2026, ~10:56–11:05 AM MDT)

| Flow | Trigger | Session | Outcome |
|---|---|---|---|
| Satr Bug-to-Regression | @mention on issue #2 | [9653489](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653489) | Reproduced the glued Arabic comma bug, opened [!2](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/merge_requests/2) with rule fix + golden case; bilingual reply. Pipeline green. |
| Satr MR Guardian | assigned as reviewer on [!1](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/merge_requests/1) | [9653498](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653498) | 4 bilingual diff notes (Latin ?, tatweel, Latin-at-edge, !), auto-fix commit 86cc68b, verdict table. |
| Satr Pipeline Medic | failed pipeline 2960557469 (demo/failing-pipeline) | [9653503](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653503) | Diagnosed the ؟→، regression in src/satr.js, opened fix MR !4 (green). Also ran on !1's subtitle-gate failure ([9653530](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653530)): classified as content, not code; no code change. |
| Satr Compliance Steward | @mention on [!3](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/merge_requests/3) | [9653509](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653509) | Blocked the change that broadened Pipeline Medic's toolset (separation of duties), with owners per check. |
| Satr Release Scribe | @mention on issue #3 | [9653512](https://gitlab.com/gitlab-ai-hackathon/transcend-october-2026/43481824/showcase/-/automate/agent-sessions/9653512) | Drafted EN/AR notes and paused at the human gate. The draft wrongly counted open MRs as merged, so the maintainer **rejected** it. The flow was fixed (v1.1.0). |

Fixes made from these runs:
- **pipeline-medic v1.1.0:** dedupe branch+MR pipelines for the same commit (the first run opened duplicate !5/!6); don't open revert MRs on deliberate permission-change MRs, leave a note instead.
- **release-scribe v1.1.0:** include only MRs whose state is merged into the default branch, and commits that are on the default branch itself.
- **.gitlab-ci.yml:** `*.srt` and `*.vtt` added to the change rules, because a subtitle-only MR update produced an empty pipeline.

Cleanup: closed !3–!6, deleted demo/failing-pipeline, demo/medic-faster-fixes and duo-medic/* branches. main stays green.
Files: issue_*.json, mr_*.json, notes_all.json (every agent comment), sessions.json, release_scribe_events.json (session checkpoint), flow_update_*.json.
