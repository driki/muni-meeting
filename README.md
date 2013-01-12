Muni Meeting
============

Muni Meeting is a meeting management tool specifically designed for Municipalities and how they run public meetings.

What problem is being solved?
----
Local government is too sexy. It gets people excited. We can't get enough of it.

OK, it isn't really any of those things, but it could be made much simpler to understand and follow. Most of the work that takes place in local government is done in Select Boards, Town Councils, School Boards and Sub-Committees like Finance and Transportation. Most people could care less what goes on these meetings until their local property tax bill comes. Most cities and towns live in the stone age when it comes to the processes for running their meetings. **It's like the Internet never even existed**. On the left is a Word document created, saved, printed, scanned as an image and then turned into a PDF to be posted online. This is very common in our cities and towns and it has to stop. Having good, quality, structured data about the policies, ordienances and legislation is important as many state and federal laws have their roots in local legislation.

<img width="50%" src="https://www.evernote.com/shard/s131/sh/fe59993b-dfc5-40c8-b8f3-f5d9970b5ec2/8e6a6e631f38dc83e36685120cdd1f4e/res/bc410902-43ba-4815-ae7a-076716934f19/skitch.png"/>
<img width="50%" src="https://www.evernote.com/shard/s131/sh/1471e6d2-662e-493b-887a-00ecffde5adc/82939d95f33bb567a545aa4b5857c52f/res/f0731d63-6f5f-4096-bb2e-b2b57d61d4e3/skitch.png"/>

At NearbyFYI, http://said.nearbyfyi.com we've been working on a set of tools to collect meeting minutes, agendas and reports from hundreds of cities and towns in Vermont. We have over 150,000 documents now. We're doing the best that we can to extract meaningful, structured data from the blobs of PDFs, Word documents and the most poorly formatted HTML you've ever seen. We're finding useful, interesting bits of data in this local legislative soup, Vermont Public Radio with their Public Post tool: http://www.vpr.net/public-post/ is using the information we're finding to write stories that have been picked up by NPR and the Associated Press.

We're never going to win the battle though. The upstream source is so polluted. We need to clean things up. Muni Meeting is an online tool specifically designed for Municipalities and how they run meetings.

Muni Meeting benefits for cities and towns:
----
* Reduce meeting taker and organizer time
* Real time publishing of notes - zero publish time
* eDelivery of Meeting Packets (Police Officers usually hand these out manually)
* No need to convert Word docs and flatbed scanner documents to PDF
* View voting histories, profiles
* Record meeting audio via iPhone and Android apps
* Meeting topic trends
* Searchable meetings
* Low-cost or FREE tool
* Open source, open APIs for data
* Useful, structured data and information for analysis

There is a closed source, commercial vendor in this space called Granicus: http://www.granicus.com/Solutions/Granicus-Open-Platform.aspx. They build decent tools, they have an API (limited non-public access) but they create an expensive, closed and complicated tool. It is a tool designed for larger cities and towns. Towns with closed circuit camera systems and $40,000,000+ budgets. Most towns in the United States have fewer than 50,000 residents. These are the towns where a Selectboard meeting might take place in a library or in a kitchen of a member. These smaller towns pass important laws and ordinances that are rarely noticed in our busy lives. **Democracy is happening in public view, but we just don't see it**.

If you have gotten this far it's likely that you'd be interested in talking with us about we're hoping to do. We'd love to collaborate with others on this.

> "My Administration is committed to creating an unprecedented level of openness in Government.  We will work together to ensure the public trust and establish a system of transparency, public participation, and collaboration. Openness will strengthen our democracy and promote efficiency and effectiveness in Government." -- BARACK OBAMA http://www.whitehouse.gov/the_press_office/TransparencyandOpenGovernment


App Vision, features and goals
----

Muni Meeting SHOULD allow two deployment modes, single user and multi-tenant. Most of the smaller communities in the United States are not likely to have the ability and resources to setup and maintain their own Muni Meeting instances, but those that can should have the ability.

Access to data within Muni Meeting MUST be accessible via APIs and bulk exporting. A production Muni Meeting instance must not turn public, programmatic access off.

