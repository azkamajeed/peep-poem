HOW TO RUN 
The project is simply an html file with css script embedded in it hence no imports and is a single file project, just double click it and it will run in any browser on local machine.



STACK CHOICE
Vanilla HTML, CSS and Javascript all in one file and no database.This was the right choice because the app is self-contained , no imports , fonts load from google and it uses local storage for poem storage , there is nothing to install for this level of complexity and project and hence no extra tech was needed.
A bad choice could have been using REACT and a backend database and then its deployment.Since the app is for personal use , deployment is unnecessary and that tech stack would have made the same task more complex.




ONE REAL EDGE CASE
file : index.html
the savePoem() function, line 744
jstitle: document.getElementById('title-input').value.trim() || 'untitled',

If a user saves a poem without any title , the trim () function would collapse the white space and the fallback  "untitled" would take title's placeholder .If that not handled, the sidebar would show a blank title and hence impossible for the user to make a valid search.



AI USAGE
I used AI mainly for the UI development , I used CLAUDE , asked it to make it simple and minimalistic and add a paper editor for writing the poems . I also asked it to  add the option of using a font of choice  and add time of last edit for  each poem.
For the UI , it used Italics and some other font which were awkward .  I changed all the app text to non-Italic Cormorant Garamond . For the time of edit requirement , it only mentioned the date of "last-modified " , I changed it to render the exact time as well.



HONEST GAP 
The app is using localstorage that means once the browser data is deleted , all the poems will be vanished with no way to recover them.
Later  on I will add the option to export the poems in JSON file and an import option too which will import the JSON file and render them again on the app as the normal poems , in the original format.