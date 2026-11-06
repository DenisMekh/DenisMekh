# Profile README maintenance

The profile is the root `README.md`. It is written in English for recruiters and peers.

## Visual assets

- `assets/header-{light,dark}.svg` — original vector header with a system-flow motif.
- `assets/stack-backend-{light,dark}.svg` — compact, custom monogram tiles for backend and messaging.
- `assets/stack-platform-{light,dark}.svg` — custom monogram tiles for data and infrastructure.
- All six files are original SVG artwork (no copied logo assets or remote icon requests).
- Update light and dark variants together. Check legibility at mobile widths.

## Activity cards

The four `profile/*.svg` cards are automatically refreshed via
`.github/workflows/profile-stats.yml` on a daily schedule (04:29 UTC),
on selected pushes, and manually through GitHub Actions. The placeholder
versions are only for the first PR preview; the workflow replaces them with
real stats when it runs successfully.

The stats action is pinned by commit and uses the repository's `GITHUB_TOKEN`,
not a personal access token. Its public repository language breakdown
is not a measure of professional skill or private employer work.

If metrics do not refresh:
1. Check the latest **Refresh profile statistics** workflow run in Actions.
2. Confirm Actions and write permissions are enabled for this repository.
3. Re-run the workflow manually.
4. Check whether scheduled actions were auto-disabled for inactivity.

## Contribution animation

The existing `.github/workflows/snake.yml` already publishes two SVGs
to the `output` branch. The README links to them using
`raw.githubusercontent.com`; it does not create an additional snake workflow.

## Content

- Keep T-Bank statements general; never copy private source or internal diagrams.
- Keep featured projects limited to public, inspectable work.
- If tech stack or project descriptions change, update `README.md`.
- Validate image paths, both themes, links, and mobile display before merging.
