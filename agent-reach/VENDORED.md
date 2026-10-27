# Vendored: Panniantong/Agent-Reach (skill only)

- Source: https://github.com/Panniantong/Agent-Reach
- Commit: 14c213405669414492bda0f8d52cc6531d062c45 (v1.6.0)
- License: MIT (see LICENSE)

Only the agent skill is vendored: `skill/SKILL.md` is upstream `agent_reach/skill/SKILL_en.md`
with `{{VERSION}}` set to 1.6.0 and `{{CHANNEL_TABLE}}` replaced by a pointer to
`agent-reach channels`. `skill/references/` is copied as is (partly in Chinese).
It is exposed to Claude Code through the symlink `/.claude/skills/agent-reach`.

The skill drives the `agent-reach` CLI, which is not vendored. Install it per upstream
`docs/install.md` (from the GitHub release, never the unrelated `agent-reach` package on PyPI):

    uv tool install https://github.com/Panniantong/Agent-Reach/releases/latest/download/agent-reach.zip
    agent-reach setup

To update: re-clone upstream and redo the copy and substitutions above.
