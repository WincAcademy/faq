+++
title = "Waarom is inline JavaScript niet handig?"
extra.tags =[ "javascript", "project",]
created = "Feb 10, 2020 1:45 PM"
+++
# Waarom is inline JavaScript niet handig?
Je kan je JavaScript code in je HTML file stoppen. Dat doe je met <script>tags. Je kan ook met (bijvoorbeeld) het onclick attribuut event listeners aan je HTML toevoegen.

Deze manieren van JavaScript aan je pagina toevoegen is niet handig. Waarom niet? De belangrijkste redenen zijn:

1. als je meerdere HTML files hebt en je wil dezelfde JavaScript gebruiken moet je je code gaan kopiëren, dat wordt snel onhandig
2. als je aan meerdere elementen event listeners wil hangen moet je ook code gaan kopiëren, dat wordt snel onhandig
3. als je de JavaScript van je website aan het bekijken bent is het handig om alle JavaScript code bij elkaar te hebben en niet te hoeven switchen van je HTML file terug naar je JavaScript file terug naar je HTML file

Als laatste: de meeste developers gebruiken geen inline JavaScript, als jij dat wel doet wordt jouw code moeilijker te lezen voor andere developers.