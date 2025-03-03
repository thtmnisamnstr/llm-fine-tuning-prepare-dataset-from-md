Moving data between applications and warehousing data for analysis are recurring issues for app builders, data engineers, and IT teams. But we all know our businesses can benefit in significant ways if we are [smart with our data](https://venturebeat.com/2021/06/23/linux-foundation-unveils-new-permissive-license-for-open-data-collaboration/).

There are plenty of options for moving data now. Some have been around for years and have evolved, such as ETL (extract, transform, load) and custom-built integrations. Others have been spawned out of necessity, like ELT (extract, load, transform) and event streaming. Requirements and use cases for these data pipeline tools have grown more advanced and more demanding. From these ever-increasing demands, a novel (but sensible) use case has surfaced in the last few years: moving data from your data warehouse to the cloud applications your company uses. And a new category of [data](https://venturebeat.com/2021/06/25/precisely-82-of-data-executives-cite-data-quality-as-a-barrier/) pipeline has emerged to satisfy it: reverse ETL.

## What is reverse ETL?

Reverse ETL is straightforward in function — move data from your data warehouse to your cloud applications. Reverse ETL tools synchronize data on a recurring schedule (configurable between a few minutes to 24 hours or longer) or when triggered by calling an API (application programming interface) endpoint the reverse ETL tool exposes or through integrations with tools like [Airflow](https://airflow.apache.org/) and [dbt](https://www.getdbt.com/).

## What can I do with reverse ETL?

Reverse ETL tools let you realize a lot of the promise of data science. The complex, valuable modeling and analysis your data teams produce lives in your data warehouse. Being able to use this enriched, post-analysis data and automate keeping your business applications up to date with it makes the work your data scientists do more valuable. It also ensures their work delivers value in closer to real time compared with the manual processes that exist in most businesses today.

Reverse ETL tools focus on customer data and are best used for solving problems that require combining data across your websites, digital products, and any cloud applications you use. The specific use cases reverse ETL tools address best are:

* Building better, more comprehensive customer profiles (sometimes called “customer 360”)
* Creating more specific, granular audience segments
* Scoring leads based on your unique, business-specific criteria
* Identifying “at-risk” customers, or customers likely to churn
* Delivering data to cloud applications for better reporting

## Who are the leading reverse ETL vendors?

There are several reverse ETL tools available, and they all operate similarly. You configure a source connection to your data warehouse, configure a destination connection to a cloud application, and then write an SQL (structured query language) statement (or choose a table) to select the data you want to sync, choose your mappings, and set a sync schedule.

Despite the similar functionality of reverse ETL tools, three vendors stand out:

### [Hightouch](https://www.hightouch.io/)

Hightouch believes your data warehouse is your source of truth for customer data. The company makes it easy to sync that data to the cloud tools your business uses. Hightouch stands out because its tool is mature and has more source and destination integrations than any other [pure-play reverse ETL](https://www.hightouch.io/blog/reverse-etl) tool. The company has also grown its integration library faster than Census (see below) over the last six to 12 months. This is important because integrations dictate the level of flexibility your company can have with its tool selection. More integrations are better for reverse ETL.

Hightouch customers include Grafana, Plaid, Zeplin, and Mattermost.

### [Census](https://www.getcensus.com/)

If there was an industry standard for [reverse ETL](https://blog.getcensus.com/what-is-reverse-etl/), it would probably be Census. Census hasn’t been around much longer than Hightouch, but it gained traction first and has an impressive customer lineup. It is a mature tool and has a lot of integrations, but fewer than Hightouch.

Census customers include Fivetran, dbt, Netlify, and Notion.

If you’re choosing between reverse ETL tools, you’re most likely choosing between Hightouch and Census. Your decision criteria will come down to available integrations and pricing, as Hightouch and Census have different pricing models. Hightouch prices based on the monthly volume of records synced, while Census prices based on the number of data synchronization workflows you run.

### [RudderStack](https://rudderstack.com/)

[RudderStack](https://rudderstack.com/blog/reverse-etl-is-just-another-data-pipeline) isn’t a pure-play reverse ETL tool — it’s an event streaming platform. The company made its name and grew its customer base by being the open source alternative to [Segment](https://segment.com/). Earlier this year, RudderStack released ETL and reverse ETL features that have made it a competitor in the reverse ETL space.

The reason this combination of features makes sense is that reverse ETL relies on event streaming or event collecting tools (frequently Segment, [Snowplow](https://snowplowanalytics.com/), or RudderStack) and ETL tools to bring data into the warehouse. RudderStack is the only reverse ETL tool that can also bring the necessary customer data into your warehouse. And the company offers significantly more destination integrations than either Hightouch or Census. This is because it is an event streaming tool, and such tools need extensive integration libraries to compete.

RudderStack customers include Crate & Barrel, Priceline, Acorns, and Hinge.

Segment has reverse ETL functionality too, but the company doesn’t market itself as such. Personas SQL Traits lets you sync data from your warehouse to your cloud applications, but it has to go through Segment’s Personas audience builder.

​​Segment introduced new functionality late last year with [Segment Data Lakes](https://segment.com/blog/introducing-segment-data-lakes/), which builds a customer data lake for you. This reduces the importance of the company’s reverse ETL functionality.

## ​​**Alternatives to reverse ETL**

Reverse ETL is great for things like creating customer profiles, segmenting audiences, and other customer-centric processes. The real-time requirement for these processes is not strict, which makes a lot of sense because loading and analyzing data in your data warehouse in real time is not a good architectural pattern. Data warehouses and OLAP (online analytical processing) databases can run complex analytical queries and models quickly, but they aren’t built for real-time application response.

The emerging solution to these real-time requirements is to use tools like [Rockset](https://rockset.com/) to provide real-time analytics to your applications. In function, Rockset isn’t dissimilar from Elasticsearch, but Rockset is built cloud-native and emphasizes SQL compatibility. This means you’ll be able to scale beyond what Elasticsearch supports and do core SQL functions — like joins — that Elasticsearch doesn’t support.

An example use case for Rockset is feeding data to a continuously updated leaderboard in a large multiplayer online game. If you have millions of simultaneous players, it is incredibly difficult to ingest events, calculate millions of independent scores, and sort that list in real time, but this is a bread-and-butter use case for tools like Rockset.