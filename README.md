# PerchCMS-Typinator-Set
Expansions for Perch CMS using Typinator 7+
# Typinator
Requires Typinator 7.
http://www.ergonis.com/downloads/

#Setting it up
Once you have Typinator installed, you can use its new subscribe function to connect to this set of Perch expansions.
Under the Action menu, select Sets, and then select Subscribe to Set via URL...
In the window that pops up, enter this address:

  *https://github.com/montlewis/PerchCMS-Typinator-Set/raw/master/PerchCMS.typubset*

So now the Perch expansion set should be in the sets panel of the Typinator application and you should be able to start using them!
You can set which applications your expansion sets are active in. This is done with the little application icon under the list of sets.
Also, there is one expansion pHelp\, that's pretty handy and calls up Typinator's quick search window for searching through the expansions. (the help one that searches though the expansions) that is set to {key:⌥⇧⌘"."} use a key command of shift-option-command-.(period). So you should go to Typinator's preferences and set the quick search to that set of keys.

So let's take a look at the exansions! **(Note: when you type an expansion, case doesn't matter. It's just added here for clarity)**

#Here's the list of expansions by group:
##Perch Termplating

|Abreviation   | Exands to accomplish 
|:----------	| -----------
| **appspace**\       | Set the Perch App Space                                                                                                     | 
| pt**Block**\        | Creates a Perch Block within the Perch Blocks Framework                                                                     | 
| pt**Blocks**\       | Creates a Perch Blocks Framework                                                                                            | 
| pt**Checkbox**\     | Creates a checkbox type field on your template                                                                              | 
| pt**Com**\          | Begin a Perch Comment Section (<!--*)                                                                                              | 
| pt**Comment**\      | Adds a Perch comment line \(\<\!\-\-\*  \*\-\-\>)                                                                                                   | 
| pt**Composite**\    | Creates a composite field of other field values                                                                             | 
| pt**Dataselect**\   | Creates a dataselect type field in your template                                                                            | 
| pt**Date**\         | Creates a date type field in your template                                                                                  | 
| pt**Else**\         | Creates a Perch else tag in your template                                                                                   | 
| p**Template**\      | Creates a Perch Template Call. This can be used in templates to call in other templates.                                    | 
| pt**EventsTags**\   | List of all Perch Event IDs                                                                                                 | 
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
| pt**Period**\       | Creates a period type field in your template                                                                                | 
| pt**Radio**\        | Creates a radio type field in your template                                                                                 | 
| pt**Select**\       | Creates a select type field in your template                                                                                | 
| pt**Slug**\         | Creates a slug field for an id                                                                                              | 
| pt**Smarttext**\    | Creates a smarttext field in your template                                                                                  | 
| pt**Text**\         | Creates a text field in your template                                                                                       | 
| pt**Textarea**\     | Creates a a multi-line block of text in your template                                                                       | 
| pt**Time**\         | Creates a time only field on your template                                                                                  | 
| pt**Vimeo**\        | Creates an Vimeo type field in your template. Requires Vimeo fieldtype                                                      | 
| pt**Youtube**\      | Creates an YouTube type field in your template. Requires YouTube fieldtype                                                  | 
| **reset**\          | Resets Typinator's variables for the Perch Expansion Set                                                                    | 
| **suppress**\       | Adds the suppress tag for fields                                                                                            | 

##Blog Expansions
|Abreviation   | Exands to accomplish 
|:----------	| -----------
| pb**Custom**\       | Creates a Perch Blog Custom block                                                                                           | 
| pb**Functions**\    | List of all the Perch Blog functions details.                                                                               | 
| pb**URL**\          | Creates a perch:blog URL Tag                                                                                                | 

##Content Expansions
|Abreviation   | Exands to accomplish 
|:----------	| -----------
| pc**Create**\       | Creates a perch\_content\_create block                                                                                        | 
| pc**Custom**\       | Create a perch\_content\_custom block                                                                                         | 
| pc**Functions**\    | A guide to the Perch Gallery Functions and Documentation                                                                    | 
| pc**Get**\          | Outputs a perch\_content call                                                                                                | 

##Navigation Expansions
|Abreviation   | Exands to accomplish 
|:----------	| -----------
| pn**Functions**\    | A guide to the Perch Navigation Functions and Documentation                                                                 | 
| pp**Atributes**\    | A guide to the Perch Page Attributes and Documentation                                                                      | 

##Layout Expansions
|Abreviation   | Exands to accomplish 
|:----------	| -----------
| p**Layout**\        | Use to make a call to perch_layout function with optional value pairs                                                       | 
| pl**Functions**\    | A guide to the Perch Layout Functions and Documentation                                                                     | 

|Abreviation   | Exands to accomplish 
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
| /ptCom          | End a Perch Comment Section                                                                                                 | 
| /ptError        | Closing Perch:Error                                                                                                         | 
| /ptEvery        | Closing Perch:Every                                                                                                         | 
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
| pcCollection\   | Creates a perch_collection block                                                                                            | 
| pcCreate\       | Creates a perch_content_create block                                                                                        | 
| pcCustom\       | Create a perch_content_custom block                                                                                         | 
| pcFunctions\    | A guide to the Perch Gallery Functions and Documentation                                                                    | 
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
| psFunctions\    | A guide to the Perch Shop Functions and Documentation                                                                       | 
| pShowall\       | Adds the Perch Show All tag to temaplate for debugging                                                                      | 
| ptA\            | Opening Perch:After Tag                                                                                                     | 
| ptAll\          | Creates a Perch Show all tag for debugging                                                                                  | 
| ptBlock\        | Creates a Perch Block within the Perch Blocks Framework                                                                     | 
| ptBlocks\       | Creates a Perch Blocks Framework                                                                                            | 
| ptBlogTags\     | List of all Perch Blog IDs                                                                                                  | 
| ptCheckbox\     | Creates a checkbox type field on your template                                                                              | 
| ptCom\          | Begin a Perch Comment Section                                                                                               | 
| ptComment\      | Adds a Perch comment line                                                                                                   | 
| ptComposite\    | Creates a composite field of other field values                                                                             | 
| ptDataselect\   | Creates a dataselect type field in your template                                                                            | 
| ptDate\         | Creates a date type field in your template                                                                                  | 
| ptElse\         | Creates a Perch else tag in your template                                                                                   | 
| pTemplate\      | Creates a Perch Template Call. This can be used in templates to call in other templates.                                    | 
| ptEventsTags\   | List of all Perch Event IDs                                                                                                 | 
| ptFile\         | Creates a file field in your template                                                                                       | 
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
| ptPeriod\       | Creates a period type field in your template                                                                                | 
| ptRadio\        | Creates a radio type field in your template                                                                                 | 
| ptSelect\       | Creates a select type field in your template                                                                                | 
| ptSlug\         | Creates a slug field for an id                                                                                              | 
| ptSmarttext\    | Creates a smarttext field in your template                                                                                  | 
| ptText\         | Creates a text field in your template                                                                                       | 
| ptTextarea\     | Creates a a multi-line block of text in your template                                                                       | 
| ptTime\         | Creates a time only field on your template                                                                                  | 
| ptVimeo\        | Creates an Vimeo type field in your template. Requires Vimeo fieldtype                                                      | 
| ptYoutube\      | Creates an YouTube type field in your template. Requires YouTube fieldtype                                                  | 
| reset\          | Resets Typinator's variables for the Perch Expansion Set                                                                    | 
| suppress\       | Adds the suppress tag for fields                                                                                            | 

