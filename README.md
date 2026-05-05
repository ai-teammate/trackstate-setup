# TrackState.AI Setup

This repository is the lightweight fork-and-run template for TrackState.AI.

Fork this repository to your own GitHub account or organization, enable GitHub Pages with **Source: GitHub Actions**, then run **Install / Update TrackState** from the Actions tab. The workflow downloads the selected version of `IstiN/trackstate`, builds the Flutter SPA for your fork, and deploys it to GitHub Pages.

## First install

1. Fork `IstiN/trackstate-setup`.
2. Open **Settings > Pages** in your fork.
3. Set **Build and deployment > Source** to **GitHub Actions**.
4. Open **Actions > Install / Update TrackState**.
5. Click **Run workflow**.
6. Keep `trackstate_ref` as `main` for latest, or enter a tag/commit SHA for a fixed version.

Your app will be published at:

```text
https://<owner>.github.io/<repo>/
```

## Updating TrackState

Run the same **Install / Update TrackState** workflow again:

- `main` installs the latest source from `IstiN/trackstate`;
- a tag such as `v0.1.0` installs that release line;
- a commit SHA pins the app to an exact build.

The workflow does not commit generated web assets to this repository. It publishes the compiled app as a Pages artifact, keeping the fork clean and focused on tracker data/configuration.

## Tracker data

The demo project is stored in `DEMO/` using Git-native markdown and JSON files. You can replace it with your own project while preserving the same structure.

```text
DEMO/
  project.json
  config/
  DEMO-1/
    main.md
    DEMO-2/
      main.md
      acceptance_criteria.md
      comments/
      DEMO-3/
        main.md
```

Large attachments should be stored through Git LFS. `.gitattributes` already tracks common binary formats.