Standalone Muni Meeting instances MUST be discoverable by other Muni Meeting instances.

Muni Meeting takes an opinionated approach to how public local government meetings are run. Each city and town has a unique process but there is significant overlap to them. Muni Meeting is designed to solve 90% of the overlapping concerns, it is not intended to be tailored for each specific workflow.

Muni Meeting is designed for the 30,000 cities and towns in the United States with fewer than 50,000 residents. While it SHOULD and likley will support the facilitation and meeting process of larger cities and towns, it isn't intended to address larger, complicated legislative processes.

Meetings can often take place in low/no network connectivity locations, especially in more rural towns without public WiFi. The Muni Meeting tools should take this into account and when possible use local storage so they can be used without network connectivity.

Ideally an API specification and data exchange format for for Open Meetings develops similiar to what Open311 has done for call center related activities.

Proposed Models & Roles
----
* **Municipalities** like Watertown, MA or Cambridge, MA have many **Organizations**
* **Organizations** like Town Council, School Board, or the Finance Committee have many **Members**
* A **Member** can belong to many **Organizations**, like Matt is the Chair of the Finance Committee and the Vice-Chair of the Transportation Committee
* A **Guest** is someone who attends a **Meeting** but isn't a **Member** of the **Organization** running the **Meeting**
* Each **Municipality** has a list of **Administrators** that can *create*, *edit* and *manage* **Organizations**, **Meetings** & **People**
* Members, Guests and Administrators are all required to have First & Last Names
* Members & Admistrators must have contact information including email, phone and street address
* Guests should have an address and optionaly contact information
* Organizations have many meetings
* Organizations have Regular Meetings on a defined schedule
* Each Meeting often has an Information Packet that needs to be delivered to Members
* A Meeting follows a Meeting Template or Meeting Script
* Each Organization might have a different Meeting Template
* Each Meeting has many Agenda Items
* Each Agenda Item can have many Attachments like PDFs, Word docs, etc.
* Each Meeting has a Scribe often referred to as a Secretary, Note Taker or Minute Taker
* **Motions** are made on some Agenda Items and the Votes of Members are recorded
* Each Meeting has **Minutes** which are recorded by the Scribe and are often required to be posted publicly
 
Municipal Meeting Workflow & Process
----
For each Organization Meeting that takes place an Agenda is created, usually by the Scribe (referred to as the Secretary in most cities). The Scribe constructs an Agenda that looks very similar to previous meetings and often they maintain a Template of the Meeting in Microsoft Word so they can copy it and quickly get a new one created. The Scribe enters a number of new Agenda Items into the template to create a *DRAFT* Agenda. Agendas across Municipalities follow a typical structure:

* Call to Order - Bob opened the meeting at 6:32pm.
* Roll Call - Matt: Present, Jason, Present, Chris: Absent
* Executive Session
* Pledge of Allegiance
* Ammending of and/or Adoption of prior Minutes - Jason moved to accept the October minutes 
* Public Comments/Forum - An opportunity for those in attendance to speak about non-Agenda Items
* Agenda Items unique to this Meeting - Motions can be made and Votes are tallied
* Public Comments/Forum - An opportunity for those in attendance to speak about non-Agenda Items
* Closing Remarks
* Meeting Adjouns

The Scribe is responsible for Organizing the Meeting, posting Public Notices to Newspapers, websites and other Media outlets. When the Agenda has been set and supporting documents are ready the Scribe will send out the Meeting Packet to Members of the Organization responsible for the Meeting. Often this is only done for Selectboard and Town Council Meetings as the smaller sub-committees don't have the resources to prepare for Meetings like this. Typically the Scribe hands the Meeting Packet to a Police Officer who then will physically drive to Members homes and hand deliver the Meeting Packet.

Organization Members are responsible for reading and preparing for the coming Meeting, though often many Town Councilors or Selectboard members will often show up to a Meeting ill-prepared and not having had time to read the materials until just moments before the Meeting. There are Town Counciors that fight e-Delivery of Meeting Packets and request that manual, paper deliver still takes place.

Municipal Government will likely take considerable time to transition to digital only workflows so any Muni Meeting documents MUST provide downloadable, printable formats.

