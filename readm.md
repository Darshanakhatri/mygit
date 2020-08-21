# Code Duplication on Stack Overflow

## Authors

Sebastian Baltes, christoph treude 

>When: Tue 7 Jul 2020 08:29 - 08:35 at Baekje - I4-Clones and Changes
Chair(s): **_Chanchal K. Roy_**

[summary1 link](https://empirical-software.engineering/assets/pdf/icse20-clones.pdf)

https://www.youtube.com/watch?v=QVN4f7qhHk0


## Introduction and Motivation 

In this paper, we motivate why studies on code duplication within SO are needed and how 
existing studies on code reuse differ from this new research direction. We present similarities 
and differences between code clones in general and code clones on SO and point to open 
questions that need to be addressed to be able to make data-informed decisions about how to 
properly handle clones on this important platform. We present results from a first preliminary 
investigation, indicating that clones on SO are common and diverse. We further point to 
specific challenges, including incentives for users to clone successful answers and difficulties 
with bulk edits on the platform, and conclude with possible directions for future work.
Code clones have been extensively studied in the software engineering research community. 
Code clones on stack Overflow can suffer from similar issues as code clones in software 
projects, it is only recently that researchers started investigating them. Studies have shown that 
developers utilize code snippets from stack Overflow in their software project regardless of 
maintainability, security, and licensing implications. The main focus of that previous work was, 
however, to study how and why developers use SO code snippets outside of the question and 
answer platform. While researchers worked on identifying duplicate questions, their main goal 
was to replace or support the manual moderator process for marking duplicate questions 
rather than supporting the maintenance and evolution of code on stack Overflow.
In this paper we want to discuss two use cases of duplicated code on stack Overflow that have 
not been adequately targeted by previous research.
Case 1: original code snippets being reused in multiple threads 
Stack Overflow users utilize code clones to accumulate views and up votes. At the same time 
they can reject edit proposals referencing the clones. 
Case 2: Externally available snippets reused in multiple threads
Many snippets on stack Overflow are copied to and from the platform, not all snippets are 
posted originally there. Stack Overflow users copy code snippets from reference 
documentation into stack Overflow posts. Besides licensing and copyright implications, it is 
questionable whether this behavior  contribute to the sustainability of the platform, because 
users may reuse outdated information in case of authoritative source gets modified. Even if one 
of the clones gets updated, the changes are not automatically propagated within the network 
of clones on stack Overflow.  

## Research 
Motivated by the two cases outlined above, we argue that there are three research questions 
need to addressed to be able to make an informed decision on how to handle code clones on 
stack Overflow . The goal is that is to provide the data informed actionable recommendations 
which the community and stack Overflowï¿½s internal team can use to update their user guides, 
but also to built tool support for managing and maintaining code clones on the platform.
RQ1: How frequently are code snippets copied between stack Overflow posts?
RQ2: What types of clones exist and how are they related?
RQ3: What are typical external sources of code snippets on stack Overflow and which licensing 
and maintainability implications are associated with those sources?
First question helps us to access how common the outlined problem is, the second is to deepen 
our understanding of the different use cases of clones on stack Overflow and the third one is to 
understand the implications beyond the platform.
To detect code clones on SO, we utilized the Big Query version of stack Overflow First, we 
selected all code blocks from the most recent post versions and normalized the contained 
whitespace characters. To this end, we: (1) replaced sequences of new lines with a single new 
line character, (2) removed new lines at the end of the last line, and (3) removed lines only 
containing brackets (()[]{}). Using this normalized content, we calculated the normalized line 
count of those code blocks. To derive fingerprints of the snippets, we only considered 
alphanumeric characters and applied Big Queryï¿½s FARM_FINGERPRINT function to the 
normalized code block contents. This yielded 43,942,960 distinct fingerprints. We then used 
this fingerprint to determine the posts which contain a certain snippet, aggregating that 
information per thread. To select cloned code blocks, we first selected the ones present in at 
least two different threads, yielding 909,323 distinct fingerprints. This provides a first estimate 
for RQ1: 2.1% of all distinct code blocks have a copy in another thread.
To address RQ2 and RQ3, we first ranked the code snippets according to their thread count and length 
and then qualitatively analyzed the first 50 snippets according to that ranking using a web tool we 
specifically designed for that purpose. The tool allows to focus on a single snippet in a dedicated view, 
showing the snippet, its fingerprint, the posts containing the snippet sorted by their creation date, other 
posts linked from those posts, and linked external sources. The latter information helped us to identify 
if and from where a snippet may have been copied into SO. While we still categorized ten snippets as 
configuration files, 29 snippets were non-trivial source code snippets. The main external sources were a 
website providing android tutorials and official Android documentation. We identified possible licensing 
conflicts in 31 cases either because the website did not provide a license or because the content was 
distributed under a restrictive license or restrictive terms of use. 
Leaving the licensing implications aside, code clones within stack Overflow are also problematic for the 
platforms maintainability and usability. Code duplicates could for example indicate that different 
threads solved a similar problem. If there is no link between the threads information is spread over the 
platform and hard to capture for readers. Another example is stack Overflows recommendation to 
always quote the most relevant part of an important link in case the target site is unreachable or goes 
permanently offline. While it makes sense to quote important aspects of external sources, it can be 
questioned whether it is reasonable to maintain several independent copies of external code snippets 
on stack Overflow. Assuming that a snippet in the reference documentation is updated, all copies on 
stack Overflow would require a manual update as well.

## Result
With this paper, we want to point to the fact that code clones on SO, similar to clones in regular 
software projects, affect the maintainability of posts and can lead to licensing issues. However, we also 
point to differences such as the fact that SO users may be encouraged to clone successful answers to 
achieve a higher reputation and that snippets are difficult to modify through bulk edits. These 
differences have practical implications and might suggest new features for SO, such as allowing bulk 
edits for adding attribution information or improving detection of overly zealous self-plagiarism. We 
also mentioned that SOï¿½s current recommendation for handling content from external resources may 
not be suitable for code taken from reference documentation, because the authoritative source should 
be the reference documentation and not SO. Moreover, when clones on SO are not updated, users 
consulting SO threads instead of the reference documentation may be prone to using outdated or 
erroneous information.
Our preliminary results suggest that code duplication on SO is relatively common (RQ1). Despite our 
limitation on exact clones, we found that 2.1% of all unique code blocks were used in more than one 
thread. Our analysis also revealed that a wide variety of snippets is being cloned (RQ2). We noticed 
cases where the same user copied the same snippet into several answers in different threads.
Identifying typical external sources and developing ways to keep the content on SO up-to-date is a 
promising direction for future work. This research could even be extended to include other online 
forums or code hosting platforms.

