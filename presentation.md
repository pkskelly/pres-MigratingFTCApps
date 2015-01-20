FTC to CAM
==============
 - Transitioning Full Trust Code to the New App Model





Full Trust Code
===============
- Challenges with multi-tenant code isolation
- Code cannot be run on server
- Cloud App Model requires CSOM or REST



Why not FTC or Sandbox Solutions?
=================================
- DRP challenges with ghosted files 
- Upstime requirements (cannot have downtime)
- Cannot inherently "trust" code in hosted service 


Development Options
===================
- FTC
- Sandbox (deprecated)
- App Model 


Sandbox Solutions 
=================
- Code-behind deprecation
- Lack of central control
- Potential orphan issues (with deactivation)
- Requires deep tribal knowledge (xml, features, etc.)



Transition Mindset
===================
- Not a 1 to 1 mapping of technology
- Focus on the functionality
- User's care about the funcitonality



Transition Recommendations
==========================
- Move gradually 
- Align with the product and service roadmap
- Concentrate on end users
- Avoid Sandbox Solutions 



Transition Approach
====================
- Readiness : understanding the App Model and Hosting
- Assessment : anaylze requirements and existing solutions
- Planning : planning based on business and functional requirements 
- Develop and Test: technical planning and development
- Deployment : deployment and management of apps



Consider Impact of Customizations
========================
- maintanance and operational costs
- Agility to deploy updates
- Long term roadmap impact



Redefining SharePoint Applications - Client Side
===================================
- JavaScript controls on master page and layouts 
- Remote provisioning
- Embrace the unghosted model
- API based deployment



Redefining SharePoint Applications - Server Side
===================================
- Embrace provider hosted applications
- App catalog solutions
- Package reusable solutions
- API based deployment 



FTC - Site Columns, Content Types
=================================
- Deploy using code
- Using  remote feature receivers
- Objects are created unghosted (in the db)
- CTypes have no dependency on feature files



FTC - List Templates
====================
- Avoid custom list templates   
- Custom list template unique id in schema.xml
- List instances have dependency on the schema.xml
- Depoly using code



Branding
=================
- Avoid Custom Master pages
- Prefer Themes if possible (Suite level themeing)
- Consider using Alternate CSS web property
- Use Remote Provisioning model
- Ensure you are willing to pay the "branding tax"


Site Provisioning
=================
- DO NOT use site or web templates
- Use "remote provisioing" pattern (CSOM)
- Deploye artifcats WITHOUT Features
- Update using "Remote Management" pattern
- Separate code from content 



Site Provisioing Models
=======================
- Feature Stapling
- Custom Site Definitions
- WebTemplates
- Server Side Solutions



Feature Stapling (bad)
======================
- Cannot be used to bring new template options
- Only available in O365 at site collection scope in Sandbox Solutions (to every site coll)



Custom Site Definitons (bad)
============================
- impacts major version upgrades
- not supported in O365
- Farm level deployments



WebTemplate
===========
	- maintenacnce challenges due to replacement of oob site defintiion
	- Supported in site collection in O365
	- Maintenace management nightmare - onet.xml HELL

Full Server side code
======================
- time jobs, site provisioing provider, and more
- not supported in O365
- maintenance and update complexitities


Provisioning Matrix
===================
|  |Site Defintion | Site Template | WebTemplate | Server Side | Remote |
|Options||||||
|Cloud Support| No | Yes | Yes | No | Yes |
|Rating| Good | Fair | Average  | Good | Excellent |
| Cost Impact | $$$ | $$ | $$ | $ | $$ |



Async Provisioning Model
========================
- Using PHA and CSOM
- "queued" to SP List or table or other
- Possible Workflow or business processing
- Remote Timer Job (Web Job) to provision
- Notification
- PowerShell, C#, PHP, Python, etc. 


Provisioning Diagram
====================
- See MVA Module 3 @ 27:05...

DEMO 1
=====
- Provisoiing Clud Async
- PnP Solutions from GitHub


- QUES for VESA - how do you override the subsite creation... 

DEMO 2
==========
- SubSite Provisioning App 


Hybrid Provisioning Patterns
============================
- Provisioin to cloud and on prem per bus requirements
- helps with reducing IT cost by using Cloud is bus requirements are viable
	- no need for dta privacy
	- external sharing
	- ...?


Updating Site COllecitons (post - provisioing)
==============================================
- provision new assets (css, images, javascript, etc.)
- loop through sites and update as needed
- QUES : Is it a best practice to have "sentinal properties" as the web properties bag?






Migration Matrix
=================
| FTC           | App Model     | Office 365  |
| :------------- |:-------------:| :-----:|
| List Template      | Provision by CSOM | N/A|
| Site Template      | Provision by CSOM      |   N/A |
| Custom CSS | Provision by CSOM      |    Provision by CSOM |
| X|X|X|



But We're Still On Premises
========================
- Use REST whenever possible
- Use CSOM when needed
- Use REST *EVEN* if you are creating WSP's on premises
- Provision using code vs. declarative files



Benefits 
==========
- Quicker rampe time for new resources (no tribal knowledge)
- More consistent and quality SDLC (testing, deployment, upgrades)
- Opportunity to "pay off technical debt"
- Facilities decoupled updates for platform and apps 
	- reduces IT cost and increases busines ROI
- If you know web developmnet, you know SharePoint Development!


Key Points
==========
- Focus on functionality, NOT technology
- Focus on the business objective to be achieved
- Apps for Office 365 AND on premises! 
- RE-evaluate requirements and use new approaches
- NO MORE FEATURE FRAMEWORK - use PnP Core Code for provisioning



References
=================
- [Office Developer Center](http://dev.office.com/)
- [API Sandbox]()
- [Office 365 Developer GitHub](https://github.com/OfficeDev/PnP)
- [Office 365 Developer PnP Home GitHub](https://github.com/OfficeDev/PnP)
- [FTC to CAM] (http://blogs.msdn.com/b/vesku/archive/2013/11/06/ftc-to-cam-stop-creating-content-types-and-site-columns-declaratively.aspx)



Speaker Bio
==============
Pete Skelly is the Director of Technology and Principal Consultant at [ThreeWill](http://www.threewill.com/).
Pete has been in the industry for more than 20 years but has focused on SharePoint and Office
Solutions for the last 9 years.

Pete has over 20 years of experience in SMB and Enterprise application support, custom development, architecture design and project management.
Pete was a Principal Consultant at ThreeWill with responsibilities ranging from solution design and development to account and project management across Financial Services, Healthcare, Insurance and Communications industries.
Prior to ThreeWill, Pete worked for HP where he was a Technical Lead and Architect designing and developing world wide applications for service provisioning and help desk automation.

Pete holds a BA in Philosophy from the University of Hartford. Pete enjoys spending time with his wife and two sons, and the occasional round of golf.