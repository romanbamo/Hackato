>Introducció
	En el cas es tractaran els dataframe de soroll per barri de Barcelona al 2017 i el dataframe de lloguer per barri de Barcelona al 2017.
	Les dades escollides per tractar la comparativa són: el rang de soroll i el preu mitja del lloguer per metre quadrat.
	S'han escollit aquestes dades perque es considera la hipotesí que la contaminació acústca de la zona afecta negativament al preu del lloguer d'aquella mateixa zona.
	Es valoraran per separat i conjuntament mitjançant un 3r dataframe per tal d'unificar-los a traves de la variable Codi_Barri.

>Depuració de les dades
	El primer tractament de les dades és l'eliminació dels valor nuls i la dada de Preu que fa referencia al preu/mes, ja que es considera que la més representativa és el lloguer Preu/m2, ja que no esta afectada pel tamany de les vivendes del barri.
	Es passa la variable Rang_soroll a una variable numérica de l'1 al 10 per tal de poder tractarla.
		La conversió seria la següent:
			MAGNITUD	RANG
			¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
		 	  <40 dB---------> 1
			40-45 dB---------> 2
			45-50 dB---------> 3
			50-55 dB---------> 4
			55-60 dB---------> 5
			60-65 dB---------> 6
			65-70 dB---------> 7
			70-75 dB---------> 8
			75-80 dB---------> 9
			  >=80dB---------> 10

	Es normalitza el preu i el codi de rang de soroll amb la formula de max-min.
	Es procedeix a la creació d'un tercer dataframe on s'unifiquen les dades a traves de la variable Barris.
	Tot que que despres s'utilitzara la variable Districte per treballar amb les dades.
	S'eliminen les dades repetides.

>Resultats i conclusions
	Despres de relacionar les variables preu i rang soroll mitjançant plots, 
	histogrames i taules de frequencia, s'arriba ala conclució que les variables son independents, 
	ja que segons districte, la frequencia dels diferents rangs de soroll està repartida per igual per a cada rang, 
	variant nomes de districte a districte, 
	pero sent les freqüències per a cada rang de soroll (del més lleu al més alt) igual.
	En canvi, el preu del lloguer per superficie si que varia entre rang de preu i districte.
	
	A continuació per expossar la conclussió, mitjançant la mostra obtenida al districte de Ciutat Vella per comparar-la amb Nou Barris, es genera una taula de freqüències
	absolutes per poder comparar directament els preus amb la contaminació acústica:

	DISTRICTE					RANG DE PREU
	¯¯¯¯¯¯¯¯¯					¯¯¯¯¯¯¯¯¯¯¯¯
		    0-4.4  4.4-6.2  6.2-8  8-9.8  9.8-11.6  11.6-13.4  13.4-15.2  15.2-17  17-18.8  18.8-20.65 <---RANG DE PREU	
	Ciutat Vella  0       0       0       0       0         0         2340       780      0        1040
	Nou Barris    0      260    1820    2080    6500      1040          0         0       0         0

	             <40    40-45   45-50  50-55   55-60      60-65      65-70     70-75    75-80     >=80     <---RANG DE SOROLL en (dB's)	
 	Ciutat Vella 104     104     104     104     104       104         104       104     104       104
	Nou Barris   338     338     338     338     338       338         338       338     338       338

	Tal com es veu, hi ha la mateixa densitat de contaminació acústica per a cada rang de soroll: 104 mostres a Ciutat Vella i 338 mostres a Nou Barris.
	En canvi, entre els dos districtes hi ha diferencia en el rang de preu.
	És aquesta comparació la que ens diu que les variables son independents.

	Es podria presentar la hipotesi, segons l'observat, que el que si sembla afectar negativament al preu es la quantitat de barris que trobem a cada districte.
	Això es una dada que es pot trobar al prop dataframe de lloguer, per tant, no és vàlida per el nostre cas.

