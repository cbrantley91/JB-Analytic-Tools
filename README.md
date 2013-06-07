JBCollect and JBAnaltyics
===========

Python Webserver + Android Java Library for collecting and viewing analytical data about your Android application.

JBAnalytics
===========
JBAnalytics is the dashboard end of our program: it provides a webserver to generate data based on the database you provide the secret key for. As a general rule, the database must be using our database schema (currently only really set up for Force.com databases), but easily changeable.

The webserver provides a dashboard from which to select your apps.  From there, you must select values for the axes, as well as any filters you'd like, and it will generate a graph.  Currently, some heavier work is being done in Javascript, so it is not as scalable as we'd like it.

The webserver is Python-based, using Django, and can be started locally simply by using the command:
<code>python manage.py runserver</code>

(an edit will be done if we find any database values that must be changed)

JBCollect
===========

JBCollect is the Android collection API we've developed.  You must initialize your application, then register the type of data it is of the pre-established enums.  Once that's done, you can simply log data with the logData function.

Currently, JBCollect has no real error-handling routine; however, we may soon make it Observable, so that it may notify a class if it fails to send (such as the case of having a lack of connection).

===========

For more information about the application or the project itself, please see se-capstone.appspot.com.
