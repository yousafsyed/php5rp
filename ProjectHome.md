# PHP5 Reverse Proxy #
This is a reverse proxy written in PHP5. It uses [cURL](http://us.php.net/curl) to handle the back-end connections. I wrote it to replace some mod\_perl code that was slow because it had to talk to our back-end API via XML calls. This turned out to be faster.

## What is it useful for? ##
Some uses may include
  * Extend the class to add an SSO layer to back-end app servers not written in PHP
  * Extend to handle authorization and authentication to a back-end database (SVN, for example)

## Limitations ##
It does not, currently, handle any caching. I expect that caching could be implemented in a sub-class.

## How do I get the code? ##
From the google docs:

Non-members may check out a read-only working copy anonymously over HTTP.
svn checkout http://php5rp.googlecode.com/svn/trunk/ php5rp

Read the readme.txt. There is an assumption that you know what a reverse proxy is for, and how to configure apache. Other documentation is welcome! :)