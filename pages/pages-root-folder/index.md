---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: "bg4.jpeg"
  title: "Environmental And Low Temperature Geochemistry Lab"
  caption: "We study fluid-mediated surficial processes with isotopic precision"
widget1:
  title: 'Publications'
  url: '/publications/'
  text: '<div style="font-size:100px;text-align:center;">39</div>'
widget2:
  title: 'Patents'
  url: '/publications/'
  text: '<div style="font-size:100px;text-align:center;">3</div>'
#  video: '<a href="#" data-reveal-id="videoModal"><img #src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-##responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: 'Citations'
  url: '/publications/'
  text: '<div style="font-size:100px;text-align:center;">461</div>'

widget4:
  title: 'Orcid Id'
  url: '/publications/'
  text: 'Insert Orcid ID here'
  buttontext: 'Visit Orcid'
widget5:
  title: 'Scopus Id'
  url: '/publications/'
  text: 'Insert Orcid ID here'
  buttontext: 'Visit Scopus'
widget6:
  title: 'Google Scholar Id'
  url: '/publications/'
  text: 'Insert Orcid ID here'
  buttontext: 'Visit Google Scholar'

#Contact, I reused the widgets here for convenience
widget7:
  title: 'Principal Researcher'
  text: |
    Dr. Indra Sekhar Sen
    <br />
    IIT Kanpur
    <br />
    CESE 214
    <br />
    Kanpur, UP 208016
    <br />
    E-mail: isen [at] iitk.ac.in
    <br />
    Phone: +91—0512-679-6440
    
widget8:
  title: 'Administrative Contact'
  text: |
    Mr. Aditya Tripathi
    <br />
    IIT Kanpur
    <br />
    CESE 214
    <br />
    Kanpur, UP 208016
    <br />
    E-mail: taditya [at] iitk.ac.in
    <br />
    Phone: +91—0512-679-7514


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
callforaction:
  url: /research/
  text: LEARN MORE
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---
<div class="row l15 r15">
<h1 style="margin-top:100px;text-align:center">About Us</h1>
<div class="masthead-caption" style="text-align:left">
Clean Environment is not a Luxury,
But a Necessity for Everyone!
</div>
<p>Welcome to the Home of Environmental & Low-Temperature Geochemistry Research Group at Indian Institute of Technology Kanpur led by Indra S. Sen. Our research is aimed at understanding the chemical interactions between Earth's surface environment. We mainly focus on the impact of anthropogenic and natural processes on the chemistry of freshwater and biogeochemical element cycling. A process-level understanding is achieved using various stable, radiogenic, and non-traditional isotopes.</p>
<p>We are always looking for motivated Postdocs, Ph.D., M.Tech. and Research Scholars! If you are interested, please contact Dr. Indra S. Sen.</p>
</div>

{% if page.widget4.image or page.widget4.video or page.widget4.title or page.widget5.image or page.widget5.video or page.widget5.title or page.widget6.image or page.widget6.video or page.widget6.title %}
<div class="row t60 l15 r15">
    <h1 style="text-align:center">Academic Identity</h1>
    {% if page.widget4.image or page.widget4.video or page.widget4.title %}
        {% include _frontpage-widget.html widget=page.widget4 %}
    {% endif %}

    {% if page.widget5.image or page.widget5.video or page.widget5.title %}
        {% include _frontpage-widget.html widget=page.widget5 %}
    {% endif %}

    {% if page.widget6.image or page.widget6.video or page.widget6.title %}
        {% include _frontpage-widget.html widget=page.widget6 %}
    {% endif %}
</div><!-- /.row -->
{% endif %}

{% if page.widget7.image or page.widget7.video or page.widget7.title or page.widget8.image or page.widget8.video or page.widget8.title %}
<div id="#contact" class="row t60 l15 r15">
  <h1 style="text-align:center">Contact Us</h1>
  {% if page.widget7.image or page.widget7.video or page.widget7.title %}
    {% include _frontpage-widget.html widget=page.widget7 %}
  {% endif %}

  {% if page.widget8.image or page.widget8.video or page.widget8.title %}
    {% include _frontpage-widget.html widget=page.widget8 %}
  {% endif %}
</div><!-- /.row -->
{% endif %}