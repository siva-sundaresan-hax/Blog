# Who's responsible for a Production bug?

Like “Death, Taxes and me never giving up on standup comedy…” discovering bugs in a production system is a reality of Software Development. The critical aspect of finding these bugs is to find them early! That’s why I always preach and practice
> “Test it soon, Test it often, Test via Automation”

Now let's discuss a scenario, QEs are all too familiar with…

*Monitoring sets of alerts, on a critical Production bug in the middle of the night, and it’s impacting your system( one or a combination of functionality, performance, availability etc)!!! Monitoring alerts start getting fired. The team is summoned, a vid bridge is set up, engineers and stakeholders join the vid chat, in their PJs, half-awake, questioning their life choices. 10mins after a debrief, all hands on deck, and the team flex their combined muscles to develop a hotfix and a production deployment. Everybody’s relieved, the customer success team is happy, the team goes back to sleep & the world is a happy place again!*

Except …

*The spotlight falls on the QE working on the project in Scrum tomorrow.*

Few of us have been lucky to work with outstanding teams, where there’s a blameless culture(Rackspace, Cylance & now Secureworks), but the flip side also exists where companies with a good reputation of a great culture also fall prey to looking at the wrong side of Quality…

Picture this...

Post a midnight hotfix ...

The QE walks into work, sleep-deprived, over-caffeinated, emotionally drained from the happenings of last night. The mood is one of relief, where everyone recalls the events of last night. The QE gets a notification on his/her mobile. 5 mins to daily Scrum…

### Why wasn't the Prod issue caught in testing?
![Who?](https://miro.medium.com/max/700/0*PXDYGmE91VMbt214)
A classical question is posted to QEs time and again when a critical bug is found in Production! There might be multiple reasons for this, lack of QE understanding of the scope of feature, inadequate detail in specs/stories, lack of defensive code(logging, memory dereference, etc.) from the development team, the exact scenario that caused the bug is a previously discussed, yet dismissed as an unlikely edge case by the team. So who do you think is responsible for this issue???

> The answer is… does it matter?

Promoting a blameless culture, where postmortems(root cause analysis) happens with the sole intent of improving the Product and avoiding a repeat, is the mark of a highly successful engineering team, IMHO.

The business still wants to know, and the management would like to address the issue constructively. So the answer to the question of,

> Who's responsible for a Production bug? Everyone!


It might not be the answer you’re looking for, but this less glamorous and noncontroversial answer is a key mindset for building highly successful, high-quality software!

> **Quality is a shared mission…**

Getting a little more into detail on the core topic of this blog, I firmly believe, Quality is and should be a shared mission. By that I mean, multiple stakeholders are involved in taking an idea to a customer usable feature/product. And it’s all of their responsibility!

Let’s dive into our key stakeholders.
- Product Manager
- Project Manager
- Software Architect
- Software Engineers
- UX/UI Designers
- Quality Engineers

Intentionally I have QE at the end. QE is the last line of defense! Now, let’s look at how each of the stakeholders should play their part towards Quality, IMHO.

#### Product manager
They are, in my opinion, the first in line when it comes to Quality! They are the visionaries; they are the ones who come up with the idea of what the customer wants and what the company should build. They can play their part in Quality by backing their vision with solid market research on what the customer likes, what the competitors are doing, and where the gap is in the market and by clearly stating their intent in quantifiable, well-defined stories, write-ups, and clear communication with the development and quality engineering teams. Development & Quality teams must be in sync with a Product Manager’s vision!

#### Project Manager
Project Managers are the conduit between management and engineering! They must be equally adept at Managing Up while managing the team’s commitments and release schedule. They can play their part in Quality by ensuring that the project timelines match with the vision and that roadblocks & impediments are addressed right away. The team can demonstrate value to Product management and Leadership by scheduling feature demos progress pitstops.

#### Software Architect
The architect should bring up items like the strengths of the engineering team, the technology stack options, realistic timelines on how long it will take for the implementation, etc., with the Product Manager during the discovery phase. The architect also implements a proof of concept for viability and the as soon as the POC is out ,the architect should make an effort to socialize the POC with Development and Quality teams. Successful architects I’ve worked with back up the POC with well-defined, clearly written technical documentation talking about the macro and micro aspects of the system.

#### Software Engineers
Engineers should make an effort to understand the scope, understand the Product’s use case, and have a very tight feedback loop with the soft architect and product manager. Only then the design choices and implementation details of the Product or feature will be very high-quality! They could play their part on Quality by adding good unit tests for every module developed, keeping their commits focused and targeted towards more minor and frequent changes, defensive programming, and using sound design patterns, adequate logging, implementing a monitoring and availability system, etc.

#### UX/UI Designers
The engineering team developing an idea, is usually focused on creating a functional product. In the quest of producing a robust, well-architected product, usability is left by the wayside! Customers must have a good user experience when they interact with the Product and the UX/UI Designers are a vital cog in this in the freight train creating the Product. A UX/UI designer must develop a good working relationship with the Product owner and must not shy away from pushing back on choices, which might adversely impact User Experience. In addition to this, frequent and brief user surveys/preview sessions must be conducted with beta users, both internal and external to the org, and the feedback from these surveys/sessions must be communicated back to the PO & the engineering team in a structured manner for course corrections.

#### Quality Engineers
Quality Engineers are the last line of defense! A poorly-developed Software product or a bad first experience in the hands of a customer would mean a loss of revenue, loss of a potential customer, and essentially lousy rep for the Product. The quality engineer should look into implementing a holistic approach towards Quality. The test automation system should address all the sub-systems present in the Product. Modern Software systems have many different backends, a Family of APIs or microservices, the presentation layer, or UI. Quality engineers must strive to achieve automation for all these systems and pay close attention to all the different aspects that might impact the customer, such as functionality, performance, security, etc. QE must also establish a tight feedback loop with all the stakeholders to ensure good quality gates for all the incoming changes and revisions. QE must advocate for building robust systems with monitoring and availability checks to ensure high customer satisfaction!

Him/Her should be always asking the question

> Are we pulling the right product?
> Are we building the product right?

Answers to these two simple questions will result in a list of areas to focus on, areas to improve, and places to solidify, all in the quest for landing that perfect Product in the customer’s hands!

So… 

The next time you ask the question who is responsible for the production bug, the answer is **YOU!**

![It's You](https://images.app.goo.gl/1pm1JFastumy2NX68)

<I'd like to thank [Bruce Hartman](https://github.com/BruceIanHartman) for the idea behind the Uncle Sam pic!>

