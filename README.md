# CMS Security Track Record (2010 & 2011)


**After making a (probably unwarranted) [remark on TYPO3's security](https://twitter.com/#!/xeraa/status/158250289005207553) on Twitter, [Søren Malling](https://twitter.com/sorenmalling) challenged me to it: "["All" those issues are dated since 2005..  Do some comparising and you will find its nothing!"](https://twitter.com/#!/sorenmalling/status/158325493224062976). So I decided to give it a go and do a little comparison.**


## The Contenders
I'll include the following projects:

* [WordPress](https://wordpress.org)
* [Drupal](https://drupal.org)
* [TYPO3](https://typo3.org)
* [Joomla](http://joomla.org)
* [SilverStripe](href="http://www.silverstripe.org) -- I might be [a little biased here](https://www.amazon.com/SilverStripe-Module-Extension-Themes-Widgets/dp/184951500X), but I'll try to keep it as fair as possible

Why isn't X included? Ask nicely or even provide some research and I might include it :-).


## Are They Even Comparable?
Good question! Probably, you can't compare TYPO3 to Wordpress for example -- both in terms of features, lines of code, age of codebase,... To get a better "feeling" for the projects, I'll run the latest stable version of each project through [CLOC](https://cloc.sourceforge.net). That still doesn't make it a "fair" comparison (if there is such a thing), but we're at least getting a better picture of the differences.

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
[http://prdownloads.sourceforge.net/typo3/blankpackage-4.6.3.tar.gz?download](http://prdownloads.sourceforge.net/typo3/blankpackage-4.6.3.tar.gz?download) -- I went with the "Blank Package" as it's probably the one most similar to the other releases

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

### Quick Comparison
A graphical comparison of the projects' size in terms of files and lines of code (LOC) -- note the logarithmic scale of the y-axis:

![Graphical comparison of the project size](https://github.com/xeraa/cms-security/raw/master/size.png)

* Drupal is the slimmest project as practically everything is a module. Less code provides fewer possibilities to introduce bugs, so the highly modularized approach might be an advantage in terms of core vulnerabilities.
* WordPress comes in second with three times the lines of code compared to Drupal.
* Joomla takes the third place sitting pretty much in the middle of the enclosing projects.
* TYPO3 and SilverStripe are nearly of identical size, so their comparison might be the most balanced one. However, TYPO3's lines of PHP code are nearly twice as high as SilverStripe's one, making it hard to give an unbiased relation.
* One could compare quite some interesting facts about the projects (lines of code per file, comments per LOC, ratio PHP to JavaScript,…), but that's not relevant for the security analysis, so we'll leave it at that.


## Quantitative Comparison
A quantitative comparison should be simple: Count the vulnerabilities and that's it.

### Assumptions
However, the devil is in the details and we're making the following assumptions:

* How do you count vulnerabilities only present in version A (still supported), if a newer version B is already available? If the same vulnerability is present in multiple versions, it's only counted as one. However, all vulnerabilities in supported releases are taken into account, not just the latest stable release..
* What about issues in release candidates? We're only considering final code.
* How should "hardening" be counted (I'm looking at you, WordPress)? If it needs hardening, it's counted. If other projects fix those silently: mea culpa.
* What about features disabled by default? All the core code is counted, disabled or not.
* Does it make a difference if a flaw is being fixed a single time or in multiple places with one update? If it's the same defect it's only counted a single time, even if it occurs multiple times.
* What's a sensible time frame to consider? Too long and you're taking long gone code into account, too short and you're not getting the complete picture. Let's settle on the years 2010 and 2011.
* What about modules, especially with Drupal? While the security of a CMS also depends on its modules, it's impossible to make a comparable selection. Should we try to achieve the same functionality across all systems, should we include the most popular X modules for each project,…?
* Vulnerabilities per hundred thousand lines of code (LOC^5), rounded to thousands: Which lines do you count? HTML or CSS are not or at least less susceptible to security issues, while JavaScript or PHP are far more problematic. For simplicity we'll use the overall lines of code and not try to only count a subset or even weigh them.
* Where do we get the list of vulnerabilities from? We're taking the official announcement of each project, specifically: [https://wordpress.org/news/category/security/](https://wordpress.org/news/category/security/), [https://drupal.org/security](https://drupal.org/security), [http://typo3.org/teams/security/security-bulletins/typo3-core/](http://typo3.org/teams/security/security-bulletins/typo3-core/), [http://developer.joomla.org/security/news/](http://developer.joomla.org/security/news/), and [http://www.silverstripe.org/security-releases/](http://www.silverstripe.org/security-releases/)

### Vulnerabilities

| Year | Project       | Advisories | Vulnerabilities | Vulnerability per LOC^5 |
|------|---------------|------------|-----------------|-------------------------|
| 2010 | WordPress     |  3         |  4              |  4 / 1.54 =  2.60       |
|      | Drupal        |  2         |  8              |  8 / 0.53 = 15.09       |
|      | TYPO3         |  6         | 21              | 21 / 4.36 =  4.82       |
|      | Joomla        | 10         | 10              | 10 / 2.35 =  4.26       |
|      | SilverStripe  |  7         | 16              | 16 / 4.87 =  3.29       |
| 2011 | WordPress     |  6         | 17              | 17 / 1.54 = 11.04       |
|      | Drupal        |  3         |  5              |  5 / 0.53 =  9.43       |
|      | TYPO3         |  4         |  8              |  8 / 4.36 =  1.83       |
|      | Joomla        | 35         | 35              | 35 / 2.35 = 14.89       |
|      | SilverStripe  |  1         |  3              |  3 / 4.87 =  0.62       |
| Sum  | WordPress     |  9         | 21              | 21 / 1.54 = 13.64       |
|      | Drupal        |  5         | 13              | 13 / 0.53 = 24.53       |
|      | TYPO3         | 10         | 29              | 29 / 4.36 =  6.65       |
|      | Joomla        | 45         | 45              | 45 / 2.35 = 19.15       |
|      | SilverStripe  |  8         | 19              | 19 / 4.87 =  3.90       |

A graphical comparison looks like this:

![Graphical comparison of the number of vulnerabilities](https://github.com/xeraa/cms-security/raw/master/quantitative.png)

### A Word on the Announcements

* The [announcements of WordPress](https://wordpress.org/news/category/security/) are awful. First, the page was by far the hardest to locate. Second, the overview is extremely limited -- all other projects are doing this much better. Third, statements like ["Version 3.1.4 also incorporates several other security fixes and hardening measures […]"](https://wordpress.org/news/2011/06/wordpress-3-1-4/) really aren't transparent. The change log is referenced, but I really don't want to look through that to decide how important the update is. Finally, it mixes security vulnerabilities and regular issues making it pretty confusing.
* [Drupal](https://drupal.org/security) does this much better, I would even say best. The overview is both compact and contains all the relevant information (affected version, risk assessment, local / remote).
* [TYPO3's list](http://typo3.org/teams/security/security-bulletins/typo3-core/) isn't bad and the detail pages contain all relevant information. I just didn't understand the numbering schema in 2010: 001 (1 issue) is being followed by 004 (3 issues); next is 008 with 1 issue again.
* [Joomla](http://developer.joomla.org/security/news.html) has probably too much information on the overview page, but everything of interest is there, so I can't really fault them for that.
* The [overview page of SilverStripe](http://www.silverstripe.org/security-releases/) is very basic, but the linked detail pages contain a lot of information. A severity rating on the overview page would be nice, though.

### Interpretation

* While Joomla is still supporting 1.5, 1.6 has been replaced by 1.7 so they have only been supporting two versions at the same time (like most other projects). This is important as we don't want to punish projects for providing more support than others.


## Qualitative Comparison
While a fair quantitative comparison is already hard, a balanced qualitative evaluation is probably impossible.

Due to the fuzziness of WordPress's announcements, I can't give a sensible assessment. Therefore, WordPress will not be included in the qualitative comparison.


## What About the Future and Overall Security?
While the past track record can't make certain predictions for the future

`.htaccess`

## Conclusion




&copy; 2012 [Philipp Krenn](https://twitter.com/xeraa): [Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/)
