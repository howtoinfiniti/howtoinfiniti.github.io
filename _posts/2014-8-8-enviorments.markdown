---
layout: default
title:  "Enviorments"
---

There are several environments that ensure that every deployment artifact can be tested and verified by different parties. Figure Environments and actors. shows an overview of the environments. Note that the flow is always from dev to qa, from qa to staging and from staging to production.

<span class="bg bg-danger">Important:</span> Always adhere to this order of deployment. <span class="bg bg-danger">Never</span> skip environments unless you have really good reasons. Otherwise you risk introducing changes that will make debugging and deployments very complicated.

The enviorments that a content entry person normally would use are:

- <span class="bg bg-int" >INT :</span>
	- This is where all developers test their code after commits from all parties have been merged. On this environment developers decide whether a release candidate is ready for QA.
- <span class="bg bg-info" >QA :</span>
	- Here the first round of testing and verification is performed. Only builds that developers consider done done should be deployed to this environment.
- <span class="bg bg-staging" >STAGING :</span>
	- This is the last step before deploying content to production. Staging is the environment closest to the actual production environment.
- <span class="bg bg-prod" >PRODUCTION :</span>
	- This is the live page of Infiniti, when the project reaches this point is more likely to be done, production author is the one you have to be more careful with, anything you activate here will go live.



<img src="/images/infiniti-global-environments.png" alt="User properties" class="img-responsive centered">

<h2 class="page-subtitle"><small>1.</small> Enviorment setup</h2>

Initially all enviorments has the same color palette, this will make them hard to distinguish and in the long run it could cause serious trouble. Fortunately you can change their presets colors, QA will be in their preset blue, Int now will become a blue-ish gray, Staging will be completly gray and Production purple. 

<strong>How to change the preset palette:</strong>

<h4>1. Go to the enviorment you want to change and click <strong>"User properties"</strong>:</h4>

<img src="/images/user_properties.png" alt="user properties" class="img-responsive" />

<h4>2. Select the <strong>"User interface"</strong> tab and choose the correspondant color scheme:</h4>

<img src="/images/user_interface.png" alt="user interface" class="img-responsive" />

<h2 class="page-subtitle"><small>2.</small> Which enviorment should I use?</h2>

Usually the Project manager provide this kind of information, nevertheless is common to omit this <strong>very important</strong> detail, the easiest way to know where you should adress a project is <span class="bg bg-success">asking to the person that assigned it to you</span>.

This might sound obvious but sometimes the project sounds like is an update made in Production, but actually is intented for QA, and being Prod such a <span class="bg bg-warning" >delicated place to work</span>, <strong>always ask</strong>, keep in mind: <span class="bg bg-danger">Assuming is always a risk</span>.

<h2 class="page-subtitle"><small>3.</small> About Production</h2>

This segment can be synthesized in the following sentence: <span class="bg bg-danger">Never activate nodes in Prod <strong>unless</strong> the project is completly done and ready to be live</span>. But lets explain why.

When a node is activated it means that is ready to be published or is published already, the importance of this lays in that if for example lets imagine the following: A developer is working on a brand new slider for the homepage, and a content entry person is setting up the vehicle data for an upcoming model, you as the hypotetical content entry person finishes first than he does and activate your nodes, however you made some mistakes in the ticket assigned, so is currently on QA. Meanwhile the dev finishes the slideshow and everything looks good, so he activate the nodes and clear the Akamai server that lets the content storaged in Prod to go live.

This process of activation will update everychange made in activated nodes, incluying yours. That means that the mistakes you made also will be pushed to live.

Of course anybody wants that, so hold up your activations until the proper time.

<h5>Cases when you can activate the nodes:</h5>

- If QA reviewed the project on <strong>Author</strong> and it's ok to put everything live.
- If you have been asked to push over your work on <strong>Origin</strong>, Origin will have every change made on prod that is activated even if Akamai hasn't been cleared, so it serves as a final QA, be sure to only activate the nodes and <span class="bg bg-danger">wait for direction for the Akamai</span>.


	
