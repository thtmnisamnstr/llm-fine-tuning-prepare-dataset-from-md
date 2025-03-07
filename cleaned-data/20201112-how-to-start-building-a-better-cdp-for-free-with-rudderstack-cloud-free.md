[RudderStack](https://rudderstack.com) is an [open-source](https://github.com/rudderlabs/rudder-server), warehouse-first customer data platform (CDP) that builds your CDP on your data warehouse for you. RudderStack makes it easy to collect, unify, transform, and store your customer data as well as route it securely to a wide range of common, popular marketing, sales, and product tools.

Today, we launched [RudderStack Cloud Free](https://app.rudderlabs.com/signup?type=freetrial), a no time limit, no credit card required, completely free tier of [RudderStack Cloud](https://resources.rudderstack.com/rudderstack-cloud) (read the blog post announcing RudderStack Cloud Free [here](https://rudderstack.com/blog/start-building-a-better-cdp-for-free-with-rudderstack-cloud-free/)). You get the same great experience you get with RudderStack Cloud Pro, with the only limitation being a cap of 500,000 events per month (that’s roughly 10,000 monthly active users for most sites and apps).

*[Click here to skip the exposition and jump straight to the how to.](#how-to-sign-up)*

## Here’s what you get with RudderStack Cloud Free
*   **Warehouse-first**: RudderStack is the warehouse-first CDP. RudderStack builds your CDP on your data warehouse, with support for cloud data warehouses like [Amazon Redshift](https://aws.amazon.com/redshift/), [Google BigQuery](https://cloud.google.com/bigquery), and [Snowflake](https://www.snowflake.com). This approach makes it more cost effective, secure, and flexible than other CDPs.
*   **Secure by design**: RudderStack’s core architecture was built around the principles of privacy and security. That’s the reason it is warehouse-first. RudderStack is a modern CDP that can be hosted SaaS, on-prem, or in your own cloud, so you control your customer data.
*   **Built for devs**: RudderStack is open source and built API-first, so it is easily customizable and fits into your existing development processes. Its multitude of SDKs, sources, and destinations make it easy to instrument, ingest, and route customer data from all of your digital touchpoints.
*   **Speed and Scale**: RudderStack is extremely scalable. A single node can easily handle hundreds of thousands of events per day. You can also have a multi-node RudderStack setup, where you can easily scale to millions of events per day. All of this is configurable in a highly secure and available environment.
*   **Community support**: We have built a rich community of core developers who, along with our engineers, provide daily support on [Slack](https://resources.rudderstack.com/join-rudderstack-slack).

## How to sign up for and start using RudderStack Cloud Free
*   Go to the [RudderStack signup page](https://app.rudderlabs.com/signup?type=freetrial).
*   Enter your information in the required fields - your email address, name, organization name and the password needed to sign-in. Then, click on **Create New Account**.

*   You should get a verification code sent to your email. Enter the code in the field and click on **Submit Verification Code**, as shown:

That’s it. You should now have full access to the RudderStack dashboard.

Now, you can start instrumenting your website or app using RudderStack’s [11 SDKs](https://docs.rudderstack.com/rudderstack-sdk-integration-guides), configuring your customer data **[Sources](https://docs.rudderstack.com/sources)**, and setting up integrations with over 60 third-party **[Destinations](https://docs.rudderstack.com/destinations)**. 

The following sections demonstrate how you can instrument your site with RudderStack’s JavaScript SDK to track and collect events and then route the collected event data to a common destination, [Google Analytics](https://analytics.google.com/).

### Step 1: Adding a source
*   Sign up for RudderStack Cloud Free by following the steps mentioned above. Once you’ve signed up, log into RudderStack Cloud Free to access your dashboard:

*   Next, click on **Add Source**.

*   Choose the source from which you want to collect the event data. 
 
For this example, we will choose the **RudderStack JavaScript SDK** to track and collect events from your website. Select **JavaScript**, and click on on **Next**.

*   Add a name for your source, and click on **Next**.

*   You should now seen the following window, containing the source details:

Your JavaScript source is now configured and ready to collect event data from your website.

### Step 2: Adding a destination in RudderStack for routing your event data
*   Once you have added a source, click on the **Add Destination** button, as shown:

*   Choose the destination platform from the list of destinations and then click on **Next**. For this example, we want to route the collected website events to **Google Analytics**.

*   Add a name for your destination and click on **Next**.

*   The next step is to connect your event data source to this destination. Your previously configured JavaScript source should now appear automatically. Select the source and click on **Next**.

*   Next, you need to specify the connection settings for your destination. For Google Analytics, you will need to enter the **Tracking ID**, which you can retrieve from your Google Analytics admin dashboard, as shown:

*   Enter this tracking ID in the **Connections Settings** window, as shown. You can also configure the other settings as per your requirements, and then click on **Next**.

*   RudderStack also lets you transform your event data before routing it to your destination. You can choose an existing transformation or create a new transformation function to do so. Select the appropriate option and then click on **Next**. 

That’s it! Your destination is now configured successfully. The events from your JavaScript web source will start flowing to Google Analytics via RudderStack. You can also view the events coming from your source in real-time via the **Live Events** tab on the top right, as shown:

You can refer to our [documentation](https://docs.rudderstack.com/) for more information on how to configure and use RudderStack.

## Start building a better CDP with RudderStack

Start building a better, warehouse-first CDP that delivers complete, unified data to every part of your marketing and analytics stack. Sign up for [RudderStack Cloud Free](https://app.rudderlabs.com/signup?type=freetrial) today.

Join our [Slack](https://resources.rudderstack.com/join-rudderstack-slack) to chat with our team, check out our open source repos on [GitHub](https://github.com/rudderlabs), and follow us on social: [Twitter](https://twitter.com/RudderStack), [LinkedIn](https://www.linkedin.com/company/rudderlabs/), [dev.to](https://dev.to/rudderstack), [Medium](https://rudderstack.medium.com/), [YouTube](https://www.youtube.com/channel/UCgV-B77bV_-LOmKYHw8jvBw).