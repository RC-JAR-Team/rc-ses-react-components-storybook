# rc-ses-react-components Storybook

This repository hosts the public Storybook build for `registrucentras/rc-ses-react-components` without modifying the source repository.

## Required GitHub configuration

Add these repository variables:

- `SOURCE_REPOSITORY=registrucentras/rc-ses-react-components`
- `SOURCE_BRANCH=develop`

Add this repository secret:

- `SOURCE_REPO_TOKEN`

`SOURCE_REPO_TOKEN` must be a GitHub token that can read the private source repository.

## GitHub Pages

Enable GitHub Pages in this public repository and set the source to `GitHub Actions`.

## Deployment behavior

The workflow:

- checks out the private source repository from `develop`
- runs `npm ci`
- runs `npm run storybook-build`
- publishes `storybook-static` to GitHub Pages

It can be run manually and also runs every 30 minutes to pick up new `develop` changes.
