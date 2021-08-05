# Didomi custom template for Google Tag Manager
GTM template for Didomi

This template integrates with GTM Consent APIs to allow consent mode and settings in Tag Manager. It is part of the Tag Manager Community Template Gallery.

## Didomi clients
To better understand how to setup and enable GTM within Didomi's SDK, please refer to https://developers.didomi.io/cmp/web-sdk/third-parties/custom-integrations/tag-managers/google-tag-manager

In order to use this GTM template to setup the default consent values for Analytics and Ad Storage, you will still need to enable the GTM integration in Didomi's console https://developers.didomi.io/cmp/web-sdk/third-parties/custom-integrations/tag-managers/google-tag-manager#option-1-didomi-console

To setup the default values via the template (not via Didomi's console), follow the instructions below.

## Developers

The official GTM documentation regarding templates can be found here
https://developers.google.com/tag-manager/templates

### Loading the template in a test account
In order to use this GTM template (Didomi CMP), you will need to create a new tag and associate the template with at least one trigger.

#### Creating a new tag
After accessing your Google Tag Manager account and selecting a workspace (we use the Default Workspace for testing purposes),

1. Click the "New Tag" button as shown here,
<img width="556" alt="uploading_template_00" src="https://user-images.githubusercontent.com/30706016/128257772-25becf03-3933-452a-8f1d-812b27cc8fcb.png">


Or navigate to the "Tags" tab, and click on the "New" button at the top right side of the tags table.
<img width="1224" alt="uploading_template_00a" src="https://user-images.githubusercontent.com/30706016/128257780-83929c88-0006-4c0d-a111-14fb1d301670.png">


2. Use a relevant name for the new tag ("Didomi CMP" was used for this example) and hit the "Tag Configuration" card.
<img width="1201" alt="uploading_template_01" src="https://user-images.githubusercontent.com/30706016/128257793-23fb07a4-1457-4196-9aab-0121880e7d7e.png">


3. From that screen you should have access to all the templates in the Community Template Gallery, including the "Didomi CMP" one. Look for it and load it.

<img width="643" alt="uploading_template_02" src="https://user-images.githubusercontent.com/30706016/128257687-d36f0833-9814-4592-8c74-79a8ccf5ef9a.png">

At this point you should have access to the template UI - which includes two checkboxes to set the desired default status for GCM.
<img width="1201" alt="uploading_template_03" src="https://user-images.githubusercontent.com/30706016/128257853-a30bf642-1273-4e3d-bc7c-27dda7e4c891.png">


#### Associating a trigger to a tag
We want our tag to be fired on all pages. In order to achieve that,

1. Click on the "Triggering" card to choose a trigger so that the tag fires.
<img width="940" alt="associating_trigger_00" src="https://user-images.githubusercontent.com/30706016/128259753-938464b6-fe65-4b43-90c3-1dba7f754865.png">

2. Select the "All pages" trigger
<img width="1431" alt="Screen Shot 2021-08-05 at 10 28 38 AM" src="https://user-images.githubusercontent.com/30706016/128379353-3d7b3317-bc5b-47f7-bdb9-86126de740b7.png">


3. Save the tag. **Here it is where you will choose the default values for Analytics and Ad storage**
<img width="1191" alt="Screen Shot 2021-08-05 at 10 29 00 AM" src="https://user-images.githubusercontent.com/30706016/128379385-aa130f91-8ed9-4ade-a094-6bcc8fd97e4e.png">



### How to code/test it on a website

#### Previewing the tag on a website
In order to test the tag on a website, you can make use of the "Preview" feature of the GTM platform. You can find a "Preview" button at the top right of the GTM nav bar menu.
<img width="1440" alt="preview_00" src="https://user-images.githubusercontent.com/30706016/128261119-745ef7ec-fb78-4809-91fd-656a79968d85.png">
Note that for the example above, three tags are active("Analytics Demo", "Didomi CMP Test" and Google Analytics GA4 configuration") and one tag is paused("Track Consent Value")

You will be prompted the following screen where you can setup the URL of the website you can to test the tag on. We used https://sandbox.didomi.io/gtm.html for our tests. Clicking continue opens the "Tag Assistant" website.
<img width="664" alt="preview_01" src="https://user-images.githubusercontent.com/30706016/128261167-d8dc858c-5502-4583-83c3-cdd2a4d04945.png">

The tag assistant is a live tool that can help tremendously with debugging your tags and/or templates.

We can see that the tag we created is in fact being fired during the initial load of the site.
<img width="1432" alt="Screen Shot 2021-08-05 at 10 32 19 AM" src="https://user-images.githubusercontent.com/30706016/128379448-39b95cfe-8334-4715-aae3-da03badd94b8.png">


#### Submitting the tag on a website
Once the testing/previewing process has been sucessful, you can "Submit" a tag to a website so that it goes live.

In this case, click on the "Submit" button at the top right of the GTM nav bar menu.
<img width="1440" alt="preview_00" src="https://user-images.githubusercontent.com/30706016/128261879-14750697-a362-450b-bb2f-64e2f6bf8f52.png">




### How to write and run tests

Unit tests can be written and run per template. You will find a "Tests" tab in the Template Editor where you can do so.
<img width="724" alt="tests_00" src="https://user-images.githubusercontent.com/30706016/128263011-ed5c62dd-14c3-4320-bde0-61480de03196.png">

A sucessfully ran test-suite looks like this
<img width="730" alt="tests_01" src="https://user-images.githubusercontent.com/30706016/128263049-d9198a1b-785f-4f85-af8a-69a435c49787.png">

You can follow this documentation to better understand unit testing for templates https://developers.google.com/tag-manager/templates/tests

And these are the Test APIs that work with GTM Sandboxed Javascript https://developers.google.com/tag-manager/templates/api#test_apis


### Editing this template

#### Uploading a template.tpl file
If you need to load a `template.tpl` of this repo into GTM,

1. Get a copy of this repo on your local environment.

2. Go to the "Templates" tab and click on "New"
<img width="1238" alt="Screen Shot 2021-08-05 at 10 55 14 AM" src="https://user-images.githubusercontent.com/30706016/128381918-4ebd865a-82a2-49f2-9ffb-5f9d244ef17b.png">

3. At the top right of the template editor menu, choose "Import"
<img width="1437" alt="Screen Shot 2021-08-05 at 10 58 11 AM" src="https://user-images.githubusercontent.com/30706016/128382288-4a2f8865-4c72-40c5-8ab2-8e721e2a1435.png">

4. Navigate to the `template.tpl` file in your local environment. Click "save" and then "continue".
<img width="496" alt="Screen Shot 2021-08-05 at 10 50 15 AM" src="https://user-images.githubusercontent.com/30706016/128382153-bff24851-de3d-4d01-8ee1-f2c9f4975cd0.png">
<img width="435" alt="Screen Shot 2021-08-05 at 10 50 22 AM" src="https://user-images.githubusercontent.com/30706016/128382162-fcf2674b-e126-4a38-974c-b3371ef5b4fd.png">

The template should load correctly,
<img width="1434" alt="Screen Shot 2021-08-05 at 10 57 58 AM" src="https://user-images.githubusercontent.com/30706016/128382357-33b69508-2290-4c16-a406-988adf5b7e36.png">



#### Updating metadata.yaml

Everytime the `template.tpl` is updated and you would want the Community Template Gallery version to reflect those changes, the `medatada.yaml` file should also be updated. The `sha` value must reference the specific template.tpl file that you want to publish. Don't forget to update this value correctly with every new version!

See https://developers.google.com/tag-manager/templates/gallery#metadatayaml

