# Who's responsible for a Production bug?

Like "Death, Taxes and me never giving up on standup comedy", discovering bugs in a production system, is a reality of Software Development.The key aspect of discovering these bugs is to discover them early! That's why I always preach and practice
> "Test it soon, Test it often, Test via Automation"

Now let's discuss a scenario, QEs are all too familiar with…

A critical Production bug has been found in the middle of the night and it's impacting your system( one or a combination of functionality, performance, availability etc)!!! Monitoring alerts start getting fired. The team has been summoned, a vid bridge is set up, engineers and stakeholders join the vid chat, in their PJs, half-awake, questioning their life choices. 10mins after a debrief, all hands on deck, and the team flex their combined muscles to come up with a hotfix and a production deploy. Everybody's relieved, the customer success team is happy, the team goes back to sleep & the world is a happy place again!

Except …

In the scrum tomorrow, the spotlight falls on the QE working in the project.
Few of us have been lucky to work with amazing teams, where there's a blameless culture(Rackspace, Cylance & now Secureworks), but the flipside also exists where companies with a good reputation of a great culture also fall prey to looking at the wrong side of Quality! Picture this, post a midnight hotfix ..

The QE walks into work, sleep-deprived, over-caffeinated, emotionally drained from the happenings of last night. The mood is one of relief, where everyone is recalling the events of last night. The QE gets a notification on his/her mobile. 5 mins to daily Scrum…

### Why wasn't the Prod issue caught in testing?
A classical question, which is posted to QEs time and again when a critical bug is discovered in Production! There might be multiple reasons for this, lack of QE understanding of the scope of feature, inadequate detail in specs/stories, lack of defensive code(logging, memory dereference, etc) from the development team, the exact scenario that caused the bug is a previously discussed, yet dismissed as an unlikely edge case by the team. So who do you think is responsible for this issue???

> The answer is… does it matter?

Promoting a blameless culture, where postmortems(root cause analysis) happens with a sole intent of improving the product and avoiding a repeat is the mark of a highly successful engineering team, IMHO.
But, the business still wants to know, the management would like to address the issue in a constructive way. So the answer to the question of

> Who's responsible for a Production bug? Everyone!


It might not be the answer you're looking for, but this less glamorous and noncontroversial answer is a key mindset for building highly successful, high-quality software!
Quality is a shared mission…
Now getting a little more into detail on the core topic of this blog. I firmly believe, Quality is and should be a shared mission. By that I mean, there are multiple stakeholders who are involved in taking an idea to a customer usable feature/product. And it's all of their responsibility!

Let's dive into, who are our key stakeholders I'm referring to.
- Product Manager
- Project Manager
- Software Architect
- Software Engineers
- Quality Engineers

I have QE at the end. This is intentional because IMO, QE is the last line of defense! Now, let's look at how each of the stakeholders, should play their part towards Quality, IMHO.

#### Product manager
They are, in my opinion, the first in line when it comes to quality! They are the visionaries, they are the ones who come up with the idea of what the customer wants and what the company should build. They can play their part in quality by backing their vision with solid market research on what the customer wants what the competitors are doing and where the gap is in the market and by clearly stating their intent in quantifiable, well-defined stories, write-ups, and clear communication with the engineer and quality teams on what it's being aimed for. It is critical that Development & Quality teams are in sync with a Product Manager's vision!

#### Project Manager
Project Managers are the conduit between management and engineering! It is vital that they are equally adept at Managing Up while managing the team's commitments and release schedule. They can play their part in quality by making sure, the project timelines match with the vision, that roadblocks & and impediments are addressed immediately andThe team is able to demonstrate value to Product management and Leadership by scheduling feature demos or progress pitstops.

#### Software Architect
It is of paramount importance that the architect while discussing with the product manager about the idea/feature, should bring up items like the strengths of the engineering team, the technology stack on which the product/ideas can be implemented, realistic timelines on how long will it take for the implementation, etc. quite often the architect also implements a proof of concept for viability and the as soon as the POC is out the architect should make an effort to socialize the POC with Development and Quality teams. Also, the successful architects, I've worked with back up the POC with we'll define, clearly written technical documentation talking about the macro and micro aspects of the system being built.

#### Software Engineers
They are a vital cog in the quest of "vision to product". Successful suffer engineers in my opinion should make an effort to understand the scope, understand the product's use case, and have a very tight feedback loop with the soft architect and product manager. Only then the design choices and implementation details that are being made during the lifecycle of the product or feature being built will be very high-quality! They could play their part on Quality by adding adequate unit tests for every module developed, keeping their commits focused and targeted towards smaller and frequent changes, defensive programming, and making use of good design patterns, adequate logging, implementing a monitoring and availability system, etc

#### Quality Engineers
The reason I have them listed at the end is they are indeed the last line of defense! A poorly-developed Software product or a bad first experience the hands of a customer would mean a loss of revenue. loss of a potential customer and essentially bad rep for the Product. The quality engineer should look into implementing a holistic approach towards quality. The automation system being built should address all the sub-systems that are present in the product. Quite often than not in modern Software systems, there are a bunch of different backends, a Family of APIs or microservices, the presentation layer or UI. The quality engineer must strive to achieve just automation for all the systems will keep in mind the different aspects that room packed the customer such as functionality, performance, security, etc.The quality engineer must work in a tight feedback loop with all the stakeholders, to ensure adequate quality gates are implemented for all the incoming changes and revisions to the product. The quality is your must Be an advocate for building robust systems with monitoring and availability checks to ensure high customer satisfaction! Him/Her should be always asking the question

> Are we pulling the right product?
> Are we building the product right?

Answers to these two simple questions will result in a list of, areas to focus on, areas to improve, and areas to solidify, all in the quest for landing that perfect product at the hands of the customer!
So… The next time you ask the question who is responsible for the production bug, the answer is YOU!

![It's You](https://images.app.goo.gl/4mVVHgnQNbSKVrji8)

<I'd like to thank [Bruce Hartman](https://github.com/BruceIanHartman) for the idea behind the Uncle Sam pic!>

