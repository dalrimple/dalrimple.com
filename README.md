#dalrimple.com blog site

This is the repo for the dalrimple.com blog. Hosted as static files, it is built using [Jekyll][jekyll].

I've also mashed together the [Fluid Baseline Grid][FBG] and [Skeleton][skeleton] CSS libraries for the basis of the site's styling.

[jekyll]: https://github.com/mojombo/jekyll "Jekyll static site generator"
[FBG]: http://fluidbaselinegrid.com/ "Fluid Baseline Grid CSS library"
[skeleton]: http://www.getskeleton.com/ "Skeleton responsive CSS library"


###Notes
List of design requirements for the various responsive breakpoints  
Desktop font size: 19px (good for readability)  
Desktop paragraph width should be close to: 580px (Maintains about 12 words per line at 19px)  
Layout becomes fluid below 580px;  
Font size decreases below 420px to keep the text readable on mobiles.  
Images should ideally be full width (580px). If they aren't centered with whitespace either side to stop narrow columns of text when in fluid mode.