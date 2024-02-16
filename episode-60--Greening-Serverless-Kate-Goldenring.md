Chris Adams is joined by special guest Kate Goldenring, Senior Software Engineer at Fermyon. Together, they ask the real questions “is serverless computing the greener choice?” and “if so, under what circumstances is this true?” Tune in for an illuminating conversation on the current state, news, and future of green computing, digging into the topics of cloud computing,  soft allocation, WebAssembly, and more.  
  

**Learn more about our people:**

- Chris Adams: [LinkedIn](https://www.linkedin.com/in/mrchrisadams/) | [GitHub](https://github.com/mrchrisadams) | [Website](https://www.thegreenwebfoundation.org/)
- Kate Goldenring: [LinkedIn](https://www.linkedin.com/in/kate-goldenring/) | [X](https://twitter.com/KateGoldenring)

**Find out more about the GSF:**

- [The Green Software Foundation Website](https://greensoftware.foundation/) 
- Sign up to the [Green Software Foundation Newsletter](https://greensoftware.foundation/)

**News:**

- [The first pull request to the Environment Variables Podcast Transcripts. Thanks Ross Fairbanks!](https://github.com/Green-Software-Foundation/podcast-transcripts/pull/1) [09:00]
- [PLATYPUS - the timing attack you need to know about when measuring energy usage from servers](https://platypusattack.com/) [09:30]
- []https://github.com/orgs/Green-Software-Foundation/discussions/78
- [Sysdig 2023 Cloud-Native Security and Usage Report - the report detailing average utilisation by most cloud hosts running containers](https://sysdig.com/blog/2023-cloud-native-security-usage-report/) [13:40]
- [Firecracker: Lightweight Virtualization for Serverless Applications - the paper used as the basis for AWS Lambda](https://www.usenix.org/system/files/nsdi20-paper-agache.pdf)
- [XFaaS: Hyperscale and Low Cost Serverless Functions at Meta | Proceedings of the 29th Symposium on Operating Systems Principles- the paper that kicked off this whole episode](https://dl.acm.org/doi/10.1145/3600006.3613155) [14:03]
- [Fermyon and Civo](https://www.civo.com/case-studies/fermyon) - on [their Deep Green options](https://www.civo.com/carbon-neutral-gpu) 

**Events:**

- [Carbon Hack 24: Where measurement meets innovation, and impact knows no bounds](https://greensoftware.foundation/articles/carbon-hack-24-where-measurement-meets-innovation-and-impact-knows-no-bounds/) 
 

**Resources:**

- [tag-runtime/wg/iot-edge.md at main](https://github.com/cncf/tag-runtime/blob/main/wg/iot-edge.md) [04:24]
- [Bytecode Alliance - the body where various groups working on WASM collaborate](https://bytecodealliance.org/) [05:47]
- [Basic Alpine Climbing Course - Seattle - 2024 — The Mountaineers](https://www.mountaineers.org/locations-lodges/seattle-branch/committees/seattle-climbing-committee/course-templates/alpine-climbing-courses/basic-alpine-climbing-course/basic-alpine-climbing-course-seattle-2024) [08:09]
- [A greener, cost effective cloud with serverless WebAssembly - Kate's talk at the CNCF Sustainability week](https://www.youtube.com/watch?v=GGHwYLaRe-g&t=1920s) [13:00]
- [Surprising Scalability of Multitenancy - Marc's Blog](https://brooker.co.za/blog/2023/03/23/economics.html) [22:34]
- [Introducing Spin - the WASM focussed serverless framework](https://www.fermyon.com/blog/introducing-spin) | Fermyon [31:01]
- [Software Carbon Intensity (SCI) Specification Project | GSF](https://greensoftware.foundation/articles/software-carbon-intensity-sci-specification-project/) [39:17]
- [Take it to the limit: peak prediction-driven resource overcommitment in datacenters - this is the paper detailing the default scheduling approach now used by Google to run all the servers](https://dl.acm.org/doi/10.1145/3447786.3456259) [41:06]
- [GitHub - fermyon/spin: Spin is the open source developer tool for building and running serverless applications powered by WebAssembly.](https://github.com/fermyon/spin) [42:36]
- [Fermyon Discord server - where to speak to other folks hacking on Ferymon and Spin the serverless framework](https://discord.gg/FKFe5mthQB) [43:09] 
- [Challenges and Opportunities in Sustainable Serverless Computing - the paper presented at HotCarbon 2022, explaining the difficulties with Serverless](https://hotcarbon.org/assets/2022/pdf/hotcarbon22-sharma.pdf) [43:30]
- [Fermyon Technologies](https://www.fermyon.com/blog/index) [45:56]



**If you enjoyed this episode then please either:**

- Follow, rate, and review on [Apple Podcasts](https://podcasts.apple.com/us/podcast/environment-variables/id1618265745)
- Follow and rate on [Spotify](https://open.spotify.com/episode/0C4N7dk5p461ugjeoZGLqz)
- Watch our videos on The Green Software Foundation [YouTube Channel!](https://www.youtube.com/channel/UCj0m2KL1yQzcCbmSj7AaAoA/videos)

Connect with us on [Twitter](https://twitter.com/gsfcommunity?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor), [Github](https://github.com/Green-Software-Foundation) and [LinkedIn](https://www.linkedin.com/company/green-software-foundation/)!  
  
**TRANSCRIPT BELOW:**  
  
**Kate Goldenring:** It is very clear that you reduce operational emissions by not running your application when you're not using it, so by leaving the gym. But actually, by oversubscribing, we're also reducing embodied emissions by having higher density and not needing as many servers. And so, I think this whole concept can help us decrease our software carbon intensity.  
  

**Chris Adams:** Hello, and welcome to Environment Variables, brought to you by the Green Software Foundation. In each episode, we discuss the latest news and events surrounding green software. On our show, you can expect candid conversations with top experts in their field who have a passion for how to reduce the greenhouse gas emissions of software.  
  

I'm your host, Chris Adams.  
  

Hello, and welcome to another episode of Environment Variables, where we bring you the latest news, And updates from the world of sustainable software development. I'm your host, Chris Adams. When we talk about reducing the environmental footprint of software, it's common to talk about making an application more efficient by using better algorithms or relying on languages that make more efficient use of resources than others.  
  

However, the fact remains. That for most software in the world, most of the energy use comes from having millions of computers waiting for something to happen, rather than actively doing work themselves. So if you have software designed to let someone book a ticket, or buy a book, any time of day the transaction might only take a few minutes to complete, but the software still needs to be running 24/7 in a powered up state, constantly consuming resources to make that possible.  
  

Now, common wisdom was that you need to design for peak amount of traffic you'd ever expect to see, and then just accept that paying to run all those servers all the time, waiting for something to respond was just the way it had to work. Serverless computing broke this assumption. Instead of paying per hour to have your software constantly running and available, waiting for responses, you'd design your software a specific way and pay to use it on a per request basis instead. When your software wasn't actively serving requests, it would scale all the way down to zero and you wouldn't be billed for these dormant periods. If an incoming request did come in, your software would wake up, serve them again, before going back to sleep.  
  

And in aggregate, this would result in fewer machines needing to be run. Because computing resources were being allocated in a more efficiently across a large number of programs, running them only when they needed to do work. So that was the idea, at least. While we touch on the details later in this episode, there are definitely trade offs you need to accept when designing serverless programs.  
  

And while the term serverless implies a lack of servers, there are still racks of kit required to run this infrastructure. So, is serverless computing the greener choice? If so, under what circumstances this is true, and what's the difference between a virtual machine, container, or even a WebAssembly runtime?  
  

Joining me today is Kate Goldenring, whose work I came across when she answered a really specific, really detailed question I'd asked about serverless computing. In the Green Software Foundation discussion forums, when I was trying to make sense of it all, she responded with a really helpful answer, citing a number of peer reviewed papers, as well as linking to a really informative talk that she delivered at the Cloud Native Computing Foundation Sustainability Week a few days earlier.  
  

So when I asked her if she'd be up for coming on the show to talk about some of the details of serverless computing, she agreed and I'm really happy to welcome her on to Environment Variables. Kate, welcome.  
  

**Kate Goldenring:** Hi Chris, thank you for having me. So I am very happy that that forum existed and brought us together. I am a senior software engineer at Fermyon, and we're very excited about serverless WebAssembly. And so that's something that we'll be talking about throughout this and in general, to touch on my career, I started at Microsoft, where I was actually focused on edge computing solutions.  
  

And I developed a project called Akri, which is a Cloud Native Computing Foundation, CNCF, sandbox project for managing IoT devices around Kubernetes clusters. So from the start, I was very into open source software and got to really kick off my career there, which I'm very grateful for. And I'm still in the IoT edge space.  
  

I serve as co chair of the CNCF iOT edge working group and have authored a couple of white papers on edge computing best practices within that working group.  
  

**Chris Adams:** Oh, Kate, can I just stop you just for one second? Did you say, so you were with Microsoft back then and you mentioned Akri. Now I think that was like a few years back. Was there a project called Deus that was floating around in Microsoft land there? Like they want a little bit like say, wow, that takes us 10, back 10 years or so actually.  
  

Okay. So Deus was one of these platform as a service things, a bit like Cloud Foundry and stuff like that. Right?  
  

**Kate Goldenring:** Yeah, and Deus was acquired by Microsoft and Deus Labs was how it was renamed. And it became this hub within Microsoft for its open source cloud native projects. And so Akri became a project under Deus, and then it was donated to the CNCF after that.  
  

**Chris Adams:** Okay, gotcha. Thanks.  
  

**Kate Goldenring:** Yeah, so a bit of an evolution in how open source worked within Microsoft as well, and I actually, while working on Akri and in that open source world within Deus, I learned about WebAssembly, and I got very excited, in part because I saw the potential of it for green computing and reducing the carbon intensity of software, and so I actually decided to leave Microsoft to join Fermyon, which is a startup in the WebAssembly space.  
  

And I'm still in the open source world contributing to our open source tooling there. And we actually work with the Bytecode Alliance, which is an alliance, as it sounds, of companies such as Microsoft, Amazon, Adobe, Fermyon were involved. And it's all about building out WebAssembly specifications so it can do more in more places.  
  

So that's kind of also where I am now within the weeds of the WebAssembly world.  
  

**Chris Adams:** Okay, cool. All right. I'm, I'm glad you mentioned WebAssembly because we'll touch on that a little bit later about what it actually is and why some of that is relevant, but I should probably introduce myself too, for people who are new to this podcast. So my name is Chris Adams. I am the executive director of the Green Web Foundation, which is a Dutch nonprofit focused on reaching a fossil-free internet by 2030.  
  

I'm also one of the policy chairs of the Green Software Foundation policy working groups. And I'm also one of the maintainers of a library called co2.js, which as you imagine is a library to help you work out the carbon footprint of various digital services. Alright. So, Kate, you're sitting comfortably, right?  
  

**Kate Goldenring:** Of course.  
  

**Chris Adams:** Okay, cool.  
  

Before we dive into the finer points of serverless computing, I understand it's quite early. It's earlier for you than it is for me. So it's about 4 p. m. in Berlin, 7 a. m. or 8, 7 a. m. for you, right? In Seattle, yeah?  
  

Okay. And as I understand it, when you're not in front of a computer, there are some upsides to living in Seattle.  
  

So maybe you could tell me a little bit about that before we dive into the nerdery, because when you shared some stories here, it pleased me actually, and I quite enjoyed some of the kind of names of some of the groups you're, you're part of.  
  

Okay,   
  

**Kate Goldenring:** Yeah, I'm happy to be running advertisement for the city of Seattle. I absolutely love it out here. I am an outdoor enthusiast, and I was even before I moved here. But moving here kind of took that to new heights, if we're going to be a little bit punny about it. But when I, right, soon after moving here, I actually learned that I had some.  
  

Some history with one of the mountains here, Tahoma is also known as Rainier. And I found out that my mom actually attempted to summit it when she was pregnant with me. And we did not make it to the top. I think you could probably blame me for that. But after hearing that, I was curious. And so I tried as well with a guided group and also did not make it to the top, but got to weirdly the same spot, which kind of continues this weird chain of events. But what did happen was that I really fell in love with the sport. And so I joined my local climbing club, which is called the Mountaineers. And now a few years later, I spend a fair bit of my week, three to six hours, probably helping instruct that course that I kind of kicked off this love with and teaching a cohort of students, leading trips and climbs.  
  

So I definitely, when I'm not in front of my computer, am thinking about planning trips, going on trips, and definitely grateful to be in Seattle.  
  

**Chris Adams:** Okay, cool. Thank you for that, Kate. All right. It seems we're going to continue this run of peak related puns with the next section as well, actually. So before we dive into this show and some of the things we'll be talking about, here's a reminder that everything we talk about, every project that we speak about will link in our show notes.  
  

And the show notes are also published in markdown form on a GitHub repo now. And this is my point to thank one of the, one of the people from who actually submitted a pull request to our last set of show notes, Ross Fairbanks of FlatPeak. He made the first PR to the transcript where he helped us name, basically last week, we were talking about some of the specifics about,  
  

how do I say, about a certain kind of attack, security attack that is actually named after an animal. We couldn't remember it, but it's, you need to know about this if you're going to do decent energy and carbon reporting. So we were asking, "can someone please name this?" And Ross was dutifully the person to come in and name, "yes, this is called the platypus attack," and not just that, it's one of these cool IT security vulnerabilities with a really, really nice looking website.  
  

So we've now updated that. I will link to both the PR and this attack. So you now know when someone is telling you why they can't share information, you can say, "well, no, yes, we've heard of the Platypus attack and this is the mitigation for it." So yeah, that's like the depths of our nerdery that we go into.  
  

All right then. So we've covered that. And if there are any typos or things that we mentioned that you don't see linked, you will be able to make a pull request and we will basically thank you in just the same way we thanked Ross. So you can get your 35 seconds of fame as well as you do this. Okay. And hopefully that should be a good incentive for listeners to basically help create a useful artifact for other people moving forward.  
  

All right then. Okay. Kate, I tried to give a good intro into serverless computing. And when I saw the talk that you presented, you had a really interesting framing that I hadn't come across where you spoke about the value of a service versus the costs of making it available to people. And I figured this might be a nice way to kind of open up, because this is actually, I find it really, really enabling for me to think about kind of having websites available and how you even do that, or even why you might even have a website running in the first place. So maybe if I just like gave you the floor, it would help us set things up for some of the later conversation, actually.  
  

**Kate Goldenring:** Sure. And I want to call out that I similarly had an epiphany when I discovered this concept and I actually found it within Mark Brooker's blog. He's a distinguished engineer at AWS and one of the original authors of AWS Lambda. And in this blog, he talks about how the cost of a system does not always equal the value you get out of the system. And in a cloud context, the cost of running an application on a piece of hardware is the amount of compute resources you need available for it. And so as you mentioned at the start, oftentimes we provision for the peak. So the traffic to an application is rarely constant. And when you're choosing how many resources to provision, you have to make sure there's enough of those resources of CPU and memory to handle a burst of requests. And so this means that we pay for the short term peak traffic that an application may get. However, when we think about the value we get out of a system, that's the long term average traffic. And you can think about this and even see this in payment models for serverless platforms, where you may be paying for average requests per month. And so the problem with this, when you're paying for the peak but you're receiving the average is that we have this gap and that can cause low resource utilization. And so we ideally want to close this gap and a way to do that is with multitenancy. And so multitenancy is running multiple independent applications in a shared environment. And if you increase the multitenancy of a system, so you throw a bunch of uncorrelated applications on the same hardware, where each has its own traffic ebbs and flows, the idea is that their peaks balance each other and traffic flattens. And this line gets as close to average traffic as possible. And so now we've had our costs equal our value and it's, we're all happy. But this is in some ways very idealistic. We're assuming applications are uncorrelated. We're also assuming that you have some underlying technology wherein when you aren't running your application, it is scaled absolutely to zero. It's using no resources. So this is where I get a little excited. Cause I do think we are coming upon a world where that can happen. And that is with WebAssembly, which can have these sub millisecond cold starts. And the whole goal of all of this from the context of green software is that we want higher hardware utilization, as you mentioned earlier.  
  

**Chris Adams:** Okay. So what it sounds like you're saying is that this, like this idea of like multitenancy or maybe a little bit like a gym, multiple people using the same thing. This is actually a kind of a common theme. And this basically increases the average amount of use of the kit. So it's not sitting there just waiting to do stuff, essentially.  
  

Right?   
  

All   
  

**Kate Goldenring:** Yeah. And just to point out a stat to kind of nail that home. Sysdig did a report in 2023, the Cloud Native Security and Container Usage Report, and found that 69 percent of CPU is unused in containerized cloud deployments. So we're really only using 30 percent of the resources there. And ideally we would flip that number and we would be constantly using 70 percent of the resources. And one of the ways to do this is with higher multitenancy and different technologies, and there's a really interesting paper from Meta about XFaaS, which is a serverless solution they now have created for private clouds that came out in 2023, and they found this phenomena that we talked about, the peak to average, and they describe it as the peak to trough, so not the average, but the lowest amount of requests at any given point, and found that it can be 4.3 times. So these peaks are quite high is the point of that. And the way they respond to it is by determining which workloads are delay tolerant. And so then they'll move the delay tolerant workloads to execute as a different time. And time shifting is a common thing and common recommended practice in green software.  
  

So I also want to mention that this isn't always the way we expect it to be. Not, you can't perfectly fill a piece of hardware with uncorrelated applications and you might have to find some other techniques to balance out your request frequency.  
  

**Chris Adams:** Okay. There's a couple of things that you mentioned that I just want to drill down on first of all. So you first mentioned this idea that most of the time, most computers are doing nothing, right, or they're waiting, like even with something like containers, which are considered a relatively efficient way to have lots and lots of programs running, more than two thirds of the time, they're just like not actually in use.  
  

And this is at the kind of higher levels, like say when we talk about, say hyperscale providers, you might see people talking about, "Oh, we're really good. We've achieved say 30 percent level of utilization. And that's like 10 times higher than what you might have when you're using like a series of virtual machines or even like physical machines."  
  

So there's a, basically a bunch of waste that this is designed to kind of get rid of, and I think the paper you referred to with XFaaS, they were, they basically said, "well, yeah, 30 is good, but we can go higher than that. If by, by doing some of these tricks, we've hit like 50 or 60%, which again means that many fewer bits of hardware to run this."   
  

Okay. But you also touched on something there. You said that this was a private cloud, so there's certain assumptions. What about, about the softwares? Because it's the same company, they can trust each other's workloads and they don't need to keep these things as safe from each other as they, as other ones might, or there might not be the same, there might be the same priority compared to like, say, if you're running a cloud provider with lots and lots of different customers who don't necessarily want to share each other's stuff.  
  

Maybe you could talk a little bit about this idea of virtualization and actually serverless and this idea of like isolation and why it's important. Because I think for a lot of people, they don't really, this is not something that you need to think too much about as a customer so much. You just need to know it's there, but when you're designing a system, there's actually quite a few things that you need to take into account for this.  
  

And there's been different approaches that have been developing over the last, say, 10 to 15 years, for example.  
  

**Kate Goldenring:** Yeah, I think we talked about how great it is to throw a bunch of different people's applications all together on the same piece of hardware. But that is a very scary statement to a lot of people to have their application running next to someone else's application. So there's this concept of isolation.  
  

The idea that I will be okay with you running my application next to someone else's in a public cloud so long as these criteria are met. And isolation really just means that you know that your application won't be prevented from using resources because you have an application that's hogging them. And you also know that there's not another application that's going to access your application's data.  
  

And we can actually look at the cloud as having gone through waves of this concept of isolation and keeping things separate from each other. And with each wave being motivated by a more finite mechanism of isolation, and also leading to a new type of cloud application that's come out of that wave and you hinted that kind of the start, which is virtual machines and that the advent of virtual machines, the ability to virtualize hardware with hypervisor technology has made it so that we can have multiple independent applications running on the same piece of hardware. And it didn't change the way people necessarily built their applications. It was still monolithic applications, but we could do more with the same amount of hardware now, and for context of time to start up and scale up, virtual machines take a few minutes to start.  
  

So, if you wanted to scale up the number of virtual machines, it was a slower process. Next wave, you can think of as the wave of containers, and with containers, now we're virtualizing a smaller set of technology. We're virtualizing the operating system, and now we can run dozens of tenants on the same physical hardware. And this has brought about the advent of microservices, so I can scale up individual parts of my application instead of just scaling up the whole entire application.  
  

**Chris Adams:** So could I just check, so you, so we spoke about VMs, virtual machines, so it might take a few minutes to spin up and down and then containers will be a little bit faster. Maybe Sub second or around a second. And both of these, like, these are, these are still an improvement on a physical machine, which can be weeks to get a new box set up, for example.  
  

But the advantage of a physical machine is like you have like literal physical isolation, it's totally separate from computing. So that's the idea. And there are very different approaches you can have to separate this out. And you were talking about containers and VMs, and I understand there's a few other, there's a few other steps on this kind of continuum from a total separate machine to your share of a physical machine inside it in a VM or a container or something like that. Right?  
  

**Kate Goldenring:** Exactly. And so we've gotten smaller. And then you can think of as the next wave being one of serverless. So being able to have even more applications on the same physical hardware. And this was really pioneered by the advent of the micro VM. And if you're familiar with AWS Lambda, the underlying technology for that is the micro VM, and with micro VMs now we, it only takes 125 milliseconds to start up a micro VM, and so it creates this opportunity to be able to run something only when you need it, which is a great, great future to realize.  
  

The only issue with that number is that we, we know that a hundred millisecond is kind of the boundary of where you start to notice latency, and when you add execution time and network on top of this, this 125 milliseconds becomes a bit larger. And so the result was they had to pre warm these instances, so they had to get them running before you even needed them, so they have to use resources, even when they're not being used.  
  

And that, that eats into our cost and value equation we had earlier. And so Serverless has these great opportunities, but hadn't been realized quite yet. And so the next way that I'm particularly excited about is powering and realizing serverless with WebAssembly, and achieving even higher density, and having those instant cold starts, and we're still isolated, just like a micro VM.  
  

But instead we use a WebAssembly runtime to isolate your application using linear memory and WebAssembly also has a capability-based security model so that you only have access to resources you've been explicitly granted access to in the runtime. And so you still, through all these waves can have varying, but pretty solid levels of confidence that your workload is isolated, but we're getting into different levels and ways of computing and building our applications  
  

**Chris Adams:** Uh, Ah, okay, thanks. Alright, so you spoke about this, this thing called micro VMs, which I understand was it, it sounds like basically an virtual machine, but smaller. And as I understood that, that might be, it's smaller because rather than trying to create totally virtual machine where you have all the kind of things that a regular virtual machine might have.  
  

Like you can plug a printer in or plug stuff like that. It's just a much, much smaller service area. And as I understand it, there's a service called fly. io. They use Firecracker as one of their main options. Okay. I think I understand where you're going with that. And that, so that's an improvement on VMs and possibly has offered some of the kind of isolation benefits that some people have basically criticized containers for not having.  
  

But then with like WebAssembly, this smaller thing, there's a, there are basically different approaches taken to make sure that other people's code isn't going to touch your code and vice versa. That's what you're talking about with things like linear memory and this capabilities based thing where you almost, you have to grant access to something first, right?  
  

**Kate Goldenring:** Exactly. There's different methods to achieving isolation. And I also want to point out that we've been talking about one type of isolation, which is per-tenant isolation. So the idea that one tenant is isolated from the other, but there's also an even finer grained type of isolation that we can get in this latest wave of cloud computing.  
  

And that is per-request isolation. So the idea is that my one request to my application should be isolated from the other. And in an ideal serverless world, you'd be able to guarantee statelessness across requests so that if my first request triggered a bug, It should at most affect that request. And the way you do that is by creating a new instance or a new isolation for each request.  
  

And that's been really hard to do in the past when it takes 125 milliseconds to start up your virtual environment. But with WebAssembly, because it can start in a millisecond, you can actually create a new instance of your application for every single request on request. So you have an even finer interpretation of this isolation world.  
  

**Chris Adams:** Ah, okay. All right. That helps me. Okay. So you've gone from like 125 to one, which is much, much, much faster. So that's the general idea that you have there. And I should probably ask. When you're doing something like this, I, I kind of understand the idea that if you are able to ramp up and down really, really, really fast, then you you can probably fit more peaks inside it because someone else's peak will end, will end faster than making space for someone else's peak to come in, basically.  
  

So that's the general idea. I'm not that familiar with WebAssembly myself, and maybe it might be worth just talking about what that part actually is, because I'm a developer. I might code in Python or possibly JavaScript sometimes. Do I need to learn something new? Maybe you could just touch on some of that before, and then we could see how some of that fits in, because this sounds cool and something starting up 125 times faster also sounds good, as well as being much, much more efficient. But I quite like coding in Python and I'm getting a bit old, so I'm not sure if I want to dive into learning yet another language, if I can help it, basically.  
  

**Kate Goldenring:** I definitely don't want to take Python from you. So WebAssembly, as its name suggests, was actually made for the browser. So the browser, most applications were built in JavaScript, and people were tied to their language of choice, say Python. And so WebAssembly was created so that you can build web applications in languages other than JavaScript.  
  

It is just a target for a language runtime and a universal bytecode. And so you can write your application in Python and compile it to WebAssembly, and then you could run it in the browser. That was the whole idea. And because it was run in the browser, it got all these different characteristics, such as being isolated because the browser has a bunch of. public code running next to each other. And so you need to isolate it. And that's also why it's fast. But the result is that we have this portable bytecode that can be compiled to from a lot of different languages. And if you're curious which languages can compile to WebAssembly, there are different categories of the level of support a language can have for WebAssembly.  
  

It can compile to Wasm. And also just to clarify, I've been using this word Wasm. Maybe as well, Wasm is an acronym, so a shortening of WebAssembly. So I might  
  

**Chris Adams:** Ah, thank you. I was going to ask about that. Cheers.  
  

**Kate Goldenring:** So their WebAssembly, it can compile WebAssembly. It can also compile to a WASI compliant version of WebAssembly. And if you've heard WASI before, that stands for the WebAssembly systems interface.  
  

So it's a set of interfaces that describe how a WebAssembly module can have access to host resources such as IO, networking, et cetera.   
  

**Chris Adams:** Okay.  
  

**Kate Goldenring:** So different languages have better support for that as well.  
  

**Chris Adams:** All right. So can I come in just, so can I come in just one second there? Because you've got me quite excited now, the idea that, okay, I don't need to learn a new language and me basically spending 10 years or 15 years, in my case, trying to get kind of basically some more competent Python. I don't need to throw that away.  
  

And other people can, in whatever languages they use, they can also use that. And I think you said something quite interesting about, like, I know that under the hood, when I'm coding in Python, really something's being compiled down to some kind of like assembly. As for example, but I know that when I was using my, I'm using a MacBook right now, which has a Mac chip, and previously I had like an Intel Mac.  
  

And then I had all these problems because there's different bits of, there's different architecture that these have. And I know that when I'm pushing code into say cloud sometimes. I'll be told that, "Oh, this doesn't work because you're not using an Intel machine." How does this relate there? Because it sounded like there was one kind of binary to like rule them all.  
  

But I'm, I'm not, is it really like that? That sounds kind of quite helpful. And I'm, I would appreciate that, but that sounds a bit too good to be true, basically.  
  

**Kate Goldenring:** I think it is good and it is true,  
  

**Chris Adams:** Oh, wow.  
  

**Kate Goldenring:** So, the thing about a browser is that it has to be able to run on all these different operating systems. So the code that runs in it needs to be able to do the same. And so WebAssembly, that .wasm file that you've compiled your application to, can run on pretty much the majority of operating systems and platforms.  
  

So, Windows, Linux.  
  

**Chris Adams:** I see.  
  

**Kate Goldenring:** Et cetera. also like 64 architectures, ARM architectures, et cetera. You can execute that same .wasm file. And we're going back to like the people listening to this, who are passionate about green technology. This means there's no more cross builds. So if you think about how much your GitHub runners or whatever CI you're using, how they have to build everything for all these different  
  

**Chris Adams:** all those  
  

matrixes, like all for a version of Python that go, okay. All right. So you get rid of, wow. Okay. Yeah. Okay. I didn't know that hadn't actually picked up on that. And when you say this WASI thing, so if you are used to Linux or even Unix, there's this thing, idea of like POSIX compliant, right? Where  
  

they're all going to talk to like a foster in more or less the same way. Is that kind of comparable? Was that generally the idea for that as well?  
  

**Kate Goldenring:** People will definitely compare WASI to POSIX and I think there is some comparison there for sure. WASI is definitely different in that it is a set of interfaces. So, it's basically defining a contract or an interface between a WebAssembly module and the host, or even another WebAssembly module. And this is where we get maybe into something that is called the component model, which we don't need to dig into, but it's providing a new way of building applications so that these different languages can actually talk to each other within an application.  
  

So you can imagine a universal URL library that's maybe built in Python, but can be called from Rust. And that's by adding a wrapper of the component model on top of a WebAssembly module, and they're all talking through these interfaces. And yeah, WASI describes a set of interfaces and actually. 0. 2 of WASI was just released, and that was a huge milestone.  
  

It happened only a month ago, and that has promoted the standardization and the stabilization of these interfaces. So we now have a stable release that you can target with all of these interfaces and you can find them within the WASI repo, what exactly those interfaces are  
  

and what capabilities it provides.  
  

**Chris Adams:** Okay. So if I understand it, that's basically, so this, why is he thinking? Yes, it's a little bit like POSIX, but it's, it's, it's a bit more involved in that. Like it's, the idea would be that you could have that connect to maybe another system with a kind of predefined way. So rather than me having to kind of send a bunch of json in a serialized fashion, then you have to un serialize it, there's like predefined ways of these talking to each other.  
  

Okay. I think I understand where you're going with that. And that does sound quite attractive. And that sounds useful to someone who's a developer or making some stuff here. Now, I understand that you are working on some of this yourself, and I understand that there is a, that you're, you're using one platform that, so I think when you showed me this talk, when you responded in this forum, you pointed to a talk with a platform called Fermyon Cloud, which does cover a sub, a couple of these languages that lets you run things in this new framework, Wasm thing, for example, could you maybe talk a little bit about,  
  

about that part of what the experience looks like, cause I just, it has me quite curious and I assure you, we'll get back to other things, but that was, did sound kind of cool. And I just want to go down that rabbit hole for a second, if I may, actually.  
  

**Kate Goldenring:** Yeah, and I think I've been painting this beautiful picture of WebAssembly, but it is still a fairly nascent technology. And so Fermyon is the company I work for, and we were really excited about simplifying the developer experience. So having someone come in and say, "Hey, I want to use this WebAssembly technology.  
  

How can I use it?" And so if you're familiar with Docker, which kind of created that experience for containers. They created this Docker build, Docker run experience. We wanted to do that for WebAssembly with also the step of helping you even create that application. And so the open source tool for this that we've created is called spin and it is becoming the way to build serverless WebAssembly applications.  
  

And so just with a simple spin new, you'll have templates that pop out for all these different languages. So we have 10 different languages that you can scaffold an application for. And there's SDKs for Rust, Go, Python, JavaScript.  
  

**Chris Adams:** Ah, I see.  
  

**Kate Goldenring:** Yeah, so now you've created this application, you've scaffold it, and then you can do a spin build and a spin up and run it locally. And remember, this is very universal. So whether Windows or Linux, et cetera, you can run it and then you can do a spin cloud deploy and deploy it to Fermyon cloud where we can host your applications and it's free and you can even share it with someone or if you use Kubernetes you can deploy it there.  
  

So we're really trying to simplify the developer experience of using WebAssembly and also running it in your place of choice.  
  

**Chris Adams:** Okay. You said a couple of things that caught my interest there. So first of all, yes, there is basically a tool, a little like how I might use Fly, Kotal, like to make an app or Heroku or basically some CLI to create a kind of harness for me to be developing in. And then I push to cloud, and presumably like Fermyon cloud, that's maybe a paid service or something like that.  
  

But you said I can run it on Kubernetes, which isn't necessarily run by yourselves. And you, I think in the demo, you showed me, I think the demo I saw was running on Nomad, which is a service that we use as well, where I work basically. So. You're not tied to any particular platform and once something is in this kind of Wasm format, you could have it in a number of different places that do serverless.  
  

You're not tied to like one ginormous provider or maybe two or three massive hyperscalers. You've got a bit of freedom in who you choose to work with in that scenario. Yeah.  
  

**Kate Goldenring:** Yeah, and I think that is what is really exciting also about this wave of serverless is the cross platform agnosticity of your, your bytecode that you've created. So this same dot Wasm file ideally isn't locked into one cloud, so you can run it on Fermyon cloud, or you can run it on AKS's WASI node pools, or you can run it on other serverless platforms or locally and that same  
  

application shouldn't be locked into anywhere because we're using the standard interfaces to run it. And so I think that's very exciting because what made Kubernetes so powerful was that people could switch from one cloud provider to the other. They didn't feel locked into their decision, and that's what was able to spread and kind of evangelize that kind of cloud computing.  
  

And so I think the lack of vendor lock in is very powerful here.  
  

**Chris Adams:** Okay. All right. So that's quite helpful. And this actually opens the door for some of the kind of, well, something we spoke about last week with on the last episode, there were some people talking about a company called Civo, I think Civo, who we talk about pools of resources, and we were joking about pools of resources in literal swimming pools, because they have a whole thing where they basically run computers  
  

which generated lots and lots of waste heat, somewhere where the actual heat is useful. Because, the swimming pools would typically need to be, basically get the heat from somewhere. And they often do it by burning lots and lots of gas. So, the idea was by having something like a kind of, something which was kind of compliant in this way.  
  

I think they run like a bunch of Kubernetes boxes somewhere, for example, and they don't literally put it in the bottom of this room for like some kind of piratical servers treasure chest. It's actually like, it's somewhere near, but this is one way of actually systemically thinking about some of the outputs from computing and basically doing it in a more kind of environmentally sustainable fashion.  
  

It sounds like basically tools like this, or even serverless like that, you can run in these places. And that's actually one of the options.  
  

**Kate Goldenring:** Yeah, I think, I think you're talking about Deep Green and that,  
  

that work with, and we actually use Deep Green with spin applications. You have access to all these external resources cause they themselves are stateless, but you can still attach them to key value stores, SQL stores. And another resource we've provided is LLM inferencing on some GPUs that is powered by Deep Green.  
  

And like you say, they're submerged in pools. And I believe. in vats of oil. And that captures first in the oil, then in the pool, like in a confined space. And that captures that heat externality and powers a pool. So I get very excited about the idea of capturing that externality of that compute. And yeah.  
  

**Chris Adams:** Okay, cool. That sounds, all right. I'm glad you mentioned some of that because this is something we're trying to figure out because when, when we, if you listen to the episode last week, it sounds like we think that the servers are literally at the bottom of the pool. And obviously that that's not how it really works, but basically there is some way of using some of the heat from that.  
  

Okay. All right. So I think I've got a good understanding of this, of where WebAssembly might fit into this. And I can see why when you make something, which is easy to run in lots and lots of places, then you can reduce the amount of hardware needed, but you can also reduce some of the impact that it might have by putting it in a, in a place that's more, I guess, sympathetically designed to like it's surrounding, for example, rather than venting heat into the sky, you're putting it, you're making use, you know, a sensible use of that heat.  
  

Okay. Can I just talk about something else as well? Because. We've spoken about efficiency so far, mainly in terms of matching different peaks, going up and down and everything like that and averaging this out. So that's like one option. But I think that one thing I saw you speak about, which was a new concept to me, that I just want to like check if I understand it correctly.  
  

You spoke about this idea of over subscription or soft allocation. So you've got servers and scaling them up and down. That's one way that you might make better use of the resources. But the other one, and I'm going to try and use a gym analogy, because I think that was what I thought of when you spoke about this.  
  

You said like, if you go to a gym there's like more memberships that get sold than the amount of kit that's inside it. So if everyone all tried to like use the same machine at the same time, it would work and there'd be massive fights. But because people aren't using them all at the same time, you, people kind of, you can almost oversubscribe and oversell some of this.  
  

And in the context of computing, you see something a little bit like this. So you might have like a physical server with, I don't know, let's call it say 32 gigabytes of RAM and 16 cores. Let's pretend it like a few years ago, right? And rather than only allocating 32 gigabytes worth of, of servers or programs and 16 cores, you do more than that.  
  

You'd over allocate that. This idea of over subscription is a, is a common way to make better use of the existing hardware resources. Maybe you could talk a little bit about that because. I don't think this is something that people are that aware of. And in many cases, if you think about how you might allocate the environmental impact to a server to do some calculations, you might not be aware of how many other machines are really running on that computer.  
  

It's not a one to one mapping in all these cases. I think that's my understanding. Maybe you could shed some light on that because this is something that I think a lot of people don't have too much exposure to.  
  

**Kate Goldenring:** Yeah, I, I really like that gym analogy. And I think that idea is that say I haven't... that 32 gigabyte and 16 core machine and I deploy a thousand applications to it. If all 1, 000 got a request at the same time, some would be slowed, some would not succeed because there's not enough resources on that machine.  
  

But I'm making a statistical bet here and it's informed. Usually you do some sort of understanding of traffic flows. That no, they're not all going to receive requests at the same time. In fact, I'm expecting only 30 percent to be running at once. I don't know. That's a random number. But because of that, you're able to over, you're over oversubscribing that machine. And what the result of this is, is that I'm using one machine instead of two or three, which is very exciting. And the reason, the only way you can do this is if you know that when it's not being used, it's not at the gym. So the key to this is that you leave the gym when you're not at the gym. And so you need a technology that does that.  
  

Something that actually can scale to zero. And in the past, we've been oversubscribing already with technologies that at least scale down. And even microservices, when they're not in use, are scaled down. They're just kind of idly sitting there using less resources. And if we put this in a formulaic terms there, you were saying measuring is something that we like to do, and in measuring our software carbon intensity, the Green Software Foundation has that Software Carbon Intensity formula,  
  

and that is a sum of operational emissions and embodied emissions, and it is very clear that you reduce operational emissions by not running your application. When you're not using it, so by leaving the gym,  
  

but actually by oversubscribing, we're also reducing embodied emissions by having higher density and not needing as many servers. And so I think this whole concept can help us decrease our software carbon intensity.  
  

**Chris Adams:** I see. Okay. And that degree to how much you're oversubscribing is like, that's flexible. For example, you might choose to massively oversubscribe and just accept that the performance might be a little bit ropey or in some cases, or you might be a bit more conservative in which case you're probably going to be using a bit more hardware, but you're going to have more of a guarantee that these things will work at their speed,  
  

at the desired speed. And that was probably the approach that we've taken over the last 10 years, but there are new approaches available, like you're describing with Wasm and stuff like that. All right.  
  

**Kate Goldenring:** Yeah, exactly. And I think when I talk about it being something that is hopefully it informs decision on how much to oversubscribe. We personally did load testing. So I had a fairly small machine, like eight cores, 32 gigabytes, and just a hundred gigabytes of disk and just threw as many applications as we could on there. Figured out what that density limit was and then hit it with a bunch of requests and a loader and a prober to try and figure out what are we comfortable with and setting our own limit there. And so I think everyone has to do that to kind of figure out what that, that important level of density is for them.  
  

**Chris Adams:** Okay, cool. Thank you for explaining some of that. For those who are listening, we've linked to a couple of papers specifically about this. There's one by a gentleman called Noman Bashir, who has written a bit about how this over subscription thing works. And we'll also link to this paper. There's lots of reasons you might be ambivalent about Facebook, but the paper, this XFaaS paper is actually quite interesting.  
  

And the thing that, one of the things that's interesting in the context of CarbonAware software is that, well, they, this idea that you might over subscribe and rather than that, you might also kind of offload to entirely separate data centers as another strategy to kind of keep serving things when maybe other parts of the kind of fleet of machines that are able to kind of pick some of that up, especially if they are maybe low carbon intensity because they're running a particularly green part of the grid, for example.  
  

Okay. All right then. So we've covered quite a lot of ground and quite a lot of, you know, quite detailed concepts here. And we're definitely going to link to a bunch of papers for this. I wanted to just actually ask you about, about this, cause you mentioned a little bit about Fermyon and you mentioned a little bit about WASI and some of these tools.  
  

If people are curious about some of this, where would you suggest people look? Because until I actually had this call with you, I knew there was a thing called Wasm. I knew like, it's this thing that I've seen in Pyodide as a way of like running Python in the browser. And I kind of understand that, but I didn't know where to start.  
  

And it sounds like you don't need to be writing everything in Rust, so you can do things that you could write in, like, can you write in JavaScript, for example, to have something run that runs on a platform like this, for example?  
  

**Kate Goldenring:** Exactly. You can use JavaScript. And if you want to try this out with Spin, Spin is on GitHub, but also Fermyon.com will lead it to you or developer.fermyon.Com as well. And. JavaScript works there, and we've simplified that experience by we have actually plugins to help you compile it to WebAssembly, and so you just install the plugin for that language, and then the spin build works correctly for you, and you can then immediately run it.  
  

And so it really is hopefully making that experience easier. Simpler and, and getting you going and it is an open source community. So if you are an open source developer and want to contribute, we have a discord that you can join to join the discussion, or if you have an issue, put up the issue or even maybe grab one too.  
  

So we're really trying to grow the ecosystem. And I think we have around 75 contributors currently, but we're always looking for more hands.  
  

**Chris Adams:** Okay, cool. All right. We're just going to wrap this up. And I know there will be at least one person asking, how do I do some of this work and make sure it runs in a swimming pool? Not in a swimming pool, but in a kind of very, very green fashion. If you would be able to share a link for that for the show notes, I'd be very, very grateful because that sounds kind of cool.  
  

And the idea of putting computers in lots of new places where the heat is useful rather than a waste sounds kind of exciting to me.  
  

**Kate Goldenring:** Happy to do that.  
  

**Chris Adams:** Okay, cool. All right then. So we spoke a little bit about... okay, this is like a kind of serverless that's somewhat flexible and quite resource efficient. And one thing that I think you demonstrated, which caught my eye was you were spinning up how many, it was like a thousand applications on your laptop to demonstrate that, yeah, you can run serverless in lots of places.  
  

Can I just actually ask you a little bit, how about that came about because it was a pretty cool demo and it was lots of fun and I haven't seen nerds clap over for a demo for a while, but it was really, really nice actually.  
  

**Kate Goldenring:** Yeah, so I hinted a little bit about the motivation for that, and that was to figure out how much we could handle in our cloud. So I was tasked with load testing our cloud and basically coming up with a number of, this is the size of our instances we use, and, and how many applications can we put on each instance.  
  

And so, as you pointed out, I was using Nomad there, and we basically had a multi tenant version of Spin that had a listener for every single application that was deployed. And then just deployed as many applications as we could on my laptop, my poor laptop, until it couldn't handle it anymore and just cleaned it with a bunch of requests. And that was all in the vein of trying to figure out how dense we could go.  
  

**Chris Adams:** That was really useful for me to know because I, until I'd seen that, I generally assumed that serverless almost always means either some massive, chunky Kubernetes cluster, or it's going to be some proprietary tool that, okay, I understand why they're, they're, they're necessary, but that makes you feel a little bit uncomfortable about, okay, this is my future is only one provider, for example, that provided a bit of freedom on that.  
  

Okay. Brandy, if people wanted to follow your work, for example, where would you direct people's attention to? Cause we're just coming up to time and this has been lots and lots of fun and I've really enjoyed seeing some of your talks and some of the things you've been writing about. And I suspect there may be other, other ones as well, because yeah, this has been really helpful for me.  
  

**Kate Goldenring:** Yeah. I tend to try to promote the interesting things I find or I'm putting out there on my LinkedIn predominantly and sometimes on X as well. And both of those are just my full name, Kate Goldenring, as the handle. But if you want to talk more specifically and personally about a question, I'm on the CNCF Slack, the Kubernetes Slack, Bytecode Alliance's Zulip, and then if you're just interested in following blogs about WebAssembly and Serverless, Fermyon, we have a pretty active blog on our, our website, so just.  
  

permian. com, you can find it. And so, and that's where we can find more out more about those swimming pools that we have some GPUs running in.  
  

**Chris Adams:** Okay. Kate, well, this was lots and lots of fun. I really enjoyed it. And I, if nothing else, I enjoyed actually reading all the papers and learning so much about this. So, Kate, it should be coming up to eight o'clock for you. So I should probably say, have a lovely day and thank you very much for that. Kate, I really enjoyed this and I learned a bunch of new things about serverless, scaling up, scaling down, gyms, swimming pools, and Wasm. Thanks, Kate.  
  

**Kate Goldenring:** Thank you so much, Chris.  
  

**Chris Adams:** Hey, everyone. Thanks for listening. Just a reminder to follow Environment Variables on Apple Podcasts, Spotify, Google Podcasts, or wherever you get your podcasts. And please, do leave a rating and review if you like what we're doing. It helps other people discover the show, and of course, we'd love to have more listeners.  
  

To find out more about the Green Software Foundation, please visit greensoftware.foundation. That's greensoftware.foundation in any browser. Thanks again, and see you in the next episode!