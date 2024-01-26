Join TWiGS host Chris Adams in talking to Kristina Devochko, tech lead of the Environmental Sustainability TAG at the Cloud Native Computing Foundation. Kristina shares her journey from economics to tech sustainability, and eventually joining this Technical Advisory Group. Further, they discuss the mission and projects of the group, as well as how anyone interested and willing is able to contribute. She elaborates on her experience of diving into this new field with no prior knowledge and acts as a reminder that no matter how scary it seems, you can do it too.

**Learn more about our people:**
- Chris Adams: [LinkedIn](https://www.linkedin.com/in/mrchrisadams/) | [GitHub](https://github.com/mrchrisadams) | [Website](https://www.thegreenwebfoundation.org/)
- Kristina Devochko: [LinkedIn](https://www.linkedin.com/in/krisde/) | [Website](https://www.kristhecodingunicorn.com/)
**Find out more about the GSF:**
- [The Green Software Foundation Website](https://greensoftware.foundation/) 
- Sign up to the [Green Software Foundation Newsletter](https://greensoftware.foundation/)
**News:**
- [TAG Environmental Sustainability](https://tag-env-sustainability.cncf.io/) [09:56]
- [The Week in Green Software: Carbon Aware Spatial Shifting](https://podcast.greensoftware.foundation/e/489vqm0n-the-week-in-green-software-carbon-aware-spatial-shifting) [15:13]
- [Kepler](https://sustainable-computing.io/) | [16:07]
- [GSF Oslo Meetup group](https://www.meetup.com/gsf-oslo/) [34:08]
**Events:**
- [CNCF Cloud Native Sustainability Week](https://tag-env-sustainability.cncf.io/events/cloud-native-sustainability-week/) (**2023**) [14:43]
- [Green Software Foundation Oslo - February Meetup](https://www.meetup.com/gsf-oslo/events/298048644/) [34:31]
- [Carbon Hack 24 | Online | 26th Feb to 15th March](https://hack.greensoftware.foundation/?utm_source=github&utm_medium=online&utm_campaign=hack24) [39:02] 
**Resources:**
- [Cloud Native Computing Foundation](https://www.cncf.io/) [01:53]
- [Kristina’s cat, Penelope](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/537965iA3CCCB1F7861D1AF/image-size/medium?v=v2&px=400) [02:51]
- [Kristina’s cat, Sofie](https://techcommunity.microsoft.com/t5/image/serverpage/image-id/537970iED707D14AA09F6DB/image-size/medium?v=v2&px=400) [02:51]
- [TAG ENV | Linktree](https://linktr.ee/cncfenvtag) [09:29]
- [Kepler GitHub repository](https://github.com/sustainable-computing-io/kepler) | CNCF 
- [Exploring Kepler’s potentials: unveiling cloud application power consumption | CNCF](https://www.cncf.io/blog/2023/10/11/exploring-keplers-potentials-unveiling-cloud-application-power-consumption/) [23:23]
- [Environmental Sustainability Glossary](https://tag-env-sustainability.cncf.io/glossary/) [24:33]
- [Green Reviews WG task board](https://github.com/orgs/cncf/projects/10/views/12)[24:45]
- [Green Reviews WG project repository](https://github.com/cncf-tags/green-reviews-tooling) [26:45]
- [[WG Green Reviews] Design Document](https://docs.google.com/document/d/19fzZW-IMv2kDNatKFHeHh7wqcEN0e2N60wzxvCGZd48/edit) 
- [TAG ENV Slack Channel](https://tr.ee/-cFaJgMJRl) [31:31]
- [GitHub - cncf/tag-env-sustainability: 🌳🌍♻️ TAG Environmental Sustainability](https://github.com/cncf/tag-env-sustainability) [31:44]
- [Green Software Champions](https://speakers.greensoftware.foundation/) | Speakers [35:38]
- [Platypus - power side channel attack for RAPL](https://platypusattack.com/) [23:15]

**If you enjoyed this episode then please either:**
- Follow, rate, and review on [Apple Podcasts](https://podcasts.apple.com/us/podcast/environment-variables/id1618265745)
- Follow and rate on [Spotify](https://open.spotify.com/episode/0C4N7dk5p461ugjeoZGLqz)
- Watch our videos on The Green Software Foundation [YouTube Channel!](https://www.youtube.com/channel/UCj0m2KL1yQzcCbmSj7AaAoA/videos)
Connect with us on [Twitter](https://twitter.com/gsfcommunity?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor), [Github](https://github.com/Green-Software-Foundation) and [LinkedIn](https://www.linkedin.com/company/green-software-foundation/)!
**TRANSCRIPT BELOW:
Kristina Devochko:** You know, there weren't many there at that meeting, but they were so passionately discussing the different topics around the topic of sustainability in tech, specifically in the cloud native technologies. And I really loved the passion and interest from those who were there.

**Chris Adams:** Hello, and welcome to Environment Variables, brought to you by the Green Software Foundation. In each episode, we discuss the latest news and events surrounding green software. On our show, you can expect candid conversations with top experts in their field who have a passion for how to reduce the greenhouse gas emissions of software.

I'm your host, Chris Adams.

Hello, and welcome to another episode of Environment Variables, where we bring you the latest news and updates from the world of sustainable software development. I'm your host, Chris Adams. Well, we talk a lot about green software on this podcast. If you've listened to some of these episodes, you'll realize that cloud is a really, really, really big part of green software now.

And last year, the Cloud Native Computing Foundation set up a sustainability focused working group. And given that it's the new year, 2024, it seemed worth checking in on it to see what's new. So today, I'm joined by Kristina Devochko, who's part of the CNCF and some of these groups. Kristina, thank you very much for joining us on the course.

Should I give you a bit of space to introduce yourself and talk about where you're coming from today?

**Kristina Devochko:** Yes, of course. Hello Chris and hello everyone listening into this episode. Thanks for inviting me. My name is Kristina Devochko. I am a platform engineer at Tietoevry and I'm based in Oslo, Norway, and I am very excited to be here. I am also a Microsoft MVP and a CNCF ambassador. And what comes out of that is that I do a bunch of different activities in the tech community that are mainly related to the topics of cloud computing, green tech, Kubernetes. And one of such activities is my involvement in the CNCF Technical Advisory Group for environmental sustainability, which kind of also correlates with, with a bit of my personal passion for this domain.

And a fun fact about me is that I am what you can call a cat mom at heart. And actually yesterday, right before we joined today with you, Chris, for this podcast, I, me and my husband welcomed two new family members, two adopted kittens that I will run to after we are done with this episode and kind of keep, continue training them to feel safe in their new home.

**Chris Adams:** Wow, I was not expecting cat pics so early in 2024, but it sounds like we might need to have some reference to this, because you can't talk about cats without sending pictures of cats. So maybe that's something we add to the show notes.

**Kristina Devochko:** Yeah, that's, by the way, one thing. I love adding the photos, fun photos of my cats into all the technical content I make. So if you would like, we could totally do that.

**Chris Adams:** All right, if anyone who's not watching for this, I have to say, while I'm using like a basic headphone, Kristina has an awesome set of headphones with glowing cat ears on this. So this may be a running theme for the rest of 2024. All right, so if you're new to this podcast, my name is Chris Adams. I work at the Green Web Foundation, which is a Dutch nonprofit focused on reaching a fossil-free internet by 2030.

I also work in the policy working group inside the Green Software Foundation, where we do work on policies and respond to future coming legislation and things like that. But for the purposes of this show, what I can share with you is that while we talk about this, and we're going to mention various projects, we do our best to share a transcript and set of show notes for all of these things.

And because it's New Year, we're going to be trying something new. We're going to be posting a transcript of this plus all the links onto GitHub. So if there's something that you're curious or you want to learn more about or we've got something wrong, we'll be accepting pull requests for the transcript if there's anything that you really were curious about.

And yeah, we'll be sharing that on podcast.greensoftware.Foundation as per usual. And I think with that, should we begin then, actually, Kristina?

**Kristina Devochko:** Yeah, let's do it.

**Chris Adams:** All right. Okay. So, Kristina, you mentioned before that you're calling from Oslo, and I no longer live in England, but I grew up in England, so old habits die hard, and we always talk about the weather.

And I'm calling you from Berlin today, which is coated with snow. So I should actually ask, how is the weather in Oslo today? 

Wow. 

**Kristina Devochko:** Oh, that's a very relevant question because it's quite freezing, actually. And like, personally, I love winter and I love snow. And we were lucky enough this year to have a truly white winter and Christmas and the New Year's Eve. But I need to say that this year we had like a few extreme cold waves happening in Norway.

And I was recently reading an article, I live just outside of Oslo and like, right after the New Year's, in the beginning of January, there was a new record that was hit in the Oslo municipality, where it was registered to be minus 31.1 degrees Celsius, and that's like, the previous record was from 2011, and it was 28.8 degrees, I think. And today I had an appointment at 9am before this podcast recording. And when I went outside, I saw that the temperature was minus 20 degrees. So that's kind of when you feel that your nose is full of needles at that point. So I love winter, but not when it's that freezing. But I'm here now in a warm room and happy to be joining you for this podcast. So...

**Chris Adams:** Well, I'm glad. I'm glad we're both in somewhat warmer temperatures than minus 31 degrees Celsius. All right. Okay. Fun fact for this, if people follow along, there is, if you have any kind of carbon aware websites today, the coldness is actually changing some of the carbon intensity for some websites. So there's a website called Branch that me and some friends maintain.

It actually broke the code because it was so cold and so not windy in the UK for a certain time that the carbon intensity went higher than we've ever seen it. So this is an example of how some of this can manifest in software itself. All right, so we'll get to that a little bit later on, but I should basically, before we dive into this, it's worth asking, you now work in green cloud computing and that's like your new specialization.

But that hasn't always been the case. So if I understood it, you did, you worked as, you trained as an economist first before you came to working with cloud and development, and then you changed directions into this field. Is that the case? 

**Kristina Devochko:** Yeah, yeah, that's true. I mean, I never, I never thought of working in tech as being my kind of career. I wasn't born and raised with like all this programming knowledge from the start. So I came from a culture where it was natural for women to do something else than computer science. So for me, in my head, it was natural to do something like economics.

And that's what I started with. I got accepted to the bachelor's program at the university. And then I figured out that it was so boring. The first year I started, it just didn't work out. I couldn't find the motivation. And I had a friend who was studying computer science, but more into the NLP domain, into natural language processing.

And she kind of challenged me because kind of the atmosphere there was good and people were nice. And it was interesting. So I just took a chance and applied and got in. And from that point on, there was kind of no way back. So I started working with as a full stack developer and got really that spark after studies.

And for two years ago, I think there was someone from the community who challenged me, like, why don't you start contributing to the tech community as well? There is so much you can do there if you really love working with tech also outside your full time job. So I actually started doing that, and from that point on, it's like, I've tried a lot of different things, and I find it being a lot of fun, so it's for me like more, it has become more than a full time job, a source of income, it has become a hobby, and a sort of passion, and like if, since we are talking more about the sustainability in this podcast, personally, I've been really focused on that area, like in my life, in my everyday life, living a more eco-friendly, planet-friendly lifestyle. And from that, it kind of naturally transitioned into also putting focus on that at work, in my company. And from there, I ended up joining the Environmental Sustainability Technical Advisory Group. So it was like a very interesting journey starting, now that I look back at it, starting with economics and thinking that this is my only way to kind of take my career and then like ending up in a totally different space.

That's, yeah, that is somewhat, somehow that was a bit of magic for me.

**Chris Adams:** Okay, cool. Thank you for that. So there's from an academic transition to I guess an energy transition really. And as I understand it, so in the last year you got involved because you mentioned the Cloud Native Computing Foundation Technical Advisory Group for Environmental Sustainability. That's quite a mouthful.

I mean, I have to ask, is there a short name for it or is there something I should use instead when I'm using that? Because I don't think it rolls quite off the tongue and I'm sure there's a faster way I can refer to that, right?

**Kristina Devochko:** Oh, yeah, totally. I know. That's like, that's a bit of a wording there because you need to kind of also showcase where this technical advisory group come from. So, like, we call it the TAG ENV, like TAG ENV. So TAG for technical advisory group and ENV is That's kind of our abbreviation for environmental sustainability.

So we just call it TAG ENV or CNCF TAG ENV. So that's what we also use in our writing, writing content. 

**Chris Adams:** TAG ENV is easy. TAG ENV I'm going to use from now on if I'm going to refer to this, because that's much, much faster, and it's kind of fun to say. All right, okay. So I should have to ask then. There is now a TAG that's focused on ENV, right? And maybe you could tell me a little bit about actually what it does, and what kind of work or what kind of projects might be associated with that, for example.

Or maybe even how you got involved in it, actually.

**Kristina Devochko:** Yeah, of course. So, CNCF has, and CNCF, the Cloud Native Computing Foundation, so I'll call it CNCF. It has a specific structure as an organization, so it has different groups in order to ensure that the different projects and users and organizations that are supporting the foundation can kind of develop and improve in a sustainable, expandable manner. So the, therefore there is a concept called Technical Advisory Groups. And this is basically a group that is led by people that are community members that are specialized in that specific domain that the group covers. And then anyone from the community can join those groups depending on their area of interest and participate in the meetings, participate by contributing to the different projects and activities that are going on in those, in those TAGs, which is the short version of the name. And there are many different areas. There is security, observability, there may be networking and like for, I think now it's two years ago, like one and a half years ago, the Environmental Sustainability TAG was founded by some of the community members. And at first we didn't hear about it. Like I personally haven't heard about it until spring last year, because I was starting to prepare more content on the topics of green tech. And I got in as a speaker at the KubeCon and CloudNativeCon Europe conference, which was in Amsterdam in April last year. And I start, and I was doing my research, preparing for the talk, and I, by chance, found this TAG, this group, and I was like, wow, okay, CNCF has a dedicated group now, but it, it didn't seem very active because it was just starting out. And then I, of course, highlighted it also during my talk and also saw on the schedule during the conference that they had the pro, a group meeting. So I just joined that, actually knowing nothing about the community in that group. And that was really for me as a beginner, a bit scary, but at the same time, when I joined, I was very warmly welcomed and I loved the engagement, you know? There weren't many there at that meeting, but they were so passionately discussing the different topics around the topic of sustainability in tech, specifically in the cloud native technologies. And I really loved the passion and interest from those who were there that I thought, "wow, cool. This seems like people really care about it, not just do it for, you know, to check, have a checkmark somewhere." Yeah, And I started just after that, I came back home and I started joining the regular meetings and just contributing with small steps, just doing some minor changes, asking questions.

And now it's less than a year actually. And now right before Christmas, I got appointed to be a tech lead for the technical advisory group. And I'm really happy about that because I've been putting a lot of love into supporting the TAG and we have grown and it's really great to see more and more people joining us and also joining on the activities that we are doing. And kind of the main mission of this group is to raise focus and raise awareness about the importance of sustainability in the cloud native landscape.

Like what is the current state of that?

What kind of challenges we have and how can we help both the CNCF landscape, the projects there, but also the companies that are utilizing those projects that are running in cloud, be it public cloud or private cloud, are running in a cloud native manner, how can we help them get the sustainability of their systems and software better, basically? 

**Chris Adams:** Okay. I'm somewhat aware of the TAG ENV'S work. I remember that, I think, last week, there was this, last, towards the end of last year, there was a sustainability week with a bunch of online talks by various people presenting, yeah, and we'll share a link to that, and I know there's a couple of other projects that we're going to talk about in a bit more detail, and you've mentioned this idea of, well, what is a state of the art, how do you make some of this visible to people, and you name checked some things like observability.

Are there any kind of particular projects that you're particularly excited about, or you might be seeing kind of repurposed, because you, I believe you mentioned one project, and I think in July we had Niki and, Niki and Ross, who were also part of the TAG at the time, talking about some of the work in making carbon emissions more, more, more observable and visible to people.

Maybe you could talk a little bit about that, because I think that's one thing that you've mentioned to me that you're quite excited about.

**Kristina Devochko:** Yeah, absolutely. And Niki and Ross, it's great that they have been on the podcast because I know that they have been talking also about Kepler, which I also wanted to highlight in this episode as well. And they are also driving now the kind of subgroup in our Environmental Sustainability TAG that also has a separate project, which I also would like to talk a bit more about afterwards.

But like the first CNCF project that I would like to highlight that kind of touches upon the observability piece in context of measuring, like, the sustainability of your, of your system. And that is Kepler. And this, this project has now, for a few months ago, I think, entered the CNCF landscape as a sandbox project, so that's kind of a big deal for the whole project and everyone who was supporting it. And for those of you who are listening in and haven't heard about Kepler, it's the short name for Kubernetes-based Efficient Power Level Exporter.

So that. sounds like a very complex name, but that actually makes meaning. So that's a word with the meaning behind it. So this project, its main goal is to measure energy consumption so that this data can be gathered, collected, and afterwards you could feed it to the machine learning models that can perform a specific analysis on that power usage utilization data. And then you could visualize that. And by visualizing that over time, you could also understand how efficiently your resources, your power is being used and what kind of optimizations you can make based on that. So you could kind of...

This could help you make more informed choices on, in terms of optimizing your resource usage.

**Chris Adams:** So there's a couple of things I just want, so I just want to check if I, check my understanding and also for other listeners on this. So there's a tool called Kepler, and because measuring power usage inside the cloud can be quite challenging at times, this is essentially an open source tool that goes some of the way to looking to making that more accessible and observable to people who are responsible for, like, operating clusters of computers and things like that.

And, if I understand it correctly, it's using what was the kind of hip and trendy software, like, Extended Berkeley's Packet Filters. It's using something quite close to the metal, so it doesn't actually slow down the system to report information as much as other things. Or, at least, that's one of the considerations that people have been taking some steps for.

Is that correct?

**Kristina Devochko:** Yeah, you're correct. And I think an important piece to mention here, like coming on to your point that it's not that easy, necessarily, to gather this type of metrics for power consumption. Like if you think about bare metal, that type of data can be more, in a more easier manner gathered because it is available directly from the hardware when you're running on bare metal, but when it comes to cloud providers, or like when you're running on virtual machines, this, there is no support in virtual machines to be able to make these types of metrics available.

So there, that's why it may be challenging for example to get 100 percent accuracy of running Kepler on, on managed Kubernetes service. And to just make a notion of that, Kepler is mainly targeting the Kubernetes-specific workload. So when you're running Kubernetes clusters, be it on bare metal or be it in, as a managed Kubernetes service, for example, in public cloud. And like you mentioned, it also uses BPF to gather some of that specific metrics specifically that would be specifically useful in, in public cloud. But we would link a blog post as well that I would recommend to check out because it goes in more very technical details around the different deployment models and architecture for Kepler because they have, they are currently working on a specific deployment model that I really hope we will get to see public cloud providers collaborating with Kepler project on, which would potentially allow to not use a pre-trained model with some kind of pre, pre tested, yeah.

Pre, there is like a data set that was based on some of the other data that the Kepler community has collected, for example, from running on bare metal.

And it does make some assumptions based from that. So it provides some pre-trained power models that you could use in public cloud to get somewhat close to reality type of data, but still, for example, things like idle power, you will not get that information or that metrics from Kepler because there is no way for the tool knowing about how many VMs are running on the host when it comes to public cloud.

**Chris Adams:** Oh, I see. 

**Kristina Devochko:** There, that's kind of the, there are some limitations there and this blog post goes very nicely into those details. But the deployment mode that they're working on, that would allow you to install Kepler on the host first, that public cloud providers could do. They would install Kepler on the host first, that would gather that hardware specific metrics for power consumption.

And then you would kind of have a layer. 

**Chris Adams:** The visibility at that point, rather than like, you're inside the virtual machine guessing how many other neighbors are also using your physical machine, you're actually getting the physical machine saying, "yeah, you actually have 10 neighbors and six of them are mining Bitcoin."

Or they wouldn't be doing that. But like, you get the general idea. I'm not sure if you're allowed to do that in some, in a lot of clouds. Okay. I'm glad you mentioned that. 

**Kristina Devochko:** Hmm. Yeah. So that would require some collaboration with public cloud providers since they have control of the hardware. But then in that case, you would kind of install Kepler twice. You would install it on the host and you would install it in the Kubernetes cluster. But then by doing that, cloud providers, maybe by making Kepler data from their hosts available as an add-on on, yeah. 

**Chris Adams:** Service you could then subscribe to. 

**Kristina Devochko:** So you could get that data. Yeah.

So you could get that data and you could get an even more, more accuracy on that power consumption metric. So I really hope that the adoption of the project takes off and we get to see it available in the managed Kubernetes services in public cloud, for example. So i, it's, it looks really promising, to say least. 

**Chris Adams:** I'm glad you mention that, because there's one project inside the GSF, this is the Green Software Foundation for other people, called the Realtime Cloud Project, which is currently led by, amongst others, Adrian Cockcroft, formerly VP of AWS, and there's people from Microsoft and also Amazon who are working to essentially do the carbon part if, if things like Kepler are actually exposing some of this.

And for the nerds who are on this, listening on this podcast, I'm going to ask for your help. Because one of the reasons that's cited for not sharing this information is there's a very particular kind of attack that you can use if you have direct energy emissions being exposed at a very high resolution.

You can find out what programs are running or even some information like that. So there are reasons cited for not sharing this information. There's a whole line between zero knowledge and letting everyone get hacked and like the, the research that we've seen or that's been shared inside there is that around the minute resolution, that's still enough for operators like yourself to kind of like tune and manage carbon, but also is something that still mitigates against most of these attacks.

And I do forget the name of the animal that the attack is named after, but if you're listening to this and you submit a PR, I'll be very grateful for this because it's got a cool name. It really does. But I'm totally blanking on this. If you're curious about this as well, we did actually do a podcast in July last year with both Ross Fairbanks of Flat Peak and Niki...

I can never pronounce her surname. Niki, I'm so sorry. Niki, she works at Grafana and, Manoladeki, I believe. So that's the people. And we'll share a link to that podcast, which dives into a bit more detail about some of that. Okay, so we spoke about that. And that's one of the wider projects that has some application clearly inside this.

But there's maybe some projects, there's a, well, there's one or two projects inside the TAG ENV that you're also involved in, that you said that you'd like to kind of talk a little about. Maybe if we give you a bit of space to mention one of those, perhaps.

**Kristina Devochko:** Yeah, of course. So like Kepler and other projects that are coming out that are related to sustainability, we support them as a technical advisory group. But we also are looking for ways we can also contribute by starting some of the projects inside the TAG. And we have a few like content focus projects, like the landscape document that Kind of covers the state of sustainability in the cloud native space that we are working right now on creating a version two for. And we have recently published the glossary for cloud native sustainability glossary that could help clarify some of those specific terms. But when it comes to more technical contributions, I wanted to highlight the project that we are working on in the subgroup of the TAG that is called Green Reviews, so it's a working group that is run by Nicky, Antonio, Antonio DeRosso, which is one of our TAG contributors and now is his co chair in the group, and Ross Fairbanks as well, that is the technical lead for that group. And what we are working on in that group is that we are building a workflow that can be used to target the projects in the CNCF landscape, like Kepler for like, not like Kepler, but the other projects that you would be using, for example, Kubernetes, Kubernetes, I think would be a better suggestion in this case, because the workflow actually uses Kepler together, some of the, of those metrics.

So this workflow would then be connected towards those CNCF projects that will be running under load and so that we could simulate a load on kind of the application itself so that we could gather the sustainability specific power and resource utilization specific metrics over time so that we and that workflow could analyze the data and publish information about the sustainability posture of that project.

And this statistics can then be publicly available for all the projects in the CNCF landscape so that over time, the project maintainers and project contributors could look into the states of their projects from the sustainability side and improve the resource utilization of those projects over time, make them more resource efficient, which also is one of the goals for Kepler projects, for example. 

Find those bottlenecks that, find those ways to improve and make those projects more lightweight and more resource efficient. So this is also something that is open for anyone to contribute. So if you like to code, you could just join and pick an issue and, you know, start helping out.

So if you would like Chris, you're also welcome to join. 

**Chris Adams:** Maybe some, there may be some things we look into a little bit later on. So, if I understand that correctly, there's a couple of things you mentioned, and you use this term sustainability posture of a project. I'm taking that to mean like, what the kind of profile might be like, where, under what, so how it might perform under certain circumstances and what in certain places it's, is it more efficient here or less efficient there, is that what you mean when you say that?

So, the idea, you get an idea of where there might be common areas for improvement across the whole portfolio of projects, for example, based on some of the real world data. Is that the thinking behind it?

**Kristina Devochko:** Yeah, we are like still in very early phases. So this working group has been like a few months old. So the piece, for example, of what kind of methodologies we would use to calculate that, that kind of sustainability posture, how efficient a project is, we have still not 100 percent defined that. So I think we want to start like simple by just gathering some of the Metrics like the SRE specific metrics, you know, like CPU, memory usage, maybe use, use the Kepler specific power consumption metrics.

Start there. And then the next step would be to see what other metrics we would need, or those metrics that we have collected by now, should we use as, the Software Carbon Intensity Specification, should we use that in combination with something else? Should we use something like Impact Framework Engine, right?

From GSF. So we have been looking into that. There are some discussions around if we should use, for example, SCI as a Software Carbon Intensity methodology. 

**Chris Adams:** That's one way of measuring the basic, it's a bit like, a little bit like PUE for data centers. It's like the amount of emissions associated, a kind of rate, as a software. Okay.

**Kristina Devochko:** So that we could provide some of that information, like you say, that we could provide, like how much power has been used, if we could correlate that to the amount of carbon emissions, maybe water consumption at some point, because this is also becoming very important these days with enhancements in artificial intelligence and machine learning.

So we're still figuring that out. So I don't have an exact answer for how exactly it will look like, but this is an opportunity for anyone also from... Yeah. 

**Chris Adams:** Refer to some of the existing state of the art. Okay, that's cool. For folks who were interested in listening along to this, so, Kristina, what you've actually described might make you think of an episode that we did with Arne from Green Coding Berlin. We've interviewed him as well.

He spoke about some of this in a bit more detail. We should share a link to that because he dives into very deep amounts of data for this and also his organization has been sharing some really interesting stuff about the difficulties of tracking some of this stuff on the cloud. Because, you know, one of the, while the cloud can be extremely convenient, there are knock-on effects on basically having an amorphous blob of compute that you kind of tap into, rather than having a direct machine that you can direct measure directly.

All right, great, and I'm really glad you mentioned the glossary and some of the other things you had, because one thing that I found really helpful when helping other people actually to talk about something for the first time is having this stuff saying, "well, this means this," or even just having the landscape with you seeing that, well, "wow, there's actually a really wide range of projects where the sustainability aspects do touch on a bunch of these things."

So, thank you for mentioning those, actually. I should probably ask you now on relating to that. We spoke about, like, TAG ENV. And we spoke about some of the projects that are ongoing, but it might be useful to talk a little bit about how you folks organize and how people can get involved, because I was able to join the Slack and chat to a few people to kind of more get a kind of feel for it, but I figure it might be useful for other people to realize that it is actually quite easy, and this is something that you've invested a bit of time in to make accessible to people, and well, you're here, so I should, I guess I should ask you really.

**Kristina Devochko:** Yeah, I appreciate you asking that because we are always looking for ways to communicate to the other community members that it is not that scary and difficult as it may seem to start contributing to some of these groups and organizations. So in the TAG, it's pretty, I think it's quite simply structured.

So of course we have some of the chairs of the TAG, and we have also tech leads that kind of overview the different types of activities in the TAG and in subgroups are done in accordance with our mission and our goals and contribute in that area. But it is open for anyone to join. So we don't have necessarily like a membership or anything. So everyone can just join our slack our regular meetings we have both meetings for the TAG in itself, which are bi-weekly, and the working groups-specific meetings as well. And anyone can just join and start asking questions, participating in discussions, you can go to our GitHub repository and in the issues filter on 'help wanted' or 'good first issue' labels.

And then you could see if there is something that resonates with you, or you could just start by contributing to the existing discussions in those issues. You could contribute content. So if there is a specific topic that you would like to write a blog post on when it comes to cloud native sustainability, you could just submit that, and then we will help you to get it there, to get it on our website, to get it on the CNCF blog. So there are quite a few ways you could just start. And even if, yeah, and even if you feel like, it feels a bit scary, you are very much welcome to reach out to me. We could probably share some contact info, or just go on the Slack and send me a message if you need some guidance on how to join us.

And we have a separate blog post that we recently wrote.

Step by step guide. 

**Chris Adams:** Like how to take your... okay, well you heard it here first, you have a direct offer from one of the members to help you in if you're curious about doing this. This is one thing I actually quite admire about the CNCF. With the Green Software Foundation we, while it's a membership organization, it can feel a little bit difficult to get in, and this is one thing that I've been really impressed by.

And I'm aware that yes, there are all these weekly calls and there's things where it's very easy to see what's going on if you're remote, for example. But as I understand it, you do a fair few things in Oslo as well for like people who like to meet up and physically share the same physical space as other people sometimes, like doing meetups as well.

Maybe you might want to just briefly touch on that before, because I know this is one of the first things we have coming up in 2024 that you mentioned actually. 

**Kristina Devochko:** Yeah, that's true. And like, like you mentioned with the Green Software Foundation, I, when I first started learning more about it, I was like, "Oh yeah, I would like to become a member." And then I realized that my company was not part of that yet. So it was not, not that easy, but still, you, you of course have some opportunities to just follow and participate in discussions.

But what I also liked when I saw that GSF started with local meetups, local meetup groups and supporting that initiative. And then when I checked, there was no one, no such meetup group in Norway. So it was open for anyone to just start one under the GSF umbrella. So in September last year, I just asked if I can do that.

And then we started a group, Green Software Foundation Oslo Meetup Group, basically, which will, I hope can become an arena for the, to grow and strengthen the local community of technologists who are passionate about the topics of green software and green coding in general. And we had one meetup last year to launch the group in October and hopefully can have it on quarterly basis.

So now the next meetup coming up is in, in February, and we'll have some nice topics about the impact of AI and machine learning on sustainability and also the adoption of Cloud Carbon Footprint, open source tool in one of the Norwegian companies called ODA, and I believe one of the recent episodes was precisely on that topic, wasn't it? 

**Chris Adams:** No one admits to using it, but it's basically underpinning so much of all this stuff. Yeah. That's really, I'm glad, I didn't actually know that Oda was actually doing that kind of work. And it's quite nice to hear that, yeah, it shows up in various places, because I, I really enjoyed chatting to, chatting to the guys last, for the last episode, and nerding out about like Legend of Zelda, if nothing else.

That was of

the

call 

**Kristina Devochko:** yeah. 

**Chris Adams:** was some of it. Okay, so we've shared a link to the Oslo meetup group, so people can find out about that and when that's taking place. I believe that's open to anyone who's physically in Oslo. You don't need to be a member of anything like that, you just need to be interested along those lines.

I should probably, at this point here, just give people a heads up that if you're not in Oslo, and you're not on remote event, and you're maybe organizing events, it's worth knowing that there is actually a directory of potential speakers at speakers.greensoftware.foundation. This is one place where, if you're running an event, and you're looking for someone who can contribute some expertise, or is able to kind of help with it then, that's one resource.

And also, I believe that you've shared a link here, which is run from the CNCF, which basically has a listing of other events coming up as well. Is that the case?

**Kristina Devochko:** Yeah. On the website for the TAG ENV, we have a separate events section and currently we are working on adding, implementing some automation because we have the tool that was donated by some of the community members so that we could use to scrape the data about different sustainability related conferences, sessions, meetups, and then we could continuously update that events page.

So hopefully there will be coming out there automatically in not too long. So you could check that one out as well.

**Chris Adams:** That sounds cool. I can't believe in 2024 we still don't have a kind of, like, solved problem. Like, we haven't solved the problem of events yet, like finding out when they're coming up. Because this is something I really struggle with, and I'm glad that you have that mentioned. And I think you just said something kind of cryptic but interesting there. So there was a Cloud Native Sustainability Week in October, and I will happily admit on air that I basically plundered that place for all these videos and people to speak to for future shows.

And we've got one or two of the speakers who've been presenting there talking about some really deep dives. We've got, we've got some of those episodes lined up. You're planning one for 2024 as well. Is that likely to be around the same time, like October-ish?

**Kristina Devochko:** Yeah, I hope so. I, we will need to see if this is the date we should go for. We haven't decided on the date yet, but we have seen that it has been a success. It was the first time in 2023 that we decided to do it. So we were not sure how it would work out, but actually, despite the virtual mini conference that we had like a two hour event with some speakers presenting virtually, we also had like, I think we were around 20 plus local meetups that were, we calculated that it was happening in 17 countries across four continents.

So we think that it has been quite a success. So we hope we could do it on an annual basis. And now we have just started planning for the Cloud Native Sustainability Week in 2024. So if you or any of the listeners would like to contribute, it's totally open. And we have a tracking issue in the repository for that as well.

Yeah.

**Chris Adams:** you for that, Kristina. We'll share a link to the last one because there was really, I actually filed an issue in the TAG because I was like, "hi, I missed all the talks because I was in the wrong time zone." Or moreover, I might have been asleep at the time or something like that. But and then I think within two or three days, I had someone basically show like here's a list on YouTube of every single talk with links back to the slides and everything like that. It was so, so nice to see that. And there was some fantastic content. I was really impressed by that. So yeah. 

**Kristina Devochko:** Yeah, it was really good, I agree. 

**Chris Adams:** Oh, we're talking about events and I almost forgot. I should mention that there is, there's a quick announcement I kind of have to share as part of like me working in the GSF.

There is an event coming up later in this year called Carbon Hack 24. This is the Green Software Foundation's kind of global event, basically. Essentially, the idea is that it's a little bit like what Carbon Hack was like last year. So it's a week's long kind of hackathon kind of thing. This time, the focus is around a piece of software I believe you mentioned called the Impact Framework.

This is an idea which is a bit like something like a kind of manifest file or an executable manifest file for us, for people to kind of understand and measure the impacts of software. The idea would be that there's this piece of work that the GSF has been working on called Impact Framework, and the idea is a bit of a hackathon around something like that.

And at the, right now, there, we often talk about sustainability in terms of carbon only, but Kristina, you mentioned water as one, one possible dimension. And there's a number of other dimensions that we've actually spoken about as well, which are also fair game for exposing or looking into and things like that.

So that's one thing coming up. And I should say, it's online. It starts on the 18th of March and ends on the 8th of April. You don't need to stay awake for that entire time, surviving on Red Bull and chocolate. That's not a good idea. But the idea is that there's space to make it kind of accessible to people regardless of where you are in the world.

And if you go to 0hack.greensoftware.foundation, then people can see and learn all about that. And the only thing to bear in mind is that the registration is the 22nd of January. So there's a, it will need to move relatively quickly on that. Okay, there's a, there are a series of awards for that, that we'll be referring to.

And yep, I think that's the plug that I've done while we were talking about events. So thank you for bearing with me for that, Kristina. 

Kristina... 

**Kristina Devochko:** Of course, I'm very excited for that. I'm very excited for the hackathon and it's cool to see that it's not just a one day, one day, 24 hours type of activity.

**Chris Adams:** Here's my free idea that I'm unable, that I would like to work on, but I don't want to promise myself that I'll do it, because that's, I'm getting older, I'm not sure how much time I have, but I know there's a thing called Node-RED, I want there to be Node Green, to use some of the ideas behind Node-RED to create a visual representation of all of the inputs of data that you might have in, so you can work out some of this, because when we talk about this kind of stuff, it can be a bit hard to understand where information about carbon intensity might be coming from or where, like you've described utilization or how hard a machine is working is coming from.

And I think if there's a visual way to present that, that would be useful. And if there's absolute precedent of things like Node-RED being used in all these different places. So that's like kind of my lukewarm take, I suppose. Alright, Kristina. Thank you so much for spending the time to talk with us.

I really enjoy, appreciate you coming on and talking all about the TAG ENV and how people can get involved. And yeah, this has been really fun. Thank you for giving us your time and talking about this. This has been good.

**Kristina Devochko:** Thank you, Chris. It's been a great discussion. It's, it's been fun. So thank you for inviting me. It's been a pleasure. So I hope some of you would be listening in to this episode, would be interested in joining us and don't hesitate to reach out if you're not sure about anything. 

**Chris Adams:** That's a really good point. Just before we close off, we should, if people are interested in the work that you're doing, either personally or the actual TAG ENV ,what's the best, what should people be typing into their search bars, for example, just to learn about your work or learn about the CNCF's environmental work?

**Kristina Devochko:** Yeah, I think that if you would like to get in touch with me, you could probably just type my name, Kristina Devochko, and on LinkedIn, normally I use most, mostly LinkedIn, and then I have a separate technical blog where I write some technical content on those different topics, kristhecodingunicorn.com.
And if you would like to join the Environmental Sustainability TAG, you could just, I hope we will add the links to the website and to the repo, but we are also at the CNCF Slack. So if you join that, you could search for a channel called TAG-environmental-sustainability, and we'll warmly welcome you there.

**Chris Adams:** Brilliant. Thank you so much. I'm also really glad you mentioned Kris, the Coding Unicorn, because although this is an audio podcast, you need to Imagine that behind Kris there is a neon sign saying, Kris, the coding unicorn. And that's, it's... That's all I've been able to see or look at when on this conversation, so I'm really glad you mentioned that.

**Kristina Devochko:** Almost like product placement.

**Chris Adams:** Yeah. Okay. Well Kristina, thank you very much for this and hopefully you stay warm and cozy for the rest of the day. Take care of yourself.

**Kristina Devochko:** Thank you, Chris. Thanks everyone.

**Chris Adams:** Okay, bye.

**Kristina Devochko:** Bye.

**Chris Skipper:** Hey everybody, this is Chris, the producer of Environment Variables, just butting in to tell you about an additional resource that we have for the upcoming Hackathon 2024. Join us every Monday at 2:30pm GMT for our regular live stream, which explains how the IMPACT framework works and shares hack project ideas.

You can visit hack.greensoftware.foundation to find out more about that and sign up for both the live stream and the Hackathon. That's all for now, see you next time.

**Chris Adams:** Hey everyone, thanks for listening. Just a reminder to follow Environment Variables on Apple Podcasts, Spotify, Google Podcasts, or wherever you get your podcasts. And please do leave a rating and review if you like what we're doing. It helps other people discover the show, and of course, we'd love to have more listeners.

To find out more about the Green Software Foundation, please visit greensoftware.foundation. That's greensoftware.foundation in any browser. Thanks again, and see you in the next episode.
