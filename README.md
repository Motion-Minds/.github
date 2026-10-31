# Motion-Minds/.github

Organization-wide files for [Motion-Minds](https://github.com/Motion-Minds) on GitHub.

| Path | What it is |
|---|---|
| `profile/README.md` | The public organization profile shown on [github.com/Motion-Minds](https://github.com/Motion-Minds). |
| `profile/assets/` | MotionMind logo files used by the profile. Copied from the landing page's `public/brand/`, which copies them from the logo masters, so update them together. |

## Publishing

GitHub only shows the profile when this repository is **public**, named **`.github`**, and owned by the organization. The logo is loaded from `https://raw.githubusercontent.com/Motion-Minds/.github/main/profile/assets/…`, so keep the default branch named `main`.

```bash
gh repo create Motion-Minds/.github --public --source=. --push
```

The other images (the walkthrough GIF) and the badges come from the public [motionmind-video](https://github.com/Motion-Minds/motionmind-video) repository and shields.io.

## Editing

- Write in English, and keep the facts in line with the [motionmind-video README](https://github.com/Motion-Minds/motionmind-video#readme): commands, requirements, the four gates and the QA numbers.
- Only link public repositories. Private ones show visitors a 404.
- Check the rendered result in both the light and dark GitHub themes: the logo switches with `prefers-color-scheme`.
