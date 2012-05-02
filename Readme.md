# Researcher Publication application

## ID attribute values  

1. `menudiv` Applied to a div tag. Contains the list of the main pages in the application; the navigation menu.  

1. `author` Applied to a div tag. Representation for a single researcher. 

1. `listpublications` Applied to a div tag. List of all publications - in the system, for a search or filter, or for a given researcher. 

1. `publication` Applied to a div tag. Representation for a single publication. 

1. `listresearchers` Applied to a div tag. List of all researchers in the system.


## Rel attribute values  

1. `homepage` Applied to an A tag. A reference to the application homepage/starting URI.  

1. `all researchers` Applied to an A tag. Used on links for the list-researchers page which points to all researchers resource.

1. `all publications` Applied to an A tag. Used on links for the list-researchers page which points to all publications resource.

1. `researcher` Applied to an A tag. Used on links that point to an individual researcher resource.

1. `publication` Applied to an A tag. Used on links that point to an individual publication resource.


## Class attribute values

1. `menu` Applied to a ul element. List of the top menu items. Inlcudes style for UL and LI elements in the list. 

1. `main` Applied to a div element. Main content on a page, beneath the menu. 
Could be a list of publications or researchers, or an individual researcher or publication information. 

1. `respic` Applied to a div tag. Contains the photo of a researcher when viewing a researcher representation. 

1. `resinfo` Applied to a div tag. Contains the information for a researcher when viewing a researcher representation.

1. `leftdiv` Applied to a div tag. Left div in a publication representation. Contians the researcher, journal and publication date. 

1. `abstract` Applied to a div tag. Contains the abstract for a publication.

1. `control` Applied to a div tag. Contains a form and its elements. Used on multiple pages with form to add, update or get a resource. 


## Name attribute values

1. `addpublication` Applied to a form element. Uses POST (method="post" action="/publications/) to add a publication for a researcher. 

1. `updatepublication` Applied to a form element. Uses POST (method="post" action="/publications/<%=item._id%>">) to update a publication resource. 
Will actually use PUT since it has a hidden input with method="put".

1. `addresearcher` Applied to a form element. Uses POST and PUT to add and update a researhcer resource. 

1. `searchpub` Applied to a form element. Uses GET (method="get" action="/publications/") to display publication information.

1. `item[id]` Applied to input[text] element. The ID for a researcher. 

1. `item[name]` Applied to input[text] element. The name of the researcher. 

1. `item[bio]` Applied to a textarea element. The biography of a researcher. 

1. `item[image]` Applied to an input[text] element. The URL of the researcher's image.

1. `item[field]` Applied to an input[text] element. The field of study for the researcher.

1. `item[articleID]` Applied to input[text] element. The ID of the publication.

1. `item[title]` Applied to input[text] element. The title of a publication.

1. `item[journal]` Applied to input[text] element. The journal that published the article. 

1. `item[pubdate]` Applied to input[text] element. The date the article was publised.

1. `item[abstract]` Applied to textarea element. The abstract of the publication/article.

1. `item[researcher]` Applied to input[text] or input[hidden] element, ID of a researcher. Also applied to a select element, 
researcher name for editing a publication. 


## Deploying to Heroku

When you've got your app running how you want it, and you're ready to turn things in, it's time to deploy to [Heroku](http://www.heroku.com/). Heroku is a free (for us) cloud hosting platform. It will enable your app to run longer than it can in the Cloud9 debugger.

First, [sign up](https://api.heroku.com/signup) for Heroku. Then, follow [these instructions](http://support.cloud9ide.com/entries/20710298-deploy-your-application-to-heroku) to deploy your app. Don't worry about the `package.json` and `Procfile` files: those already exist, and you shouldn't have to change them except to change the project name in `package.json` (see above).

