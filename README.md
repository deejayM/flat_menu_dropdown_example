# flat_menu_dropdown_example
Using Wagtailmenus and solution to adding Flat Menus as a dropdown item to the main menu. 

In my previous post I gave a example of a template for a ‘main_menu’ in wagtail menus.  
https://www.blogger.com/blog/post/edit/preview/8608610523928821757/2576531812455589045

My next task was in Wagtailmenus how to display custom flat menus as dropdowns.  And so it seems it wasn’t that straightforward. In hindsight may be solved by better planning and partly due to the fact I’d taken a Django site and made it into a Wagtail CMS driven one.  Meaning that not all APP pages are created and accessible through the Wagtail CMS - Ideally they would be.  In which case you could use the ‘Allow sub-menu for this item’ tick box that would automatically generate the menu items.

So anyway I thought it’d be handy to be able to have ‘Flat menus’ that I could add to the Main Menu, and I’ve come up with a way to facilitate that.  It feels a little hacky in areas, so feel free to contribute any changes that you think would help.  I’ve added the code to Github .  

In my Main Menu template I use 'item-handle' to check against an 'if' statement to switch the menu I'm showing.  I would need to do this but in the call up 
{% flat_menu 'sub-folder' %}
I can't use 
{% flat_menu 'sub-{{ item.handle }}' %}

Which would make my code look a lot better. 
