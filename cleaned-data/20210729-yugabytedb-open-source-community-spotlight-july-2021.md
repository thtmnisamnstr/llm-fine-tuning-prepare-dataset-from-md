_The Yugabyte community is always active and its members are constantly having interesting conversations and making valuable contributions. We spotlight members of the community to recognize their contributions to making the Yugabyte community a great place._

Radek Gruchalski

Managing Director & Software Engineer @ Klarrio GmbH

**GitHub:** [https://github.com/radekg/](https://github.com/radekg/)

**LinkedIn:** [https://linkedin.com/in/radgruchalski](https://linkedin.com/in/radgruchalski)

**Blog:** [https://gruchalski.com/](https://gruchalski.com/)

If you’re on the [Yugabyte community Slack](https://www.yugabyte.com/slack) often, you’ve seen Radek Gruchalski. He’s an active member of the community and has even written blog posts about YugabyteDB. Radek is a veteran software developer with decades of diverse database experience. He’s built applications with Microsoft Access, Microsoft SQL Server, MySQL, PostgreSQL, and several NoSQL databases like Cassandra, MongoDB, CouchDB, and HBase. Currently, Radek is a Managing Director and Software Engineer at [Klarrio GmbH](https://klarrio.com/) where he focuses on delivering distributed applications in the cloud, on-premise, and in hybrid environments.

## TELL US ABOUT YOURSELF

#### HOW LONG HAVE YOU BEEN CODING? WHAT GOT YOU INTERESTED? WHAT LANGUAGES/DBS HAVE BEEN YOUR FOCUS?

I have been building software for over 20 years. My first job was for a local photo equipment shop. They also had an online store. My task was creating printed magazines and dabbling with HTML bits for their online offers. One day, I tried changing some things in the shop’s Perl backend. That’s how it all started. Many, many sleepless nights later, Perl was the first programming language I learned properly, but I’ve never got to the Perl Golf mastery level. Afterward came ASP 3.0, PHP 3 with MySQL, followed by a lot of ColdFusion, Java, JavaScript, and Flash with ActionScript 2. Flash Media Server was a great product. At the beginning of my career, I did a little bit of everything: front end, back end, websites, mobile apps, and integrations.

Today, I am a Managing Director at Klarrio GmbH, where I also write and deliver software to spec daily. My focus is distributed architectures and, primarily, backend applications — mainly Scala, Go, and Kafka—deployed in the cloud, on-premise, and in hybrid environments. My work cuts through all aspects of software delivery:  R&D, architecture, implementation, documentation, operations, and some bits of SRE. I create open source tools, my [Terraform Ansible provisioner](https://github.com/radekg/terraform-provisioner-ansible) being the most popular.

The most enjoyable work for me is on systems directly contributing to users’ quality of work. One of my favorite contracts, some years back, was for a UK-based aircraft parts supplier. The task was to develop a modern alternative to a COBOL back office system that powered all the operations of their business. Together with company employees and top management, I began working on improving internal CRM, ERP, warehouse storage, warehouse operations, and logistics processes with the newly built software deployed in multiple geographical locations. The most gratifying part was seeing how the software directly contributes to the performance of the group of 70+. Working so closely with them shaped me as a developer and created immense respect for the end-user.

## DESCRIBE YOUR DATABASE EXPERIENCE

#### WHICH DATABASES HAVE YOU WORKED WITH BEFORE? WHICH DO YOU CURRENTLY WORK WITH? WHAT PAIN POINTS HAVE YOU ENCOUNTERED?

Does Microsoft Access count? I’ve done plenty of that! The real databases I’ve worked with include MySQL, PostgreSQL, and a lot of Microsoft SQL Server 2008. I have very fond memories of Transact-SQL. The craziest database thing I’ve done was with MSSQL back in 2010. I was running an active-active replication between the UK and Florida, USA, with log shipping via Dropbox. I have worked with a fair share of NoSQL databases: Cassandra, MongoDB, CouchDB, HBase to name a few.

The biggest pain points? Database operations can be mentally taxing. Traditional RDBMS is very reliable but notoriously difficult to automate for horizontal scalability without a dedicated DBA or an SRE team.

## HOW DID YOU FIRST HEAR ABOUT YUGABYTEDB?

#### WHAT CAUGHT YOUR ATTENTION? WHY WAS IT INTERESTING? WERE YOU TRYING TO SOLVE A PROBLEM?

At Klarrio, we have been following YugabyteDB for over two years. Recently, we were on a hunt for a PostgreSQL-compatible database (optionally distributed), and we have decided to evaluate YugabyteDB. What caught our attention was the fact that YugabyteDB reuses the actual PostgreSQL engine but augments it with a purpose-built distributed consensus layer, which does all-things-sharding almost no-op for the operator. Our use case is a multi-tenant database with workload isolation. The choice of YugabyteDB was cemented by the ability to pin the selected tablespaces to selected cluster nodes using geo-replication features.

## WHAT HAS YOUR EXPERIENCE BEEN LIKE WITH YUGABYTEDB?

#### WHAT WERE YOUR EXPECTATIONS? WHAT HAVE YOU BEEN FOCUSING ON? WHAT ARE YOUR THOUGHTS ABOUT IT?

Considering how difficult distributed systems can be and that RDBMS are not easy to automate at scale, I expected that trying out YugabyteDB would be frustrating. There are so many technologies out there never delivering on the promises they make.

The task of evaluating different distributed database options landed on my plate. I had a specific end-to-end scenario to trial. It was surprising how painless it was to get YugabyteDB going. The core of the use case was implemented in a couple of days. YugabyteDB hasn’t failed me even once in the process. What was my thought afterward? “Well, that was easier than I ever expected”.

## DESCRIBE WHAT SURPRISED YOU THE MOST

#### TECHNICALLY, OPERATIONALLY, ETC.

I had a 30+ node cluster up and running on a home lab server using Docker Compose in less than a day. It was very easy to hit the ground running. Everything else is like Postgres: databases, schemas, tablespaces on steroids, triggers, stored procedures, plugins. I really enjoy the geo-replication features.

It’s a very solid product with a permissive license. YugabyteDB is a complex distributed system but the complexity is well hidden behind an intuitive set of APIs and command line tools.

Before jumping into the code, I spent a couple of days reading through the documentation, which was very easy to follow.

Finally, I’m not very familiar with C++ but I was able to follow the source code without major issues.

## HAVE YOU BUILT OR MIGRATED ANY APPLICATIONS TO YUGABYTEDB?

#### WHY? WHAT WERE YOUR EXPECTATIONS? HAS YUGABYTEDB DELIVERED ON THEM?

I am in the process of delivering a multi-tenant database as a service for a client. So far, YugabyteDB delivers on the promise. My personal interest lies in IAM / IdP systems and I am evaluating the Ory stack on YugabyteDB.

## WHAT FUTURE PLANS DO YOU HAVE FOR YUGABYTEDB?

#### CONTRIBUTIONS TO THE CODE BASE, BUILDING OTHER PROJECTS WITH YUGABYTEDB AS A BACKEND, ETC.

Something like Keycloak but with row-level geo partitioning would be great to have in the IAM / IdP world. As time goes, I hope to contribute to YugabyteDB. Especially in the documentation and operational procedures area. I share my knowledge on [my personal blog](https://gruchalski.com/); I will post more YugabyteDB material there.

## WHAT PRODUCT FEATURE/ENHANCEMENT ARE YOU MOST LOOKING FORWARD TO?

#### YOU CAN ALWAYS FIND [OUR UP-TO-DATE ROADMAP ON GITHUB](https://github.com/yugabyte/yugabyte-db#current-roadmap).

Having a more recent database engine is always worthwhile, so I’m definitely looking forward to the PostgreSQL 12 compatibility. The other ones are online schema migrations, full ALTER TABLE support, and more day two operations documentation and guides.

## HAVE YOU LOOKED AT OTHER DISTRIBUTED SQL OR DISTRIBUTED DATABASES IN ADDITION TO YUGABYTEDB?

#### IN YOUR OPINION, WHAT SETS YUGAYBTEDB APART FROM THE REST?

Before starting with YugabyteDB, I evaluated Cloud Spanner with the Postgres compatible proxy, Amazon Aurora, CockroachDB, CitusDB, and creating custom tooling for managing distributed PostgreSQL. The offerings from the major hyperscalers fell short fast: they do not provide a complete Postgres API as they tend to be an add-on feature on top of a different paradigm, and they do not offer a possibility to run on-premise. The other distributed databases were disqualified based on the licensing model.

YugabyteDB is the only database on the market with a complete, distributed PostgreSQL API which can be deployed on-premise and operated as a service.

## HOW WOULD YOU DESCRIBE YUGABYTEDB TO SOMEBODY JUST STARTING THE PROCESS OF FINDING A NEW DATABASE?

#### WHAT ADVICE WOULD YOU GIVE THEM?

If you need PostgreSQL and plan for scale, definitely consider YugabyteDB. It will take you from a single node to global scale with little-to-no effort. My advice would be to read through the documentation first. The documentation covers a lot of interesting aspects of the system and that knowledge will be beneficial long-term.

## ANYTHING ELSE YOU WOULD LIKE PEOPLE TO KNOW?

Erlang is awesome for learning functional programming. Tests and documentation aren’t boring. Integration tests are better than unit tests. Don’t assume, talk to your users.