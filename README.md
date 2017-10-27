project_structure
=================

Voorgestelde project structuur voor data scientists
---------------------------------------------------
Deze repository bevat een concept structuur voor data science projecten binnen DUO. 
Doel is om projecten op zo'n manier in te delen, dat het makkelijk is voor collega's om midden in een project aan te schuiven.
Deze structuur is slechts een richtlijn, waar vanaf kan worden geweken wanneer hier een logische aanleiding toe is.

Uitleg structuur
----------------
*data* bevat alle data die gebruikt wordt in het project. In de subfolder *raw* komen de oorspronkelijke databestanden te staan. Deze moeten beschouwd worden als *read-only*. Data bestanden die getransformeerd zijn, bijvoorbeeld doordat extra attributen zijn toegevoegd, komen in de subfolder *processed*. Wanneer zulke getransformeerde databestanden nog een work-in-progress zijn, komen ze in de subfolder *intermediate*. Data bestanden die extra worden toegevoegd ten behoeven van de modellen komen in de map *external*. Denk hierbij bijvoorbeeld aan een bestand met stopwoorden welke gebruikt wordt bij de preprocessing. 

In *notebooks* komen alle jupyter notebooks te staan die gebruikt zijn tijdens het project. Deze notebooks dienen opgeslagen te zijn in het format '$ID_$AUTHOR_$SUBJECT'. Hierin is $ID een uniek nummer per notebook, $AUTHOR de inintialen van de maker en geeft $SUBJECT een beschrijving van de inhoud van het notebook. Het is niet de bedoeling dat een notebook tegelijkertijd door meerdere mensen wordt gebruikt. Wanneer je aanpassingen wil maken aan een notebook van iemand anders, kan deze simpelweg gekopieerd worden en een andere filename krijgen. 

*reports* is de plek waarin verslagen, presentaties en andere rapportages worden verzameld. De subfolder *figures* bevat afbeeldingen en visualizaties die in de verslagen gebruikt kunnen worden.

*models* bevat opgeslagen versies van getrainde modellen. Van al deze modellen moet duidelijk zijn hoe deze tot stand zijn gekomen. Denk hierbij aan het documenteren van de gebruikte trainingsdata, model type, model parameters en gebruikte features. Ook kan het handig zijn om bij te houden hoe goed het model heeft gescoord op de validatie data. Wanneer trainingstijden lang zijn en veel verschillende configuraties geprobeerd worden, is het van groot belang dat deze gegevens goed worden bijgehouden. 

*src* bevat alle code die nodig is om het uiteindelijke resultaat te verkrijgen. Denk hierbij aan aparte scripts voor het verkrijgen van data, het voorbewerken van de data, feature engineering, het trainen van modellen, het voorspellen met de getrainde modellen en het maken van visualizaties die gebruikt worden in de verslaglegging. Idealiter is er een bash-file welke een gerund kan worden, die in één keer het volledige process van data laden, trainen en predictie uit voert. 
