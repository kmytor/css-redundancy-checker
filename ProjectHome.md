# CSS Redundancy Checker #

A simple script that, given a CSS stylesheet and either a .txt file listing URLs of HTML files, or a directory of HTML files, will iterate over them all and list the CSS statements in the stylesheet which are never called in the HTML.

Basically, it helps you keep your CSS files relevant and compact. And it's reasonably accurate.

## Usage ##

```
css-redundancy-checker.rb [cssfile] [directory of html files OR .txt file listing urls to use]
```

## Requirements ##

you'll need Rubygems and Hpricot, plus a reasonably up-to-date version of Ruby (built on 1.8.5; should be fine on at least 1.8.4).

## More detailed instructions (if the above wasn't clear enough) ##

First, you'll need Ruby and Rubygems installed. That's left as an exercise for the reader.

Next, you'll need the Hpricot gem:
```
sudo gem install hpricot
```

Pick the most recent version for your OS (mswin32 for Windows, ruby for anything else)

Once you've got all that, you should be set. Now, get the redundancy checker script (or update it to the latest version):

```
svn checkout http://css-redundancy-checker.googlecode.com/svn/trunk/ css-redundancy-checker
```

Navigate to the directory you've checked the code out to. Then, it's just a case of doing this:

```
ruby css-redundancy-checker.rb [cssfile] [directory of html files OR .txt file listing urls to use]
```

The first argument should be a CSS file. The second argument should EITHER be a directory, containing HTML files, or a .txt file with one URL per line for an HTML file. The script will process all the relevant files, and at the end, list any CSS statements which are not relevant to ANY of the HTML files.

## Notes ##

The script will NOT work with incomplete HTML files (eg: template components, partial fragments, etc). You should only use it on complete HTML, either in the form of flat files, or rendered output from your web application.

## Bugs and correspondance ##

...should be addressed to tom@infovore.org

---
Released under the MIT License.