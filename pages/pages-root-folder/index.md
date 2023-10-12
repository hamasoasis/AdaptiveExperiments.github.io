---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: gallery-example-1.jpg
widget1:
  title: "EASI Workshops"
  url: /workshops
  image: gallery-example-1.jpg
  text: 'EASI will sponsor annual workshops for Researchers and Instructors on how to setup Adaptive Experiment.'
widget2:
  title: "EASI Call for Experiments"
  url: /participate
  image: gallery-example-1.jpg
  text: 'We are accepting application from researchers with interest in Psychology, Machine Learning, Computer Science and Education'
widget3:
  title: "Training Material"
  url: /training_material
  image: gallery-example-1.jpg
  text: 'Curated training material will be available and open-source for the community to use locally and suggest changes'
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
  url: /participate/
  text: How to conduct your next research ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>