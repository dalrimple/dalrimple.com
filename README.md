#dalrimple.com blog site

This is the repo for the dalrimple.com blog. Hosted as static files, it is built using [Jekyll][jekyll].

I've also mashed together the [Fluid Baseline Grid][FBG] and [Skeleton][skeleton] CSS libraries for the basis of the site's styling.

The CSS is generated using [Compass][compass] for its sass compiling and rich collection of mixins.

##Maintenance instructions

###CSS

To update the CSS, make sure you have [Compass][compass] installed, open terminal and cd to the site root, then:

	$ compass watch --config _config/compass.rb

The compass.rb file hass all the config options set.

###Jekyll

To update the site, make sure you have [Jekyll][jekyll] installed, open terminal and cd to the site root, then:

	$ jekyll serve -w --config _config/jekyll.yml

The jekyll.yml file has all the config necessary to output the site. The config file sets the output directory to the HTML folder on the same level as the project directory. Until you hit ^C jekyll will watch for changes and update the files and <http://localhost:4000> will serve the output site.

[jekyll]: https://github.com/mojombo/jekyll "Jekyll static site generator"
[FBG]: http://fluidbaselinegrid.com/ "Fluid Baseline Grid CSS library"
[skeleton]: http://www.getskeleton.com/ "Skeleton responsive CSS library"
[compass]: http://compass-style.org/ "CSS authoring framework"

###Notes
List of design requirements for the various responsive breakpoints  
Desktop font size: 19px (good for readability)  
Desktop paragraph width should be close to: 580px (Maintains about 12 words per line at 19px)  
Layout becomes fluid below 580px;  
Font size decreases below 420px to keep the text readable on mobiles.  
Images should ideally be full width (580px). If they aren't centered with whitespace either side to stop narrow columns of text when in fluid mode.