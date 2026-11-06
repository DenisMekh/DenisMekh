# Profile README maintenance

The profile is the root `README.md`. It is written in English for recruiters and peers.

## Visual assets

- `assets/header-{light,dark}.svg` — original vector header with a system-flow motif.
- `assets/stack/<technology>-{light,dark}.svg` — individual technology tiles (actual brand icon glyph, name, short role label).
- The four-icon group layout wraps on narrow screens instead of shrinking a whole strip.
- Icon glyphs come from [Simple Icons](https://github.com/simple-icons/simple-icons) (CC0) and [Devicon](https://github.com/devicons/devicon) (MIT; gRPC). The tiles and color palette are original. See `assets/stack/ICON-LICENSES.md`.
- All icons are local, with no runtime CDN dependency. Update both theme variants together and review mobile wrapping.

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
