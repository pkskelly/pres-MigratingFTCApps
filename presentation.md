FTC to CAM
==============
 - Strategies to migrate Full Trust Code to the new App Model



Full Trust Code
===============
- Challenges with multi-tenant code isolation
- Code cannot be run on server
- Cloud App Model requires CSOM or REST


Development Options
===================
- FTC
- Sandbox
- SharePoint Hosted
    - App web
    - Host Web
- Provider Hosted

Branding
=================
- Avoid Custom Master pages
- Prefer Themes if possible
- Use Alternate CSS web property
- Use Remote Provisioning model 


Migration Matrix
=================
| FTC           | App Model     | Office 365  |
| :------------- |:-------------:| :-----:|
| List Template      | Provision by CSOM | N/A|
| Site Template      | Provision by CSOM      |   N/A |
| Custom CSS | Provision by CSOM      |    Provision by CSOM |
| X|X|X|



Still On Premises - What Should I Do?
========================
- Use REST whenever possible
- Use CSOM when needed
- Use REST *EVEN* if you are creating WSP's on premises
- Provision using code vs. declarative files



References
=================
- [Office Developer Center](http://dev.office.com/)
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