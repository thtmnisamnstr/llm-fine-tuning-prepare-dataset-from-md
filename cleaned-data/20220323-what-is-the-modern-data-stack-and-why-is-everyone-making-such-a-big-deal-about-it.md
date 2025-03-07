*This is the first of a 2-part series giving a primer on the Modern Data Stack. You can read the second post, "[What tools are used in a Modern Data Stack, and what do they do?](https://segment.com/blog/tools-used-in-modern-data-stack-and-what-do-they-do/)"*

Driven by demand from businesses seeking greater value and more control over their customer data, a new 
approach to data analysis and activation has emerged and become the “go-to” approach for building a data 
architecture. 

The Modern Data Stack (MDS) is centered around an ecosystem of tools businesses use to collect, move, 
store, transform, analyze, and operationalize their data. 

The MDS market has seen explosive growth in the last 5+ years. In fact, between 2015 and 2020 alone, the 
[top 30 data infrastructure startups raised over $8 billion of venture capital](https://future.a16z.com/emerging-architectures-modern-data-infrastructure/). 
Compared to traditional data architectures and approaches, MDS tools are easier and faster to implement, 
easier to deploy and maintain, easier to build on top of, usually less expensive, and offer speed and 
scale as features. 

So, with the category gaining so much traction, we thought it would be helpful to put together a primer on 
the Modern Data Stack.

## What is a Modern Data Stack?
An MDS is a combination of easy-to-integrate tools that can be tailored to solve very specific business 
use cases. It’s difficult to pinpoint when exactly the MDS took off, but it’s likely the first tools that 
spawned the creation of them were cloud-based CDPs like [Twilio Segment](https://segment.com/). 

CDPs are often a foundational piece of an MDS. CDPs make integrations, one of the most challenging parts 
of building a traditional data stack, easy. This easy integration has allowed tools that run on customer 
data to flourish and an ecosystem of data tools to form.

MDS tools share some common features that make them easy to use and economical compared to old-school data 
architectures. 

Common characteristics are:
* **Cloud-based.** MDS tools are cloud-based and managed. They commonly have a free-tier to their managed 
  offering and are often open-source projects that can be hosted on cloud infrastructure.
* **Warehouse-centric.** MDS tools operate directly on the data in your own warehouse or lakehouse. Our 
  research showed that the warehouse is the main trusted data source because it maximizes access, control, 
  governance, and flexibility. **Note:** We use “warehouse” to mean both data warehouse and data lakehouse 
  architectures in our writing. Their use cases are converging and the functionality they offer is 
  overlapping and intermingling (for example, [Snowflake’s external tables](https://www.snowflake.com/blog/external-tables-are-now-generally-available-on-snowflake/) 
  support data lakes by acting as the analytics layer on top of them).
* **Modular and Best-of-Breed.** MDS tools can be swapped out for other tools that provide the same or 
  similar functionality. This lets customers of MDS tools choose the best tool for their specific needs and 
  circumstances. This also helps customers of MDS tools avoid vendor lock-in.
* **Easy to configure.** You don’t have to know how to code or manage VMs or k8s on your cloud platform to 
  use MDS tools. They are built to operate with existing cloud platforms and other cloud services. It’s 
  generally as simple to integrate two systems as configuring access via their SaaS APIs or UIs.

## What business problems does a Modern Data Stack help solve?
All-in-one marketing platforms – such as Salesforce Marketing Cloud and HubSpot Marketing Hub – have 
become popular over the last 10-15 years, and with good reason. 

They give businesses a single platform for all their digital marketing activities and help create unified 
customer profiles. They are far from perfect though.

They are rigid in their functionality, the customer profiles they create are often limited and rigid in 
use, and they make it difficult to work with your data outside of their tooling. Businesses that build an 
MDS avoid this rigidity and expand the possibilities of what they can do with their data.

This helps them solve problems such as:
* **MarTech and Marketing Analytics.** The pandemic made it clear that businesses lacked the agility they 
  needed to operate in a digital-first market. The expectation is you deliver a personalized experience to 
  your customers. To do that, you need the ability to target the right audience with the right message 
  across your digital properties, respond to customer behavior quickly across channels, and measure the 
  impact of everything you execute so you know what works and what doesn’t. All-in-one marketing platforms 
  make it difficult to be as agile as your business needs. Integrating a set of best-of-breed tools is 
  often the best way to help your Marketing team be more agile and deliver better, personalized 
  experiences. The MDS was born from this use case and is often the best way to solve it. This is one of 
  the primary use cases for Twilio Segment as well.
* **ML and Data Science.** Durable data storage is inexpensive with an MDS. This encourages collecting 
  every bit of customer data you can and storing it in a warehouse. Smart businesses then unleash data 
  scientists and analysts to extract the most critical insights from their data and then apply those 
  insights to their products, processes, and businesses.
* **Operational Analytics.** Businesses want fast, reliable activation of their data analytics to help 
  solve an array of use cases from Sales to Marketing to Product and beyond. The manual, error-prone 
  processes that exist today to get this data into the tools they use are too fragile and slow. MDS 
  tools – specifically reverse ETL – allow you to automate the integration of your data team’s work into 
  any business application. These data pipelines are consistent, resilient, and automated.

## What benefits do businesses get from a Modern Data Stack?
Beyond avoiding the pitfalls of all-in-one marketing platforms, a well-built MDS offers businesses several 
other benefits. These benefits stem largely from the fact that MDS tools are almost exclusively managed 
SaaS, are frequently built to be cloud native, and are intentionally designed to integrate with other 
tools in the MDS ecosystem.

The primary benefits a well-built MDS offers businesses are:
* **Solve bleeding edge use cases.** MDS tools give your digital business a competitive advantage by 
  giving you faster and greater value out of your customer data. These tools along with new, long-term 
  data storage strategies enabled by the low cost of storage in the warehouse, let you layer MDS tools on 
  top of large, historic data sets to enable specific, tailored solutions that you couldn’t build before 
  such as conversion attribution, advanced lead scoring, and ML-driven personalization.
* **Speed and scale of data.** Since MDS tools are almost always managed SaaS, they can scale almost 
  infinitely. Expensive computations that took hours or longer with on-prem systems can be scaled in the 
  cloud – often transparently to the user – driving down the time they take to execute.
* **Easier and faster implementation.** It doesn’t take weeks or months to add a new data system anymore. 
  You don’t have to provision infrastructure or deploy software. It’s easy to swap out or add MDS tools to 
  suit your specific use cases. Now you can maximize flexibility and control while still keeping your 
  costs low. You sign up for a new service and configure the integrations you need via the UI. It can take 
  as little as a few hours to set up and integrate a new tool now.
* **Reduced cost and maintenance.** MDS tools generally have consumption-based pricing. You only pay for 
  what you use. Since MDS tools are almost always managed SaaS, you don’t have to invest in maintaining 
  the systems. Maintaining five nines and scaling for peak are no longer your concern. That’s what you pay 
  your vendor for.
* **Easier to build on top of.** MDS tools are built to plugin with other tools. They frequently offer 
  out-of-the-box integrations with popular cloud services and platforms, so stitching together 
  low-or-no-code systems is easier. Product-oriented MDS tools also regularly offer APIs or SDKs, so 
  plugging them into custom-built applications or websites is easy.

## Looking ahead
Now that we’ve given you the tl;dr of the MDS, join us for [part two](https://segment.com/blog/tools-used-in-modern-data-stack-and-what-do-they-do/) 
where we'll cover the tools used in an MDS and what they do.