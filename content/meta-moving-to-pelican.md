Title: Moving to Pelican & Reclaiming Old Writing
Date: 2021-11-01 14:31
Category: meta
Authors: Bhargav Bhat
Summary: Moving to Pelican and Reclaiming Old writing across notes, text files, emails and shared docs

This post is just a summary of me doing a Deepawali cleaning of all of my notes, old emails, text files and Google Drive stuff and moving it all under a managable blog hosted on GitHub pages with [Pelican](https://docs.getpelican.com/en/latest/).

#### Installation & Theme Selection
Pelican install was very quick and straight forward process, just follow the instructions laid out in the "quickstart" section of the docs and a fully functional, ready to serve blog was ready on my local machine. This also allowed me to try out a few themes, verify formatting (most of the posts I have were written a email, text files or shared docs, not markdown) and ensure that everything looked fine.

Theme selection was a slighly longer task, mostly consisted of [browsing](http://www.pelicanthemes.com/) available options, trawling the respective github repos and picking one that clicked visually and feature-wise. Then came the testing phase of trying it on the articles and pages that I had migrated/created so far. My main criteria for theme selection were a clean design, pleasing colours, tags & categories support along with a search function. Although I couldn't find one that checked all the boxes, I found that [pelican-hss](https://github.com/laughk/pelican-hss) had all that I wanted (save the search function). I picked that theme, made a few tweaks to the supplied pygments CSS and `base.html` template and decided to call it a day.

#### Deployment to Github Pages
My previous homepage was a rather simple landing page, with links to social media profiles:
![Previous Homepage]({static}/images/home_page.png)

and this was served out of github pages as a simple `index.html` file, forked from the html5up repo. Moving to pelican meant setting up branches slightly differently. I chose to use the `content` branch to contain all of the Pelican stuff.

#### Learning
The real power, flexibility & convenience of static hosting is apparent from all of the personal blogs and project pages hosted on GH pages. For me, a lot of the learning was around pelican,setting up venv right and migrating content

#### Road Ahead
A lot of my old notes, shared docs and learning are still scattered all over platforms. Although not too many public/shared posts and notes exist, I still have to sift through them all, deal with dead links and filter out stuff that's relevant and applicable to a wider audience. Most of the notes that I have are specific to the particular teams, products or siutations. I've gotten thru a few of these notes and will continue to add them to the site as fast as I can. As I make my way around this old stuff, a lot more posts should start popping up on the homepage. 

PS: Dates and stuff for these old posts is from file meta data, may not be 100% accurate. Stuff that was once WIP has likely been abandoned and/or is no longer relevant. Links have been updated and dead links removed (where applicable). If you find something odd or inaccurate, please do reach out. :)
