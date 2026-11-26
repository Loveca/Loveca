# Hi, I'm Loveca

**Backend & agent infrastructure engineer** · Peking University

Contributing to [bytedance/deer-flow](https://github.com/bytedance/deer-flow) — [6 merged PRs](https://github.com/bytedance/deer-flow/pulls?q=is%3Apr+is%3Amerged+author%3ALoveca), 2 in review.

> Previously engineered at **Amazon**, **Alibaba (Taobao & Tmall)**, **Tencent**, and **Xiaohongshu** — trading systems, database infra, and GPU inference.

## Open source: DeerFlow

[DeerFlow](https://github.com/bytedance/deer-flow) is ByteDance's open-source long-horizon agent harness: LangGraph-driven runs with sandboxes, memory, subagents, skills, and an IM gateway. My merged work, by area:

- **Agent runtime** — start subagent execution timeouts at admission, so queued subagents are no longer charged for wait time ([#8356](https://github.com/bytedance/deer-flow/pull/8356)); authorize local-file acceptance checks before metadata probes ([#8595](https://github.com/bytedance/deer-flow/pull/8595)).
- **Goal synthesis for IM channels** — `/goal from-chat`: turn a multi-turn conversation into an executable goal, with PII redaction before truncation, CAS-guarded checkpoint reservation, and explicit 409/403 failure modes for concurrent writes and unauthorized calls ([#8200](https://github.com/bytedance/deer-flow/pull/8200), +2,071 lines / 19 files).
- **Skill self-evolution** — an evidence-gated propose → evaluate → apply → rollback example: deterministic static evaluation on frozen skill bundles, content-addressed revisions, and an append-only rollback chain ([#7984](https://github.com/bytedance/deer-flow/pull/7984)).
- **Channels & security** — parse Feishu post attachments from the top-level files array ([#8190](https://github.com/bytedance/deer-flow/pull/8190)); return explicit errors for malformed URLs in the SSRF guard ([#8079](https://github.com/bytedance/deer-flow/pull/8079)).

[All merged PRs →](https://github.com/bytedance/deer-flow/pulls?q=is%3Apr+is%3Amerged+author%3ALoveca) · [In review →](https://github.com/bytedance/deer-flow/pulls?q=is%3Apr+is%3Aopen+author%3ALoveca)

Larger features in flight (temporarily closed under the project's open-PR limit; reopening as slots free up):

- **Incognito chats** — a storage boundary that keeps incognito threads out of persistent memory and history ([#8516](https://github.com/bytedance/deer-flow/pull/8516), +6,658 lines / 122 files).
- **Sidebar reordering** — user-defined entry order with overflow entries collapsed into a More group ([#8315](https://github.com/bytedance/deer-flow/pull/8315), +3,229 lines / 22 files).
- **Context window composition** — a live breakdown of what occupies the model's context, right in the composer ([#8237](https://github.com/bytedance/deer-flow/pull/8237), +2,725 lines / 34 files).

Also writing [tiny-claude-code](https://github.com/Loveca/tiny-claude-code), a 21-chapter build-it-yourself guide to the internals of a coding agent — the same layer I work on upstream.