# Import Fidelity Rule

Use this when importing existing chats, documents, transcripts, research dumps, strategy notes, or mixed notes.

## Fidelity Modes

Choose one mode before or during the import summary:

| Mode | Use When |
| --- | --- |
| `Verbatim Preservation` | Exact wording, chronology, quotes, commitments, or nuance may matter later. Preserve source material in `00-import/source-material.md` or point to a stable source file. |
| `Structured Faithful Summary` | The project needs broad context, claims, alternatives, and questions, but exact wording is unlikely to matter. Preserve structure and source references. |
| `Decision-Focused Summary` | The project needs only decision-relevant conclusions, options, risks, assumptions, and open questions. Omit low-value narrative and log the compression risk. |

## Required Import Summary Fields

Record in `00-import/import-summary.md`:

- Chosen fidelity mode.
- Why that mode was chosen.
- What was preserved.
- What was omitted.
- Remaining risk.
- Source pointer when exact wording may matter later and source material is available.

Old chat conclusions remain candidate decisions until the user confirms them.

Do not require every import to preserve huge verbatim transcripts. Make the fidelity choice conscious, record the risk, and keep progressive file creation intact.
