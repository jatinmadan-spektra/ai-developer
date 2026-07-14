# Exercise 1: Microsoft Foundry Fundamentals

### Estimated Duration: 20 Minutes

## Scenario

Contoso Innovations is planning to build AI-powered business applications using Microsoft Foundry. As an AI Developer, you have been tasked with exploring the Microsoft Foundry environment, deploying foundational AI models, and interacting with them through the playground. 

## Overview

In this exercise, you will gain hands-on experience setting up **Microsoft Foundry** and deploying the gpt-5.4 model. You will create an Azure AI Search resource to enable document retrieval capabilities and configure a Microsoft Foundry AI Hub to deploy the gpt-5.4 model. Finally, you will test the deployed model's capabilities in the Foundry Playground.

## Objectives

In this exercise, you will complete the following tasks:
- Task 1: Create Azure AI Search
- Task 2: Set up Microsoft Foundry

## Task 1: Create Azure AI Search

In this task, you will create an Azure AI Search resource.

1. On the Azure portal search bar, search for **AI Search (1)** and select **AI Search (2)** from the results.

    ![](./media/new/c1.png)

1. From the left navigation pane, ensure **AI Search (1)** is selected and then click on **+ Create (2)** from the top menu bar.

    ![](./media/new/c2.png)

1. On the **Create a search service** page, provide the following details, then click on **Review + create (6)**:

    - **Subscription:** Leave the default one **(1)**

    - **Resource group:** Select **ai-foundry-<inject key="Deployment ID" enableCopy="false"></inject> (2)**

    - **Service name:** Enter **ai-search-<inject key="Deployment ID" enableCopy="false"></inject> (3)**

    - **Region:** Select **<inject key="Region" enableCopy="false"></inject> (4)** 

    - Pricing tier: Select **Standard (5)**

        >**Note:** In case you do not see the Standard tier, it means that the region selected does not have the Standard tier available right now. Please select another region and deploy the resource.

      ![](./media/new/css.png)

1. Click **Create** to deploy the search service.

    ![](./media/new/csscr.png)

## Task 2: Set up Microsoft Foundry

In this task, you will explore different flow types in Microsoft Foundry by creating an AI hub through Azure portal, then deploying the gpt-5.4 model, and testing its capabilities in the playground from the Microsoft Foundry.

1. On the **Azure portal**, search for **Microsoft Foundry (1)** and select **Microsoft Foundry (2)** from the results.

    ![](./media/new/a1.png)

1. From the left navigation pane, expand **Use with Foundry (1)**, select **AI Hubs (2)**, open the **Create (3)** drop-down, and click **Hub (4)**.

    ![](./media/new/a2.png)

1. On the **Azure AI hub** page, provide the following details and then click on **Review+create (5)**:

    - **Subscription**: Leave the default one **(1)**

    - **Resource group:** Select **ai-foundry-<inject key="Deployment ID" enableCopy="false"></inject> (2)**

    - **Region:** Select **<inject key="Region" enableCopy="false"></inject> (3)**

    - **Name:** Enter **ai-foundry-hub-<inject key="Deployment ID" enableCopy="false"></inject> (4)**

      ![](./media/new/huubrc.png)

1. Once the Validation passed, click on **Create**.

    ![](./media/new/hubcr.png)

1. Once the deployment is completed, click on **Go to resource**.

    ![](./media/new/a5.png)

1. From the **Overview** page of the **Azure AI hub**, click **Launch Azure AI Foundry** to open the Foundry workspace.

    ![](./media/new/laif.png)

1. On the **Create a project** screen, provide the following details and then click on **Create (3)**:

    - **Project name:** Enter **ai-foundry-project-<inject key="Deployment ID" enableCopy="false"></inject> (1)**

    - Disable **Set up recommended resources so I can explore everything Foundry has to offer. (2)**

      ![](./media/new/image-01.png)

1. Wait for the project to finish provisioning this can take a few minutes. Once it's ready, the Foundry portal opens the project's **Overview/Home** page.

    >**Note**: You can close all the pop-up windows.

1. On the **Home** page, select **View deployments**.

    ![](./media/new/image-02.png)

1. On the **Models (1)** page, under **Deployments**, select **Deploy (2) > Deploy a base model (3)**. Search for **gpt-5.4 (4)**, and then select the **gpt-5.4 (5)** model.

    ![](./media/new/image-03.png)

    ![](./media/new/image-04.png)

1. On the **Deploy gpt-5.4** blade, click **Custom deploy** and configure the required deployment settings as specified below:

    - **Deployment type**: Choose **Global Standard (1)**

    - **Model version**: Select **2026-03-05 (Default) (2)**

    - **Tokens per Minute Rate Limit**: Limit to **50K (3)** (You can use keyboard arrows to increase or decrease the value)

    - Click on **Deploy (4)**

      >**Note**: If the selected region is not supported, please choose an alternative supported region and proceed with the deployment.

      ![](./media/new/image-05.png)

1. On the **gpt-5.4** deployment under **Playground**, in the **Instructions** section, replace the existing text with `Extract the United States Postal Service (USPS) formatted address from the following email` **(1)**. Using this you can explore the capabilities of the gpt-5.4 model.

    ![](./media/new/uspsapply.png)

1. Provide the below mail in the chat **(2)** then click on **Send (3)** to identify and extract the postal address from the following email:

    ```
    Subject: Elevate Your Brand with Our Comprehensive Marketing Solutions!
    From: BrightEdge Marketing
    To: John Doe

    Dear John,
    At BrightEdge Marketing, we believe in the power of innovative marketing strategies to elevate brands and drive business success. Our team of experts is dedicated to helping you achieve your marketing goals through a comprehensive suite of services tailored to your unique needs.

    Please send letters to 123 Marketing Lane, Suite 400, in area 90210, Innovation City, California.

    Thank you for considering BrightEdge Marketing.
    Best regards,
    Sarah Thompson
    Marketing Director BrightEdge Marketing
    ```

    ![](./media/new/image-06.png)

1. You will receive a response similar to the one shown below:

    ![](./media/new/image-07.png)

  > **Congratulations** on completing the lab! Now, it's time to validate it. Here are the steps:
  > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
  > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
  > - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help

<validation step="ceb8c2ae-28bf-492f-98f5-dcf416c1fc3c" />

## Summary

In this exercise, you have completed the following:

- Created Azure AI Search.

- Set up Microsoft Foundry.

### You have successfully completed this exercise. Kindly click **Next >>** to proceed further

![Launch Azure Portal](./media/new/image-08.png)