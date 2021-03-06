Securing your application against Cross-Site Request Forgery has never been easier. Why rewrite every form on your website when a program can do it for you? Simply drop this at the top of every PHP file:

require_once '/path/to/csrf-magic.php';

...and let the magic take care of the rest. Download it now! Or try out the demo. 


<h2>News</h2>

Bleeding edge git repo
Posted 3:59 AM EDT on Thursday, January 30, 2014

moved bleeding-edge git repo to gitgub for better stability, can still find stable versions at http://csrf.htmlpurifier.org/


<b>csrf-magic 1.0.5 critical upadate</b>
Posted 6:05 AM EDT on Tuesday, January 28, 2014

csrf-magic 1.0.4 contained a bug that allowed users to bypass check using multibyte encoding, this has been fixed in the 1.0.5 release


csrf-magic 1.0.4 released
Posted 3:02 AM EDT on Wednesday, July 17, 2013

csrf-magic 1.0.4 contains some bug fixes for secret hashing and JavaScript support, and also has improved the default CSRF check failed splash page.


<h2>What is CSRF?</h2>
Cross-Site Request Forgery (CSRF) is a relatively new attack vector on websites today. It involves an attacker tricking a browser into performing an action on another website. Imagine this scenario: Bob, the human resources manager for a large and important company, has the ability to hire and fire with a click of a button. Specifically, a web form button. Mallory, as a practical joke, decides to stage a CSRF attack against Bob. She baits Bob with a webpage that automatically submits a form to the hire'n'fire website. The next morning, every employee finds a pink slip in his inbox. 


<h2>Why csrf-magic?</h2>
The current standard for preventing CSRF is creating a nonce that every user submits with any form he/she submits. This is reasonably effective, but incredibly tedious work; if you are hand-writing your forms or have multiple avenues for POST data to enter your application, adding CSRF protection may not seem worth the trouble.

This is where csrf-magic comes into play. csrf-magic uses PHP's output buffering capabilities to dynamically rewrite forms and scripts in your document. It will also intercept POST requests and check their token (various algorithms are used; some generate nonces, some generate user-specific tokens). This means, for a traditional website with forms, you can drop csrf-magic into your application and forget about it! 


<h2>Changelog</h2>

2014-01-28	Edward Z. Yang  Hardened against multibyte bypass attacks 
2013-09-17 	Edward Z. Yang	BSD license the project.master
2013-07-17 	Edward Z. Yang	Release 1.0.4v1.0.4
2013-07-17 	Edward Z. Yang	Add 'Try again' support for default splash page.
2013-07-17 	Edward Z. Yang	Fix bug grabbing wrong secret, thanks sparticvs for...
2013-07-17 	Edward Z. Yang	JavaScript updates: new libraries, load all libraries.
2013-07-17 	Edward Z. Yang	Properly do IE match (I can't believe this was broken).
2012-01-31 	Edward Z. Yang	Release 1.0.3v1.0.3
2012-01-31 	Edward Z. Yang	Don't clobber the secret global, use the right variable...
2009-03-19 	Edward Z. Yang	Fix IE8 bug with JavaScript.
2009-03-08 	Edward Z. Yang	Release 1.0.2.v1.0.2
2009-03-08 	Edward Z. Yang	Fix broken secret-detection algorithm, making anonymous...
2008-11-02 	Edward Z. Yang	Release 1.0.1.v1.0.1
2008-10-22 	Edward Z. Yang	Fix bug in CsrfMagic.send() function, resulting in... 
2008-09-02 	Edward Z. Yang	Disable frame-breaker on JS tests; upgrade YUI to versi... 
2008-08-07 	Edward Z. Yang	Defend against CSS iframe overlay attacks using a frame...
2008-08-07 	Edward Z. Yang	Add a two hour expiration on all tokens. 
