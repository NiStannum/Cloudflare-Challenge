Introduction

In the gaming industry, there are two major entities - the Publishers who fund the game projects and the Developers, who design and develop the games. A few of the prominent publishers are Activision, EA, Ubisoft who fund the projects from multiple Game Development studios. 


Where can we play?

There are three stages of game development: 1. Pre-Production (Planning, Designing) 2. Implementation (Development, Integration of elements), and 3. Deploy (Testing, Maintenance). In two of these phases, we can utilize Cloudflare Workers; Implementation and Deployment. In the Implementation phase, Developers either use an in-house (eg. CD Project's REDengine) or generic engine (Unity, Unreal, Lumberyard). In conjunction with the engines, some tools are used to create 3D assets and audio elements of the game, but Game Development primarily revolves around game engines. To run these engines, the Development studios need powerful machines that can process millions of game assets and provide lag-free development experience to the Developers. Cloudflare Workers can be utilized to assist this by enabling the engines to execute the code on the nearest nodes, thereby negating the requirement of having on-premise infrastructure. But since the impact of latency is substantially low in engine usage, studios have a lot of flexibility in having on-premise systems and edge-less Cloud computing services. On the other hand, the Deploy phase, can leverage our capabilities. Specifically, deployment and maintenance of Multiplayer experience. There are three reasons for choosing this phase:
1) Multiplayer games provide extended player engagement 
2) They are more profitable 
3) Latency is an important factor for player experience.  
Therefore, our first headway in the gaming industry should be the multiplayer experience. 


What we have

Since Cloudflare Workers utilizes edge computing to provide quick response to the client requests, it is an ideal fit for Multiplayer games servers because:
1) Workers run the request on the closest node, it will greatly reduce in-game lag. 
2) Game servers are volatile and the number of players keeps changing based on factors, like the time of the day, latest releases, initial hype. 

Therefore, a per-request cost model will be a good fit for publishers who have to deal with multiple varying factors and want to provide consistently low latency to every player. Also, the cost estimation will be easier to predict since the client can deduce the cost based on the Request volume. Therefore, we must focus our efforts on developing a Multiplayer Matchmaker and Session-handler feature, wherein the Matchmaker will take care of matching players and team creation according to player levels and the Session-handler will relay input/output from the client to the node. Since with Cloudflare Workers, the node will be closer to the client, it will thereby provide overall low latency for a lag-free gaming experience to the user.


Our Competition

Now before taking any concrete decisions, we need to analyze the competitive landscape. There are two players which can be an issue to our initiatives :
1) Amazon’s Lambda 
2) Microsoft’s Azure Functions. 
Since Microsoft already has its in-house gaming studio and a strong gaming pedigree( Xbox and Halo), we must consider them our biggest competitor. While Amazon should be our second threat, considering they are aggressively pushing their Game studios, the Lumberyard Engine and Lambda FaaS service. Despite their early mover advantage, given in Multiplayer environment users are distributed throughout the world and this is a challenge for them where Cloudflare Workers’s edge computing capabilities can provide Multiplayer experience with low latency even to the distributed users.


Are we winning or losing? 

Finally, to measure success we need to look at a few metrics: 
1.	Is the ratio of users with high latency to users with low latency, less than 0.5? Meaning, are we providing a great experience to at least 66% of our users. 
2.	Are we profitable enough i.e. is the cost per request less than the price per request? If not, can we be profitable at scale in the future? 

As the threat of competition from Amazon and Microsoft is high, we need to maintain consistency in providing the lowest latency service. Apart from that, we can foray into a different segment called Indie Game development, a term used for individual or small developers who develop games independent of any financial support from the publishers since even Indie games require low latency Multiplayer servers at a cheap price. Cloudflare Workers’s Multiplayer Matchmaker/Handler with per-request cost structure can be a great fit for Developers who do not have financial funding to acquire in-house or memory/performance-based computing infrastructure.


