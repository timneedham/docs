---
title: Configuring Dependabot alerts
intro: 'Enable {% data variables.product.prodname_dependabot_alerts %} to be generated when a new vulnerable dependency {% ifversion GH-advisory-db-supports-malware %}or malware {% endif %}is found in one of your repositories.'
shortTitle: Configure Dependabot alerts
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: how_to
topics:
  - Dependabot
  - Security updates
  - Alerts
  - Dependencies
  - Pull requests
  - Repositories
---

## About {% data variables.product.prodname_dependabot_alerts %} for vulnerable dependencies{% ifversion GH-advisory-db-supports-malware %} and malware{% endif %}

{% data reusables.repositories.a-vulnerability-is %}

{% data variables.product.prodname_dependabot %} scans code when a new advisory is added to the {% data variables.product.prodname_advisory_database %} or the dependency graph for a repository changes. When vulnerable dependencies{% ifversion GH-advisory-db-supports-malware %} or malware{% endif %} are detected, {% data variables.product.prodname_dependabot_alerts %} are generated. For more information, see "[AUTOTITLE](/code-security/dependabot/dependabot-alerts/about-dependabot-alerts)."

You can enable or disable {% data variables.product.prodname_dependabot_alerts %} for:
* Your personal account
* Your repository
* Your organization{% ifversion dependabot-alerts-enterprise-enablement %}
* Your enterprise{% endif %}

## Managing {% data variables.product.prodname_dependabot_alerts %} for your personal account

{% ifversion fpt or ghec %}

You can enable or disable {% data variables.product.prodname_dependabot_alerts %} for all repositories owned by your personal account.

### Enabling or disabling {% data variables.product.prodname_dependabot_alerts %} for existing repositories

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security-analysis %}
1. Under "Code security and analysis", to the right of {% data variables.product.prodname_dependabot_alerts %}, click **Disable all** or **Enable all**.
 ![Screenshot of "Configure security and analysis" features with "Enable all" or "Disable all" buttons emphasized](/assets/images/help/dependabot/dependabot-alerts-disable-or-enable-all.png)
1. Optionally, enable {% data variables.product.prodname_dependabot_alerts %} by default for new repositories that you create.
  ![Screenshot of "Enable Dependabot alerts" with "Enable by default for new private repositories" checkbox emphasized](/assets/images/help/dependabot/dependabot-alerts-enable-by-default.png)
1. Click **Disable {% data variables.product.prodname_dependabot_alerts %}** or **Enable {% data variables.product.prodname_dependabot_alerts %}** to disable or enable {% data variables.product.prodname_dependabot_alerts %} for all the repositories you own.
  ![Screenshot of "Enable Dependabot alerts" with "Enable  Dependabot alerts" button emphasized](/assets/images/help/dependabot/dependabot-alerts-enable-dependabot-alerts.png)

When you enable {% data variables.product.prodname_dependabot_alerts %} for existing repositories, you will see any results displayed on GitHub within minutes.

### Enabling or disabling {% data variables.product.prodname_dependabot_alerts %} for new repositories

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security-analysis %}
3. Under "Code security and analysis", to the right of {% data variables.product.prodname_dependabot_alerts %}, enable or disable {% data variables.product.prodname_dependabot_alerts %} by default for new repositories that you create.
  ![Screenshot of "Configure security and analysis" with "Enable  for all new private repositories" check emphasized](/assets/images/help/dependabot/dependabot-alerts-enable-for-all-new-repositories.png)

{% else %}
{% data variables.product.prodname_dependabot_alerts %} for your repositories can be enabled or disabled by your enterprise owner. For more information, see "[AUTOTITLE](/admin/configuration/configuring-github-connect/enabling-dependabot-for-your-enterprise)."

{% endif %}

## Managing {% data variables.product.prodname_dependabot_alerts %} for your repository

{% ifversion fpt or ghec %}You can manage {% data variables.product.prodname_dependabot_alerts %} for your public, private or internal repository.

By default, we notify people with admin permissions in the affected repositories about new {% data variables.product.prodname_dependabot_alerts %}. {% data variables.product.product_name %} never publicly discloses insecure dependencies for any repository. You can also make {% data variables.product.prodname_dependabot_alerts %} visible to additional people or teams working on repositories that you own or have admin permissions for.

