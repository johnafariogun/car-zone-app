using base templates in django templates helps you to maintain unifromity in your web pages as they all have the same page css which is extended to all of the pages
\n you use \n {% block content %} \n \n {% endblock%} \n in the space for the code in ythe base.html file \n
while in the actual home.html file you extend to the base.html file using {% extends 'base.html'%}
then wrapping the actual html scripts and special css in the \n {% block content %} \n \n {% endblock%} \n
in your end result you have a base.html file which contains the general css and js links for the whole webpage, and any other page to be added to the project extends their html and css code into the base ensuring uniformity
to create the other html pages you first log their urlpatterns in the app(urls.py) with the name of the page e.g about. and then create the view either fbv or cbv. then you replace the href of the page in the referrence html document with "{% url '<name of the page i.e about>'% }". 
NB: when deleting any view and urlpattern, you delete the urlpaytern first before the view if the server is still running, otherwise it will start giving error.