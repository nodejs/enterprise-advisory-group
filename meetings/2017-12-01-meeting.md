# Node.js Enterprise Advisory Group

## Attendees

* Trevor Livingston (expedia / homeaway)
* Todd Moore (ibm)
* Sarah Novotny (google cloud platform)
* Dan Shaw (Node.js at Large)
* Monica Ene-Pietrosanu (Intel)
* Chris Castle (Heroku)
* Laurie Voss (npm)
* James Snell (nearForm, TSC)
* Scott Anderson (MasterCard)
* Gaurav Seth (Microsoft)
* Matt Hernandez (Microsoft)
* Ahmad Nassri (TELUS)
* Scott Hammond (Joyent)

## Notes

James: Purpose statement of Advisory Group

Dan: This group might end up inside the end user feedback group, the scope of that group is much broader, this group will be more focused on small but very active large scale deployments of Node.js in the enterprise

Introductions around the table

James: 
Lots of representation on the TSC from individual companies … but decisions by the TSC are guided by limited metrics -- how many NPM modules use this $THING.  (API, feature etc.)

The TSC wants to have this group drive the agenda and offer information back to the TSC to better inform decisions of the future of the platform.

Process:  if this group is to be part of the CommComm, there must be a charter developed and porposed to the CommComm -- AI: DShaw -- charter developemnt

Volunteer needed for agenda and meeting management

DShaw
	
Just starting to set up End User Feedback group.  5-10 hours of work
Wants to hand off this group ASAP - (happy to help at the beginning)

JSnell

Main output from this group would be a statement of core priorities of development in NodeCore.  What are your pain points (or customers).  Think in terms of things that would go into a roadmap for 1-2y.  Use this as part of the input for making decisions in Node Core TSC.  evaluate impact of changes against the Enterprise Advisory lists.

Q Trevor:  Will the TSC bring proposed large changes to this group for input?  
A James: Yes. Liaison between TSC and EAG

DShaw :  roundtable “biggest concerns”  off the cuff

DShaw: node’s relationship with the web platform -- node grew up and came to market relevance with web platform.  Node + frontend are starting to diverge.  Most fissures are healed or healing….  Node is important enough to work as a partner in the broader web platform.

Ahmad: Security (in userland) from the perspective of the platform -- recommended approaches . world of security tooling.  Leadership?  Unified voice from Node.js is missing.

Laurie: npm brings two priorities:
Technical: front end interoperability is paramount.  Node needs to move to JS in the browser more than trying to move browser JS to Node.  ES6 modules in node should work well … the way they work now isn’t good enough.
Cultural: improve the inclusivity of the project and diversity of contributors.  We will lose contributors to projects who are more friendly to non traditional developers.

Trevor:  Availability -- error handling and resilience.  As node has evolved to incorporate promises error handling is a big topic.  Unhandled rejections does not cause a process failure today but may in the future.  There is a need to have request context for when such a unhandled rejection occurs. This has been worked through with unhandled exceptions using domains but we need something similar for promises.  API evolution in general can be a concern because promises are wrapping more APIs and may obfuscate underlying event emitters.  Are we going to lose observability with async/await and promises? For larger enterprise concerns avail/perf/security is bread and butter, but observability is how we accomplish drive these.  No standard logger.  Need a lot of manual instrumentation of code.

Scott Anderson, Mastercard:
Node.js ABI -- a lot of add on in C++.  NAN has been a wonderful thing … as it’s replaced with ABI it must be mature.
ES6 module loader -- feeling pain of that now. Front end devs have to make concessions as they join the node work. 
maturity in async-hooks implementation.  Still experimental, but watching and wanting evolution and maturation.

Scott Hammond, Joyent: popularity of client side JS is causing pressure to have node move toward that.  This is a conflict with node server side needs.   Scale, debuggability, observability.  Work around promises were being advanced but never got adopted … possibly because of a wish to align with client side?  Platform more relevant on server scale out sw.  (diverges from front end JS though.)
https://github.com/nodejs/post-mortem/issues/16
https://github.com/nodejs/node/pull/5020

Monica: performance -- we need to extract performance from apps written in node. Node is enabling any new HW capabilities.   Measuring performance today -- establishing new benchmarks not relative to “real workloads” … joint effort with performance committee.

[nobody can find the unmute button; feedback for UberConference]

Gaurav -- 
Diagnostics  and Tools - both inner and outer loop [how to make devs more productive.  , how do we keep advancing the debugging story, context tracking, promises etc.]
Node.js on Azure - Security, performance, making Node.js *the choice* in modern cloud native paradigms/architecture that developers are adopting as they move to the cloud
Understanding when and how security patches impact our services using Node
[How do we make security problems/vuln.  When will our services be impacted. Performance perspective.  Perf cost analysis on the cloud is different.  How do we make node *the choice* on cloud (and cloud native archi)  continue collaboration with google to push] 
VM diversity and partnership in TC39 - To help platform and language evolution be considerate of the need of both frontend and backend app needs

Matt: diagnostics top of mind.  
 

Todd: large usage perspective.  Diagnostics, security, performance, end users, front end side comes from IBM customers.  Balance…

Sarah: Google interested in project health and sustainability

James: diagnostics/observability extending primitives or add’l tooling.  Top work in next 12 mo from nearform.  


From a core perspective.

Async hooks out of experimental by v10 -- need more feedback from adopters.  More validation.
AI to everyone -- ACTIVE FEEDBACK

API alignment with TC39 -- there was no conversation happening before (now?).  TSC is engaging actively with TC39 to improve this situation… 

AI to everyone -- PRIORITIES and what specifically you’d like to see.

Next steps --  activities to get the group chartered.  Mode of operation for this group?  call/email/prs?

Dshaw -- flip this around.  What are the ways that the TSC would reach out to this group?  I.e. a security issue or breakign change?  Would that go onto an agenda for regular cadence?  

James
monthly/bimonthy email to share outstanding decisions/conversations of interests etc.  also any questions for discussion with this group.   Would like this group to proactively reach out to the TSC askign for current status for important items.

Occasional issues come up which might -- this group should proactively engage with the TSC for things which are impactful.


Comms Email/ Meeting?
James: at least monthly email summary.

Do we need a meeting?

Trevor: regularly scheduled meeting - async method for agenda generation/evaluation.  Save questions and have a real time discussion … emails get fragmented

Laurie: in person/voice more productive.  Crowdsourced an agenda.

Trevor: rotate chairing meetings/agenda generation?

AI: setup next meeting -- january (mid-late) -- VOLUNTEERS for agenda and scheduling?
AI Dshaw: GH repo  
