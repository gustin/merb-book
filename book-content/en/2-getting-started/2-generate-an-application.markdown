# Generate an application
Merb comes with a generator (<tt>merb-gen</tt>) in order to create Merb applications. The generator can generate different types of Merb applications, to see all the generator options available type

    $ merb-gen -h
## Types
Merb can be used for anything from  very small, quick, single-file applications to large complex web-services.  Different application structures can be generated depending on the developers needs. The different application structures you can generate are <tt>app</tt>, <tt>core</tt>, <tt>flat</tt> and  <tt>very_flat</tt>.

### App
The opinionated Merb stack.  This generates a full application directory structure with a full set of configuration files, and also adds a <tt>config/dependancies.rb</tt> file which includes all of <tt>merb-more</tt> and <tt>DataMapper</tt>.

    $ merb-gen app my-application

This app has everything needed to start building a first-class web application, and it the most simular to the default structure of Rails.  Much of this book will work with the assumption that you have started like this.

Run this application by running <tt>merb</tt> in the root directory.  This will start Merb and bind it to the default port 4000. To see your application in action, visit [http://localhost:4000/](http://localhost:4000/).

### Core
Core will generate the full application directory structure with a full set of configuration files.  Unlike the <tt>app</tt> -- the opinionated full stack, no dependancies will be added.

    $ merb-gen core my-application

Run this application by running <tt>merb</tt> in the root directory.  Notice that unlike the other three generated apps, there is no default content in core.  Visiting [http://localhost:4000/](http://localhost:4000/) will generate an error until content and routing are added.

### Flat
A flat application still keeps all its logic in a single file, but has seperate files for configutation and it's own view directory.

    $ merb-gen flat my-application

Flat applications are run like any other generated merb app by running <tt>merb</tt> in the root directory.  By default, all methods in the <tt>my-application</tt> class will be treated as actions with <tt>my-application</tt> as the controller. e.g.: [http://localhost:4000/my-application/foo](http://localhost:4000/my-application/foo)

This will call <tt>MyApplication#foo</tt> and render the output from the <tt>foo.html.*</tt> template.

### Very Flat
A Very Flat application is is similar to other Ruby micro frameworks, where the entire application is in one file.

    $ merb-gen very_flat my-applcation

To run a very flat application you start up Merb with the following command (within your application directory):

    $ merb -I my-applcation.rb

This will start Merb and bind it to the default port 4000. To see your application in action, visit [http://localhost:4000/](http://localhost:4000/).





