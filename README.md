#Chymeric Photography Repository

Git repository for the Chymera Network photography blog.
This repository contains all files unique to the blog and their history dating back to the orginal publication date.

##Cite Stable Versions

Websites in general and blogs in particular are often unsuited for citation in texts striving to provide reliable sources.
This is chiefly because content of a web-URL (to a blog post or wiki article) may be modified at any time without notice or ways to retrieve the previous version.
The [Chymeric Photography Blog](http://photo.chymera.eu) provides a high degree of reliability as a citable source by backing up and versioning its entire content.

While we recommend viewing our content through our website for the best reading experience;
we encourage citation of fixed versions via links to our repository hosted on the reliable and stable GitHub service.
In this way your citation links will remain accessible whatever happens to our website, and the content they point to will always be the same.

You can view a history of our updates by clicking the ["commits" link above](https://github.com/TheChymera/chymeric_photography/commits/master).
You may browse versions of each particular file by clicking through the file tree above.
Our actual articles are all under [```/source/_posts/```](https://github.com/TheChymera/chymeric_photography/tree/master/source/_posts).

##Reproduce this Website

Reproducible content is a vital to the quality control and transparency of any source of information.
To this end, we are happy to offer you the possibility of cloning **our entire** website.

To obtain a publishing-ready identical copy of the [Chymeric Photography Blog](http://photo.chymera.eu) on your machine, please follow the instructions below.

###Get Octopress

Clone Octopress:

    $ git clone git://github.com/imathis/octopress.git photo
    $ cd photo

Install dependencies:

    $ gem install bundler
    $ bundle install
    
###Get our Theme of Choice

Clone Whitespace:

    $ git clone git://github.com/lucaslew/whitespace.git .themes/whitespace

Install Whitespace:

    $ bundle exec rake install['whitespace']
    
###Remove the Octopress Git Data

    $ rm -rf .git
    
###Create the Chymeric Photography Git Repository

    $ git init
    $ git remote add origin https://github.com/TheChymera/chymeric_photography.git
    $ git fetch --all
    $ git reset --hard origin/master
    
And generate the [Chymeric Photography Blog](http://photo.chymera.eu):

    $ bundle exec rake generate

###Push Content
If you would like to contribute to our website you would have to contact us for ssh login data.
If you would like to host a mirror or fork of our website somewhere else, you would have to edit the following bits

    ssh_user       = "m4nt1s@redwings.dreamhost.com"
    ssh_port       = "22"
    document_root  = "~/photo.chymera.eu/"

of your ```Rakefile``` file.

Other than that you're good to go!
