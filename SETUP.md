# Setting up

You will have your own animated GitHub profile README in about five minutes.

1. **Create your copy.** Click **Use this template**, then **Create a new repository**.
   Name it **exactly your GitHub username** and make it **public**. That name is what makes
   GitHub show the repository's README on your profile.
2. **Run it once.** Open the **Actions** tab, choose **Starforge**, and click **Run workflow**.
   If GitHub asks you to enable workflows first, do that. The first run takes a few minutes: it
   draws five animations. The run also fills in your username and image links, so there is nothing
   to edit by hand.
3. **Look at your profile.** Open `github.com/<your username>`. After the first run your page is
   live, and it refreshes every day on its own.

## Make it yours

- **Pick other presets.** Edit `presets` in `starforge.config.json`. The choices are `galaxy`,
  `tunnel`, `tree`, `atom` and `chess`. If you change which ones you use, change the matching
  `<img>` lines in `README.md` too: each preset's card is `<preset>-card.svg`.
- **Your private contributions.** By default the workflow can only see your public activity. To
  include private contributions, create a personal access token with the `read:user` scope and
  save it as a repository secret named `STARFORGE_TOKEN`.
- **Your own character.** `heroCharacter` points at `assets/character`, which holds the animation
  strip. To use your own, bake one from a rigged 3D model with the scripts in the
  [Starforge repository](https://github.com/ShyneChikwapulo/Starforge) (see its "Hero card"
  section), and replace the files in that folder. Check that your model's licence lets you publish
  renders of it, and replace `ATTRIBUTION.md` with the credit it needs. To drop the character
  entirely, remove `heroCharacter` from the config.
- **Lighter page.** The page is a few megabytes of animation. Lower `frames` or `quality` in the
  config to make it smaller, at some cost in smoothness.

## If something is wrong

- **My profile shows no README.** The repository must be public and named exactly like your
  username. The workflow prints a warning if it is not.
- **The images are broken.** The workflow has not finished yet. Check the Actions tab; the first
  run publishes the images to a branch called `starforge-assets`.
