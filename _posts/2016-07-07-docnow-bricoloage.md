---
layout: post
title: DocNow's Theoretical Bricolage
tags:
- archives
- docnow
- conference

---

*Below are some remarks I made on a panel at Archival Education and Research
Institute ([AERI]) 2016 about the [Documenting the Now] project.*

---

Thank you for the opportunity to be here at AERI today. I have to apologize for
not being able to present on the topic proposed by Bergis Jules a little less
than a year ago. If he was able to make it Bergis was hoping to talk to you
today about research that he has been doing into how African Americans’ access
to traditionally privileged digital information spaces presents archivists with
opportunities and challenges around collecting and preserving social media
records. In many ways that particular research was eclipsed by a project he and
I have been collaborating on for the last year called [Documenting the Now].
When deciding whether to continue the presentation Ricky suggested that I use
this time to share some background information and preliminary work about the
Documenting the Now project. For the purposes of this panel I thought I would
also try to highlight some of theoretical perspectives that I think are guiding
the project.  Please bear in mind that this is largely what we might call in the
software world *vaporware*. It is research that is still in the process of
becoming.

### Documenting the Now

A good friend of mine once advised me to lead presentations with the punchline:
to start with the thing I want the audience to remember, in case they decide to
tune out, or walk out. Perhaps that window has already closed. But just in case
I thought I would start by briefly describing the goals of the Documenting
the Now project.

The Documenting the Now project is a two year partnership involving Washington
University in St. Louis, the University of Maryland and the University of
California at Riverside that will achieve three distinct but interdependent
goals:

1. To deposit a collection of 13M tweets into an institutional respository running at Washington University in St. Louis.
2. To develop an open source application, DocNow, that allows researchers and archivists to create their own collections of Twitter and Web content.
3. To build a community of practice and documentation around social media
archiving, with particular attention to ethical practices of collecting "public"
data from Twitter.

If you remember nothing else from this presentation just remember those three things we are trying to achieve. I'm going to spend the rest of my time here telling you a bit more about each of the goals, and their theoretical context.

### The Dataset 

Almost two years ago, Michael Brown, an 18 year old black man was killed by Darren Wilson, a white police officer in Ferguson, Missouri. The killing initiated a series of ongoing protests and demonstrations in Ferguson, that were then amplified by the emerging BlackLivesMatter movement. Two days after Michael Brown was killed, the Society of American Archivists annual meeting began in Washington, DC. There was much conversation among attendees about the need to document what was going on in social media and on the Web around the protests. It makes sense that this would be the case, for as @Punzalan:2016 recently wrote:

> ... the cause of social justice has been a topic of discussion on various archival
> fronts for at least 40 years. If the birth of the modern Western archival
> profession occurred in 1898 with the publication of the Dutch Manual, then the
> field has been tackling various aspects of social justice issues for nearly
> half of its modern history. With this trajectory, we believe that the
> conversation will continue in years to come. (p. 32)

Standing on these 40 year old shoulders Bergis and I decided to do what we could
to collect the conversation in Twitter that was happening in response to killing
of Michael Brown. We collected 13 million tweets that mentioned the word
"ferguson" in the two weeks following his death. The process highlighted the
strengths and weaknesses of the tools that were available to us, and ultimately
raised questions about the ethics of performing this data collection that was 
generated by hundreds of thousands of users. Our work took a new turn in the
following year as the #BlackLivesMatter movement raised awareness about the
deaths of Eric Garner, Tamir Rice, Walter Scott, Freddie Gray, Sandra Bland and
Samuel DuBose--many of which we collected Twitter conversations for. Indeed, it
continues still today as awareness was raised in Twitter about the killing of
[Alton Sterling] and [Philando Castile] just days ago.

Bergis and I wrote about this data collection work on Medium in the [On Archivy]
publication, which tapped into an existing wellspring of interest in the role of
archives in social justice, and the emerging BlackLivesMatter movement. The
analysis of @Jackson:2015b as well as @Freelon:2016 has since confirmed the
pivotal role that Twitter played in incubating and building awareness about
the killing of Michael Brown. They write:

> Without focusing on the first week of the Ferguson network and further
> unpacking the network by day, we would not have been able to see the important
> influence of key crowdsourced elites and members of American counterpublics.
> In particular, our data spotlight the discursive labor of initiators and other
> influential everyday citizens, most of whom were young and/or African-
> American, who pushed the larger public sphere to address what happened to
> Michael Brown and offered ideological interpretations of Brown’s death and
> resulting events firmly situated in minority experiences with state
> oppression. [@Jackson:2015b, 412-413]

This Ferguson dataset is what we are planning to deposit in some form into the Fedora based institutional repository at Washington University in St. Louis.

### The Application

We performed data collection using a utility I had previously created called [twarc]. I think it's fair to say that twarc is a user *unfriendly* tool. It runs (assuming you can install it in the first place) from the command line, which isn't really accessible to a large number of users. There are a variety of other [tools] available, but none that would allow us to easily search tweets that had already been sent, and save the richly structured data available from the Twitter API. Realistically, twarc was also *ready-to-hand* since I was already familiar with it, and time was of the essence.

