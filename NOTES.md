## INTERESTING TOOLS
- https://github.com/telekom-security/tpotce
- https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
- https://github.com/SwiftOnSecurity/sysmon-config

A couple of thoughts from Derek:
- I would like to avoid creating a "training set" from their existing data and resulting in a duplicate set, ie duplicate risk.
- The way marauder works, it does not use AI/ML, it is a straight duplicate of network names... for this project, straight duplicates or even jumbled duplicates, would be of no value.
- To me, the goal would be to ingest and use an emphemeral training set, and even I accept that we will run into limits around training and output.
- How do we best verify the output dataset does not contain any false negatives, i.e. the AI just spit out a random dupe? or lazyily mixed two records together.
- Typical high-value data fields; PII, Names, Addresses, Contact Details, Payment Methods, Private Content.
- The private content aspect is interesting because we could also explore a honeypot "juicy-content", that looks like a data set but literally contains the code to change dynamically once copied or moved.
- While listing these out- It made me think- what if Blue Teams employed more reverse red team tactics? To a degree this is a Purple Team- but how many of these actually exist in practice?
- Lastly, do we deploy a reinforcement approach to enhance the output based on real attack data?
- How could we approach obfascation of real data in a way that it looks like a bad honey pot.
- Also generating development data sets...

## PRIOR RESEARCH
Some "prior research", not all related, but may help think out side of the box...
- https://arxiv.org/abs/2009.11208
- https://www.hindawi.com/journals/scn/2020/8865474/
- https://www.hindawi.com/journals/scn/2019/2627608/
- https://www.rapid7.com/blog/post/2016/02/29/the-yellow-brick-road-to-machine-learning-with-honeypot-data-our-lessons-learned/