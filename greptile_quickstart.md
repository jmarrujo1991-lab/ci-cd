> ## Documentation Index
> Fetch the complete documentation index at: https://www.greptile.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# 5-Minute Quickstart

> Set up Greptile AI code reviews in 5 minutes. Connect GitHub or GitLab, configure review triggers, and get automated feedback on your first pull request.

This guide covers GitHub/GitLab setup, repository configuration, and your first automated code review.

## Installation & Setup

GitHub or GitLab users can follow the outlined steps to successfully enable Greptile within their repositories.

[Log in](https://app.greptile.com/login) to your Greptile account or [sign up](https://app.greptile.com/signup) via email, Google, Github, or GitLab.

Ensure you have the required permissions to allow the AI code reviewer access to all or specific repos. Each platform offers a different procedure for integration.

### GitHub App installation

The GitHub app gives Greptile access to your repositories and lets it post reviews on pull requests.

<Steps>
  <Step title="Open Code Providers">
    Go to **Code Providers**. Click <kbd>Connect GitHub Cloud</kbd> or <kbd>Add Provider</kbd>, then select GitHub.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/code-providers.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=a2063769204adea7e190186ec1ed41b8" alt="GitHub installation page listing accounts and organizations for Greptile Apps" width="2280" height="1408" data-path="images/code-providers.png" />

      <figcaption>Open the Greptile Apps installer in GitHub</figcaption>
    </Frame>
  </Step>

  <Step title="Choose a GitHub account or organization">
    In GitHub, choose the account or organization where you want to install **Greptile Apps**. Use **Configure** for an existing installation.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/github-install-account-selection.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=40fbd37eb1be3104f34817f0ac1933dc" alt="GitHub Greptile Apps install page with account and organization options" width="2270" height="1614" />

      <figcaption>Choose a GitHub account or organization</figcaption>
    </Frame>
  </Step>

  <Step title="Grant repository access">
    Select which repositories GitHub lets Greptile access:

    * **All repositories**: Grant access to all current and future repositories in the account or organization.
    * **Only select repositories**: Grant access only to selected repositories. Select at least one repository.

    Click <kbd>Install</kbd> or <kbd>Update access</kbd>.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/github-install-repository-access.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=f2f557a8580e72d2b4fd5c3ebf23a3ba" alt="GitHub App install page with repository access and permissions" width="1950" height="1816" />

      <figcaption>Install Greptile Apps in GitHub</figcaption>
    </Frame>
  </Step>

  <Step title="Link the GitHub organization in Greptile">
    After you click <kbd>Install</kbd>, GitHub automatically returns you to Greptile. Select the GitHub organization, then click <kbd>Link</kbd>.

    You can add more organizations later from **Code Providers**.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/github-link-organization.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=c4024d33e9505cec64f6e2da5246e625" alt="Greptile onboarding screen for selecting a GitHub organization to link" width="2758" height="1698" />

      <figcaption>Link a GitHub organization to Greptile</figcaption>
    </Frame>

    <Tip>
      If your GitHub organization is missing from this list, see [Troubleshooting: GitHub organization not listed](/troubleshooting/common-issues#github-organization-not-listed).
    </Tip>
  </Step>

  <Step title="Enable repositories for review">
    Select the repositories you want Greptile to review, then click <kbd>Enable</kbd>.

    Use <kbd>Enable All</kbd> to turn on all repositories that GitHub granted access to.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/github-enable-repositories.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=a47dd73e151fd66665be85375db8a2c0" alt="Greptile onboarding screen for enabling GitHub repositories for review" width="2758" height="1698" />

      <figcaption>Enable GitHub repositories for review</figcaption>
    </Frame>
  </Step>
</Steps>

### GitLab Integration

Greptile supports GitLab service account personal access tokens, group access tokens, and project access tokens. We recommend a service account because its credentials are not tied to a person. The service account must have the **Developer** role for the groups or projects Greptile will review. Its personal access token must have the `api` scope.

<Steps>
  <Step title="Open GitLab integration">
    Go to **Code Providers** in Greptile and click **Add Provider**, then select GitLab. Greptile shows the token requirements and a field for the generated token.

    <Frame>
      <img src="https://mintcdn.com/greptile/KNJdf4DwzT1-8n6L/images/gitlab-integration-token-modal.png?fit=max&auto=format&n=KNJdf4DwzT1-8n6L&q=85&s=10886a71b2a2ad140d66f4601e937e9d" alt="Greptile modal with GitLab integration token instructions" width="2418" height="1610" />

      <figcaption>Add GitLab integration in Greptile</figcaption>
    </Frame>
  </Step>

  <Step title="Create or select a service account">
    In GitLab, open the group that contains the projects Greptile needs to review, then go to **Settings** → **Service accounts**. Create a service account or select an existing one. Add it to every group or project Greptile needs to access with the **Developer** role.

    See [GitLab's service account documentation](https://docs.gitlab.com/user/profile/service_accounts/) for details.
  </Step>

  <Step title="Create the service account personal access token">
    From the service account's menu, select **Manage access tokens**, then **Add new token**. Create a personal access token with:

    * **Token name**: `Greptile`
    * **Scope**: `api`
    * **Expiration date**: follow your GitLab policy

    <Note>
      You can also use a group or project access token. Create it under **Settings** → **Access tokens** with the **Developer** role and `api` scope.
    </Note>
  </Step>

  <Step title="Copy the generated token">
    Copy the token. GitLab only shows it once.
  </Step>

  <Step title="Submit the token in Greptile">
    Paste the token into the GitLab integration modal, then click <kbd>Submit</kbd>.

    <Frame>
      <img src="https://mintcdn.com/greptile/KNJdf4DwzT1-8n6L/images/gitlab-integration-token-modal.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=10886a71b2a2ad140d66f4601e937e9d" alt="Greptile GitLab integration modal with token field and Submit button" width="2418" height="1610" />

      <figcaption>Submit the GitLab token in Greptile</figcaption>
    </Frame>
  </Step>

  <Step title="Configure the webhook in GitLab">
    Greptile generates the details you need to create a GitLab webhook — a **URL**, a **secret token**, and the required **triggers**. The webhook is what lets Greptile review merge requests automatically.

    <Frame>
      <img src="https://mintcdn.com/greptile/n1DJD5Cq07WZmn2N/images/greptile-gitlab-details-for-webhook.png?fit=max&auto=format&n=n1DJD5Cq07WZmn2N&q=85&s=13c4e5cb641dc44e5553d11678d97409" alt="Greptile-generated GitLab webhook details: URL, secret token, and triggers" width="1336" height="331" />

      <figcaption>Webhook details generated by Greptile</figcaption>
    </Frame>

    1. In GitLab, open your project or group, then go to **Settings** → **Webhooks** → **Add new webhook**.
    2. Fill in the **URL** and **Secret token** from Greptile, and enable the required **triggers**: **Comments**, **Issues events**, **Merge request events**, and **Emoji events**.
    3. Click <kbd>Add webhook</kbd>.
    4. Back in Greptile, click <kbd>Done, I've made the changes</kbd>.
  </Step>

  <Step title="Link the GitLab group">
    Select the GitLab group, then click <kbd>Link</kbd>.

    <Frame>
      <img src="https://mintcdn.com/greptile/KNJdf4DwzT1-8n6L/images/gitlab-link-group.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=bd70cb8eb84c8d03e890a1a194480cba" alt="Greptile onboarding screen for selecting a GitLab group to link" width="2450" height="1552" />

      <figcaption>Link a GitLab group to Greptile</figcaption>
    </Frame>
  </Step>

  <Step title="Enable repositories for review">
    Select the GitLab repositories you want Greptile to review, then click <kbd>Enable</kbd>.

    Use <kbd>Enable All</kbd> to turn on every listed repository.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/gitlab-enable-repositories.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=400835f09108912e80b2e630b89ce5fa" alt="Greptile onboarding screen for enabling GitLab repositories for review" width="2456" height="1568" />

      <figcaption>Enable GitLab repositories for review</figcaption>
    </Frame>
  </Step>
</Steps>

### Repository Selection & Configuration

The following configuration steps are common to GitHub and GitLab:

<Steps>
  <Step title="Enable repository indexing by Greptile">
    1. Go to your team's **Repositories** page
    2. Click **Manage Repos** (or **Enable Repositories** if no repos are enabled yet)
    3. Select the repos you want reviewed, then click **Enable Repos** (or use **Enable All**)

    To automatically enable future repos, go to **Code Review Settings** and toggle **Auto-enable New Repos**.

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/repositories-manage-repos-modal.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=43468002417a3e1c4164037aab2eb01e" alt="Repo Settings modal for enabling and disabling repositories" width="2192" height="1338" />

      <figcaption>Enable or disable repositories</figcaption>
    </Frame>
  </Step>

  <Step title="Configure PR Summary">
    Customize how Greptile summarizes pull requests:

    * **PR Summary**: Include a text summary of the changes
    * **Confidence Score**: Show confidence levels for each PR
    * **Issue Table**: Show important changed files with ratings
    * **Sequence Diagram**: Add a diagram of the changes

    [Learn more about PR summaries →](/code-review/first-pr-review#pr-summary)

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/code-review-pr-summary-settings.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=54f606f30ef8e5f3dcf59144700bdb50" alt="PR Summary settings in Code Review Settings" width="3164" height="2062" />

      <figcaption>PR summary settings</figcaption>
    </Frame>
  </Step>

  <Step title="Control Review Behavior">
    Configure what Greptile comments on in **Code Review Settings**:

    * **Strictness Level**: Adjust how often Greptile comments
    * **Auto-review on new commits**: Review new commits after a PR is opened
    * **Review draft pull requests**: Review drafts before they are marked ready
    * **File change limit**: Set the largest PR Greptile reviews automatically

    [Learn more about controlling nitpickiness →](/code-review/controlling-nitpickiness)

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/code-review-review-trigger-settings.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=e0cbacc4fd717b2e4d3fc5bdf1347637" alt="When Greptile Reviews settings with strictness level and review trigger options" width="3164" height="2062" />

      <figcaption>When Greptile reviews</figcaption>
    </Frame>
  </Step>

  <Step title="Add Filters">
    Set when Greptile comments in **Code Review Settings** under **Greptile Comments**:

    * **Labels**: Only review PRs with specific labels (e.g., "needs-review")
    * **Authors**: Include/exclude specific developers or bots
    * **Branches**: Target specific branches (e.g., main, develop)
    * **Keywords**: Trigger on PR title/description keywords

    [Learn more about triggers →](/code-review/controlling-nitpickiness#trigger-configuration)

    <Frame>
      <img src="https://mintcdn.com/greptile/8PzYIxBdzrtuAyXk/images/code-review-add-filter.png?fit=max&auto=format&n=8PzYIxBdzrtuAyXk&q=85&s=0410aaf1001eb792ba3e52a18c131ad3" alt="Greptile Comments filter settings with Add Filter button" width="3154" height="1046" />

      <figcaption>Add review filters</figcaption>
    </Frame>
  </Step>
</Steps>

After a repository has been indexed (typically 1-2 hours for very large repos), any new pull/merge request will initiate automated code reviews by Greptile.

***

## Create Your First Test PR

Try Greptile on a test pull request to see it in action:

<Steps>
  <Step title="Create a pull request">
    Make a test PR to your indexed repo with some code changes.
  </Step>

  <Step title="Wait for review (~3 minutes)">
    Greptile analyzes your PR with full codebase context and posts a comprehensive review.

    <Frame>
      <img src="https://mintcdn.com/greptile/pPDrEYn7_-Bi_2Mg/images/greptile-pr-comment.png?fit=max&auto=format&n=pPDrEYn7_-Bi_2Mg&q=85&s=b8e0b17c33779d085e4952c302952b43" alt="PR Summary" width="931" height="827" />

      <figcaption>Greptile PR Comment</figcaption>
    </Frame>
  </Step>

  <Step title="Review the feedback">
    You'll see a summary of changes, inline comments on issues, and suggested fixes.

    <Frame>
      <img src="https://mintcdn.com/greptile/sJeefWhR1h6iqsSa/images/pr-summary.png?fit=max&auto=format&n=sJeefWhR1h6iqsSa&q=85&s=6464ca32169feabc1024e9bebd94d643" alt="pr summary" width="914" height="486" />

      <figcaption>PR Summary</figcaption>
    </Frame>
  </Step>
</Steps>

When issues are spotted, Greptile suggests potential code fixes:

<Frame>
  <img src="https://mintcdn.com/greptile/sJeefWhR1h6iqsSa/images/issue-fixes.png?fit=max&auto=format&n=sJeefWhR1h6iqsSa&q=85&s=0a0084ab113ad1bb8c39c767c548b44e" alt="code fixes" width="865" height="287" />

  <figcaption>Suggest code fixes</figcaption>
</Frame>

<Note>
  You can trigger a code review manually by tagging **@greptileai** with a comment. This is helpful for reviewing older PRs from before Greptile was integrated.
</Note>

***

## What's next?

* **For developers**: Learn how to [work with Greptile reviews →](/code-review/developer-essentials)
* **For team admins**: Set up [organizations and teams →](/code-review/team-setup-basics)
* **Deep dive**: Understand the [anatomy of a review →](/code-review/first-pr-review)
