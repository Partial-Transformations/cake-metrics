# DEFINITIONS

This document will contain our definitions, from high level concepts all the way down to the data models and their properties.

## Training Sets

For this project, we define our training sets as follows:

### Schema Training Set

To create this training set, we will need to collect examples of database schemas that represent real-world configurations. We will extract the properties from these schemas, but not the individual PII associated with the records. The properties (now tokens), will be used to represent a vast example of these real-world configurations.

Strategies for creating this data set:
- Public examples of database schemas which have been shared willingly. An example would be a dev blog where the development team has exposed some of their schema.
- Public examples of database schemas which have been shared unwillingly. An example would be a breached data set, left in a public space.
- Scrape API documentation and rebuild database schema from model defintions.
- Rebuild database schemas from API activity collected using tools like Burp.

Commentary:
We initially believed we could approach this entirelly using breached datasets. Initial research suggests that we can leverage these, but there may not be enough useful examples to build a training set from. After exploring OSINT tools and building a simple Port Scanner- it dawned on me that we could approach the problem through the lense of OSINT by reverse engineering open API's through their open documentation and scanning techniques.

#### Real-world configurations

This definiton will expand in detail once we have created our schema distributions. Until then, this could be describe as the "common approach and naming conventions employed by everyday engineering teams".

#### Sources

Early on we will attempt to leverage examples from various sources like leaked data sets from breaches. We will also need to figure out a way to "scan" and "infer" this from more private sources.

### Honeypot Training Sets

To create this trainign set, we will use a combination of our Schema Training Set, Real-world configurations, and LLM (possibly reinforcement if necessary) via OpenAI, to generate realistic looking sets of records that match the associated generated database schema, or a complete honeypot dataset.

### Network Topology Training Sets

This is a stretch goal, but would provide additional value and layers of defense. The aim would be analyze, extract, and complie a training set of common network topologies and traffic, to generate realistic looking network infrastructure and activity, both delaying the attacker, and leading them to the honey pot data set.

Sources list:
- 

