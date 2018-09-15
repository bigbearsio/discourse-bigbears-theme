# BigBears.IO Discourse Theme

Discourse theme used in https://forums.bigbears.io/

## Development workflow using Discourse Theme Creator

1. Install **discourse_theme** CLI tool.

   1. Install Ruby.

   2. Install [discourse_theme](https://github.com/discourse/discourse_theme)
      from RubyGems: `gem install discourse_theme` (on macOS: `brew install ruby` and restart terminal first or use rvm)

   For more information, see the forum post
   [Discourse Theme CLI (console app to help you build themes)](https://meta.discourse.org/t/discourse-theme-cli-console-app-to-help-you-build-themes/82950)

2. **Fork** this repository and clone it to your computer:

   ```sh-session
   $ git clone https://github.com/<fork_username>/discourse-bigbears-theme
   ```

3. Set up **Discourse Theme Creator** account.

   1. Go to https://theme-creator.discourse.org

   2. Click **Log In** and create an account. You may also sign in using GitHub
      or any other social provider. This should bring you back to Theme Creator
      homepage.

   3. Click **My Themes**.

   4. Click **Import**.

   5. Click **From the web** and enter the URL:

      ```
      https://github.com/<fork_username>/discourse-bigbears-theme
      ```

      Submit the form. This should bring you to a copy of **BigBears.IO** theme.

   6. **Refresh the page** and change the **Color Scheme** to **BigBears.IO**,
      then click the checkmark to confirm color scheme change.

   7. At the bottom of the page, click **Edit Locally**. A modal popup should
      open. Then click the **Retrieve API Key**. This should give you an API
      key. Note the API key, as you will need it in later step.

4. Run the **Discourse Theme CLI** in **watch mode.**

   1. Open a Terminal and `cd` to the folder.

   2. Run **`discourse_theme watch .`**

   3. It will ask: “No site found! Where would you like to synchronize the theme
      to:”

      Answer: `https://theme-creator.discourse.org`

      Then it will ask “Would you like me to store this site name at:
      /Users/$USER/.discourse_theme? (Yes|No).” You can answer `yes` so that
      this question can be skipped in subsequent runs.

   4. It will then ask “No API key found in DISCOURSE_API_KEY env var enter your
      API key:”

      Paste in your **API key.**

      Then it will ask “Would you like me to store this API key in
      /Users/$USER/.discourse_theme? (Yes|No).” You can answer `yes` so that
      this question can be skipped in subsequent runs.

   5. The CLI tool will synchronize the theme to the Theme Creator. You should
      see:

      ```
      Uploading theme from /path/to/repo to https://theme-creator.discourse.org : (done)
      ```

      Keep this tool running. It will automatically re-upload the theme when it
      detects a file change.

5. Preview the theme inside **Theme Creator.**

   1. Go to https://theme-creator.discourse.org

   2. Go to **My Themes** and select **BigBears.IO**.

   3. Click **Preview**.

   4. You will see the preview of the theme.

      With the CLI tool running, you can change the theme files, and the theme
      will be synchronized to Theme Creator automatically. For CSS files,
      changes will be applied on the web page automatically.
      
6. Once you are satisfied with your change, **Commit** and **Push** your changes,
   then create a **Pull Request** on this repository (https://github.com/bigbearsio/discourse-bigbears-theme)
   so that we can review your changes.

   Please add a screenshot of the changes to make it easier for us to review, thanks!
