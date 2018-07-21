---
title: Use Lifecycle Controls to Version your API
toc: false
sidebar: labs_sidebar
folder: labs/lab4
permalink: /lab4_overview.html
applies_to: [product-manager,administrator,consumer]
---

## Objective

In the previous lab, you created a new version of the **inventory** API which is secured with an OAuth 2.0 provider. At this stage, however, the changes are still in draft mode.

In order for the changes to take effect, you must publish the APIs to the developer portal. Recall though that the `inventory 1.0.0` version is already running and has active subscribers.

In this lab, you will explore the API Lifecycle controls offered by IBM API Connect and use them to replace the existing version of an API Product with a new version.

You will learn:

+ How to create a new API Product
+ How to use lifecycle controls to replace an existing version of an API Product


1.  Click on the `inventory 1.0.0` API to open the API designer.

1.  At the top right-hand corner of the screen, click on the menu icon to expand additional options.

1.  Select the option to `Save as a new version`.

    ![](./images/labs/lab3/save-new-version.png)

1.  Enter the new version number as `2.0.0` and click the `Save as new version` button.

    ![](./images/labs/lab3/new-version-number.png)

1.  At the top right-hand corner of the screen, click on the menu icon to expand additional options.

1.  Select the option to `Save as a new version`.

    ![](./images/labs/lab3/save-new-version.png)

1.  Enter the new version number as `2.0.0` and click the `Save as new version` button.

    ![](./images/labs/lab3/new-version-number.png)

    {% include important.html content="
        The Token URL will be based upon the location of your Org and Space running on Bluemix public.
        <br/><br/>
        You can find your Gateway Endpoint URL by logging into Bluemix and launching the API Connect service, then navigate into your catalog (the default catalog created is `Sandbox`).
        <br/><br/>
        From there go into `Settings`, then choose the `Gateways` option from the side menu palette. Locate the **ENDPOINT**, simply copy and paste the contents into the Token URL field of your API OAuth settings, then append `/oauth2/token`.
        <br/><br/>
        <img src=\"./images/labs/lab3/bmx-api-endpoint.png\"/>
    " %}

	{% include tip.html content="
	    You will need the Gateway Endpoint URL later. Save the Gateway Endpoing URL value to a text editor for easy access.
    " %}
    
    ![](./images/labs/lab3/api-oauth-settings-1.png)

1.  Click the `+` icon in the **Scopes** section to create a new scope. Set the following properties. Note the organization portion of the token URL will be different for each student.

    > Scope Name: `inventory`
    > 
    > Description: `Access to all inventory resources`
	
    ![](./images/labs/lab3/api-oauth-settings-2.png)

1.  Navigate to the `Security` section and check the `oauth (OAuth)` checkbox.  

    ![](./images/labs/lab3/api-security.png)
	
1.  Save your changes.

    ![](./images/common/save.png)

1.  Click on the `<- All APis` link to return to the draft API list.

1.  Return to the [API Connect Toolkit](http://127.0.0.1:9000/#/design/apis){:target="_blank"} tab in your browser.

1.  Make sure you are still in the `inventory` project.

    Click on the menu icon in the upper left-hand corner of the screen, expand the `Projects` option and select `inventory`.

1.  Click the `+ Add` button and select `OAuth 2.0 Provider API` from the menu.

1.  Specify the following properties and click the `Create API` button to continue.

    > Title: `oauth`
    > 
    > Name: `oauth`
    > 
    > Base Path: `/`
    > 
    > Version: `1.0.0`
	
	{% include important.html content="
        Make sure the **Base Path** setting is correct.
    " %}
	
    ![](./images/labs/lab3/new-oauth-props.png)

1.  The API Editor will launch. If this is your first time using the API Editor, you will see an informational message. When you are ready to proceed, click the `Got it!` button to dismiss the message.  
	
    The API Editor opens to the newly created `oauth` API. The left hand side of the view provides shortcuts to various elements within the API definition: Info, Host, Base Path, etc. By default, the API Editor opens to the `Design` view, which provides a user-friendly way to view and edit your APIs.

1.  Use the palette on the left to navigate to the `OAuth 2` section.

    Over the next several steps, we will set up OAuth-specific options, such as client type (public vs confidential), valid access token scopes, supported authorization grant types, etc. The [OAuth 2.0 Specification](http://tools.ietf.org/html/rfc6749){:target="_blank"} has detailed descriptions of each of the properties we are configuring here.

1.  For the `Client type` field, click the drop down menu and select `Confidential`.

    ![](./images/labs/lab3/oauth2-client-type.png)

1.  Three scopes were generated for you when the OAuth API Provider was generated: `scope1`, `scope2`, `scope3`.

1.  Modify the values for `scope1`, set the following fields:

    > Name: `inventory`
    > 
    > Description: `Access to Inventory API`

    Delete `scope2` and `scope3` by clicking the trashcan icons to the right of the scope definitions.
    
    {% include important.html content="
        The scope defined here must be identical to the scope that we define later when telling the `inventory` API to use this OAuth config. A common mistake is around case sensitivity. To avoid running into an error later, make sure that your scope is set to all **lowercase**.
    " %}
    
    ![](./images/labs/lab3/oauth2-scopes.png)

1.  We want to configure this provider to *only* support the Resource Owner Password Credentials grant type. Deselect the `Implicit`, `Application` and `Access Code` Grants, but leave `Password` checked.

    ![](./images/labs/lab3/oauth2-grants.png)

1.  In the **Identity extraction** section, set the `Collect credentials using` drop-down menu to `Basic`.

    ![](./images/labs/lab3/oauth2-id-extraction.png)

1.  In the **Authentication** section, set the following fields:

    > Authenticate application users using: `Authentication URL`
    > 
    > Authentication URL: `https://thinkibm-services.mybluemix.net/auth`
    
    ![](./images/labs/lab3/oauth2-authentication.png)

1.  Scroll down to the **Tokens** section, turn off the `Enable revocation` option.
    
    ![](./images/labs/lab3/outh2-tokens.png)

1.  Click the `Save` icon in the top right corner of the editor to save your changes.

    ![](./images/common/save.png)

1.  Click on the `<- All APis` link to return to the draft API list.

## Continue

Proceed to [Create a New API Product](lab4_new_product.html).
