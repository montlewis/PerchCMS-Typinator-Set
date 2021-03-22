![PERCH CMS EXPANSIONS](https://www.lewisarts.com/perchset/birdsofafeather2.gif)

# PerchCMS-Typinator-Set
Expansions for Perch CMS using Typinator 7+.
# Typinator
Requires Typinator 7. Typinator is an incredible text expansion tool and I can't recommend it more highly. It is Mac only, so sorry everyone else. Version 7 greatly enhanced the dialogs and enables for really powerful expansions. Take a look, I think you will really like how Typinator and this expansion set enhance your Perch development.

You can get it here:
<http://www.ergonis.com/downloads/>
# 8/6/20 Update
Corrects the closing brackets for `perch_layout` when there are no arguments.
# 4/13/20 Update
Adds support for Pipit Phone Template Filter(https://grabapipit.com/pipits/template-filters/phone), Tim Kinali's Swatches (https://bitbucket.org/tamburlane/perch-fieldtype-swatches/src/master/) and Calendar (https://bitbucket.org/tamburlane/perch-fieldtype-calendar/src/master/) fieldtypes, and Cognetif's PageSelect (https://gitlab.com/cognetif-os/perch-dev/cognetif_pageselect) fieldtype.

# 3/26/20 Update
Added several new expansions: `perch_shop_products`, `perch_shop_product`, `perch_shop_brands`, and `perch_shop_brand`. Fixed a bug with `return-html` value on data return expansions. Added `editor-config` to `textarea` expansion. Added `no-index` option to all template-level field expansions. Added `mailchimp`, `email`, `sharing`, and `categories` to all template-level expansions. Added `pagination` and `navigation` values to `perch:if` expansions. The `ps\` expansion now seaches the perch documentation sites as well as the old and new forums. Assorted other enhancements.

# 6/14/18 Update
With today's revision to the expansion set, Perch's new templating tag formatting introduced in version 3.1 is now supported. Select Perch version 3.1:

![PERCH 3.1 Templating Support](https://www.lewisarts.com/perch31version.png)


The tag will now be formatted like this with boolean values and without the XHTML-style `/>` closing:

`<perch:content id="partner_name" type="text" label="Partner Name" format="UC" required html size="m" suppress title >`

The expansion set still supports the older format as well. Just select an older version number from the dropdopwn menu. Just like the App Space selection, the version selection is remembered between sessions.



# Setting it up
Once you have Typinator installed, you can use its new subscribe function to connect to this set of Perch expansions.
Under the Action menu, select Sets, and then select Subscribe to Set via URL...
In the window that pops up, enter this address:

  <https://github.com/montlewis/PerchCMS-Typinator-Set/raw/master/PerchCMS.typubset>

So now the Perch expansion set should be in the sets panel of the Typinator application and you should be able to start using them!
You can set which applications your expansion sets are active in. This is done with the little application icon under the list of sets.

So let's take a look at the exansions! **(Note: when you type an expansion, case doesn't matter. It's just added here for clarity)**

# How it works
So I tried to set up the expansions in a logical way so that learning them is as easy as possible. For working in **templates**, no matter which perch application you're in, you enter an abbreviations that begins with **`pt`**, as in Perch Template, followed by the field type or code you would like, followed by a trailing `\`. So the Abreviation `ptsmarttext\` will present a dialog that looks like this:

![SMARTTEXT](https://www.lewisarts.com/perchset/perch_smarttext.png)

First, you set the `appspace`. In this case, it's `Content` to create a `perch:content` tag. The `appspace` selection is remembered through all the template dialogs until you change it, so you only need to worry about it when you change appspaces. Then you fill out the dialog box with the variables and setting you would like. When you hit ok, this is delivered to your editor:

`<perch:content id="subheadtext" type="smarttext" label="Subhead Text" size="m" />`

It only outputs the fields you specify but still shows you all the options that are available to you. So this expansion:

![SMARTTEXT](https://www.lewisarts.com/perchset/perch_smarttext2.png)

will output:

`<perch:content id="subheadtext" type="smarttext" label="Subhead Text" required="true" size="xl" title="true" order="4" suppress="true" divider-before="Event Details" title="true" help="This title will appear in the capsule summary. " />`

# If you ever get lost
`pHelp\`
If you ever get lost, typing `pHelp\` will open Typinator's Quick Search window:


![SMARTTEXT](https://www.lewisarts.com/perchset/quicksearch.png)

Typing some text (like 'template', shown above) will show the expansions available involving templates... Then just click on the one you would like to open the expansion.

# Why I Love it
**The expansion set is designed to be smart.** For example, if you create a field on a template using one of the `ptFieldType\` expansions, and then do a `ptIf\` expansion:

![Perch If](https://www.lewisarts.com/perchset/perch_if_smarttext.png)

It inserts the field ID for the field you last created in case that's what you wanted. so hiting enter delivers:

`<perch:if exists="subheadtext">`

By the way, some of the expansions, like the `Perch:If` tag above, create just the opening tag. So to close the tag later, you would put the backslash first, like this: `\ptif`. Perch:before `ptb\` `\ptb`, perch:after `pta\` `\pta`, pearch:repeater `ptr\` `\ptr` and some others work that way as well.

The `\ptif` expansion is really powerful, here's a list of what's available in the `perch:if` Special IDs dropdown:

![Perch If Special IDs](https://www.lewisarts.com/perchset/if_options.png)

Here's an example of an expansion that creates a `perch_content_custom` block:

![SMARTTEXT](https://www.lewisarts.com/perchset/perch_content_custom.png)

With the `Align Assignment Operators` set to `Aligned Operators` You will get this delivered to your editor:
~~~~
<?php
  perch_content_custom('Birds', array(
     'page'          => '/birds.php',
     'template'      => '/birds/roosts.html',
     'filter'        => 'feathered',
     'match'         => 'eq',
     'value'         => 'true',
     'skip-template' => 'true',
  ));
?>
~~~~
If you prefer `Non-Aligned Operators` (`=>`) output:
~~~~
<?php
  perch_content_custom('Birds', array(
     'page'=>'/birds.php',
     'template'=>'/birds/roosts.html',
     'filter'=>'feathered',
     'match'=>'eq',
     'value'=>'true',
     'skip-template'=>'true',
  ));
?>`
~~~~
or if you prefer `Single-line` output:
~~~~
<?php perch_content_custom('Birds', array('page'=>'/birds.php', 'template'=>'/birds/roosts.html', 'filter'=>'feathered', 'match' =>'eq', 'value'=>'true', 'skip-template'=>'true',));?>


~~~~

_**So only the field values that you specify are output to the editor**_ as the code block is created based on your input.


## Function Guides
Another type of expansion provides a guide to Perch's attributes and functions for a particular app space or special field types. For example, here is the expansion `psFunctions\` that presents the following:

![SHOP FUNCTIONS](https://www.lewisarts.com/perchset/shop_functions.png)

In the case of these expansions, it will drop an example function into your editor and optionally take you to that function’s page in the Perch Documentation.

The options here are:

![SSOP FUNCTIONS LIST](https://www.lewisarts.com/perchset/shop_function_list.png)

So, selecting `perch_shop_brands()` will output:

`<?php perch_shop_brands(); ?>` to your editor and if the `Open Perch Docs: Shop Functions` is checked, **it will open a Safari window to that function’s page in the Perch Documentation**.



# Hope you love it, too
This is a work in progress. It's not a complete set of expansion, but it's pretty vast. If you use the subscribe function, I think that you will be updated anytime I make changes to the set on GitHub.

If you find this useful, let me know. If there's a way to make it better, I’d love to hear that as well. Not sure what the best way to collaborate on something like this is, but we'll figure it out. Happy Perching!

# Here's the list of expansions by group:
## Perch Templating

|Abbreviation   | Expands to 
|:----------	| -----------
| **appspace**\       | Set the Perch App Space and Perch version number                                                                                                    | 
| pt**Block**\        | Creates a Perch Block within the Perch Blocks Framework                                                                     | 
| pt**Blocks**\       | Creates a Perch Blocks Framework                                                                                            | 
| pt**Calendar**\     | Creates a calendar fieldtype that supports multiple dates. Requires [Tim Kinali’s Calendar fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-calendar/src/master/ "Calendar fieldtype").
| pt**Checkbox**\     | Creates a checkbox type field on your template                                                                              | 
| pt**Com**\          | Begin a Perch Comment Section (<\!--*)                                                                                              | 
| pt**Comment**\      | Adds a Perch comment line \(\<\!\-\-\*  \*\-\-\>)                                                                                                   | 
| pt**Composite**\    | Creates a composite field of other field values                                                                             | 
| pt**Dataselect**\   | Creates a dataselect type field in your template                                                                            | 
| pt**Date**\         | Creates a date type field in your template                                                                                  | 
| pt**Else**\         | Creates a Perch else tag in your template                                                                                   | 
| pt**Group**\        | Creates an opening Perch group tag in your template. (Perch 3.1 beta feature)                                                                                   | 
| p**Template**\      | Creates a Perch Template Call. This can be used in templates to call in other templates.                                    | 
| pt**EventsTags**\   | List of all Perch Event IDs                                                                                                 | 
| pt**FA**\           | Creates a Creates a Font Awesome field in your template. Requires [Pipit Font Awesome App](https://grabapipit.com/pipits/apps/font-awesome "Pipits Font Awesome App").       | 
| pt**File**\         | Creates a file field in your template                                                                                       | 
| pt**Hidden**\       | Use this to add Perch special field ids                                                                                     | 
| pt**If**\           | Creates the opening \<perch:if> conditional tag                                                                              | 
| pt**Image**\        | Creates an image type field in your template                                                                                | 
| pt**Includes**\     | Use to include one template in another                                                                                      | 
| pt**LayoutVar**\    | Use to output a layout variable using perch\_layout\_var. Optionally wrap in a conditional if perch\_layout\_has                | 
| pt**Link**          | Creates a Link type field in your template. Requires an non-standard custom fieldftype                                      | 
| pt**Map**\          | Creates a map type field in your template                                                                                   | 
| pt**NavTags**\      | List of all Perch Navigation IDs                                                                                            | 
| pt**Noresults**\    | Adds \<perch:noresults>\</perch:noresults> to your template to display something different when there are no results returned | 
| pt**Number**\       | Creates a number type field in your template                                                                                | 
| pt**Options**\      | Use this to add admin field tags to your template items                                                                     | 
| pt**Pagelist**\     | Creates a pagelist field in your template. Requires optional pagelist fieldtype                                             | 
| pt**PageSelect**\   | Creates a pageselect field in your template. Requires optional [Cognetif Page Select](https://gitlab.com/cognetif-os/perch-dev/cognetif_pageselect "Page Select fieldtype") fieldtype.
| pt**Period**\       | Creates a period type field in your template                                                                                | 
| pt**Phone**\        | Creates a formatted phone number field in your template. Requires optional Pipit phone template filter [Pipit Phone Template Filter](https://grabapipit.com/pipits/template-filters/phone "Pipit Phone Template Filter").                                                                                | 
| pt**Radio**\        | Creates a radio type field in your template                                                                                 | 
| pt**Select**\       | Creates a select type field in your template                                                                                | 
| pt**Slug**\         | Creates a slug field for an id                                                                                              | 
| pt**Smarttext**\    | Creates a smarttext field in your template                                                                                  | 
| pt**Swatches**\     | Creates a swatches fieldtype that supports multiple dates. Requires [Tim Kinali’s Swatches fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-swatches/src/master/ "Swatches fieldtype").
| pt**Table**\         | Creates a table field in your template. (Requires optional [optional fieldtype](https://github.com/siansell/perch-cms-fieldtype-table "Table Fieldtype") by Simon Ansell)                                                                                       | 
| pt**Text**\         | Creates a text field in your template                                                                                       | 
| pt**Textarea**\     | Creates a a multi-line block of text in your template                                                                       | 
| pt**Time**\         | Creates a time only field on your template                                                                                  | 
| ptTimestamp\    | Creates a timestamp field in your template (requires [optional fieldtype](https://github.com/montlewis/perch-cms-fieldtype-timestamp "Timestamp fieldtype") by Monty Lewis)                                     | 
| pt**Vimeo**\        | Creates an Vimeo type field in your template. Requires Vimeo fieldtype                                                      | 
| pt**Youtube**\      | Creates an YouTube type field in your template. Requires YouTube fieldtype                                                  | 
| **reset**\          | Resets Typinator's variables for the Perch Expansion Set                                                                    | 
| **suppress**\       | Adds the suppress tag for fields                                                                                            | 

## Blog Expansions
|Abbreviation   | Expands to 
|:----------	| -----------
| pb**Custom**\       | Creates a Perch Blog Custom block                                                                                           | 
| pb**Functions**\    | List of all the Perch Blog functions details.                                                                               | 
| pb**URL**\          | Creates a perch:blog URL Tag                                                                                                | 

## Content Expansions
|Abbreviation   | Expands to 
|:----------	| -----------
| pc**Create**\       | Creates a perch\_content\_create block                                                                                        | 
| pc**Custom**\       | Create a perch\_content\_custom block                                                                                         | 
| pc**Collection**\       | Create a perch\_collection block                                                                                         | 
| pc**Functions**\    | A guide to the Perch Content Functions and Documentation                                                                    | 
| pc**Get**\          | Outputs a perch\_content call                                                                                                | 

## Navigation Expansions
|Abreviation   | Expands to 
|:----------	| -----------
| pn**Functions**\    | A guide to the Perch Navigation Functions and Documentation                                                                 | 
| pp**Atributes**\    | A guide to the Perch Page Attributes and Documentation                                                                      | 

## Shop Expansions
|Abreviation   | Expands to 
|:----------	| -----------
| ps**Product**\      | Use to make a call to `perch_shop_product` function with optional value pairs                                                       | 
| ps**Products**\     | Use to make a call to `perch_shop_products` function with optional value pairs                                                                | 
| ps**Brand**\     | Use to make a call to `perch_shop_brand` function with optional value pairs                                                                | 
| ps**Brands**\     | Use to make a call to `perch_shop_brands` function with optional value pairs                                                                | 
| ps**Functions**\     | A guide to all the Perch Shop Functions and Documentation                                                                 | 

## Layout Expansions
|Abbreviation   | Expands to 
|:----------	| -----------
| p**Layout**\        | Use to make a call to `perch_layout` function with optional value pairs                                                       | 
| pl**Functions**\    | A guide to the Perch Layout Functions and Documentation                                                                     | 



## Third-Party App Expansions
|Abbreviation   | Expands to 
|:----------	| -----------
| pt**Calendar**\     | Creates a calendar fieldtype that supports multiple dates. Requires [Tim Kinali’s Calendar fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-calendar/src/master/ "Calendar fieldtype").
| p**FA**\        | Creates a Font Awesome call in php files. Requires [Pipit Font Awesome App](https://grabapipit.com/pipits/apps/font-awesome "Pipits Font Awesome App").                                                     | 
| pt**PageSelect**\   | Creates a pageselect field in your template. Requires optional [Cognetif Page Select](https://gitlab.com/cognetif-os/perch-dev/cognetif_pageselect "Page Select fieldtype") fieldtype.
| pt**Swatches**\     | Creates a swatches fieldtype that supports multiple dates. Requires [Tim Kinali’s Swatches fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-swatches/src/master/ "Swatches fieldtype").

![MacDown Screenshot](https://www.lewisarts.com/perchset/search_perch.png)

## Perch Site Interaction
Many of the expansion dialogs have a checkbox at the bottom that enable you to open the page for that function or tag in the Perch Documentation. There is also a built in site search (`pS\`) as shown above.

|Abbreviation   | Expands to 
|:----------	| -----------
| p**S**\             | Searches the Perch Site, Documentation, and Forum                                                                                                       | 
| p**News**\    | Opens the Grabaperch site news and current version pages                                                                     | 
| p**Account**\    | Opens your account page at Grabaperch                                                                     | 



# Complete list as of 4/13/2020

|Abbreviation   | Expands to 
|:----------	| -----------
| /pA             | Closing Perch:After                                                                                                         | 
| /pB             | Closing Perch:Before                                                                                                        | 
| /pError         | Closing Perch:Error                                                                                                         | 
| /pEvery         | Closing Perch:Every                                                                                                         | 
| /pIf            | Closing Perch:If                                                                                                            | 
| /pM             | Closing Perch:Member                                                                                                        | 
| /pNoresults     | Closing Perch:Noresults                                                                                                     | 
| /pR             | Closing Perch:Repeater                                                                                                      | 
| /ptA            | Closing Perch:After                                                                                                         | 
| /ptB            | Closing Perch:Before                                                                                                        | 
| ptCom\          | Begin a Perch Comment Section                                                                                                 | 
| /ptCom          | End a Perch Comment Section                                                                                                 | 
| /ptComment      | Creates a Perch Comment Section                                                                                                 | 
| /ptError        | Closing Perch:Error                                                                                                         | 
| /ptEvery        | Closing Perch:Every                                                                                                         | 
| /ptGroup        | Closing Perch:Group                                                                                                            | 
| /ptIf           | Closing Perch:If                                                                                                            | 
| /ptM            | Closing Perch:Member                                                                                                        | 
| /ptNoresults    | Closing Perch:Noresults                                                                                                     | 
| appspace\       | Set the Perch App Space                                                                                                     | 
| pA\             | Opening Perch:After Tag                                                                                                     | 
| pAll\           | Creates a Perch Show all tag for debugging                                                                                  | 
| pB\             | Opening Perch:Before Tag                                                                                                    | 
| pbCustom\       | Creates a Perch Blog Custom block                                                                                           | 
| pbFunctions\    | List of all the Perch Blog functions details.                                                                               | 
| pbURL\          | Creates a perch:blog URL Tag                                                                                                | 
| pCat\           | Creates a perch_category() function to display a single category when passed a category path.                               | 
| pCats\          | Creates a perch_categories() function to display a listing of your categories.                                              | 
| pcCreate\       | Creates a perch_content_create block                                                                                        | 
| pcCustom\       | Create a perch_content_custom block                                                                                         | 
| pcFunctions\    | A guide to the Perch Content Functions and Documentation                                                                    | 
| pcGet\          | Outputs a perch_content call                                                                                                | 
| pConfigBuckets\ | Adds a configuration block to the buckets config file                                                                       | 
| pConfigdebug\   | Turn on debugging in the main config file                                                                                   | 
| pCSS\           | Add a call to the for Perch's perch_get_css to a page                                                                       | 
| pDebug\         | Adds the PerchUtil debug tag to a page                                                                                      | 
| peCalendar\     | Adds a call to the Perch Events app to create a calendar                                                                    | 
| peCustom\       | Creates a perch_events_custom block                                                                                         | 
| peFunctions\    | A guide to the Perch Event Functions and Documentation                                                                      | 
| peGet\          | Creates a call for perch_event                                                                                              | 
| peListing\      | Creates a call for a perch_event listing                                                                                    | 
| pElse\          | Creates a Perch else tag in your template                                                                                   | 
| peSlug\         | Creates a tag for the Events app eventSlug                                                                                  | 
| peTitle\        | Creates a tag for the Events app eventTitle                                                                                 | 
| pEvery\         | Creates a perch:every tag                                                                                                   | 
| pFA\        | Creates a Font Awesome call in php files. Requires [Pipit Font Awesome App](https://grabapipit.com/pipits/apps/font-awesome "Pipits Font Awesome App").                                                     | 
| pfGet\          | Creates a call to perch_form function                                                                                       | 
| pget\           | Creates a perch_get tag                                                                                                     | 
| pgFunctions\    | A guide to the Perch Gallery Functions and Documentation                                                                    | 
| phelp\          | Use this to search the abreviations and expansions. Make sure Typinator quick search is set to:⌥⇧⌘"."                   | 
| pIf\            | Creates the opening \<perch:if> conditional tag                                                                              | 
| pInit\          | Creates the Initial Perch Runtime call                                                                                      | 
| pJavascript\    | Creates the perch_get_javascript call                                                                                       | 
| pLayout\        | Use to make a call to perch_layout function with optional value pairs                                                       | 
| plFunctions\    | A guide to the Perch Layout Functions and Documentation                                                                     | 
| pmFunctions\    | A guide to the Perch Member Functions and Documentation                                                                     | 
| pnFunctions\    | A guide to the Perch Navigation Functions and Documentation                                                                 | 
| ppAtributes\    | A guide to the Perch Page Attributes and Documentation                                                                      | 
| pPrefsdebug\    | Adds the PERCH_DEBUG line to the config file                                                                                | 
| pR\             | Creates an opening Perch repeater tag                                                                                       | 
| pSetVar\        | Adds a Perch:System set variable item                                                                                       | 
| psProduct\      | Use to make a call to `perch_shop_product` function with optional value pairs                                                       | 
| psProducts\     | Use to make a call to `perch_shop_products` function with optional value pairs                                                                | 
| psBrand\     | Use to make a call to `perch_shop_brand` function with optional value pairs                                                                | 
| psBrands\     | Use to make a call to `perch_shop_brands` function with optional value pairs                                                                | 
| psFunctions\    | A guide to the Perch Shop Functions and Documentation                                                                       | 
| pShowall\       | Adds the Perch Show All tag to temaplate for debugging                                                                      | 
| ptA\            | Opening Perch:After Tag                                                                                                     | 
| ptAll\          | Creates a Perch Show all tag for debugging                                                                                  | 
| ptBlock\        | Creates a Perch Block within the Perch Blocks Framework                                                                     | 
| ptBlocks\       | Creates a Perch Blocks Framework                                                                                            | 
| ptBlogTags\     | List of all Perch Blog IDs                                                                                                  | 
| ptCalendar\     | Creates a calendar fieldtype that supports multiple dates. Requires [Tim Kinali’s Calendar fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-calendar/src/master/ "Calendar fieldtype").|
| ptCheckbox\     | Creates a checkbox type field on your template                                                                              | 
| ptCom\          | Begin a Perch Comment Section                                                                                               | 
| ptComment\      | Adds a Perch comment line                                                                                                   | 
| ptComposite\    | Creates a composite field of other field values                                                                             | 
| ptDataselect\   | Creates a dataselect type field in your template                                                                            | 
| ptDate\         | Creates a date type field in your template                                                                                  | 
| ptElse\         | Creates a Perch else tag in your template                                                                                   | 
| ptFA\           | Creates a Creates a Font Awesome field in your template. Requires [Pipit Font Awesome App](https://grabapipit.com/pipits/apps/font-awesome "Pipits Font Awesome App").|
| pTemplate\      | Creates a Perch Template Call. This can be used in templates to call in other templates.                                    | 
| ptEventsTags\   | List of all Perch Event IDs                                                                                                 | 
| ptFile\         | Creates a file field in your template                                                                                       | 
| ptGroup\        | Creates an opening Perch group tag in your template. (Perch 3.1 beta feature)                                                                                   | 
| ptHidden\       | Use this to add Perch special field ids                                                                                     | 
| ptIf\           | Creates the opening \<perch:if> conditional tag                                                                              | 
| ptImage\        | Creates an image type field in your template                                                                                | 
| ptIncludes\     | Use to include one template in another                                                                                      | 
| ptLayoutVar\    | Use to output a layout variable using perch_layout_var. Optionally wrap in a conditional if perch_layout_has                | 
| ptLink          | Creates a Link type field in your template. Requires an non-standard custom fieldftype                                      | 
| ptMap\          | Creates a map type field in your template                                                                                   | 
| ptNavTags\      | List of all Perch Navigation IDs                                                                                            | 
| ptNoresults\    | Adds \<perch:noresults>\</perch:noresults> to your template to display something different when there are no results returned | 
| ptNumber\       | Creates a number type field in your template                                                                                | 
| ptOptions\      | Use this to add admin field tags to your template items                                                                     | 
| ptPagelist\     | Creates a pagelist field in your template. Requires optional pagelist fieldtype                                             | 
| ptPageSelect\   | Creates a pageselect field in your template. Requires optional [Cognetif Page Select](https://gitlab.com/cognetif-os/perch-dev/cognetif_pageselect "Page Select fieldtype") fieldtype.|
| ptPeriod\       | Creates a period type field in your template                                                                                | 
| ptPhone\        | Creates a formatted phone number field in your template. Requires optional Pipit phone template filter [Pipit Phone Template Filter](https://grabapipit.com/pipits/template-filters/phone "Pipit Phone Template Filter").                                                                                | 
| ptRadio\        | Creates a radio type field in your template                                                                                 | 
| ptSelect\       | Creates a select type field in your template                                                                                | 
| ptSlug\         | Creates a slug field for an id                                                                                              | 
| ptSmarttext\    | Creates a smarttext field in your template                                                                                  | 
| ptSwatches\     | Creates a swatches fieldtype that supports multiple dates. Requires [Tim Kinali’s Swatches fieldtype](https://bitbucket.org/tamburlane/perch-fieldtype-swatches/src/master/ "Swatches fieldtype").
| ptTable\        | Creates a table field in your template. (Requires optional [optional fieldtype](https://github.com/siansell/perch-cms-fieldtype-table "Table Fieldtype") by Simon Ansell)                                                                                       | 
| ptText\         | Creates a text field in your template                                                                                       | 
| ptTextarea\     | Creates a a multi-line block of text in your template                                                                       | 
| ptTime\         | Creates a time only field on your template                                                                                  | 
| ptTimestamp\    | Creates a timestamp field in your template (requires [optional fieldtype](https://github.com/montlewis/perch-cms-fieldtype-timestamp "Timestamp fieldtype") by Monty Lewis)                                     | 
| ptVimeo\        | Creates an Vimeo type field in your template. Requires Vimeo fieldtype                                                      | 
| ptYoutube\      | Creates an YouTube type field in your template. Requires YouTube fieldtype                                                  | 
| reset\          | Resets Typinator's variables for the Perch Expansion Set                                                                    | 
| suppress\       | Adds the suppress tag for fields                                                                                            | 
