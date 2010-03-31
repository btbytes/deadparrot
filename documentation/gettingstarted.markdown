---
title: Getting started with Deadparrot
---


Deadparrot provides a shell called `deadparrot` which is used to
create new sites, new pages and new themes. 

## The deadparrot shell
   $ deadparrot --help

will show the help file.

## Creating a new site

   $ deadparrot --new-site [projectname]
   $ deadparrot --new-site homepage

A new directory `homepage` will be created. If you do not provide
the `homepage` as a parameter, you will be prompted for one.
The structure of the `homepage` directory is: 

<pre>
        ./homepage
                ./_config.yaml
                ./_plugins
                ./_themes 
                          ./default
                                ./css
                                        ./screen.css
                               ./_templates
                                        ./base.html
                                        ./page.html
                                        ./archive.html
                                        ./tags.html     
                                        ./sitemap.xml
                                        ./atom.rss
                ./index.txt
                
</pre>

`deadparrot` ignores any file or directory starting with an
underscore.

## Compiling the new site

        $ cd homepage
        $ deadparrot
        ... some output ...
        $ ls htdocs

by default, the input files are compiled and outputted to `./htdocs`
directory. This can be configured by editing `_config.yaml`.


