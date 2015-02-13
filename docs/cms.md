The Content Management Application
==================================

This replaces the traditional server-side work done by a developer. Instead of writing custom models (linked to database tables), controllers or routers to control flow, and views to replace some or all of your built site, you construct a hierarchy of things with simple forms. This all sounds very conceptual, but you'll immediately recognize these 'things' as concepts you're familiar with.

The hierarchy goes as follows...

    site
      |__sections
              |__items
                    |__feilds
                          |__validators
                          |
                          |__values

When you start a new project you'd want to start by creating a "site". This acts as the root level entity of your website.

All the content managed bits of the site are "sections", for example "News", "People", or "Work".

Each of these sections has items, which the user creates. A "News" section with have many stories in it. A "People" section will have many profiles. A "Work" section will have many projects.

In order for your users to create items, you need to define what fields the items have. For a "People" section you might want your user to upload a photo of the person and write a brief bio, so you choose an image upload field and textarea field.

Then you might want to make sure the user fills in these fields, so you add validators. Finally, when your user fills in the resulting form, this creates values. It's these values that ultimately get sent to your site.

A site also has users. You are one of these, and you're the only person with admin rights on your sites. When a user logs in (this would be your client), they'll only be aware of the following hierarchy...

    sections
        |__items

When the user logs in they'll see a list of the sections you've created for them, and they'll be able to add, edit and delete items in those sections. They won't be able to configure fields or validators, or add new sites, sections or users. You can add as many users as you like.

You can add as many fields and validators as you see fit, but in practice it makes sense to keep things simple - there's few things more intimidating to a user than dozens of fields that they're required to fill out.

You can add fields for any purpose. A news section might have a category field that you'd like to filter stories by. The filtering would be done in the front end (we'll get to that), but you'd want your user to choose from a list of categories, so you'd add a select field and define the categories. You'd probably then want to make this field required so you'd add a validator to ensure this.

Once you've built out your content managed sections for your site in the app you can start integrating your HTML files.

- [Integration](integration/)
