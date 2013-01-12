Muni Meeting
============

Muni Meeting is a meeting management tool specifically designed for Municipalities and how they run public meetings.

What problem is being solved?
----
Local government is sexy.

It isn't really, but it could be made much simpler to understand. Most of the work that takes place in local government is done in Select Boards, Town Councils and Sub-Committees like Finance and Public Works. Most people could care less what goes on these meetings until their local property tax bill comes. Most cities and towns live in the stone age when it comes to the processes for their meetings. It's like the Internet never even existed. Word documents scanned as images then turned into PDFs that require OCR are state of the art: http://www.cityofwestfield.org/Files/AgendaCenter/Agendas/68/Archives/57/01-08-13%20Conservation%20PH%20Niemiec.pdf.

At NearbyFYI, http://said.nearbyfyi.com we've been working on a set of tools to collect meeting minutes, agendas and reports from hundreds of cities and towns in Vermont. We have over 150,000 documents now. We're doing the best that we can to extract meaningful, structured data from the blobs of PDFs, Word documents and the most poorly formed HTML you've ever seen. We're finding useful, interesting bits of data in this local legislative soup, Vermont Public Radio with their Public Post tool: http://www.vpr.net/public-post/ is using the information we're finding to write stories that have been picked up by NPR and the Associated Press.

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

If you have gotten this far it's likely that you'd be interested in talking with us about we're dreaming up. I'd love to collaborate with others on this.

> "My Administration is committed to creating an unprecedented level of openness in Government.  We will work together to ensure the public trust and establish a system of transparency, public participation, and collaboration. Openness will strengthen our democracy and promote efficiency and effectiveness in Government." -- BARACK OBAMA http://www.whitehouse.gov/the_press_office/TransparencyandOpenGovernment


App Vision, features and goals
----

Muni Meeting SHOULD allow two deployment modes, single user and multi-tenant. Most of the smaller communities in the United States are not likely to have the ability and resources to setup and maintain their own Muni Meeting instances, but those that can should have the ability.

Access to data within Muni Meeting MUST be accessible via APIs and bulk exporting. A production Muni Meeting instance must not turn public, programmatic access off.

Standalone Muni Meeting instances MUST be discoverable by other Muni Meeting instances.

Muni Meeting takes an opinionated approach to how public local government meetings are run. Each city and town has a unique process but there is significant overlap to them. Muni Meeting is designed to solve 90% of the overlapping concerns, it is not intended to be tailored for each specific workflow.

Muni Meeting is designed for the 30,000 cities and towns in the United States with fewer than 50,000 residents. While it SHOULD and likley will support the facilitation and meeting process of larger cities and towns, it isn't intended to address larger, complicated legislative processes.

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
 
Municipal Meeting Workflow & Process
----
For each Organization Meeting that takes place an Agenda is created, usually by the Scribe (referred to as the Secretary in most cities). The Scribe constructs an Agenda that looks very similar to previous meetings and often they maintain a Template of the Meeting in Microsoft Word so they can copy it and quickly get a new one created. The Scribe enters a number of new Agenda Items into the template to create a *DRAFT* Agenda. Agendas across Municipalities follow a typical structure:

* Call to Order - Bob opened the meeting at 6:32pm.
* Roll Call - Matt: Present, Jason, Present, Chris: Absent
* Pledge of Allegiance
* Ammending of and/or Adoption of prior Minutes - Jason moved to accept the October minutes 
* Executive Session
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
Meetings typically take place in the evening, usually starting between 6:00-7:00pm. A Meeting is *called to order* 
