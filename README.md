# CMS Security Track Record (2010 & 2011)


**After making a (probably unwarranted) [remark on TYPO3's security](https://twitter.com/#!/xeraa/status/158250289005207553) on Twitter and further mentioning the high number of security flaws, [Søren Malling](https://twitter.com/sorenmalling) challenged me to it: "["All" those issues are dated since 2005..  Do some comparising and you will find its nothing!](https://twitter.com/#!/sorenmalling/status/158325493224062976)" I quickly googled the topic and only found a [comparison from 2008 and 2009](http://secure.t3sec.info/comparison/), so I decided to give it a go and do a little comparison myself.**


## The Contenders
I will include the following projects:

* [WordPress](https://wordpress.org)
* [Drupal](https://drupal.org)
* [TYPO3](https://typo3.org)
* [Joomla](http://joomla.org)
* [MODX](http://modx.com) (as requested)
* [ExpressionEngine](http://expressionengine.com) (as requested)
* [SilverStripe](href="http://www.silverstripe.org) -- I might be [a little biased here](https://www.amazon.com/SilverStripe-Module-Extension-Themes-Widgets/dp/184951500X), but I will try to keep it as fair as possible

Why is X not included? Ask nicely or even provide some research and I might include it. And of course any corrections or feedback are highly appreciated in the form of [tweets](https://twitter.com/xeraa), [pull requests](https://github.com/xeraa/cms-security/pulls), or [tickets](https://github.com/xeraa/cms-security/issues) :-).


## Are They Even Comparable?
Good question! Probably, you cannot compare TYPO3 to Wordpress for example -- both in terms of features, lines of code, age of codebase,... To get a better "feeling" for the projects, I will run the latest stable version of each project through [CLOC](https://cloc.sourceforge.net). That still does not make it a "fair" comparison (if there is such a thing), but we are at least getting a better picture of the differences.

###WordPress 3.3.1
[http://wordpress.org/wordpress-3.3.1.tar.gz](http://wordpress.org/wordpress-3.3.1.tar.gz)

	686 text files.
	683 unique files.
	 14 files ignored.

	http://cloc.sourceforge.net v 1.53  T=7.0 s (95.7 files/s, 33912.6 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                            374          23240          46242         105546
	Javascript                     214           4947           3090          24773
	CSS                             65           3925           1307          21983
	HTML                            16            261              5           2025
	XML                              1              7              0             37
	-------------------------------------------------------------------------------
	SUM:                           670          32380          50644         154364
	-------------------------------------------------------------------------------

### Drupal 7.10
[http://ftp.drupal.org/files/projects/drupal-7.10.tar.gz](http://ftp.drupal.org/files/projects/drupal-7.10.tar.gz)

	890 text files.
	868 unique files.
	546 files ignored.

	http://cloc.sourceforge.net v 1.53  T=3.0 s (113.7 files/s, 24118.3 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                            109           1446          12301          36624
	CSS                            120            801            993           9191
	Javascript                      85            836           2793           5174
	Bourne Shell                    10            208              0           1427
	XML                             12              3              0            441
	HTML                             3              4              0             69
	ASP.Net                          1              3              0             40
	SQL                              1              0              0              1
	-------------------------------------------------------------------------------
	SUM:                           341           3301          16087          52967
	-------------------------------------------------------------------------------

### TYPO3 4.6.3
[http://prdownloads.sourceforge.net/typo3/blankpackage-4.6.3.tar.gz?download](http://prdownloads.sourceforge.net/typo3/blankpackage-4.6.3.tar.gz?download) -- I went with the "Blank Package" as it is probably the one most similar to the other releases

	3452 text files.
	3370 unique files.
	 515 files ignored.

	http://cloc.sourceforge.net v 1.53  T=29.0 s (100.0 files/s, 25068.4 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                           2095          53795         171948         262465
	Javascript                     374          22150          31322         123836
	CSS                            253           7587           1773          32993
	XML                             11            758              2           9178
	HTML                           127            699            898           4719
	SQL                             29            136             39           1559
	XSLT                             6            176             46            800
	DTD                              2              0              0             82
	Bourne Shell                     2              4              0             20
	-------------------------------------------------------------------------------
	SUM:                          2899          85305         206028         435652
	-------------------------------------------------------------------------------

### Joomla 1.7.3
[http://joomlacode.org/gf/download/frsrelease/16024/69674/Joomla_1.7.3-Stable-Full_Package.zip](http://joomlacode.org/gf/download/frsrelease/16024/69674/Joomla_1.7.3-Stable-Full_Package.zip)

	3383 text files.
	2374 unique files.
	 326 files ignored.

	http://cloc.sourceforge.net v 1.53  T=11.0 s (186.7 files/s, 33048.3 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                           1294          25551          68223         124153
	Javascript                     190          12463           8136          50342
	CSS                            143           7400           3282          29361
	XML                            289           2035            174          21636
	HTML                           107            489             20           6905
	SQL                             31            445            148           2768
	-------------------------------------------------------------------------------
	SUM:                          2054          48383          79983         235165
	-------------------------------------------------------------------------------

### MODX 2.2.0-pl2
[http://modx.com/download/downloading/?id=4f04c7baf2455425fb0000e1](http://modx.com/download/downloading/?id=4f04c7baf2455425fb0000e1) -- the "Traditional" package, which should be most similar to the other releases.

	3100 text files.
	3063 unique files.
	 684 files ignored.

	http://cloc.sourceforge.net v 1.53  T=9.0 s (267.0 files/s, 38849.8 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                           2079          23289          65373         171347
	Javascript                     211           3741           5387          46655
	CSS                             95           4983           1020          23957
	XML                             12            436            285           2705
	Java                             1             47             62            182
	SQL                              4             20             37            120
	HTML                             1              0              0              2
	-------------------------------------------------------------------------------
	SUM:                          2403          32516          72164         244968
	-------------------------------------------------------------------------------

### ExpressionEngine 2.3.1
Code kindly provided by [http://www.cmscritic.com](http://www.cmscritic.com).

	1043 text files.
	 939 unique files.                                          
	  40 files ignored.
	
	http://cloc.sourceforge.net v 1.53  T=7.0 s (129.4 files/s, 42751.4 lines/s)
	-------------------------------------------------------------------------------
	Language                     files          blank        comment           code
	-------------------------------------------------------------------------------
	PHP                            720          43920          51284         185995
	CSS                             20           2232            955          10492
	Javascript                     148            272           1211           1732
	HTML                            18            258            121            788
	-------------------------------------------------------------------------------
	SUM:                           906          46682          53571         199007
	-------------------------------------------------------------------------------

### SilverStripe 2.4.6
[http://www.silverstripe.org/assets/downloads/SilverStripe-v2.4.6.tar.gz](http://www.silverstripe.org/assets/downloads/SilverStripe-v2.4.6.tar.gz)

	2980 text files.
	2956 unique files.
	 161 files ignored.

	http://cloc.sourceforge.net v 1.53  T=15.0 s (186.9 files/s, 39189.2 lines/s)
	--------------------------------------------------------------------------------
	Language                      files          blank        comment           code
	--------------------------------------------------------------------------------
	XML                             452             69              0         203345
	Javascript                     1421          22089          11405         147416
	PHP                             669          19896          44052         117294
	CSS                             129           1443            745          10517
	HTML                             49            676             53           6201
	YAML                             71            102             36           2003
	Ruby                              6             44             28            170
	ASP.Net                           3              7              0            106
	Bourne Again Shell                1             19             12             74
	make                              2              5             13             18
	--------------------------------------------------------------------------------
	SUM:                           2803          44350          56344         487144
	--------------------------------------------------------------------------------

A graphical comparison of the projects' size in terms of files and lines of code (LOC) -- note the logarithmic scale of the y-axis:

![Graphical comparison of the project size](https://github.com/xeraa/cms-security/raw/master/size.png)

### Interpretation

* Drupal is the slimmest project as practically everything is a module. Less code provides fewer possibilities to introduce bugs, so the highly modularized approach might be an advantage in terms of core vulnerabilities.
* WordPress comes in second with already three times the lines of code compared to Drupal.
* The third place is taken by ExpressionEngine with a low number of files -- making it relatively similar to WordPress.
* Joomla and MODX are very alike and take the fourth place, sitting pretty much in the middle of the enclosing projects.
* TYPO3 and SilverStripe are (again) nearly of identical size, so their comparison might be well balanced. However, TYPO3's lines of PHP code are nearly twice as high as SilverStripe's one, making it hard to give an unbiased relation.
* One could compare quite some interesting facts about the projects (lines of code per file, comments per LOC, ratio PHP to JavaScript,…), but that is not relevant for the security analysis, so we will leave it at that.


## Quantitative Comparison
A quantitative comparison should be simple: Count the vulnerabilities and that is it.

### Assumptions
However, the devil is in the details and we are making the following assumptions:

* What is a sensible time frame to consider? Too long and you are taking long gone code into account, too short and you are not getting the complete picture. Let us settle on the years 2010 and 2011.
* How do you count vulnerabilities only present in version A (still supported), if a newer version B is already available? If the same vulnerability is present in multiple versions, it is only counted as one. However, all vulnerabilities in supported releases are taken into account, not just the latest stable release.
* What about issues in release candidates? We are only considering final code.
* How should "hardening" be counted (I am looking at you, WordPress and ExpressionEngine)? If it needs hardening, it is counted. If other projects fix those silently: They should not -- if pointed out I will include such changes.
* What about features disabled by default? All the core code is counted, disabled or not.
* Does it make a difference if a flaw is being fixed a single time or in multiple places with one update? If it is the same defect it is only counted a single time, even if it occurs multiple times.
* What about modules, especially with Drupal? While the security of a CMS also depends on its modules, it is impossible to make a comparable selection. Should we try to achieve the same functionality across all systems, should we include the most popular X modules for each project,…?
* Vulnerabilities per hundred thousand lines of code (LOC^5), rounded to thousands: Which lines do you count? HTML or CSS are not or at least less susceptible to security issues, while JavaScript or PHP are far more problematic. For simplicity we will use the overall lines of code and not try to only count a subset or even weigh them.
* Except for ExpressionEngine all other CMS are open source products. This comparison cannot provide any evaluation of the difference between open and closed source software. On the one hand, having only a single closed source project does not give a balanced picture. On the other hand, ExpressionEngine's source code is available to everyone buying a license. So it is quite different to Microsoft Windows for example, where the source code is a well kept secret.
* Neither [Secunia](https://secunia.com/advisories/search/), [NIST](http://web.nvd.nist.gov/view/vuln/search), [ISS](http://webapp.iss.net/Search.do?searchType=vuln&keyword=), [OSVDB](http://osvdb.org/search/advsearch), or [SecurityFocus](http://www.securityfocus.com/bid) seem to list all vulnerabilities (especially for the lesser known SilverStripe). So they cannot be used for an overall assessment.  
  *Addendum: According to [Ingo Schommer](https://twitter.com/chillu), SilverStripe tried to add their vulnerabilities to Secunia, but they [were ignored](https://twitter.com/#!/chillu/status/159212258398978048).*
* Where do we get the list of vulnerabilities from? We are taking the official announcements of each project, specifically: [https://wordpress.org/news/category/security/](https://wordpress.org/news/category/security/), [https://drupal.org/security](https://drupal.org/security), [http://typo3.org/teams/security/security-bulletins/typo3-core/](http://typo3.org/teams/security/security-bulletins/typo3-core/), [http://developer.joomla.org/security/news/](http://developer.joomla.org/security/news/), [http://forums.modx.com/board/8/security-notices](http://forums.modx.com/board/8/security-notices), [http://expressionengine.com/user_guide/changelog.html](http://expressionengine.com/user_guide/changelog.html) as well as [http://expressionengine.com/legacy_docs/changelog.html](http://expressionengine.com/legacy_docs/changelog.html), and [http://www.silverstripe.org/security-releases/](http://www.silverstripe.org/security-releases/)


### Vulnerabilities

| Year | Project               | Advisories | Vulnerabilities | Vulnerability per LOC^5 |
|------|-----------------------|------------|-----------------|-------------------------|
| 2010 | WordPress (1)         |  3         |  4              |  4 / 1.54 =  2.60       |
|      | Drupal (2)            |  2         |  8              |  8 / 0.53 = 15.09       |
|      | TYPO3 (3)             |  6         | 27              | 27 / 4.36 =  6.19       |
|      | Joomla (4)            | 10         | 10              | 10 / 2.35 =  4.26       |
|      | MODX (5)              |  2         |  9              |  9 / 2.45 =  3.67       |
|      | ExpressionEngine (6)  |  -         |  4              |  4 / 1.99 =  2.01       |
|      | SilverStripe (7)      |  7         | 20              | 20 / 4.87 =  4.11       |
| 2011 | WordPress (8)         |  6         | 19              | 19 / 1.54 = 12.34       |
|      | Drupal (9)            |  3         |  5              |  5 / 0.53 =  9.43       |
|      | TYPO3 (10)            |  4         | 15              | 15 / 4.36 =  3.44       |
|      | Joomla (11)           | 35         | 35              | 35 / 2.35 = 14.89       |
|      | MODX (12)             |  1         |  3              |  3 / 2.45 =  1.22       |
|      | ExpressionEngine (13) |  -         | 12              | 12 / 1.99 =  6.03       |
|      | SilverStripe (14)     |  1         |  5              |  5 / 4.87 =  1.03       |
| Sum  | WordPress             |  9         | 23              | 23 / 1.54 = 14.94       |
|      | Drupal                |  5         | 13              | 13 / 0.53 = 24.53       |
|      | TYPO3                 | 10         | 42              | 42 / 4.36 =  9.63       |
|      | Joomla                | 45         | 45              | 45 / 2.35 = 19.15       |
|      | MODX                  |  3         | 12              | 12 / 2.45 =  4.90       |
|      | ExpressionEngine      |  -         | 16              | 16 / 1.99 =  8.04       |
|      | SilverStripe          |  8         | 25              | 25 / 4.87 =  5.13       |

Detailed list of advisories and vulnerabilities:

1. [3.0.4](https://wordpress.org/news/2010/12/3-0-4-update/): 1,
   [3.0.3](https://wordpress.org/news/2010/12/wordpress-3-0-3/): 1,
   [3.0.2](https://wordpress.org/news/2010/11/wordpress-3-0-2/): 2 ("some additional security enhancements" are counted as one)
2. [SA-CORE-2010-002](https://drupal.org/node/880476): 4,
   [SA-CORE-2010-001](https://drupal.org/node/731710): 4
3. [TYPO3-SA-2010-022](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-022/): 8 (every vulnerability is being counted, not just the subcomponents -- this is rather misleading),
   [TYPO3-SA-2010-020](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-020/): 6,
   [TYPO3-SA-2010-012](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-012/): 15,
   [TYPO3-SA-2010-008](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-008/): 1,
   [TYPO3-SA-2010-004](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-004/): 4,
   [TYPO3-SA-2010-001](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-001/): 1
4. [20101101](http://developer.joomla.org/security/news/323-20101101-core-sqli-info-disclosurevulnerabilities.html),
   [20101001](http://developer.joomla.org/security/news/322-20101001-core-xss-vulnerabilities.html),
   [20100704](http://developer.joomla.org/security/news/318-20100704-core-xss-vulnerabillitis-in-back-end.html),
   [20100703](http://developer.joomla.org/security/news/317-20100703-core-xss-vulnerabillitis-in-back-end.html),
   [20100702](http://developer.joomla.org/security/news/316-20100702-core-xss-vulnerabillitis-in-back-end.html),
   [20100701](http://developer.joomla.org/security/news/315-20100701-core-sql-injection-internal-path-exposure.html),
   [20100501](http://developer.joomla.org/security/news/314-20100501-core-xss-vulnerabilities-in-back-end.html),
   [20100423](http://developer.joomla.org/security/news/310-20100423-core-installer-migration-script.html),
   [20100423](http://developer.joomla.org/security/news/309-20100423-core-sessation-fixation.html),
   [20100423](http://developer.joomla.org/security/news/311-20100423-core-negative-values-for-limit-and-offset.html) (the last three are dates, that is why they are exactly the same)
5. MODX does not provide an advisory for every issue -- I did not link those "missing" issues, they are only available in the [change log](https://github.com/modxcms/revolution/blob/develop/core/docs/changelog.txt).  
   2.0.5: "[#2918] Address XSS vuln in manager login that allows JS injection",
   [2.0.3](http://forums.modx.com/thread/264/modx-revolution-2-0-3-addresses-pair-of-vulnerabilities#dis-post-1670): 2,
   2.0.1: "[#MODX-2210] Added strip for xss in manager a variable",
   2.0.0: "Hardened security on some file download actions in mgr such as console output, phpinfo, properties export",
   [1.0.3](http://forums.modx.com/thread/261/security-updates-in-modx-evolution-1-0-3-you-really-should-upgrade#dis-post-1667): 3
   [1.0.4](http://forums.modx.com/thread/262/modx-evolution-sql-injection-vulnerability#dis-post-410625): 1
6. ExpressionEngine does not provide any advisories or at least I could not find them.  
   [2.1.2](http://expressionengine.com/user_guide/changelog.html#version-2-1-2): 1 ("file uploads would not be run through xss_clean in some cases"),
   [2.1.1](http://expressionengine.com/user_guide/changelog.html#version-2-1-1): 1,
   [2.1.0](http://expressionengine.com/user_guide/changelog.html#version-2-1-0): 1,
   [1.7.0](http://expressionengine.com/legacy_docs/changelog.html#v170): 1 (this might be the same issue as in 2.1.1, but there is no way to tell for sure)
7. [2.4.4](http://doc.silverstripe.org/sapphire/en/changelogs/2.4.4): 8,
   [2.4.3](http://doc.silverstripe.org/sapphire/en/changelogs/2.4.3): 2,
   [2.4.2](http://doc.silverstripe.org/sapphire/en/changelogs/2.4.2): 2,
   [2.4.1](http://doc.silverstripe.org/sapphire/en/changelogs/2.4.1): 4,
   [2.3.7](http://doc.silverstripe.org/sapphire/en/changelogs/2.3.7): 2,
   [2.3.6](http://doc.silverstripe.org/sapphire/en/changelogs/2.3.6): 1,
   [2.3.5](http://doc.silverstripe.org/sapphire/en/changelogs/2.3.5): 1
8. [3.1.4](https://wordpress.org/news/2011/06/wordpress-3-1-4/): 5 (I would count 4 issues in the [changelog](https://core.trac.wordpress.org/log/branches/3.1/?action=stop_on_copy&mode=stop_on_copy&rev=18377&stop_rev=18043)),
   [3.1.3](https://wordpress.org/news/2011/05/wordpress-3-1-3/): 5,
   [3.1.2](https://wordpress.org/news/2011/04/wordpress-3-1-2/): 1,
   [3.1.1](https://wordpress.org/news/2011/04/wordpress-3-1-1/): 3,
   [3.0.5](https://wordpress.org/news/2011/02/wordpress-3-0-5/): 5
9. [SA-CORE-2011-003](https://drupal.org/node/1231510): 1,
   [SA-CORE-2011-002](https://drupal.org/node/1204582): 1,
   [SA-CORE-2011-001](https://drupal.org/node/1168756): 3
10. [TYPO3-CORE-SA-2011-004](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-004/): 1,
    [TYPO3-CORE-SA-2011-003](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-003/): 1,
    [TYPO3-CORE-SA-2011-002](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-002/): 1,
    [TYPO3-CORE-SA-2011-001](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-001/): 12
11. [20111103](http://developer.joomla.org/security/news/375-20111103-core-password-change.html),
    [20111102](http://developer.joomla.org/security/news/374-20111102-core-password-change.html),
    [20111101](http://developer.joomla.org/security/news/373-20111101-core-xss-vulnerability.html),
    [20111003](http://developer.joomla.org/security/news/372-20111003-core-information-disclosure.html),
    [20111002](http://developer.joomla.org/security/news/371-20111002-core-information-disclosure.html),
    [20111001](http://developer.joomla.org/security/news/370-20111001-core-information-disclosure.html),
    [20110903](http://developer.joomla.org/security/news/369-20110903-core-information-disclosure.html),
    [20110902](http://developer.joomla.org/security/news/368-20110902-core-xss-vulnerability.html),
    [20110901](http://developer.joomla.org/security/news/367-20110901-core-xss-vulnerability.html),
    [20110701](http://developer.joomla.org/security/news/357-20110701-xss-vulnerability.html),
    [20110604](http://developer.joomla.org/security/news/352-20110604-xss-vulnerability.html),
    [20110603](http://developer.joomla.org/security/news/350-20110603-unauthorised-access.html),
    [20110602](http://developer.joomla.org/security/news/351-20110602-information-disclosure.html),
    [20110601](http://developer.joomla.org/security/news/349-20110601-xss-vulnerabilities.html),
    [20110409](http://developer.joomla.org/security/news/347-20110409-core-clickjacking.html),
    [20110408](http://developer.joomla.org/security/news/348-20110408-core-sql-injection.html),
    [20110407](http://developer.joomla.org/security/news/346-20110407-core-unauthorised-access.html),
    [20110406](http://developer.joomla.org/security/news/345-20110406-core-xss-vulnerabilities.html),
    [20110405](http://developer.joomla.org/security/news/344-20110405-core-xss-vulnerabilities.html),
    [20110404](http://developer.joomla.org/security/news/343-20110404-core-xss-vulnerabilities.html),
    [20110403](http://developer.joomla.org/security/news/342-20110403-core-information-disclosure.html),
    [20110402](http://developer.joomla.org/security/news/341-20110402-core-information-disclosure.html),
    [20110401](http://developer.joomla.org/security/news/340-20110401-core-information-disclosure.html),
    [20110308](http://developer.joomla.org/security/news/339-20110308-core-csrf-vulnerability.html),
    [20110307](http://developer.joomla.org/security/news/338-20110307-core-xss-vulnerabilities.html),
    [20110306](http://developer.joomla.org/security/news/337-20110306-core-dos-vulnerabilities.html),
    [20110305](http://developer.joomla.org/security/news/336-20110305-core-csrf-vulnerability.html),
    [20110304](http://developer.joomla.org/security/news/335-20110304-core-unauthorised-access.html),
    [20110303](http://developer.joomla.org/security/news/334-20110303-core-information-disclosure.html),
    [20110302](http://developer.joomla.org/security/news/333-20110302-core-redirect-vulnerabilities.html),
    [20110301](http://developer.joomla.org/security/news/332-20110301-core-information-disclosure.html),
    [20110204](http://developer.joomla.org/security/news/331-20110204-core-xss-vulnerabilities.html),
    [20110203](http://developer.joomla.org/security/news/330-20110203-core-xss-vulnerabilities.html),
    [20110202](http://developer.joomla.org/security/news/329-20110202-core-path-disclosure.html),
    [20110201](http://developer.joomla.org/security/news/328-20110201-core-sql-injection-path-disclosure.html)
12. 2.1.1: "Harden connector CSRF security by tying user session modauth to prevent hijacking of session if modauth is known", [1.0.5](http://forums.modx.com/thread/268/modx-evo-1-0-4-and-prior-sql-injection-and-directory-traversal-vulnerabities#dis-post-1674): 2
13. [2.3.1](http://expressionengine.com/user_guide/changelog.html#version-2-3-1): 1,
    [2.3.0](http://expressionengine.com/user_guide/changelog.html#version-2-3-0): 3,
    [2.2.2](http://expressionengine.com/user_guide/changelog.html#version-2-2-2): 1 ("pending members" -- does not once mention security or anything similar),
    [2.2.0](http://expressionengine.com/user_guide/changelog.html#version-2-2-0): 1 ("did not respect the IP and User Agent security setting"),
    [2.1.4](http://expressionengine.com/user_guide/changelog.html#version-2-1-4): 3,
    [1.7.1](http://expressionengine.com/legacy_docs/changelog.html#v171): 3 
14. [2.4.6](http://doc.silverstripe.org/sapphire/en/trunk/changelogs/2.4.6): 5

A graphical comparison looks like this:

![Graphical comparison of the number of vulnerabilities](https://github.com/xeraa/cms-security/raw/master/quantitative.png)

### A Word on the Announcements

* The [announcements of WordPress](https://wordpress.org/news/category/security/) are not that great. First, the page was (at least for me) pretty hard to locate. Second, the overview is very limited -- most other projects are doing this better. Third, statements like "[Version 3.1.4 also incorporates several other security fixes and hardening measures […]](https://wordpress.org/news/2011/06/wordpress-3-1-4/)" really are not transparent. The change log is referenced, but I really do not want to look through that to decide how important the update is. Finally, it mixes security vulnerabilities and regular issues making it pretty confusing.
* [Drupal](https://drupal.org/security) does this much better, I would even say best. The overview is both compact and contains all the relevant information (affected version, risk assessment, local / remote).
* [TYPO3's list](http://typo3.org/teams/security/security-bulletins/typo3-core/) is not bad and the detail pages contain all relevant information. I just did not understand the numbering schema in 2010: 001 (1 issue) is being followed by 004 (3 issues); next is 008 with 1 issue again.
* [Joomla](http://developer.joomla.org/security/news.html) has probably too much information on the overview page, but everything of interest is there, so I cannot really fault them for that.
* MODX did a great job at hiding their security notices -- or at least I had that impression. After finding [http://forums.modx.com/board/8/security-notices](http://forums.modx.com/board/8/security-notices) it got me a little bit confused. Not only does it include non-core issues for popular modules, it includes [a PHP issue and MODX filter for it](http://forums.modx.com/thread/267/critical-php-bug-security-notice-and-patch#dis-post-1673) as well. While the overview is rather useless, the detailed descriptions are decent. However, they do not seem to release an advisory for every security issue! I did only realize that when I took a look through the [official change log](https://github.com/modxcms/revolution/blob/develop/core/docs/changelog.txt). I tried to find all security related changes, but I might have missed some -- especially if you search for the term "sanity" there are quite a lot of entries, which might somehow security related. As most of them will be harmless, I did not count them. Nevertheless, I think this kind of "tweaking" is really the wrong approach, but that is something everyone will have to decide for themselves.
* ExpressionEngine's security notices are so well hidden, I am not sure if I have found the correct page or not -- the full blown change log. Adding injury to insult, it is split into the [1.x](http://expressionengine.com/legacy_docs/changelog.html) and [2.x](http://expressionengine.com/user_guide/changelog.html) change log. Do not ask for severity ratings, there are none. Together with MODX's announcements, these are the least transparent and overall worst announcement pages of all systems. Maybe that is intentional, as ExpressionEngine has been criticized for their "[Quiet release](http://www.lullabot.com/articles/drupal-and-expressionengine-security-models)" approach before.
* The [overview page of SilverStripe](http://www.silverstripe.org/security-releases/) is very basic, but the linked detail pages contain a lot of information. ~~A severity rating on the overview page or at least in the details would be nice, though.~~  
  *Addendum: A severity rating has been added (actually, I got it started): [http://doc.silverstripe.org/sapphire/en/trunk/misc/release-process#severity-rating](http://doc.silverstripe.org/sapphire/en/trunk/misc/release-process#severity-rating)*

### Interpretation

* Joomla had the most vulnerabilities, but TYPO3 followed closely.
* Drupal had the least vulnerabilities in the given period, but also had the highest number of vulnerabilities per LOC -- which I found rather surprising.
* SilverStripe has had the least security issues per LOC, but nearly double the number compared to Drupal.
* While TYPO3 and SilverStripe had significantly more security flaws in 2010 than in 2011, it is just the other way around for WordPress and Joomla. However, I would not be so bold as to suggest the code base of the former ones has matured and will be (more) secure in the future. Taking a look at only two sample years, does not give an indication of development.
* While Joomla is still supporting 1.5, 1.6 has been replaced by 1.7 so they have only been supporting two versions at the same time (like most other projects). This is important as we do not want to punish projects for providing more support than others.
* TYPO3 supports three versions (stable, old stable, and deprecated). However, if I am not mistaken, all security issues in the last two years have been part of the two latest releases (and sometimes older versions as well). Hence, the extended support policy has not been a disadvantage.
* Could the number of discovered flaws correlate with the number of audits or active users? Meaning that less popular projects might have many undiscovered issues while popular ones do not? This might be true, but I do not see a reliable way to take that into account.


## Qualitative Comparison
Besides doing a "simple" quantitative comparison, this does not give a complete picture. If a project has ten minor security flaws, it looks much worse in the previous comparison than a project having four really bad ones. In order to give a more balanced overview, we should take a better look at the "quality" of issues.

### Assumptions
While a fair quantitative comparison is already hard, a balanced qualitative evaluation is probably impossible. Nevertheless, let us try it with the given set of assumptions on the rating of severity:

* As Common Vulnerability Scoring System (CVSS) values are not available for all security flaws, we cannot use them -- this would have been the most balanced approach.
* Instead I will take a very simple approach: Count how many of the vulnerabilities are serious. We will try to only include issues which should be fixed immediately and filter out stuff that can probably wait for the next maintenance window. I find this distinction useful as I want to know how often I have to put out fires. The following points will specify what is serious and what is not for each project.
* In WordPress I will rely on the announcement text. Due to the fuzziness of the bulletins, these numbers will be less authoritative than others.
* Drupal has a good risk assessment and I will count their [risk levels](https://drupal.org/security-team/risk-levels) of "Highly Critical" (5 of 5) and "Critical" (4 of 5) as serious. Unfortunately only the whole advisory is rated, so the individual issues must be evaluated.
* For TYPO3 it is pretty similar, "Critical" (4 of 4) and "High" (3 of 4) of their [severity meaning](http://typo3.org/documentation/document-library/extension-manuals/doc_guide_security/1.0.0/view/1/3/#id2313132) are considered serious.
* [Joomla's security team](http://developer.joomla.org/security.html) uses exactly the same severity as TYPO3.
*
* As ExpressionEngines's change log is everything there is and its information is pretty limited, I will try to more or less guess. I am sorry if I err on the side of over reporting, but this is deserved, in my humble opinion.
* SilverStripe does not have severity levels for 2010 and 2011, so the very detailed changes will be used here -- pretty much the same as with WordPress.

### Vulnerabilities

| Project           | Serious Vulnerabilities | Percentage of serious issues |
|----------------------|-------------------------|------------------------------|
| WordPress (1)     |  1                      |  1 / 23 =  4%                |
| Drupal (2)        |  3                      |  3 / 13 = 23%                |
| TYPO3 (3)         | 18                      | 18 / 42 = 43%                |
| Joomla (4)        |  3                      |  3 / 45 =  7%                |
| MODX (5)             |  2                      |  2 / 12 = 17%                |
| ExpressionEngine (6) |  2                      |  2 / 16 = 13%                |
| SilverStripe (7)     |  4                      |  4 / 25 = 16%                |

Detailed list of serious vulnerabilities:

1. [3.0.4](https://wordpress.org/news/2010/12/3-0-4-update/): 1
2. [SA-CORE-2011-002](https://drupal.org/node/1204582): 1,
   [SA-CORE-2011-001](https://drupal.org/node/1168756): 0 (I would not consider any of these serious despite the bulletin's rating),
   [SA-CORE-2010-002](https://drupal.org/node/880476): 1 ("OpenID authentication bypass"),
   [SA-CORE-2010-001](https://drupal.org/node/731710): 1 ("Open redirection")
3. [TYPO3-CORE-SA-2011-004](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-004/): 1,
   [TYPO3-CORE-SA-2011-001](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-core-sa-2011-001/): 4,
    [TYPO3-SA-2010-022](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-022/): 2,
   [TYPO3-SA-2010-020](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-020/): 1,
   [TYPO3-SA-2010-012](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-012/): 7,
   [TYPO3-SA-2010-008](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-008/): 1,
   [TYPO3-SA-2010-004](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-004/): 1,
   [TYPO3-SA-2010-001](http://typo3.org/teams/security/security-bulletins/typo3-core/typo3-sa-2010-001/): 1
4. [20111103](http://developer.joomla.org/security/news/375-20111103-core-password-change.html),
   [20111102](http://developer.joomla.org/security/news/374-20111102-core-password-change.html),
   [20100501](http://developer.joomla.org/security/news/314-20100501-core-xss-vulnerabilities-in-back-end.html)
5. [1.0.5](http://forums.modx.com/thread/268/modx-evo-1-0-4-and-prior-sql-injection-and-directory-traversal-vulnerabities#dis-post-1674): 1,
   [1.0.3](http://forums.modx.com/thread/261/security-updates-in-modx-evolution-1-0-3-you-really-should-upgrade#dis-post-1667): 1 ("SQL Injection via WebLogin")
6. [2.1.1](http://expressionengine.com/user_guide/changelog.html#version-2-1-1): 1 ("in certain circumstances could result in arbitrary code execution"),
   [1.7.0](http://expressionengine.com/legacy_docs/changelog.html#v170): 1 (again, this might be the same issue as in 2.1.1)
7. [2.4.6](http://doc.silverstripe.org/sapphire/en/trunk/changelogs/2.4.6): 2 ("Possible SQL injection for MySQL when using far east character encodings", "Potential remote code execution through serialization of page comment user submissions"),
   [2.4.4](http://doc.silverstripe.org/sapphire/en/changelogs/2.4.4): 1 ("SQL injection with Translatable extension enabled"),
   [2.3.7](http://doc.silverstripe.org/sapphire/en/changelogs/2.3.7): 1 ("Fixing Member_ProfileForm to validate for existing members via Member_Validator to avoid CMS users to switch to another existing user account by using their email address")

A graphical comparison looks like this:

![Graphical comparison of the number of serious vulnerabilities](https://github.com/xeraa/cms-security/raw/master/qualitative.png)

### Interpretation

* WordPress only had a single serious vulnerability (in case I interpreted that correctly) -- impressive.
* Drupal did also well, only the percentage is a little higher due to the low number of overall issues.
* In contrast to the first two, TYPO3 appeared to not do well at all. It has by far most serious vulnerabilities both in absolute numbers and the percentage. However, I would attribute part of the difference compared to the other projects to TYPO3's stricter rating of vulnerabilities. One should probably add a CVSS comparison to Drupal to get a more balanced result.
* Joomla, while having the most vulnerabilities overall, did very well with serious ones (meaning it had few of those).
* SilverStripe seems to be floating somewhere between the other projects, neither being exceptionally good or bad.


## Conclusion
What did we learn? I think all projects are doing a pretty good job overall. There are differences, but if you factor in LOC, features,… the projects are more similar than I would have expected.

Will I take back my initial comment on TYPO3? Not really. While 2011 has been much better than 2010, I am still not too impressed with their numbers -- sorry! Having said that, it is hard or nearly impossible to have a totally fair comparison.


&copy; 2012 [Philipp Krenn](https://twitter.com/xeraa): [Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/)