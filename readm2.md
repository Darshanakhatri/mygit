# Need for Tweet: How Open Source Developers Talk About Their GITHUB Work on Twitter 

## Author

HONGBO FANG, DANIEL KLUG, HEMANK LAMBA, JAMES HERBSIEB, BOGDAN 
VASILESCU

>When: Tue 30 Jun 2020 16:00 - 16:10 at MSR:Zoom - Developer Collaboration 
Chair(s):**_Bogdan Vasilescu_**

[summary2 link](https://cmustrudel.github.io/papers/msr20tweets.pdf)

https://www.youtube.com/watch?v=DlXObspmZiI

## Introduction and Motivation

Twitter is a general social media platform. Twitter is especially popular with software 
developers and actively studied by software engineering researchers. The activities on open 
source platforms like GITHUB are only a part of the overall software development ecosystem 
and that open source developers are often active on multiple platforms simultaneously, there is 
a paucity of research studying the same populations of developers across platform.
Looking prior work, in this paper the researchers discuss that how they propose a 
computational approach to cross-link users on Twitter and GITHUB, the dominant platform for 
hosting open source development, revealing 70,427 users with accounts on both. Using this 
dataset we then report on a case study of 786 tweets by open-source developers about GITHUB
work. Specifically, we analyze tweets containing links to GITHUB repositories, combining 
automatic characterization of tweet authors in terms of their relationship to the GITHUB items 
linked in their tweets with qualitative analysis of the tweet contents. 

## Research methodology:

Social media and Software Engineering: Software Engineering researchers give attention 
to social media. As early as every researcher give his own idea about social media, that for what 
purpose it is used. Further studies have shown that different social media is used for different 
purposes and has various impacts, for improving the quality of communication, to staying 
aware of the status of other developers.
Borges and Valente found that popular open source projects are more likely to use Twitter as a 
promotion channel and hypothesized that such promotion may increase project adoption and 
popularity.
Cross-linking GITHUB and Twitter:  This section presents our heuristic approach to crosslink GITHUB and Twitter user accounts, based on mining GITHUB user profile pages and 
personal blogs for explicit URLs pointing to twitter. For example if we link two accounts and 
they share the same email address tends to be a highly precise heuristic but with relatively low 
recall (many people have multiple email addresses but they would not be linked this way). 
Matching people based on names is expected to have lower precision, but relatively higher 
recall (more accounts get merged). Facing the same precision-recall trade-off, we developed 
two heuristics expected to have relatively high precision: (1) mining explicit links to twitter 
accounts from GITHUB user profile pages; (2) crawling personal websites linked from GITHUB
user profile pages and mining links to twitter accounts therein. The aim here is to provide a 
large initial dataset to catalyze research in this promising area.
Our final dataset consists of 70,427 GITHUB-Twitter user id is available online. 
Case study: How GITHUB developers talk about their work on Twitter: According to dataset, we 
perform an exploratory case study of the content of a sample of tweets by GITHUB users in our 
dataset that contain links to GITHUB artifacts.
We focus on tweets containing links to GITHUB since these are more likely to be work related as 
opposed to social and therefore among the most relevant content on which to study the impact 
of twitter activity on software development outcomes. To create our case study sample we first 
collected all the tweets returned by the twitter API for each of the 70,427 users in our dataset. 
We then characterized the relationship of the tweet author to the GITHUB repository 
referenced in each tweet. Suspecting different tweeting behavior by different types of 
stakeholders, we distinguished between the following five mutually exclusive groups, sorted 
roughly by the level of authority and involvement with the project.
Owner: the tweet author owns the repo. Our sample contains only repositories owned by
individual user accounts, not organizations; our results should only be interpreted within this 
context.
Collaborator: the tweet author has write access to the repo, that is, closed others issues or pull 
requests.
Contributor: the tweet author contributed to the repo pull requests, commits or issues.
Follower: the tweet author follows on GITHUB any of the repo owner, collaboration, or 
contributors.
Other: none of the above.
Finally we randomly sampled 200 tweets from each of the five strata for our qualitative 
analysis. The two researchers proceeded iteratively. First each independently coded a random 
sample of the same 50 tweets then compared results. 


## Result:

Here result seem to suggest that GITHUB project role and Twitter posting patterns are related. 
We discuss how this can inform future research.
Six major themes emerged from our qualitative analysis and here is these.
Question: these tweets ask about technical details of a repository or about an open issue. Most 
tweets in this category link to a GITHUB issue.
Answer: these tweets respond to questions by other twitter users.  
Call for action: The authors of these tweets actively seek or request actions from others this 
include collective actions like starting a repository, helping to solve an issue, or requesting 
someone to merge a pull request.
Repository Advertisement: Tweets advertising or advocating for the use of the linked 
repository. Most such tweets link to a repository homepage.
Work discussion: Tweets which are part of a discussion on twitter, but are not a suggestion to 
use a certain repository.
Information Sharing: tweets which inform the public or specific individuals about the existence 
of a repository, a file, an issue discussion or other work related news but no explicit intension to 
advocate for the use.
Our result are partially aligned with YASIR et al, who found that python core contributors 
mostly tweet about software related and community related topics, the main difference 
between our results and theirs in the bulk of tweets on repository advertisement, which may be 
explained by the fact that python is a well-known language which needs less advertisement.
Cross-linking data across online platforms where open source developers participate is feasible 
and it can help provide deeper insights into how the activities of developers on one platform 
are moderated by the roles they play on the other. The social media activities of developers 
may also have direct impact on software development outcomes, including open-source project 
success. We provide a large dataset mapping 70,427 open source developer GITHUB and 
twitter accounts, as bases for future empirical research in these directions. 