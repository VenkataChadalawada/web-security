# web-security

### Security - protection of Assets
- Tangible Assets
- Intabngible Assets

#### Tangible Assets
- Physical assets valuables such as jewelry , art , collections
- confidential data such as - passwords, cc numbers, bank account transactions etc..

#### InTangible Assets
- Reputation, Trust, Good Will etc.. as a person or company

We will focus on confidential data

- we trust more and more of our personal information to websites.
- this makes things in our life very convenient but much more vulnerable.
- Hacking attacks and security breaches make headlines everyday
- They range from serious, large scale attacks
- eg:- in Dec 2015 taget anounced that 40 million debit & credit cards used in stores across the US
these nums were then available for sale in shady stores selling cards.
- eg:- A message from the CEO to someone in the org asking for money to be transfered
(social engginering)
- eg:- Ashley Madison - many prominent public personalities have been outed as a result of this breach


### Security Building Blocks
- Authentication = Ensure who loged in
- Authorization = what can you do
- Auditing = what they did
- Confidentiality = is their data safe
- Integrity = can their data be changed
- Availability = sys available for legit users

#### Authentication - who are you?
- This is used to uniquely identify the clients of your system - whether they are human or other services
- deals with IDENTITY - when you login into a website, it knows who you are

#### Authorization - what can you do?
- For an already authenticated client- what resoucres can she access?
- what actions can she perform?
- can she edit this database?
- can she transform money from one account to other

#### Auditing - Did the user actually do that?
- Auditing & logging is needed for non- repudiation - where a customer or a service cannot deny performing some action
- Did the user really pay for his book?
- Did the user request 2 units of a mobile phone?

#### Confidentiality - Is the data safe?
- This refers to keeping data private such that unauthorized users cannot read or access it- whether this data is stored somewhere or in transit?
- Data is kept private using encryption or access control lists (ACLs)

#### Integrity - can the data be modified?
- this refers to whether data srored or in transit is safe from unauthorized changes wither unintential or malicious
- Integrity for stored data is via permissions, integrity for data in transity is achiweved via hashing and message authentication codes

#### Availability - Does the system work for legitimate users?
- Denying access to real users by overwhelming the system with requests or crashing the system is a security risk
- Denial of service attacks are usually legitimate requests but in such volume that the system cannot handle it


Security issues can undermine any of these basic foundations

### Security related definitions
#### Risk, threat, vulnerability and attack
- Risk = is the likelihood of being attacked and of the attack being successful - this refres to a system's exposure
- Threat = A threat is an occurrence which can harm your system, this can be malacious or unintentional
- vulnerable = A weakness is the system which makes a threat possible - poor design, mistakes, insecure coding techniques
- Attack = An attack is an action which entacts a threat to exploit a vulnerability

#### what causes security vulnerabilities?
- Poorly written code = many developers, lot of room
- The szie and complexity of your application
- Web servers are inherently complex and have their own weaknesses
- Database servers and other systems the site integrates with have their own issues
- Sites have increasing complex interactions with users, with special permissions
- Code in your site comes from different programmers, coded at different times with different approaches

The surface area of a site that can be hacked only grows over the time if its unchecked!

### Known and Unknown Vulnerabilities
- Not all hackers are highly skilled
- A few hackers have the skills and perhaps the luck to find new vulnerabilities to exploit
- This takes intense time, effort and possibly the coordinated effort of a team
- These are unknown
- The vast majority of attacks are of Known vulnerabilities
- These becomes famous once they are applied - and thousands of copycat hackers try to use this across other sites
- Your site is the most at risk from known exploits!
- so what do you secure?
- All of [Network -> Host -> Applictaion] 
- We will just mostly focus on application level security - the secure practices you follow when you write code in your website or application






