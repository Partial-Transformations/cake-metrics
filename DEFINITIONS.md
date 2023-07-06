# DEFINITIONS

This document will contain our definitions, from high level concepts all the way down to the data models and their properties.

## Training Sets

For this project, we define our training sets as follows:

### Schema Training Set

To create this training set we will need to collect examples of database schemas that represent real-world configurations. We will extract the properties from these schemas, but not the individual PII associated with the records.

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

