# RESOURCES.md Format

`RESOURCES.md` is the curated set of trusted sources for this topic. Knowledge for explainers should be drawn from here, not from parametric guesses. Wisdom comes from the communities listed here.

Sources are ranked. The user's **own material in the workspace is the primary source** — teach from it first. Web resources are supplementary: they fill gaps, verify claims, and go deeper. Keep the two groups visibly separate so this priority is never lost.

## Structure

```md
# {Topic} Resources

## Local sources (primary)

The user's own material in this workspace. Teach from these first; cite them by path.

- `./fundamentals/01-overview.md`
  The author's framing of the whole subject. Use for: the load-bearing structure; follow its ordering.
- `./code/trainer.py`
  Working reference implementation. Use for: grounding the practice exercises in real, runnable code.
- `./papers/zatsiorsky-1995.pdf`
  Primary text the user has already gathered. Use for: periodisation, recovery, intensity zones.

_Learning path: `./SYLLABUS.md` defines the intended teaching sequence — follow it for ordering._

## Knowledge (web, supplementary)

Reach for these to fill gaps the local material doesn't cover, or to verify and update claims.

- [Book: _The Science and Practice of Strength Training_ — Zatsiorsky & Kraemer](https://example.com)
  Foundational text on programming and adaptation. Use for: anything to do with periodisation, recovery, intensity zones.
- [Article: "How Much Should I Train?" — Greg Nuckols (Stronger By Science)](https://example.com)
  Evidence-based review of volume landmarks. Use for: weekly set targets per muscle group.

## Wisdom (Communities)

- [r/weightroom](https://reddit.com/r/weightroom)
  High-signal subreddit, moderated against bro-science. Use for: programme critique, plateau troubleshooting.
- Local: Tuesday strength class at {gym name}
  Use for: real-time coaching feedback on lifts.
```

## Rules

- **Local sources rank first.** Catalogue the user's own workspace material under `## Local sources (primary)` and teach from it before reaching for the web. The web is there to fill gaps and verify, not to replace what the user already brought. If a local source turns out to be wrong, flag it to the user rather than silently dropping it.
- **High-trust only (for web).** Prefer primary sources, recognised experts, peer-reviewed work, and communities with strong moderation. If a resource is marketing dressed as education, leave it out.
- **Annotate every entry.** A bare link or path is useless in three months. Add one line: what it covers and when to reach for it.
- **Group by Local / Knowledge / Wisdom.** Mirrors the source priority in [SKILL.md](./SKILL.md). It is fine for a resource to appear in only one group.
- **Note the learning path.** If the workspace contains an intended teaching sequence (a syllabus, numbered subfolders, a "start here" file), record where it lives so future sessions follow the user's intended ordering.
- **Surface gaps explicitly.** If no good resource exists for an area the mission needs, write a `## Gaps` section listing what is missing. This drives future search.
- **Prune ruthlessly.** A resource that turned out to be wrong, shallow, or off-mission should be removed, not buried. Better five sharp sources than thirty mediocre ones.
- **Record community preferences.** If the user has opted out of joining communities, note it here so future sessions don't keep proposing them.
