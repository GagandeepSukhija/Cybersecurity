---
ID: "20250711193702"
---
# Overview:
OSINT involves studying the victim by collecting every piece of available information on the company and its employees, such as the company’s size, email addresses, phone numbers from _publicly available_ resources to determine the best target for the attack.

Since the number of free resources grows everyday through social media etc. skilled researchers can find nearly any type of data they’re looking for. OSINT isn’t limited to just public databases however, private databases and other sources can also be used which journalists, spies and ordinary people all use to collect information everyday.

Knowledge of where the right database is located is needed to get the right answers as often simply using search engines isn’t enough. There are multiple tools that can be used by beginners and seasoned investigators to assist them.

# OSINT for Defense:
OSINT is just as important for defense as it is for attack. Performing OSINT on your own company can be incredibly informative as you can see what data is public and what can be inferred about your company. This allows you to spot data that you may not expect to be public and you’ll begin to understand how an attacker could know internal details about your organisation making it easier for them to perform their attack.

# The Importance of Valid Sources:
Using verified primary source data is key. Performing OSINT based on untrustworthy data/sources. It’s important to note that “tertiary” data (data that is collected by a 3rd party - although sometimes they provide useful links to a primary source) cannot be used as evidence.

# Frameworks & Tools:
Since OSINT covers so many types of data, there are many types of investigations that can be conducted. From social media investigations using free tools, geospatial investigations using satellite imagery etc.

There are a lot of different resources for investigators looking for more tools. There are many also on GitHub.

https://osintframework.com/

GitHub Awesome Repo:
https://github.com/jivoi/awesome-osint


# Active vs Passive:
![[VAR_Active-vs-Passive_B.webp]]


# [[HUMINT]]:
OSINT is a super-charger for HUMINT, providing valuable context to investigations allowing you to use a lot more leverage. By taking advantage of company’s employees on social media and leaked internal documents found through passive search techniques, it’s easy to understand who has access to the information an investigator needs. This cuts down the time needed to get answers substantially by getting the answers needed from the right source earlier.


# Email Harvesting:
https://github.com/laramies/theHarvester
https://hunter.io/
# Phone Numbers:
Phonebooks, social media accounts, data leaked by businesses who’ve worked with them. 3rd party aggregators match the number to businesses or people. Once you’ve got a match, you can expand your scope to other web accounts, documents, addresses, names and social media usernames. Matching all of these details to even more information is how a phone number can lead to a business license or more concrete details.


# Names:
Appear in documents related to business filings. Some websites store these like the one below.
https://opencorporates.com/

For normal people, 3rd party aggregators will often attempt to stitch together lots of information about people by name, especially if you have the general area they live in. 3rd party aggregators can’t be used as evidence or provide answers to your investigation, but they often point to better sources of data. Here are some examples:
https://pipl.com/
https://www.beenverified.com/
https://www.peekyou.com/


# Businesses:
Some of the easiest entities to get information on. They need to register lots of paperwork with public entities to exist. The paperwork is often entirely public and searchable which gives you a trove of information full of details that can help to expand an investigation in the early stages.

Searching the secretary of state website of whichever state a particular organisation does business in is a good start. This can be expanded on by searching additional states too. There are tax and legal incentives to register in certain states in the US so it’s usually worthwhile to check the databases in Nevada, Delaware, California and Wyoming too.

Once you have some primary source data, 3rd party aggregators like OpenCorporates gives the ability to search all of the secretary of state databases indexed by the service, which can locate valuable primary source information you may have missed. lilsis.org is also good since it provides information about business people which includes stock options and tax information.

![[VAR_Timeline.webp]]

# Websites:
Websites can be used for their technical information, like who registered it, what servers are in use and what software is maintaining it. Services like Shodan allow you to profile an organisation’s technical infrastructure without scanning it yourself.

The contents of the site itself can include files unintentionally left public or information that’s been removed from the website.  Tools like Internet Archive can be used for this. It can also be used to see organisational changes like showing who’s left/joined the company and when.

Google Dorking is also powerful to find files and other details left open to the internet by accident. By structuring queries you can look for certain types of web-pages and files so it’s easy to find any parts of a target’s website that might be leaking confidential information.


# Dangers of Conducting OSINT:
There are always risks when doing any sort of investigation that either makes direct contact with the subject or a 3rd party who may sell your search to the 3rd party directly. For example, you may forget to sign out of your LinkedIn and when searching for someone they may use the information that you looked at their profile as part of their product. This could blow an investigation. 

The same goes for if you access a web resource that belongs to a target from your organisation’s IP address. This is especially true if your organisation doesn’t want to be identified while investigating a target. Always use a VPN or you risk making your attention to any part of the target’s infrastructure obvious.


# Regulation Compliant OSINT:
There are many loopholes in the CCPA so OSINT generally aren’t something that California residents need to worry about, however, GDPR is a lot more strict. This means that you need to make sure you don’t expose personal information of a subject and that you store it appropriately.


# Examples of OSINT Investigations:
Bellingcat - exposing Russian government denials. A lot of OSINT covers topics like war crimes in areas too remote to access and was used extensively for the downed MH17 flight.


# Who Makes Use of OSINT Reports:
It’s a critical part of both public and private intelligence, arming businesses, governments and individual investigators with a vast amount of high quality information to base and make decisions on. OSINT allows anyone to have access to some of the best data in the world.

# Further Resources:
Mike Bazell. Twitter & GitHub are full of new OSINT tools.