_The Yugabyte community is always active and its members are constantly having interesting conversations and making valuable contributions. We spotlight members of the community to recognize their contributions to making the Yugabyte community a great place._

Martin Roos

Head of Technology @ Fortumo

**LinkedIn:** [https://www.linkedin.com/in/martin-roos-16ab7532/](https://www.linkedin.com/in/martin-roos-16ab7532/)

If you’re on the [Yugabyte community Slack](https://www.yugabyte.com/slack) often, you’ve seen Martin Roos. He’s an active member of the community, often asking some of the most difficult and nuanced questions about YugabyteDB. Martin is a veteran software developer with over 20 years of database experience, working with Oracle, MySQL, PostgreSQL, and now YugabyteDB. Currently, Martin is the Head of Technology at [Fortumo](https://fortumo.com/) where he focuses on designing and building payment integration applications deployed on AWS.

### **Tell us about yourself**

#### **_How long have you been coding? What got you interested? What languages/DBs have been your focus?_**

The first time I sat behind a computer was in 1990 at age of 9 on the last days of the Soviet Union. The computer was a Russian “Electronika BK.” It had a spoonful of memory and the computing capacity of a toaster, but it ran Basic out of the box and I quickly got hooked on making my own text-based games and graphical animations. The frugal hardware was a blessing in disguise and gave me a good base to continue working efficiently while learning Pascal, Perl, and C on x86 hardware that roamed into Estonia with other Western influences. In 1999, during my last year of high school, I got my first job as a Perl programmer, working with Oracle databases and also with Sybase’s databases and PowerLanguage.

This was the time PHP took off rapidly as a popular new language and, with a MySQL storage backend, it captured worldwide web development. I studied it at university and was quickly hired by an online gaming company. I had to add Java to my mix of skills for a solid server-client implementation. The following years took me to various projects (even a 1.5 year stint into Malta) and landed me back in Estonia with Skype working on their web backend, building payment integrations.

Skype at the time was a huge PostgreSQL shop making extensive use of its features and even implementing their own message queues within PostgreSQL. Over the next 7.5 years, I learned a bunch of better coding practices and database management skills for databases that contain hundreds of millions of records. Clusters spanned across tens of machines, things like sequence scans or locks were in no-can-do territory, and no service interruptions for end users were allowed.

After Skype, I moved to Fortumo to build another set of payment integration applications on AWS/Java/PostgreSQL stacks. I am currently working on setting up YugabyteDB and evaluating its cloud deployment capabilities. My job title might sound grand but I’m still neck-deep in technical work day-to-day, writing code, reading logs, sketching solutions, and consulting with my colleagues.

### **Describe your database experience**

#### **_Which databases have you worked with before? Which do you currently work with? What pain points have you encountered?_**

In chronological order:

Oracle 2000-2002

MySQL 2000-2008

PostgreSQL 2006-2021

YugabyteDB 2021

From this set, Oracle is the old legend, but also legendary for its tall bills and mysterious error messages (deciphering ORA-44604 is not something I want to fill my days with). MySQL had a shiny prime time, but it was bringing a blunt knife to a gunfight with PostgreSQL when it came to features. It just wasn’t on par and its stellar performance degraded if you forced it into using InnoDB to have a real transactional storage backend. YugabyteDB is the new kid on the block and, if you look under the hood, it has very solid underpinnings.

### **How did you first hear about YugabyteDB?**

#### **_What caught your attention? Why was it interesting? Were you trying to solve a problem?_**

Whilst working with big clients and big volumes of data in Fortumo, clients around the world expect our services to be scalable and up 24/7. There is no way to be successful in our business if you have to take your database down for scaling, upgrades, maintenance, etc. It is hard to attract partners like Google or Amazon if you don’t have services that run like clockwork. Things just have to be up and work – period. Big partners can also hit you with surprising big workloads on short (or no) notice, so you have to be ready to react.

While I have done a bunch of PostgreSQL logical replication and quick switch upgrades, the processes are needlessly complicated and scary. Also, the clusters tend to be very sensitive and the tooling, even for big companies, is still too hard. Failures of master nodes are nightmare material, at least if you handle financial records. Man-hours invested into the maintenance just seemed to grow and grow.

I started looking around for a designed-for-cloud database that had seamless upgrades, scaling, and automatic data sharding “designed into it” and was as compatible with PostgreSQL as possible. The first I spotted was Cockroachdb, but its shortcomings quickly became apparent and revealed that it is not really an easy drop-in replacement for PostgreSQL. YugabyteDB seems to be the offering with the closest feature set to PostgreSQL out there that can be run anywhere.

As the times are right now, I see PostgreSQL falling behind, and they don’t seem to be catching up. It is not trivial to change the storage backend of their design without sacrificing or rewriting a big set of features. But, as database users in a constantly online world, we need storage that is designed for the expectations of 2021, and sadly PostgreSQL just isn’t. This is not meant as bashing on PostgreSQL. I understand they have a bunch of history and reasoning for their design, but times have changed and businesses need to keep up.

That’s where YugabyteDB comes in. I know I keep repeating it but YugabyteDB is designed to be a scalable, clustered database. Having been designed this way is essential to make it meet the goals and expectations of today. You can’t just hotfix these features into existing monolith SQL databases. Once you have seamlessly migrated tablets between servers or done a version upgrade without downtime, you start to “see the light” even if other sacrifices have to be made.

### **What has your experience been like with YugabyteDB?**

#### **_What were your expectations? What have you been focusing on? What are your thoughts about it?_**

At first, I was slightly overwhelmed by the configuration options and all the little pieces and possibilities, but, eventually, I learned to navigate the documentation and got a hang of how the system operates. I have been deliberately stress testing it and occasionally breaking it, but logs have made sense in most cases and have directed me in the correct direction to solve the issues. I have focused on reliability and maintenance-upgrade procedures, cluster management possibilities, and so forth.

### **Describe what surprised you the most**

#### **_Technically, operationally, etc._**

The biggest surprise for me was how smoothly the clusters managed data with tablets as the servers popped up and disappeared. Everything worked without my intervention. This was fantastic. I even missed out on the fact that I had lost a node in a three-node cluster for hours since the other nodes took over the traffic and load balancers correctly took the sick node out of the cluster.

I was surprised by how quickly I was able to make my applications run against YugabyteDB. If your application uses relatively simple tables and simple SQL operations, I expect you to run into little or no issues at all while converting.

### **Have you built or migrated any applications to YugabyteDB?**

#### **_Why? What were your expectations? Has YugabyteDB delivered on them?_**

We have finished test runs of a major application against YugabyteDB and are evaluating different kinds of setup scenarios to run YugabyteDB in production. The application was originally running on PostgreSQL and, during the test, we only had issues around the pessimistic locking being used for concurrency control in some scenarios which YugabyteDB does not yet cater for. Testing through disaster recovery and upgrade scenarios worked perfectly.

### **What future plans do you have for YugabyteDB?**

#### **Contributions to the code base, building other projects with YugabyteDB as a backend, etc.**

Assuming that the application will prove itself stable in production (for now we have stable results from our staging runs), we will follow suit with other mission-critical applications that have big databases.

### **What product feature/enhancement are you most looking forward to?**

#### **_You can always find [our up-to-date roadmap on Github](https://github.com/yugabyte/yugabyte-db#current-roadmap)._**

I think the number one for us is probably pessimistic locking support and YSQL point-in-time recovery support for structure changes. I think the PostgreSQL world migrators would be super happy if there were built-in tooling in YugabyteDB to do logical data replication from existing PostgreSQL databases into YugabyteDB, sort of how the AWS DMS does it. It would take a big pain point of migrations away.

### **Have you looked at other distributed SQL or distributed databases in addition to YugabyteDB?**

#### **_In your opinion, what sets YugaybteDB apart from the rest?_**

YugabyteDB shines with high PostgreSQL compatibility thanks to its reuse of PostgreSQL code. I think this is one of the biggest arguments for it. You can convert your PostgreSQL-backed application quite easily with minimal modifications and don’t have to redesign everything from the ground up like you would have to if you were to go with a database like Cassandra or MongoDB.

From direct competition, CockroachDB, Google Spanner, and Amazon’s Aurora Serverless come to mind. The first of these, CockroachDB, has many compatibility issues, and Spanner/Aurora both have issues with transparency in running costs. For some, vendor lock-in might be an argument as well.

Also on the table was a multimaster MySQL setup, but that is sort of duct tape over a monolithic SQL database, forcing it into acting as a distributed database. There are unexpected defects and every node has to carry the full dataset. The design here is an afterthought, and you can tell.

Considering my evaluation experiments of the different engines, YugabyteDB came out on top. No choice is perfect, but this seems to come pretty close. If Yugabyte stock were public, I would buy it because of the potential that I see in the long term.

### **How would you describe YugabyteDB to somebody just starting the process of finding a new database?**

#### **_What advice would you give them?_**

YugabyteDB is a database designed for the cloud, built up from the start to be run in clusters on partitioned storage across nodes. If one ventures into using it, reading the documentation is definitely a must. With expanded capabilities also comes the need for expanded knowledge on how to run it. The best way to learn the basics is to spin up a Docker cluster and make your first moves there.

If you are already using an Elasticsearch cluster in your stack then this feels very similar in many ways. Make sure you have a reliable network and fast disks.

If your application is not written yet, give YCQL a chance. Everything does not have to be SQL.

### **Anything else you would like people to know?**

When choosing your tooling, it is important to make sure the tooling supports the features that you need to have. If you are having performance issues, throwing a bit more money on hardware can take care of that, but you can’t solve missing features the same way.

## **What’s Next?**

Give Yugabyte Cloud a try by signing up for a [free tier account](https://cloud.yugabyte.com/register) in a couple of minutes. Got questions? Feel free to ask them in our YugabyteDB [community Slack](https://yugabyte-db.slack.com/join/shared_invite/zt-nvtsd9px-mV24Ue04YsJmJrSE5FJVPQ#/shared-invite/email) channel.