---
title: 'Tutorial: Azure AD SSO integration with Kantega SSO for Confluence'
description: Learn how to configure single sign-on between Azure Active Directory and Kantega SSO for Confluence.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 10/13/2021
ms.author: jeedes
---
# Tutorial: Azure AD SSO integration with Kantega SSO for Confluence

In this tutorial, you'll learn how to integrate Kantega SSO for Confluence with Azure Active Directory (Azure AD). When you integrate Kantega SSO for Confluence with Azure AD, you can:

* Control in Azure AD who has access to Kantega SSO for Confluence.
* Enable your users to be automatically signed-in to Kantega SSO for Confluence with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To configure Azure AD integration with Kantega SSO for Confluence, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get a [free account](https://azure.microsoft.com/free/).
* Kantega SSO for Confluence single sign-on enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* Kantega SSO for Confluence supports **SP and IDP** initiated SSO.

## Add Kantega SSO for Confluence from the gallery

To configure the integration of Kantega SSO for Confluence into Azure AD, you need to add Kantega SSO for Confluence from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Kantega SSO for Confluence** in the search box.
1. Select **Kantega SSO for Confluence** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for Kantega SSO for Confluence

Configure and test Azure AD SSO with Kantega SSO for Confluence using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Kantega SSO for Confluence.

To configure and test Azure AD SSO with Kantega SSO for Confluence, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Kantega SSO for Confluence SSO](#configure-kantega-sso-for-confluence-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Kantega SSO for Confluence test user](#create-kantega-sso-for-confluence-test-user)** - to have a counterpart of B.Simon in Kantega SSO for Confluence that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Kantega SSO for Confluence** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<server-base-url>/plugins/servlet/no.kantega.saml/sp/<uniqueid>/login`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<server-base-url>/plugins/servlet/no.kantega.saml/sp/<uniqueid>/login`

5. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<server-base-url>/plugins/servlet/no.kantega.saml/sp/<uniqueid>/login`

	> [!NOTE]
	> These values are not real. Update these values with the actual Identifier, Reply URL and Sign-On URL. These values are received during the configuration of Confluence plugin, which is explained later in the tutorial.

6. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

7. On the **Set up Kantega SSO for Confluence** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Kantega SSO for Confluence.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Kantega SSO for Confluence**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Kantega SSO for Confluence SSO

1. In a different web browser window, sign in to your **Confluence admin portal** as an administrator.

1. Hover on cog and click the **Add-ons**.

	![Screenshot that shows the "Cog" menu icon and "Add-ons" selected.](./media/kantegassoforconfluence-tutorial/settings.png)

1. Under **ATLASSIAN MARKETPLACE** tab, click **Find new add-ons**.

	![Screenshot that shows the "ATTLASSIAN MARKETPLACE" tab with "Find new add-ons" selected.](./media/kantegassoforconfluence-tutorial/admin.png)

1. Search **Kantega SSO for Confluence SAML Kerberos** and click **Install** button to install the new SAML plugin.

	![Screenshot that shows the "Find new add-ons" page with "Kantega S S O for Confluence S A M L Kerberos" in the search box and the "Install" button selected.](./media/kantegassoforconfluence-tutorial/install-button.png)

1. The plugin installation starts.

	![Screenshot that shows the plugin "Installing" screen.](./media/kantegassoforconfluence-tutorial/plugin.png)

1. Once the installation is complete. Click **Close**.

	![Screenshot that shows the "Installed and ready to go" screen with the "Close" action selected.](./media/kantegassoforconfluence-tutorial/installation.png)

1. Click **Manage**.

	![Screenshot that shows the "Kantega Single Sign-on with Kerberos and S A M L" plugin with the "Manage" button selected.](./media/kantegassoforconfluence-tutorial/integration.png)

1. Click **Configure** to configure the new plugin.

	![Screenshot that shows the "Kantega Single Sign-on with Kerberos and S A M L" page with the "Configure" button selected.](./media/kantegassoforconfluence-tutorial/configuration.png)

1. This new plugin can also be found under **USERS & SECURITY** tab.

	![Screenshot that shows the "USERS & SECURITY" tab with the "Kantega Single Sign-on" action selected.](./media/kantegassoforconfluence-tutorial/security.png)

1. In the **SAML** section. Select **Azure Active Directory (Azure AD)** from the **Add identity provider** dropdown.

	![Screenshot that shows the "S A M L" section with "Add Identity provider" and "Azure Active Directory (Azure AD)" selected.](./media/kantegassoforconfluence-tutorial/azure.png)

1. Select subscription level as **Basic**.

	![Screenshot that shows the "Preparing Azure AD" page with "Basic" selected.](./media/kantegassoforconfluence-tutorial/subscription.png)

1. On the **App properties** section, perform following steps:

	![Screenshot that shows the "App properties" section with the "App I D U R L" field and "Copy" button highlighted, and the "Next" button selected.](./media/kantegassoforconfluence-tutorial/properties.png)

	a. Copy the **App ID URI** value and use it as **Identifier, Reply URL, and Sign-On URL** on the **Basic SAML Configuration** section in Azure portal.

	b. Click **Next**.

1. On the **Metadata import** section, perform following steps: 

	![Screenshot that shows the "Metadata import" section with "Metadata file on my computer" selected.](./media/kantegassoforconfluence-tutorial/metadata.png)

	a. Select **Metadata file on my computer**, and upload metadata file, which you have downloaded from Azure portal.

	b. Click **Next**.

1. On the **Name and SSO location** section, perform following steps:

	![Screenshot that shows the "Name and S S O location" with the "Identity provider name" textbox highlighted, and the "Next" button selected.](./media/kantegassoforconfluence-tutorial/location.png)

	a. Add Name of the Identity Provider in **Identity provider name** textbox (e.g Azure AD).

	b. Click **Next**.

1. Verify the Signing certificate and click **Next**.

	![Screenshot that shows the "Signature verification" section with the "Next" button selected.](./media/kantegassoforconfluence-tutorial/certificate.png)

1. On the **Confluence user accounts** section, perform following steps:

	![Screenshot that shows the "Confluence user accounts" section with the "Create users in Confluence's Internal Directory if needed" option and "Next" button selected.](./media/kantegassoforconfluence-tutorial/accounts.png)

	a. Select **Create users in Confluence's internal Directory if needed** and enter the appropriate name of the group for users (can be multiple no. of groups separated by comma).

	b. Click **Next**.

1. Click **Finish**.

	![Screenshot of the "Summary" page with the "Finish" button selected.](./media/kantegassoforconfluence-tutorial/summary.png)

1. On the **Known domains for Azure AD** section, perform following steps: 

	![Screenshot that shows the "Known domains for Azure AD" page with the "Known domains" textbox highlighted and the "Save" button selected.](./media/kantegassoforconfluence-tutorial/domain.png)

	a. Select **Known domains** from the left panel of the page.

	b. Enter domain name in the **Known domains** textbox.

	c. Click **Save**.

### Create Kantega SSO for Confluence test user

To enable Azure AD users to sign in to Confluence, they must be provisioned into Confluence. In the case of Kantega SSO for Confluence, provisioning is a manual task.

**To provision a user account, perform the following steps:**

1. Sign in to your Kantega SSO for Confluence company site as an administrator.

1. Hover on cog and click the **User management**.

    ![Screenshot that shows the "Cog" icon and "User management" selected.](./media/kantegassoforconfluence-tutorial/user-management.png)

1. Under Users section, click **Add Users** tab. On the **Add a User** dialog page, perform the following steps:

	![Add Employee](./media/kantegassoforconfluence-tutorial/create-user.png)

	a. In the **Username** textbox, type the email of user like Brittasimon@contoso.com.

	b. In the **Full Name** textbox, type the full name of user like Britta Simon.

	c. In the **Email** textbox, type the email address of user like Brittasimon@contoso.com.

	d. In the **Password** textbox, type the password for user.

	e. Click **Confirm Password** reenter the password.

	f. Click **Add** button.

## Test SSO

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Kantega SSO for Confluence Sign on URL where you can initiate the login flow.  

* Go to Kantega SSO for Confluence Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Kantega SSO for Confluence for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Kantega SSO for Confluence tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Kantega SSO for Confluence for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Kantega SSO for Confluence you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).