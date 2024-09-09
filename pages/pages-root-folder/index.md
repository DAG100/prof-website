---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: "bg4.jpeg"
  title: "The Environmental And Low Temperature Geochemistry Lab"
  subtitle: "\"Studying fluid-mediated surficial processes with isotopic precision\""
  caption: ""

widget4:
  title: 'Orcid ID'
  image: "orcid.png"
  url: 'https://orcid.org/0000-0001-7302-2313'
  text: '<div style="text-align:center">0000-0001-7302-2313</div>'
  buttontext: 'Visit Orcid'
widget5:
  title: 'Scopus ID'
  image: "scopus.png"
  url: 'https://www.scopus.com/authid/detail.uri?authorId=55346514800'
  text: '<div style="text-align:center">55346514800</div>'
  buttontext: 'Visit Scopus'
widget6:
  title: 'Google Scholar'
  image: "googlescholar.png"
  url: 'https://scholar.google.com/citations?user=LXqfM3kAAAAJ&hl=en&oi=ao'
  text: '<div style="text-align:center"><br /></div>'
  buttontext: 'Visit Google Scholar'

#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#

permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---
<!-- <div class="row l15 r15"> -->
# About Us

{% include match-style class="masthead-caption" style="text-align:left"
text='Clean Environment is not a Luxury,
But a Necessity for Everyone!' %}

Welcome to the Home of Environmental & Low-Temperature Geochemistry Research Group at Indian Institute of Technology Kanpur led by Indra S. Sen. Our research is aimed at understanding the chemical interactions between Earth's surface environment. We mainly focus on the impact of anthropogenic and natural processes on the chemistry of freshwater and biogeochemical element cycling. A process-level understanding is achieved using various stable, radiogenic, and non-traditional isotopes.

We are always looking for motivated Postdocs, Ph.D., M.Tech. and Research Scholars! If you are interested, please contact Dr. Indra S. Sen.

{% include button url="/research" text="Learn more" color="#d55" %}

{% if page.widget1.image or page.widget1.video or page.widget1.title or page.widget2.image or page.widget2.video or page.widget2.title or page.widget3.image or page.widget3.video or page.widget3.title %}
<div class="row t30">
	{% if page.widget1.image or page.widget1.video or page.widget1.title %}
		{% include _frontpage-widget.html widget=page.widget1 %}
	{% endif %}

	{% if page.widget2.image or page.widget2.video or page.widget2.title %}
		{% include _frontpage-widget.html widget=page.widget2 %}
	{% endif %}

	{% if page.widget3.image or page.widget3.video or page.widget3.title %}
		{% include _frontpage-widget.html widget=page.widget3 %}
	{% endif %}
	
</div><!-- /.row -->

{% endif %}

# Contact Us

{% include contact-widget
title="Principal Investigator"
text='Dr. Indra Sekhar Sen
IIT Kanpur
CESE 214
Kanpur, UP 208016
E-mail: isen [at] iitk.ac.in
Phone: +91—0512-679-6440'
photo='IndraSen.jpeg'
%}

<!-- a gap in the columns -->
{% include contact-widget %}

{% include contact-widget
title='Administrative Contact'
text='Mr. Aditya Tripathi
IIT Kanpur
CESE 214
Kanpur, UP 208016
E-mail: taditya [at] iitk.ac.in
Phone: +91—0512-679-7514'
photo='aditya.png'
%}

# Academic Identity

{% if page.widget4.image or page.widget4.video or page.widget4.title or page.widget5.image or page.widget5.video or page.widget5.title or page.widget6.image or page.widget6.video or page.widget6.title %}
<!-- <div class="row t30 l15 r15"> -->
    {% if page.widget4.image or page.widget4.video or page.widget4.title %}
        {% include _frontpage-widget.html widget=page.widget4 %}
    {% endif %}

    {% if page.widget5.image or page.widget5.video or page.widget5.title %}
        {% include _frontpage-widget.html widget=page.widget5 %}
    {% endif %}

    {% if page.widget6.image or page.widget6.video or page.widget6.title %}
        {% include _frontpage-widget.html widget=page.widget6 %}
    {% endif %}
<!-- </div> -->
<!-- /.row -->
{% endif %}