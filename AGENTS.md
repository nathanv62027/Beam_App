- After each request, add an entry to prompts.md: what I asked, what you changed, and whether it worked.

# Project layout

This is a single-file web app published with GitHub Pages. Keep `index.html` at the project root so GitHub Pages can serve it. The other project-level documents also stay at the root:

- `AGENTS.md`: project layout and working instructions.
- `spec.md`: requirements and behavior for the app.
- `prompts.md`: request, change, and outcome log.

Put all other new files in the numbered folder that matches their purpose. Do not add miscellaneous files to the root.

- `00_planning/`: planning notes and sketches.
- `01_data/`: data files used by the project.
- `02_validation/`: hand calculations and test cases.
- `03_output/`: screenshots and exported results.

## Commit workflow

After completing and verifying a user-requested change, automatically commit only the files changed for that request. Leave unrelated or pre-existing changes untouched, and do not commit when the user asks not to. Include the required Copilot co-author trailer in commit messages.