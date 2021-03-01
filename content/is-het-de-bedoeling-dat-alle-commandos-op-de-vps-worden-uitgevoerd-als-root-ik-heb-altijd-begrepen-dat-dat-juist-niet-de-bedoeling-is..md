+++
title = "Is het de bedoeling dat alle commando's op de VPS worden uitgevoerd als root? Ik heb altijd begrepen dat dat juist niet de bedoeling is."
extra.tags =[ "hosting", "security",]
created = "Feb 22, 2021 2:48 PM"
+++
# Is het de bedoeling dat alle commando's op de VPS worden uitgevoerd als root? Ik heb altijd begrepen dat dat juist niet de bedoeling is.


In een productie-omgeving of een serieuze development-omgeving wil je op servers meerdere user accounts hebben om ervoor te zorgen dat bijv een Github action alleen bepaalde permissies heeft.

Om dat allemaal te kunnen doen moet je dus best wat weten van Linux:

- users aanmaken
- permissies geven
- eigen SSH toegang
- etc

Als je hier net mee begint mag je best een tijdje alleen als root dingen doen. Als je serieuzer met servers aan de slag gaat dan is het een goed idee om inderdaad juist zo weinig mogelijk als root te doen.