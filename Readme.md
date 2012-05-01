# Researcher Publication application

## ID attribute values  

`menudiv` Applied to a div tag. Contains the list of the main pages in the application; the navigation menu.  

`author` Applied to a div tag. Representation for a single researcher. 

`listpublications` Applied to a div tag. List of all publications - in the system, for a search or filter, or for a given researcher. 

`publication` Applied to a div tag. Representation for a single publication. 

`listresearchers` Applied to a div tag. List of all researchers in the system.


## Rel attribute values  

1. `homepage` Applied to an A tag. A reference to the application homepage/starting URI.  

1. `all researchers` Applied to an A tag. Used on links for the list-researchers page which points to all researchers resource.

1. `all publications` Applied to an A tag. Used on links for the list-researchers page which points to all publications resource.

1. `researcher` Applied to an A tag. Used on links that point to an individual researcher resource.

1. `publication` Applied to an A tag. Used on links that point to an individual publication resource.



## Class attribute values

1. `menu` Applied to a ul element. List of the top menu items. 

1. `main` Applied to a div element. Main content on a page, beneath the menu. 
Could be a list of publications or researchers, or an individual researcher or publication information. 

1. `researcher` Applied to a div tag. Representation for a researcher. content div on a page  

1. `control` Applied to a div tag. Contains a form and its elements, used to add or edit researcher or publication data. 

1. `control` Applied to a div tag. Contains a form and its elements.

1. `respic` Applied to a div tag. Contains the photo of a researcher when viewing a researcher representation. 

1. `resinfo` Applied to a div tag. Contains the information for a researcher when viewing a researcher representation.

## Name attribute values

1. `addpublication` Applied to a form element. Uses POST (method="post" action="/publications/) to add a publication for a researcher. 

1. `updatepublication` Applied to a form element. Uses POST (method="post" action="/publications/<%=item._id%>">) to update a publication resource. 
Will actually use PUT since it has a hidden input with method="put".

1. `searchpub` Applied to a form element. Uses GET (method="get" action="/publications/") to display publication information.

1. `item[title]` Applied to input[text] element. The title of a publication. 

1. `item[bio]` Applied to a textarea tag. The biography of a researcher. 

1. `item[image]` Applied to an input[text]. The URL of the researcher's image.

1. `item[field]` Applied to an input[text] element. The field of study for the researcher.

1. `item[articleID]` Applied to input[text] tag. The ID of the publication.

1. `item[journal]` Applied to input[text] tag. The journal that published the article. 

1. `item[pubdate]` Applied to input[text] tag. The date the article was publised.

1. `item[abstract]` Applied to textarea tag. The abstract of the publication/article.

1. `item[researcher]` Applied to input[text] or input[hidden] element. The ID of a researcher. 

1. `item[]` Applied to input[text] or input[hidden] element. The ID of a researcher.


    ```javascript
    var USER_OR_GROUP_NAME = ''; // TODO: Insert GitHub username or group name.
    ```

1. The [`views`](https://github.com/sils-webinfo/election/tree/master/views) directory contains all the EJS ([Embedded JavaScript](http://embeddedjs.com/)) templates for the service. You will need to create new templates suitable for your application, using these examples as models. The templates should include the metadata describing your application flow and data.

1. Finally, you need to edit [`package.json`](https://github.com/sils-webinfo/election/blob/master/package.json) and change the value of the `name` property to whatever you named your project.



Running your app in Cloud9 and looking at the console output should help you troubleshoot basic problems. You can add logging messages to `app.js` like this:

```javascript
console.log("Calculating grobble vectors…");
```

Then you when you run your app in Cloud9, you should see the text `Calculating grobble vectors…` in your console when that code is executed. Adding lots of console logging messages like this can help you understand when various parts of the program are running. You can also print out variables to see what their values are:

```javascript
// Get the item ID from the URI.
var item_id = req.params.id;
console.log("the item id is: ", item_id);
```

You may also want to verify that data is being created and updated in your database correctly. You can do this by going to [the admin tools for our shared database server](http://sils-webinfo.iriscouch.com/_utils/). Find your database in the list (it is named whatever you set `USER_OR_GROUP_NAME` to in `app.js`), and click it. You should see a list of all the "documents" (objects) in your database. Clicking on a document ID will show its details (properties and values).

## Deploying to Heroku

When you've got your app running how you want it, and you're ready to turn things in, it's time to deploy to [Heroku](http://www.heroku.com/). Heroku is a free (for us) cloud hosting platform. It will enable your app to run longer than it can in the Cloud9 debugger.

First, [sign up](https://api.heroku.com/signup) for Heroku. Then, follow [these instructions](http://support.cloud9ide.com/entries/20710298-deploy-your-application-to-heroku) to deploy your app. Don't worry about the `package.json` and `Procfile` files: those already exist, and you shouldn't have to change them except to change the project name in `package.json` (see above).