Time was of the essence because of some peculiarities related to the Twitter API. Only tweets from the past seven days are available via the Twitter search API. In addition you can only request 100 tweets at a time, and those requests can only be issued 180 times every 15 minutes. So these quotas or [rate limits] control how many tweets can be requested in a day: 1,728,000. If you do not observe these limits your requests for data will be denied, and your application can potentially be blocked by Twitter. So we were working against the clock to collect the tweets before they fell out of the 7 day window.

While it is by no means a secret, understanding social media platforms, and how
to work with them as they change and evolve over time is not knowledge that is
widely held by archivists and researchers. Bergis and I became convinced that
there was an opportunity to build an application that would empower users to
create these collections for themselves. In addition to collecting the Twitter
conversation we also wanted to build on the work of @Rollason:2015 at the
Internet Archive in using the Twitter conversation as an appraisal tool in
archives of Web content.

In his recent critical analysis of Web 2.0 technologies @Proferes:2016 offers an
interpretation of social media platforms using @Braman:2006's concept of
*information power*, where power is realized through an individual's or
collective's ability to make choices about how information about them is
collected and shared.

> What is important is that access to information about how this part of the
> platform works creates the possibility for the individual to make a choice.
> Choice creates the possibility for the expression of informational power.
> These possibilities are closed off when users do not have the basis of
> informational power from which to enter these fields of action.

I think Proferes' application of information power is a
useful critical lens to view our application development through. We know in
this post-Snowden environment that powerful entities already have the ability
collect and analyze large amounts of social media content. We want the DocNow
application to inform and empower archivists, researchers and content
creators in the building of social media archives.

### The Community

Finally, and most perhaps most importantly, we want to build a community of practice around the ethical collection of content like the Ferguson dataset from Twitter and the Web. This work began in small part at the Maryland Institute for Technology in the Humanities where we hosted a series of four [BlackLivesMatter Teach Ins] around the Ferguson dataset. We also sought out a partnership with Washington University in St. Louis since their work on the [Documenting Ferguson] project complements the work we were doing in social media.

As the Documenting the Now project took shape, and we put our proposal to the
Mellon Foundation together, Bergis assembled an [advisory board] of 20
individuals coming from a variety of backgrounds: sociologists, political
scientists, archivists, software developers, and journalists. We will be meeting
for the first time in St. Louis on August 21-23 in order to explore together
what shape the DocNow application could take using a [prototype] we have been
working on for the past few months. We will also be joined by a group of
activists who used social media during the Ferguson protests. The involvement of
activists and our advisory board in the design of DocNow is central to our work,
and is informed by two strands of theory.

[Value Sensitive Design] where the ethical values of direct and indirect stakeholders are factored into the design. In particular @Shilton:2012's work on *value levers* is an important conceptual tool for opening and sustaining conversations about values while allowing those conversations to inform the design. 

The second is the application of a feminist ethics of care recently outlined by @Caswell:2016 where relations between the archivist, record creators, subjects, users and communities are marked by an attention to the contingencies of mutual responsibility. As they say:

> We cannot ethically continue to conceive of our primary users as academic 
> scholars; survivors of human rights abuse and victims' families use records,
> community members use records. We need to build policies, procedures, and
> services with these users in mind, but even more so, we need to shift our
> affective orientations in service to these users.

We see engaging the activist community who generated content in social media as
key participants in the design of DocNow. Hopefully a year from now we will have
more to report about how this fusion of theoretical ideas plays out in the form
of the DocNow application and community.  If any of this is of interest we
welcome your feedback in our [Slack channel] which currently has over 100
members. Don't worry, not all of them are active at the same time. Also, please
join us for the livestream portions of our St. Louis meeting in August. We will
be sending out information about that via our [newsletter]. I'll be around here
at AERI till Tuesday so please find me if you want to learn anything more about
the project.

### References

[AERI]: https://www.kent.edu/aeri2016/paper-presentation-abstracts
[Alton Sterling]: https://en.wikipedia.org/wiki/Shooting_of_Alton_Sterling
[Philando Castile]: https://en.wikipedia.org/wiki/Shooting_of_Philando_Castile
[twarc]: https://github.com/edsu/twarc
[tools]: http://socialmediadata.wikidot.com/
[rate limits]: https://dev.twitter.com/rest/public/rate-limits
[Social Feed Manager]: http://gwu-libraries.github.io/sfm-ui/
[Documenting the Now]: http://www.docnow.io/
[BlackLivesMatter Teach Ins]: http://mith.umd.edu/researching-ferguson-update-previewing-miths-teach-ins-blacklivesmatter-umd/
[advisory board]: https://news.docnow.io/introducing-documenting-the-now-416874c07e0
[prototype]: https://github.com/docnow/dnflow
[Slack channel]: https://docs.google.com/forms/d/1Wk0JdF2Cty2VHMqpf_QlJXVKQdUtfeeFhaYRben3qaM/viewform
[Value Sensitive Design]: https://en.wikipedia.org/wiki/Value_sensitive_design
[Documenting Ferguson]: http://digital.wustl.edu/ferguson/
[newsletter]: http://eepurl.com/bMNJsX
[On Archivy]: https://medium.com/on-archivy