---
title: Google
---

# Google Chrome

- ctrl-l gets you to the address bar

# Google Advanced Search Operators

The below information is pruned down the [original
source.](http://www.sourcinghacks.com/google-search-operators-and-more/)

| **Search within a specific site or domain**

_site:_

| Use the **site:**  operator to search for information within a specific
website or type of site (.org, .edu).

[ **site:** linkedin.com] or [ **site:** edu]

| **Placeholder**  / **Fill in the blank**

_query \* query_

| Use an asterisk (\*) as a placeholder for any unknown or â€œwildcardâ€ terms.
Results will vary depending on its use, how Google has indexed the content of
the page or what Google feels is relevant.

["senior \* recruiter"] will include results for [senior **technical**
recruiter]

["senior \* \* recruiter"] will include results for [senior **interactive
marketing**  recruiter]

| **Search for a specific term within the Title of a website**

_intitle:_

| Place **intitle:**  immediately in front of your query to search for a
specific term or phrase within the Title of a website or page.

[ **intitle:** resume] or [ **intitle:**"resume software engineer"]

| **Search for terms within the URL of a website**

_inurl:_

| Search for a specific term or terms within the URL of a website.

[ **inurl:** resume]

**_Tip:_**  The query must be a complete or whole term, meaning that you cannot
extract a term from a string of consecutive letters or numbers.

| **Search for pages with links**

_link:_

| Use the **link:**  operator to search websites or pages that contain links to
another page or website.

[ **link:** google.com]

| **Search by file type**

_filetype:_

| Use the **filetype:**  operator to search for specific types of files, such
as PDFs, DOCs, or XLS

[ **filetype:** pdf]

| **\Find related websites**

_related:_

| Use the **related:**  operator to find sites that have similar content by
typing **related:**  immediately in front of a website URL.

**[related:**jigsaw.com]

| **Exclude a word or phrase**

_-query_

| Add a dash (-) immediately in front of a word to exclude all results that
include that word.

[-job -jobs]

You can also exclude results based on other operators, like excluding all
results from a specific site.

[developer -site:linkedin.com]

| **Include similar words with the Tilde**

_~query_

| At times, Google _may_ replace some words in your original search query with
synonyms. To tell Google that you want synonyms included, add a tilde sign (~)
immediately in front of a word to search for that word as well as synonyms.

[ software ~engineer] will also include results for [software developer]

| **Search for all words**

_query query_

_query AND query_

| To search for pages that need to have all words, include AND (capitalized) or
a space between the words. Google assumes AND when there is simply a space
between terms.

[software engineer "seattle washington"] or [software AND engineer AND "seattle
washington"]

| **Search for either word**

_query | query_

_query OR query_

| To search for pages that need to have only one of several words, include OR
(capitalized) or a pipe (|) between the words.

[software engineer seattle | "san francisco"] or [software engineer seattle OR
"san francisco"]

| **Search for a number range**

_number..number_

| Separate numbers by two periods (with no spaces) to see results that contain
numbers in a given range.

[50..300 connections]

**_Tip:_**  Use only one number with the two periods to indicate an upper
maximum or a lower minimum.

# Google Sites

My original site was based on Google Sites. This section contains some useful
tidbits I accumulated during its creation.

- As of when I created my site, Google Sites did not support LaTeX, nor did
  it have any plans to do so.
  [Workaround](http://www.codecogs.com/latex/eqneditor.php)!
- Slideshow [tutorial](http://www.steegle.com/websites/google-sites-howtos/docs-presentation-slider-gadget).

I converted my google site to Jekyll using the instructions from
- http://candland.net/2016/02/16/migrate-google-sites-to-jekyll.html

Note that I:
- Leveraged https://github.com/olbat/docker-debian-ruby-nokogiri and replaced
  reverse_markdown with docker run -i <image tag> reverse_markdown
- Had to install ack (http://beyondgrep.com/install/) and tidy (via apt)
- Was still left with a decent amount of cleanup to do

## Custom Domain with DreamHost

I had an inordinate number of struggles getting a custom domain set up with Google Sites and DreamHost. This was only exacerbated by the lack of comprehensible resources on the issue. To save myself and others from this in the future, I present the following steps:

1. Make a Google Site
2. [Go buy a domain from DreamHost.](http://www.dreamhost.com/domains/)
3. Prep your domain for mapping your Google Site
  1. Click on "Domains" -\> "Manage Domains" in the left panel
  2. Click on "Edit" under "Web Hosting"
  3. Unpark your domain (bottom of page)
  4. Click on "Host DNS only!"
  5. Go back to "Manage Domains"
  6. Click on "DNS"
  7. Add a CNAME record to your DNS configuration:
    - Name = www
    - Value = ghs.googlehosted.com)
4. [Verify your domain with Google's Webmaster Tools](https://www.google.com/webmasters/tools)
  1. Click "Add a site"
  2. Type in the URL of your DreamHost domain (including www.)
  3. Click "Continue"
  4. Select "Other" from the drop down menu
  5. Head over to DreamHost
  6. Add the indicated TXT record to your DNS configuration:
    - Leave "Name" blank
    - Enter the string Google gave you as the "Value"
  7. Click "Verify" when you're done (this may take a few minutes)
5. Map your Google Site to your new domain
  1. Head on over to the "Manage Site" Page
  2. Click on "Web Address" in the navigation bar on the left
  3. Type your web address into the bar (include "www.") and click Add
  4. You should see your web address pop up as "Canonical". This means that this is the address which Google will index.
6. That's it! Now just wait a while (e.g. 12 hours) for the gears to churn and set things up. Soon enough, your custom domain will display your Google Site.
7. Email tech-support to setup up a naked-url redirect.
