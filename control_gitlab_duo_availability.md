# Control GitLab Duo availability

{{< details >}}

- Tier: Premium, Ultimate
- Add-on: GitLab Duo Core, Pro, or Enterprise
- Offering: GitLab.com, GitLab Self-Managed

{{< /details >}}

{{< history >}}

- [Settings to turn AI features on and off introduced](https://gitlab.com/groups/gitlab-org/-/epics/12404) in GitLab 16.10.
- [Settings to turn AI features on and off added to the UI](https://gitlab.com/gitlab-org/gitlab/-/issues/441489) in GitLab 16.11.

{{< /history >}}

GitLab Duo is on by default.
GitLab Duo includes a [set of features](feature_summary.md).

You can turn GitLab Duo on or off:

- On GitLab.com: For top-level groups, other groups or subgroups, and projects.
- On GitLab Self-Managed: For instances, groups or subgroups, and projects.
- On GitLab Dedicated: Administrators can also lock specific subgroups to **Always off**
  so that users with the Owner role cannot enable GitLab Duo in those subgroups.

## Lock GitLab Duo on

{{< history >}}

- [Introduced](https://gitlab.com/groups/gitlab-org/-/work_items/21844) in GitLab 19.1.

{{< /history >}}
# Get started with GitLab Duo

GitLab Duo is an AI-native assistant that helps you throughout your planning, development, and security workflow.
GitLab Duo includes features like Code Suggestions and Code Explanation,
which help you write, review, and edit code.

## Step 1: Ensure you have access to GitLab Duo

GitLab Duo requires setup by your administrator, group, or project owner.

If you have issues accessing GitLab Duo features, your administrators
can check the health of the installation.

For more information, see:

- [Turn on GitLab Duo](../gitlab_duo/turn_on_off.md).
- [Health check details](../../administration/gitlab_duo/configure/_index.md#run-a-health-check-for-gitlab-duo).

## Step 2: Try GitLab Duo Chat in the UI

To get started, try using Chat in the GitLab UI.

Go to a project and in the upper-right corner, select the button for **GitLab Duo Chat**.
If this button is available, it means everything is configured properly.
Try asking Chat a question about a specific issue or merge request, or about GitLab in general.

For more information, see:

- [GitLab Duo Non-Agentic Chat](../gitlab_duo_chat/_index.md).

## Step 3: Try other GitLab Duo features

GitLab Duo is available throughout your workflow. From planning sprints to
troubleshooting CI/CD pipelines, from writing test cases to resolving security threats,
GitLab Duo can help you in a variety of ways.

The features you have access to might differ, depending on your subscription.

For more information, see:

- [A decision tree, to help you decide which GitLab Duo features match your workflow](../gitlab_duo/_index.md).
- [The complete list of GitLab Duo features](../gitlab_duo/feature_summary.md).
- [How to turn on GitLab Duo features that are still in development](../gitlab_duo/turn_on_off.md#turn-on-beta-and-experimental-features).

## Step 4: Prepare to use GitLab Duo in your IDE

Now try GitLab Duo features in your IDE. In VS Code and other editors, you can use
features like GitLab Duo Chat, the software development flow, and Code Suggestions.

To get started, install an extension and authenticate with GitLab.

For more information, see:

- [Set up the extension for VS Code](../../editor_extensions/visual_studio_code/setup.md).
- [Set up the extension for JetBrains](../../editor_extensions/jetbrains_ide/setup.md).
- [Set up the extension for Visual Studio](../../editor_extensions/visual_studio/setup.md).
- [Set up the extension for Neovim](../../editor_extensions/neovim/setup.md).
- [Use the Web IDE](../project/web_ide/_index.md).

## Step 5: Start using IDE features

Finally, test GitLab Duo in your IDE.

- Code Suggestions recommends code as you type.
- Chat is available to ask questions about your code or anything else you need.
- The software development flow performs tasks on your behalf.

You can choose the development languages you want suggestions for.

For more information, see:

- [Supported extensions and languages](../project/repository/code_suggestions/supported_extensions.md).
- [Turn on Code Suggestions](../project/repository/code_suggestions/set_up.md#turn-on-code-suggestions).
- [Troubleshoot GitLab for VS Code](../../editor_extensions/visual_studio_code/troubleshooting.md).
- [Troubleshoot the GitLab Duo plugin for JetBrains IDEs](../../editor_extensions/jetbrains_ide/jetbrains_troubleshooting.md).
- [Troubleshoot GitLab for Visual Studio](../../editor_extensions/visual_studio/visual_studio_troubleshooting.md).
- [Troubleshoot the GitLab plugin for Neovim](../../editor_extensions/neovim/neovim_troubleshooting.md).


Turn GitLab Duo on for all users, regardless of group or project settings.

When you set GitLab Duo availability to **Always on**,
experiment and beta features are not automatically turned on.
To use experiment and beta features, you must
[turn them on separately](#turn-on-beta-and-experimental-features).

{{< tabs >}}

{{< tab title="On GitLab.com" >}}

Prerequisites:

- The Owner role for the top-level group.

To lock GitLab Duo on for a top-level group:

1. In the top bar, select **Search or go to** and find your top-level group.
1. In the left sidebar, select **Settings** > **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select **Always on**.
1. Select **Save changes**.

GitLab Duo is locked on for all subgroups and projects.
Users with the Owner role for a subgroup or project cannot turn GitLab Duo off.

{{< /tab >}}

{{< tab title="On GitLab Self-Managed" >}}

Prerequisites:

- Administrator access.

To lock GitLab Duo on for an instance:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select **Always on**.
1. Select **Save changes**.

GitLab Duo is locked on for all groups, subgroups, and projects.
Users with the Owner role for a group, subgroup, or project cannot turn GitLab Duo off.

{{< /tab >}}

{{< /tabs >}}

## Lock GitLab Duo off for selected subgroups

{{< details >}}

- Tier: Ultimate
- Offering: GitLab Dedicated, GitLab Dedicated for Government

{{< /details >}}

{{< history >}}

- [Introduced](https://gitlab.com/groups/gitlab-org/-/work_items/22389) in GitLab 19.2.

{{< /history >}}

As a GitLab Dedicated administrator, you can lock specific subgroups to
**Always off** for GitLab Duo and GitLab Duo Agent Platform.
Users with the Owner role in those subgroups cannot enable GitLab Duo,
while other subgroups remain under owner control.

The lock applies to the subgroup and all its descendant groups and projects.
Users with the Owner role for the subgroup or its descendants cannot change this setting.
Affected owners see a message that GitLab Duo is locked by a parent group.

Only one lock can exist in any chain of ancestor and descendant groups.
When you lock a subgroup:

- If an ancestor group already has an lock, the lock is not applied.
  You must [clear the lock](#clear-the-lock-for-a-subgroup) from the ancestor group first.
- If one or more descendant subgroups already have admin locks, you are prompted to confirm.
  When you confirm, the locks on those descendant subgroups are cleared,
  and the lock is applied to the subgroup you selected.

### Lock a subgroup

Prerequisites:

- Administrator access on a GitLab Dedicated instance.

To lock GitLab Duo off for a subgroup:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **GitLab Duo**.
1. In the **Namespace availability overrides** section, find the subgroup.
1. In the row for the subgroup, under **GitLab Duo availability**, select **Always off**.

### Clear the lock for a subgroup

Prerequisites:

- Administrator access on a GitLab Dedicated instance.

To clear the admin lock for a subgroup:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **GitLab Duo**.
1. In the **Namespace availability overrides** section, find the subgroup.
1. In the row for the subgroup, select **Reset**.

The subgroup returns to the instance default.
Users with the Owner role for the subgroup can now control GitLab Duo availability.

## Turn GitLab Duo on or off

### On GitLab.com

#### For a top-level group

Prerequisites:

- The Owner role for the top-level group.

To change GitLab Duo availability for a top-level group:

1. In the top bar, select **Search or go to** and find your top-level group.
1. Select **Settings** > **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select an option.
1. Select **Save changes**.

GitLab Duo availability changes for all subgroups and projects.

#### For a group or subgroup

Prerequisites:

- The Owner role for the group or subgroup.

To change GitLab Duo availability for a group or subgroup:

1. In the top bar, select **Search or go to** and find your group or subgroup.
1. Select **Settings** > **General**.
1. Expand **GitLab Duo features**.
1. Under **GitLab Duo availability**, select an option.
1. Select **Save changes**.

GitLab Duo availability changes for all subgroups and projects.

#### For a project

Prerequisites:

- The Maintainer or Owner role for the project.

To change GitLab Duo availability for a project:

1. In the top bar, select **Search or go to** and find your project.
1. In the left sidebar, select **Settings** > **General**.
1. Expand **GitLab Duo**.
1. Turn the **GitLab Duo** toggle on or off.
1. Select **Save changes**.

### On GitLab Self-Managed

#### For an instance

Prerequisites:

- Administrator access.

To change GitLab Duo availability for an instance:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select an option.
1. Select **Save changes**.

#### For a group or subgroup

Prerequisites:

- The Owner role for the group or subgroup.

To change GitLab Duo availability for a group or subgroup:

1. In the top bar, select **Search or go to** and find your group or subgroup.
1. Select **Settings** > **General**.
1. Expand **GitLab Duo features**.
1. Under **GitLab Duo availability**, select an option.
1. Select **Save changes**.

GitLab Duo availability changes for all subgroups and projects.

#### For a project

Prerequisites:

- The Maintainer or Owner role for the project.

To change GitLab Duo availability for a project:

1. In the top bar, select **Search or go to** and find your project.
1. In the left sidebar, select **Settings** > **General**.
1. Expand **GitLab Duo**.
1. Turn the **GitLab Duo** toggle on or off.
1. Select **Save changes**.

### For earlier GitLab versions

For information on how to turn GitLab Duo on or off in earlier GitLab versions, see
[control GitLab Duo availability for earlier GitLab versions](turn_on_off_earlier.md).

## Turn GitLab Duo Core on or off

{{< history >}}

- [Introduced](https://gitlab.com/gitlab-org/gitlab/-/issues/538857) in GitLab 18.0.
- GitLab Duo availability settings and group, subgroup, and project controls [added](https://gitlab.com/gitlab-org/gitlab/-/issues/551895) in GitLab 18.2.
- GitLab Duo Non-Agentic Chat [added](https://gitlab.com/gitlab-org/gitlab/-/merge_requests/201721) to GitLab Duo Core in GitLab 18.3.

{{< /history >}}

GitLab Duo Core is included with Premium and Ultimate subscriptions.

- If you are an existing customer from GitLab 17.11 or earlier, you must turn on features for GitLab Duo Core.
- If you are a new customer in GitLab 18.0 or later, GitLab Duo Core is automatically turned on and no further action is needed.

If you were an existing customer with a Premium or Ultimate subscription before May 15, 2025,
when you upgrade to GitLab 18.0 or later, to use GitLab Duo Core, you must turn it on.

### On GitLab.com

Prerequisites:

- The Owner role for the top-level group.

To change GitLab Duo Core availability for a top-level group:

1. In the top bar, select **Search or go to** and find your top-level group.
1. Select **Settings** > **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select an option.
1. Under **GitLab Duo Core**, select or clear the **Turn on features for GitLab Duo Core** checkbox.
   If you selected **Always off** for GitLab Duo availability, you cannot access
   this setting.
1. Select **Save changes**.

It might take up to 10 minutes for the change to take effect.

### On GitLab Self-Managed

Prerequisites:

- Administrator access.

To change GitLab Duo Core availability for an instance:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **GitLab Duo**.
1. Select **Change configuration**.
1. Under **GitLab Duo availability**, select an option.
1. Under **GitLab Duo Core**, select or clear the **Turn on features for GitLab Duo Core** checkbox.
   If you selected **Always off** for GitLab Duo availability, you cannot access
   this setting.
1. Select **Save changes**.

## Turn on beta and experimental features

GitLab Duo features that are experimental and beta are turned off by default.
These features are subject to the [Testing Agreement](https://handbook.gitlab.com/handbook/legal/testing-agreement/).

### On GitLab.com

Prerequisites:

- The Owner role for the top-level group.

To turn on GitLab Duo experiment and beta features for a top-level group:

1. In the top bar, select **Search or go to** and find your group.
1. In the left sidebar, select **Settings** > **GitLab Duo**.
1. Select **Change configuration**.
1. Under **Feature preview**, select **Turn on experiment and beta GitLab Duo features**.
1. Select **Save changes**.

This setting [cascades to all projects](../project/merge_requests/approvals/settings.md#cascade-settings-from-the-instance-or-top-level-group)
that belong to the group.

### On GitLab Self-Managed

{{< tabs >}}

{{< tab title="In 17.4 and later" >}}

In GitLab 17.4 and later, follow these instructions to turn on GitLab Duo
experiment and beta features for your GitLab Self-Managed instance.

Prerequisites:

- Administrator access.

To turn on GitLab Duo experiment and beta features for an instance:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **Settings** > **GitLab Duo**.
1. Expand **Change configuration**.
1. Under **Feature preview**, select **Use experiment and beta GitLab Duo features**.
1. Select **Save changes**.

{{< /tab >}}

{{< tab title="In 17.3 and earlier" >}}

Prerequisites:

- Administrator access.
- [Network connectivity](../../administration/gitlab_duo/configure/_index.md) enabled.
- [Silent Mode](../../administration/silent_mode/_index.md) turned off.

To turn on GitLab Duo experiment and beta features for an instance:

1. In the upper-right corner, select **Admin**.
1. In the left sidebar, select **Settings** > **GitLab Duo**.
1. Expand **Change configuration**.
1. Under **Feature preview**, select **Use experiment and beta GitLab Duo features**.
1. Select **Save changes**.
1. For GitLab Duo Chat to work immediately,
   [manually synchronize your subscription](../../subscriptions/manage_subscription.md#manually-synchronize-subscription-data).

   If you do not manually synchronize your subscription, it might take up to 24
   hours to activate GitLab Duo Chat on your instance.

{{< /tab >}}

{{< /tabs >}}