{% data reusables.security.security-and-analysis-features-enable-read-only %}

### Enabling or disabling {% data variables.product.prodname_dependabot_alerts %} for a repository

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.navigate-to-code-security-and-analysis %}
1. Under "Code security and analysis", to the right of {% data variables.product.prodname_dependabot_alerts %}, click **Enable** to enable alerts or **Disable** to disable alerts.
  ![Screenshot of "Code security and analysis" section with button to enable {% data variables.product.prodname_dependabot_security_updates %}](/assets/images/help/repository/security-and-analysis-disable-or-enable-fpt-private.png)
{% endif %}{% ifversion ghes or ghae %}

{% data variables.product.prodname_dependabot_alerts %} for your repository can be enabled or disabled by your enterprise owner. For more information, see "[AUTOTITLE](/admin/configuration/configuring-github-connect/enabling-dependabot-for-your-enterprise)."
{% endif %}

## Managing {% data variables.product.prodname_dependabot_alerts %} for your organization
{% ifversion fpt or ghec %}You can enable or disable {% data variables.product.prodname_dependabot_alerts %} for all repositories owned by your organization. Your changes affect all repositories.

### Enabling or disabling {% data variables.product.prodname_dependabot_alerts %} for all existing repositories

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security-and-analysis %}
1. Under "Code security and analysis", to the right of {% data variables.product.prodname_dependabot_alerts %}, click **Disable all** or **Enable all**.
   {% ifversion fpt or ghec %}
   ![Screenshot of "Configure security and analysis" features with the "Enable all" or "Disable all" button emphasized for Dependabot alerts](/assets/images/help/dependabot/dependabot-alerts-disable-or-enable-fpt.png)
   {% endif %}
   {% ifversion ghae %}
   !["Enable all" or "Disable all" button for "Configure security and analysis" features](/assets/images/enterprise/github-ae/organizations/security-and-analysis-disable-or-enable-all-ghae.png)
   {% endif %}
   {% ifversion fpt or ghec %}
1. Optionally, enable {% data variables.product.prodname_dependabot_alerts %} by default for new repositories in your organization.
   {% ifversion fpt or ghec %}
   ![Screenshot of "Enable by default" option for new repositories](/assets/images/help/dependabot/dependabot-alerts-enable-by-default-organizations.png)
   {% endif %}
   {% endif %}
   {% ifversion fpt or ghec %}
1. Click **Disable {% data variables.product.prodname_dependabot_alerts %}** or **Enable {% data variables.product.prodname_dependabot_alerts %}** to disable or enable {% data variables.product.prodname_dependabot_alerts %} for all the repositories in your organization.
   {% ifversion fpt or ghec %}
   ![Screenshot of "Enable Dependabot alerts" modal with button to disable or enable feature emphasized](/assets/images/help/dependabot/dependabot-alerts-enable-dependabot-alerts-organizations.png)
   {% endif %}{% endif %}{% endif %}{% ifversion ghes or ghae %}
{% data variables.product.prodname_dependabot_alerts %} for your organization can be enabled or disabled by your enterprise owner. For more information, see "[AUTOTITLE](/admin/configuration/configuring-github-connect/enabling-dependabot-for-your-enterprise)."
{% endif %}

{% ifversion dependabot-alerts-enterprise-enablement %}

## Managing {% data variables.product.prodname_dependabot_alerts %} for your enterprise

You can enable or disable {% data variables.product.prodname_dependabot_alerts %} for all current and future repositories owned by organizations in your enterprise. Your changes affect all repositories.

{% note %}

**Note:** When {% data variables.product.prodname_dependabot_alerts %} are enabled or disabled at the enterprise level, it overrides the organization and repository level settings for {% data variables.product.prodname_dependabot_alerts %}.

{% endnote%}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
1. In the left sidebar, click **Code security and analysis**.
1. In the "{% data variables.product.prodname_dependabot %}" section, to the right of {% data variables.product.prodname_dependabot_alerts %}, click **Disable all** or **Enable all**.
1. Optionally, select **Automatically enable for new repositories** to enable {% data variables.product.prodname_dependabot_alerts %} by default for your organizations' new repositories.
{% endif %}
