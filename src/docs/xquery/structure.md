<br/>
The application structure follows [eXist application conventions] (http://exist-db.org/exist/apps/doc/development-starter.xml).

The `default components` included are:

* a standardized packaging format (.xar), allowing deployment into any eXist-db instance
* Integration with the XQuery IDE, eXide
* an HTML templating framework for the clean separation of HTML page content and application logic
* Deployment of RESTful services based on XQuery code annotations (RESTXQ)

The Blumenbach TEI Datenbank also includes these `custom components`:

* the capability to transform XML data from Orbeon XForms and publish it as TEI
* a Markdown documentation generator based on the [Atomic Wiki] (http://exist-db.org/exist/apps/wiki/Welcome)
* a [Lucene-based] (http://exist-db.org/exist/apps/doc/lucene.xml) search engine
 
 <br/>
 #### **Directories**

`/data/`

* Contains only XML and TEI data.
 
    * Includes subcollections:
        * `/data/br` for the Briefregesten 
        * `/data/werke` for the Bibliographie 
        * `/data/taxons` for the Taxon Registry 
        * `/data/ck-source` for the original HTML Bibliographie back-reference 
        * `/data/publish` for transformed XForm data

`/docs/`

* Contains atoms and markdown files for the documentation wiki.

`/modules/`

* Contains XQuery modules. 

`/pages/`

* Contains HTML pages and the XML descriptors for them.

`/resources/`

* Secondary resources (CSS files, fonts, images and JavaScript).

`/styles/`

* XSL Stylesheets used by different transformations.

`/templates/`

* Page templates containing all the repeating parts of the site's HTML layout, i.e. all the stuff which applies to every HTML view of the application.

`/utils/`

* XQuery utilities for bulk data changes (primarily using [XUpdate] (http://exist-db.org/exist/apps/doc/update_ext.xml)).

`/xqdocs/`

* Contains the automatically generated [XQDoc] (http://xqdoc.org/) documentation for the XQuery modules.

<br/>
#### **Root Files**
`build.xml` : The build descriptor for build deployment

`collection.xconf` : A template file for the index configuration that should apply to this application. This file will be copied into the correct system collection when the application is installed, thereby automatically indexing any data that is installed.

`configuration.xml` : A base configuration file

`controller.xql` : The URL rewriting controller which handles the URL space of the application.

`error-page.html` : an error dump page

`expath-pkg.xml` and `repo.xml` : These are the package descriptor files for the application. 

`icon.png` : The application icon that appears in the eXist dashboard.

`pre-install.xql` and `post-install.xql` : An XQuery script which will be run by the package manager before and after installing the app. 

`restxq.registry` : Contains function definitions for the restxq.xql module.  This file **must be** edited manually if new functions are added to the restxq module.

Next: [XQuery Modules](modules)