The Actual Meeting
----
Meetings typically take place in the evening, usually starting between 6:00-7:00pm. A Meeting is officially *called to order* by the Chair-Person for the Meeting and the official start time is recorded for the record. *Roll Call* is usually initialed by the Scribe and is when Members declare their attendance to the Meeting. A verbal record of *Present* or *Absent* is recorded by the Scribe. A Scribe typically takes notes either with paper and pencil or with a computer using Microsoft Word. In communities of 30,000+ there is often a cable access feed provided of the larger meetings. Smaller towns and sub-commmittee meetings typically have no audio or video recording available.

Typically a Meeting is *called to order* & *roll call* taken only to have the Meeting move into Executive Session, where the contents of the meetings are private within the constraints of a states Open Meeting Laws. After returning from Executive Session (typically 15-60 minutes) the meeting beings in front of the Public. The *Pledge of Allegiance* is often performed. 

Their is usually an Agenda Item to *review prior minutes* which often results in no amendments. There are times when Amendments are requested by Members and the Scribe is responsible for noting them and *adjusting prior minutes* at a later date.

During the Meeting the Scribe takes notes for each Agenda Item which are later posted as Meeting Minutes. Typically there is a presentation of each Agenda Item, either by a Member or Guest who has been either *requested to speak* or who has requested to speak. Agena Items are typically set 3 days in advance of a Meeting so that proper public notice can be provided for those that wish to attend.

Usually the first Agenda Item after the Pledge of Allegiance has been performed is a Public Comment or Forum period. Each Guest in the audience is given the opportunity to speak about any topic for a maximum time period. Typically the time alloted is between 3-5 minutes. Most Municipalities require that a Guest speaking during Public Forum state their name and street address. This is usually recorded by the Scribe but there are often typos and missed information because of challenges hearing new names and street addresses.

Often a Scribe will refer to Members and Regular Guests by their initials when taking notes. For example, Matt MacDonald would often be referenced as (MM) throughout the document.

After a presentation of an Agenda Item from a Guest, the Chair of the Meeting will typically *open the floor for discussion* among fellow Members. Members are given the opportunity to *comment* and ask questions of the Guest presenting. After discussion, the Chair asks if there are any *motions on this item* to be made. A Member of the Organization *makes a motion* and waits for it to be *seconded* by another Member. After *the motion is seconded* a *vote takes place*. If the motion fails to seconded no vote takes place. When voting, the Scribe verbally calls out to each Member of the Organization and asks for their vote of Yay, Nay or Abstain. The Scribe records the vote for each Member and the Chair of the Meeting announces if the *motion passes* or the *motion fails*.

This process is repeated until there are no more Agenda Items, the next public Meeting is announced and the *meeting is adjounded* with the official time recorded. 

The Scribe will often sign or write their name.

Post Meeting Process
----
Meetings are typically created in Microsoft tools like Word or written by hand on paper. Attachemnts for supporting materials are typically PDFs, PowerPoint or Excel documents. The Scribe is often responsible for converting their Microsoft Word document into a PDF that then needs to be posted to the web. Often the Scribe doesn't have the technical access or ability to post to the municipal website. More meeting minutes, agendas and documents are being posted to the web as HTML documents, while the text is easier to access the raw meeting text is usually inaccessable as the templated, wrapper navigation and links are hard to separate from the minute text.

Often, larger cities using a CMS are able to have index pages dynamically created, but often the index of prior meetings are managed by hand in long, large documents that are error prone.

Meeting Minutes are in a **DRAFT** state until they are approved by the Members at the following Meeting.

Other Challenges for Municipalities
----
* Most Meeting Minutes are not searchable, few cities or towns have useful search systems that index the content within  the PDFs and Word documents currently published.
* Most Municipalities have now database of votes from Town Councilors and Selectboard members. Citizens are unable to track how their local elected officials have voted. There is no record.
* Providing Meeting Packets is a manual process and there are time savings to be had.
* Each Scribe takes minutes in differing formats, using different date formats and templates.
* No web accessible historical record. Often cities bury this information in dark corners of the web.

