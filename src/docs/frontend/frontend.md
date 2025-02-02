The Blumenbach TEI Datenbank leverages the power of Javascript and CSS in the user interface.

#### **Resources**
The `/resources` directory contains 4 subdirectories:

* `/css` : contains a variety of CSS including [bootstrap-3.0.3.min.css](http://getbootstrap.com/)
* `/fonts` : contains supplementary fonts
* `/images` : contains images
* `/scripts` : contains Javascript including [jquery-1.11.2.min.js](https://jquery.com/) and [jquery.dataTables.min.js](https://www.datatables.net/)

The consistency of the UI on different platforms, including mobile, is a result of [Bootstrap](http://getbootstrap.com/)


### Javascript

#### **DataTables**

A useful feature of the UI is the sortable, filterable and paginated tables.  This is provided by the DataTable JS Library.

* Different table views have a separate JS file, e.g. `/resources/scripts/refs.js` that may specify unique table configurations:

```javascript
$(document).ready(function() {
    $('#refs').DataTable({
            "order": [[ 0, "asc" ]],
            "iDisplayLength": 100,             
            "sDom": '<"top"flip>rt<"bottom"p><"clear">',             
            "columnDefs": [
                { "iDataSort": 0, "sDefaultContent": "-", "targets": [ 0 ] },
                { "iDataSort": 1, "sDefaultContent": "-", "targets": [ 1 ] },
                { "iDataSort": 2, "sDefaultContent": "-", "targets": [ 2 ] },
                { "iDataSort": 3, "sDefaultContent": "-", "targets": [ 3 ] },
                { "iDataSort": 4, "sDefaultContent": "-", "targets": [ 4 ] },                 
            ]        
     });
} );
```

This configuration specifies **order by** (the first column), **number of results per page** (100), and **toolbar position** (top and bottom)

#### **Ace Code Highlighting**

The code syntax highlighting in the documentation is done with the [Ace](http://ace.c9.io/#nav=about) library

#### **Fancy Tree**

The [Inhaltsverzeichnis](/apps/blumenbach/inhalt-tree.html) is done with the [jquery.fancytree](https://github.com/mar10/fancytree/wiki) library

### CSS and Fonts

#### Font Libraries

* [Glyphicons](http://glyphicons.com/)
* [Font Awesome](http://fortawesome.github.io/Font-Awesome/)

#### CSS

* The primary local CSS files:

    * [style.css](/apps/blumenbach/resources/css/style.css) : Contains most local styles for the [Data Views](../xquery/views)
    * [br-stylesheet.css](/apps/blumenbach/resources/css/br-stylesheet.css) : Contains styles from [Blumenbach Online](http://www.blumenbach-online.de/) for Briefe Präsentation.
    * [br-stylesheet.css](/apps/blumenbach/resources/css/werke-stylesheet.css) : Contains styles from [Blumenbach Online](http://www.blumenbach-online.de/) for Werke Präsentation.
    * [docs.css](/apps/blumenbach/resources/css/docs.css) : Contains styles for the Wiki documentation
    * [fundocs.css](/apps/blumenbach/resources/css/fundocs.css) : Contains styles for the XQuery documentation    
    
* Library CSS files:

    * [bootstrap-3.0.3.min.css](/apps/blumenbach/resources/css/bootstrap-3.0.3.min.css) : Contains Bootstrap styles
    * [dataTables.css](/apps/blumenbach/resources/css/bootstrap-3.0.3.min.css) : Contains DataTables styles
    * [ui.fancytree.min.css](/apps/blumenbach/resources/css/bootstrap-3.0.3.min.css) : Contains FancyTree styles               
    
    