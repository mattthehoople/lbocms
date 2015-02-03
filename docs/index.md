Lbocms
========

Using Lbocms couldn't be easy.

Basic workflow
--------------

- Sign Up
- Create a site in your dashboard
- Add a section to your new site
- Add fields to the section.
- Add validators to your fields.
- Start adding items to your section for testing purposes.
- Build your site in nice flat html, javascript and html, just as you always would do.
- Download and install the Lbocms jquery plugin.
- Download ICanHaz.js and install it.
- Create templates from your html files.
- Add onDocumentReady code block defining your lbocms sections and, if required, pages.
- Add users to the site so your clients can edit their pages.
- Pay up.
- Put your site live.

Additional optional steps for uploaded content
----------------------------------------------

- Sign up for amazon web services
- Sign up for s3.
- Add a bucket.
- Configure the bucket to server content publicly.
- Create a user with access rights to your new bucket.
- Add details of the user and bucket to your Lbocms account.
- Start using file and image upload fields in your sites.
- Pay amazon for hosting when your tiny bill arrives.


Create ICanHaz Templates
------------------------

For example...

    <script id="listItemTemplate" type="text/html">
      <li>list item <a href="{{lbolink}}">{{ name }}</a></li>
    </script>
    <script id="itemTemplate" type="text/html">
      <h2>{{ name }}</h2>
      <p>{{{Body}}}</p>
    </script>

Add onDocumentReady to your page
--------------------------------

For Example...

    <script type="text/javascript">
      $(document).ready( function(){
        $('#item').lbocms({
              'method' 	: 'item',
              'id'		: '1',
              'key'		: '4c75f41cd9344df65d5cf6c1a691d7c7'
            });
        $('#items').lbocms({
              'method' : 'items',
              'page'  : 'page.html',
              'id'		: '1',
              'key'		: '4c75f41cd9344df65d5cf6c1a691d7c7'
            });
      });
    </script>

Support
-------

How to get help with your Lbocms site.

Pay someone else to do all this for you
---------------------------------------

It's kind of aganist the point, but if you want to, you can.
