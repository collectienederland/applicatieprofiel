# Applicatieprofiel voor CollectieNederland.nl

## Inleiding

In deze documentatie wordt het applicatieprofiel beschreven voor CollectieNederland.nl. Dit profiel is gebaseerd op het [<u>nieuwe datamodel voor Collectienederland.nl</u>](https://github.com/collectienederland/schema-profile), dat schema.org gebruikt als beschrijvende vocabulaire. Dit model is weer een uitbreiding op het [<u>NDE-applicatieprofiel</u>](https://docs.nde.nl/schema-profile/) ([versie 1.4.0](https://docs.nde.nl/schema-profile/#v1.4.0)) en volgt dit applicatieprofiel grotendeels. Dit document vormt de basis voor de aanlevervoorwaarden van CollectieNederland.nl

Op enkele punten wijkt het applicatieprofiel voor CollectieNederland.nl af van het NDE-applicatieprofiel. Het gaat hier altijd om versoepelingen en aanvullingen ten op zichten van het NDE-applicatieprofiel, nooit om striktere eisen. Deze punten zijn terug te vinden onder 1.2.5.

De velden die minimaal nodig zijn om data aan te leveren aan CollectieNederland.nl staan genoteerd onder 1.2. De thesauri die CollectieNederland.nl aanhoudt zijn terug te vinden onder sectie 1.5.

### Definities

**Kardinaliteit**: hoe vaak een waarde mag voorkomen in een veld.
Hierbinnen geeft dit document ook de specifieke datatypes aan (bijv. URI
of Date) of de thesauri die toegestaan zijn.

- 0..\* de waarde mag nul, één of meerdere keren voorkomen

- 1..\* de waarde moet minimaal 1 keer voorkomen en mag meerdere malen
  voorkomen

- 0..1 de waarde mag 0 of 1 keer voorkomen

- 1..1 de waarde moet één keer voorkomen

**Classes**: Een type entiteit in schema.org (bijv. Place of
CreativeWork). Deze worden gebruikt om te bepalen welke entiteiten
toegestaan zijn in het applicatieprofiel.

**Properties**: de kenmerken die binnen een Class vallen (bijv.
schema:name en schema:description).). Deze worden gebruikt om te bepalen
welke entiteiten toegestaan zijn in het applicatieprofiel.

**Verplichtingsniveau:**

- **Verplicht**: de waarden die altijd moeten worden aangeleverd
  (schema:license)

- **Sterk aanbevolen**: de waarden waarvan sterk wordt aanbevolen dat ze
  worden aangeleverd

- **Aanbevolen**: de waarden waarvan wordt aanbevolen dat ze worden
  aangeleverd

- **Optioneel:** de waarden die mogen worden aangeleverd
  (schema:material)

### Velden voor CollectieNederland.nl

CollectieNederland.nl is een Nederlands dienstplatform en toont de collectiedata in het Nederlands. Zorg dat de velden een ‘nl’ of ‘nl-NL’ tag hebben waarin de taal van de data wordt aangegeven.

### Minimale en sterk aanbevolen  velden

Bij het aanleveren van collectiedata aan CollectieNederland.nl wordt gekeken of de volgende minimale en sterk aanbevolen velden aanwezig zijn in de data en of de inhoud van deze velden in lijn is met het NDE-applicatieprofiel en de aanvullende bepalingen ten behoeve van CollectieNederland.nl. Als er voor een  veld een afwijking of versoepeling geldt, dan is deze leidend ten opzichte van het
NDE-applicatieprofiel. Bij overlap tussen de twee profielen verwijst dit
document door naar het NDE-applicatieprofiel.

### Overzichtstabel minimale en sterk aanbevolen velden

In de onderstaande tabel staat een overzicht van de minimale (ofwel
verplichte) en sterk aanbevolen velden voor publicatie van een dataset
op CollectieNederland.nl. Er zijn een aantal ‘keuzevelden’ opgenomen.
Voor deze velden geldt:

\- Keuzeveld 1: er moet ten minste één veld aanwezig zijn wat kan
functioneren als titel.

\- Keuzeveld 2: er wordt sterk aanbevolen ten minste één veld aan te
leveren wat kan functioneren als datering.

\- Keuzeveld 3: er wordt sterk aanbevolen ten minste één veld aan te
leveren dat iets beschrijft van en/of over het object (CreativeWork).

| *Entiteit* | *Veld* | *Betekenis* | *Verplicht* | *Type* |
|----|----|----|----|----|
| MediaObject | Schema:license | Rechtenstatement afbeelding | Ja, als schema:contentUrl aanwezig is | URI |
| CreativeWork | schema:copyrightNotice | Actuele juridische status | Ja, voor Rijksmusea | URI |
| CreativeWork | Schema:isPartOf\>schema:Dataset | Beschrijft van welke dataset het object deel uitmaakt | Ja | URI |
| CreativeWork | schema:sdDatePublished | Datum van publicatie metadata | Ja | date |
| CreativeWork | schema:name | Titel | Keuzeveld 1 – schema:name of schema:additionalType | String |
| CreativeWork | schema:additionalType | Soort object | Keuzeveld 1 - schema:name of schema:additionalType | String of URI |
| CreativeWork | schema:temporal | Periode van vervaardiging | Keuzeveld 2 – sterk aanbevolen | String |
| CreativeWork | schema:dateCreated | Vervaardigingsdatum | Keuzeveld 2 – sterk aanbevolen | Date |
| CreativeWork | schema:description | Beschrijving van het object | Keuzeveld 3 – sterk aanbevolen | String |
| CreativeWork | schema:material | Materiaal | Keuzeveld 3 – sterk aanbevolen | String/URI |
| CreativeWork | schema:size | Afmetingen | Keuzeveld 3 – sterk aanbevolen | String/QuantitativeValue |
| CreativeWork | schema:locationCreated | Plaats van productie of vervaardiging | Keuzeveld 3 – sterk aanbevolen | String/URI |

### Aanbevolen en optionele velden

In de onderstaande tabel staat een overzicht van de velden die worden aanbevolen of optioneel zijn om aan te leveren. In sectie 1.3 worden de velden toegelicht. In sommige gevallen is het zo dat als een optioneel veld wordt aangeleverd, er een verplicht veld bijkomt – dat aan het optionele veld verbonden is. Mocht dit zo zijn dan staat dit per veld aangegeven in de kolom optioneel/aanbevolen.

### Overzichtstabel aanbevolen en optionele velden

| **Entiteit** | **Veld** | **Inhoud van het veld** | **Verplicht** | **Type** | **NDE-profiel** |
|----|----|----|----|----|----|
| Schema:CreativeWork | schema:alternateName | alternatieve titel van het object | Optioneel | String | Nee, uitbreiding CN.nl |
| Schema:Creative:Work | Schema:license | Rechtenstatement van het object zelf | Aanbevolen | URI | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | Schema:url | Link van het object op de website van de bronhouder | Aanbevolen | URI | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:creditText | geassocieerde persoon of organisatie | Optioneel | String/URI | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:publisher | Uitgever object | Optioneel | String | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:datePublished | datum van uitgave door uitgever | Optioneel | Date | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:citation | Referentie naar uitgave of bron | Optioneel | String | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:temporal | Tijdsaanduiding in platte tekst | Optioneel | String | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:isPartOf/hasPart \>CreativeWork | Deelcollectie | Aanbevolen | URI | Nee, uitbreiding CN.nl |
| Schema:CreativeWork | schema:genre | Onderwerp | Aanbevolen | String/URI | Ja |
| Schema:CreativeWork | schema:about | Geassocieerde persoon of concept | Aanbevolen | String/URI | Ja |
| Schema:CreativeWork | schema:identifier | Objectnummer | Aanbevolen | String/URI | Ja |
| Schema:CreativeWork | schema:creator | Vervaardiger | Aanbevolen | String/URI | Ja |
| Schema:MediaObject | schema:contentUrl | Afbeelding | Aanbevolen | URI | Ja |
| Schema:MediaObject | schema:license | Rechtenstatement afbeelding | Ja, bij schema:contentUrl | URI | Ja |
| Schema:MediaObject | Schema:copyrightHolder | Rechthebbenden van een MediaObject | Optioneel | Schema:Person | ja |
| Schema:MediaObject | schema:thumbnailUrl | Verkleinde afbeelding | Verplicht met contentUrl | URI | Ja |
| Schema:Person | schema:name | Vervaardiger persoon of organisatie | Aanbevolen | String/URI | Ja |
| Schema:Person | schema:hasOccupation | Rol van de vervaardiger | Optioneel | String/URI | Ja |
| Schema:Person | schema:birthDate | Geboortedatum vervaardiger | Optioneel | Date | Ja |
| Schema:Person | schema:birthPlace | Geboorteplaats vervaardiger | Optioneel | String/URI | Ja |
| Schema:Person | schema:deathDate | Sterfdatum vervaardiger | Optioneel | Date | Ja |
| Schema:Person | schema: deathPlace | Sterfplaats vervaardiger | Optioneel | String/URI | Ja |
| Schema:Place | schema:latitude | Breedtegraad | Optioneel | Tekst | Ja |
| Schema:Place | schema:longitude | Lengtegraad | Optioneel | Tekst | Ja |
| Schema:Place | schema:addressRegion | Provincie | Optioneel | String/URI | Ja |
| Schema:MediaObject | schema:encodingFormat | Type media | Optioneel | String/URI | Nee, uitbreiding CN.nl |

### Afwijkingen ten opzichte van het NDE applicatieprofiel

In de onderstaande tabellen zijn de verschillen terug te vinden tussen hetCollectieNederland.nl-applicatieprofiel en het NDE-applicatieprofiel. Het gaat hier in de eerste tabel om verschillen in de aanwezigheid van Classes en Properties. In de tweede tabel worden de verschillen aangegeven in Classes en Properties die zowel het NDE-applicatieprofiel als CollectieNederland.nl-applicatieprofiel kennen, maar waarbij CollectieNederland.nl een ander verplichtingsniveau hanteert (bijv. optioneel i.p.v. verplicht) of een andere invulling geeft.

<table>
<colgroup>
<col style="width: 41%" />
<col style="width: 9%" />
<col style="width: 22%" />
<col style="width: 26%" />
</colgroup>
<thead>
<tr>
<th colspan="4"><strong>CollectieNederland.nl ten opzichte van NDE —
toevoegingen</strong> <strong>in Classes en Properties</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Property/Class</strong></td>
<td><strong>In NDE profiel</strong></td>
<td><strong>In CN.NL 2.0 Datamodel en applicatieprofiel</strong></td>
<td><strong>Uitleg op toevoeging</strong></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:publisher</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Uitgever van een boek. Publisher, ofwel, bronhouder komt mee vanuit
de datasetbeschrijving van de dataset in het dataset register.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:license</td>
<td>Nee</td>
<td>Ja — aanbevolen</td>
<td>Rechtenstatement van het object zelf</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:temporal</td>
<td>Nee</td>
<td>Ja — keuzeveld 2</td>
<td>Vrije-tekst datering (bijv. “ca. 1650”) als aanvulling op
schema:dateCreated, voor onzekere of ongestructureerde dateringen.</td>
</tr>
<tr>
<td>MediaObject&gt;schema:copyrightNotice</td>
<td>Nee</td>
<td>Ja — verplicht (alleen Rijksmusea)</td>
<td>Toevoeging voor de Erfgoedwet-verplichtingen van Rijksmusea.</td>
</tr>
<tr>
<td>Place&gt;schema:addressRegion</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Coördinaten en provincie/regio, voor kaartweergave en filtering op
CNNL.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:isPartOf (hasPart)&gt;CreativeWork</td>
<td>Nee</td>
<td>Ja - aanbevolen</td>
<td>Relatie voor het aangeven van een deelcollectie binnen een
dataset.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:alternateName</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Alternatieve naam/titel van object of
vervaardiger.<mark></mark></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:creditText</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Generieke attributie-/credittekst. Let op: voor het specifieke geval
van eigendomsgeschiedenis wordt dit veld juist afgeraden (te weinig
gestructureerd) — hier gaat het om een breder, algemeen gebruik.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:citation</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Verwijzing naar publicaties of bronnen waarin het object wordt
beschreven.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:datePublished</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Datum van publicatie, bijvoorbeeld van een boek.<mark></mark></td>
</tr>
<tr>
<td>MediaObject&gt;schema:encodingFormat</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Type media</td>
</tr>
<tr>
<td>schema:AdministrativeArea</td>
<td>Nee</td>
<td>Ja – optioneel</td>
<td>De provincie waarin de plek (Schema:Place) zich bevindt.</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 16%" />
<col style="width: 58%" />
</colgroup>
<thead>
<tr>
<th colspan="3"><strong>CollectieNederland.nl ten opzichte van NDE —
afwijkend verplichtingsniveau</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Property</strong></td>
<td><strong>NDE</strong></td>
<td><strong>CN</strong></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:creator</td>
<td>Verplicht als de vervaardiger bekend is.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>MediaObject&gt;schema:thumbnailUrl</td>
<td>Verplicht op MediaObject.</td>
<td></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:associatedMedia / afbeelding</td>
<td>Verplicht indien beschikbaar.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:identifier / PID</td>
<td>PID verplicht.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:name</td>
<td>Verplicht op CreativeWork</td>
<td>Aanbevolen. CollectieNederland.nl vraagt schema:name of
schema:additionalType, zie sectie 1.2.2.</td>
</tr>
</tbody>
</table>

### Thesauri-gebruik

Wanneer er gebruikt gemaakt wordt van thesaurustermen dan worden de volgende thesauri aangenomen, afhankelijk van metadata veld: Art & Architecture Thesaurus (AAT), Cultuurhistorische Thesaurus (CHT), GeoNames en RKDartists. Al deze thesauri zijn te raadplegen via het [Termennetwerk](https://termennetwerk.netwerkdigitaalerfgoed.nl/nl). Bekijk hier een omschrijving van thesaurustermen in het NDE-applicatieprofiel: [<u>https://docs.nde.nl/schema-profile/#reference-terms.</u>](https://docs.nde.nl/schema-profile/#reference-terms.)

## CollectieNederland.nl-applicatieprofiel 

Afwijkingen van het NDE-applicatieprofiel zijn gemarkeerd door middel van een asterisk (\*) en zijn met uitleg terug te vinden in de bovenstaande sectie 1.2.5.

### Klassediagram

Hieronder is een overzicht van het datamodel te zien. Als centrale klasse word [CreativeWork](https://schema.org/CreativeWork) gebruikt.

<!--<pre class="mermaid">-->
```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  name xsd:string 
  alternateName* xsd:string 
  creditText* xsd:string 
  publisher* xsd:string 
  datePublished* xsd:string 
  citation* xsd:string 
  dateCreated xsd:string 
  temporal* xsd:string 
  license* xsd:string 
  description xsd:string 
  size xsd:string 
  url xsd:anyURI 
  isPartOf xsd:anyURI 
  sdDatePublished xsd:date 
}

class additional["Text*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product*"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> product: material

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> defterm: genre, about
class place["Place"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person"]{
  name xsd:string 
  sameAs xsd:anyURI 
  deathDate xsd:string  
  birthDate xsd:string 
}
creativework --> person: creator
person --> place: birthPlace
person --> place: deathPlace

class occupation["Occupation, DefinedTerm"]{
  name xsd:string 
  sameAs xsd:anyURI 
}
person --> occupation: hasOccupation

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license xsd:string
  copyrightNotice xsd:string
  encodingFormat* xsd:string
}
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> person:copyrightHolder

class propval["PropertyValue"] {
  propertyID xsd:string
  value xsd:string
  description xsd:string
}
creativework --> propval: identifier
```
<!--</pre>-->

### [CreativeWork](https://schema.org/CreativeWork)
De centrale klasse in het CollectieNederland.nl-applicatieprofiel. Met deze klasse worden cultuurhistorische objecten omschreven in dit profiel.

#### [schema:name](https://schema.org/name)
- <b>Scope: </b>Verplicht, tenzij [schema:additionalType](https://schema.org/additionalType) aanwezig is. 
- <b>Beschrijving:</b> titel van het object
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> Zie [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-name) voor meer informatie en voorbeelden.

#### [schema:alternateName](https://schema.org/alternateName)
- <b>Scope: Optioneel</b>
- <b>Beschrijving:</b> alternatieve titel van het object
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1

Uitbreiding NDE-applicatieprofiel om musea de mogelijkheid te geven om objecten meerdere titels mee te geven zoals toegekende titel of originele titel.

- <b>Voorbeeld:</b> 
``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "De Schreeuw"@nl,
  "alternateName": "Skrik"@no,
}
```

#### [schema:conditionsOfAccess](https://schema.org/conditionsOfAccess)
- <b>Scope: </b>Verplicht voor Rijksmusea.
- <b>Beschrijving:</b> Actuele juridische status (Rijksmusea, Erfgoedwet)
- <b>Waarde:</b> *Waarde moet nog bepaald worden*

#### [schema:isPartOf](https://schema.org/isPartOf)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving:</b> Dataset of collectie waartoe het werk behoort
- <b>Waarde:</b> zie [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf)

#### [schema:publisher](https://schema.org/publisher)
- <b>Scope: </b>Optioneel. >> kan dus weg hier? 
- <b>Beschrijving:</b> Wordt door CollectieNederland.nl opgehaald uit het NDE Dataset Register..
- <b>Waarde:</b> ??

#### [schema:url](https://schema.org/url)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving:</b> Link terug naar het record bij de bronhouder
- <b>Waarde:</b> zie <https://docs.nde.nl/schema-profile/#CreativeWork-URI>

#### [schema:license](https://schema.org/license)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving</b>: - *NDE heeft alleen een licentie als verplicht bij MediaObject.*
- <b>Waarde:</b> *CN-extensie op CreativeWork-niveau*

#### [schema:creditText](https://schema.org/creditText)
- <b>Scope: Optioneel</b>
- <b>Beschrijving:</b> geassocieerde persoon of organisatie die is gerelateerd  aan het object.
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> 
``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "creditText": "In bruikleen van Fam. de Wit."@nl,
}
```

#### [schema:additionalType](https://schema.org/additionalType)
- <b>Scope: </b>Verplicht, tenzij [schema:name](https://schema.org/name) aanwezig is. 
- <b>Beschrijving:</b> Specifiek type van het werk (bijv. schilderij).
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> Zie [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-name) voor meer informatie en voorbeelden.

#### [schema:creator](https://schema.org/creator)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving</b>: Maker van het werk, zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-creator).
- <b>Waarde:</b> Zie [Person](#person)

### [Person](https://schema.org/Person)
<a name="person"></a>

#### [schema:name](https://schema.org/name)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving: Naam van de persoon of organisatie</b> 
- <b>Waarde: string</b> 

### [MediaObject](https://schema.org/MediaObject)
<a name="media"></a>

#### [schema:contentUrl](https://schema.org/contentUrl)
- <b>Scope: </b>Verplicht. 
- <b>Beschrijving: Directe URI naar het mediabestand, verplicht als geldige URI. <https://docs.nde.nl/schema-profile/#MediaObject-contentUrl></b> 
- <b>Waarde: URI</b> 

#### [schema:license](https://schema.org/license)
<b>Scope: </b>Verplicht. 
<b>Beschrijving: Rechtenstatement van de afbeelding, verplicht als URI.</b> 
<b>Waarde: URI</b> 

### Person, Place, Occupation 

Gegevens over het ontstaan van een werk worden in het model weergegeven als volgt.

<!--<pre class="mermaid">-->
```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  dateCreated xsd:string
  temporal* xsd:string
}
class place["Place"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person"]{
  name xsd:string 
  sameAs xsd:anyURI 
  deathDate xsd:string 
  birthDate xsd:string 
}
person --> place: birthPlace
person --> place: deathPlace

creativework --> person: creator
class occupation["Occupation, DefinedTerm"]{
  name xsd:string 
  sameAs xsd:anyURI 
}

person --> occupation: hasOccupation
```
<!--</pre>-->

#### [Person](https://schema.org/Person)
De maker van het werk. In sommige gevallen kan dit een organisatie zijn. 
#### [Occupation](https://schema.org/Occupation)
De rol van de maker van het werk, bv. 'schilder'.
#### [Place](https://schema.org/Place)
De plek waar het werk gemaakt is.
#### [GeoCoordinates](https://schema.org/CreativeWork)
De coördinaten van de plek waar het werk gemaakt is.
#### [AdministrativeArea](https://schema.org/AdministrativeArea)
De provincie waarin de plek zich bevindt.
#### [dateCreated](https://schema.org/dateCreated) and [temporal](https://schema.org/temporal)
Als de datum van de creatie door middel van een ISO-8601 conformerende waarde beschikbaar is, wordt die opgenomen in het veld dateCreated. Zo niet, kan temporal worden gebruikt.

### [MediaObject](https://schema.org/MediaObject)
De link naar beschikbare media van een werk word gemaakt door middel van het MediaObject. 

<!--<pre class="mermaid">-->
```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] 

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license* xsd:string
  copyrightNotice xsd:string
  encodingFormat* xsd:string
}
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
class cpholder["Person"] {
  name xsd:string
  sameAs xsd:anyURI
}
mediaobject --> cpholder:copyrightHolder
```
<!--</pre>-->

#### [license*](https://schema.org/license)
Rechtenstatement vanuit brondata edm:rights.
#### [copyrightNotice](https://schema.org/copyrightNotice)
Rechtenstatement vanuit brondata dc:rights.
#### [copyrightHolder](https://schema.org/copyrightHolder)
Als MediaObjecten onder copyright vallen, kunnen rechthebbenden van een MediaObject worden opgenomen worden door middel van de relatie copyrightHolder.


### [identifier](https://schema.org/identifier)
IDs, bijvoorbeeld PIDs of IDs uit het collectiebeheersysteem die voor context belangrijk zijn kunnen worden toegevoegd door middel van de PropertyValuye klasse. 

<!--<pre class="mermaid">-->
```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class propval["PropertyValue"] {
  propertyID xsd:string
  value xsd:string
  description xsd:string
}
creativework --> propval: identifier
```
<!--</pre>-->

### [additionalType](https://schema.org/additionalType), [material](https://schema.org/material), [genre](https://schema.org/genre), [about](https://schema.org/about)
Beschrijvende gegevens over het werk worden op de volgende manier opgenomen. 

<!--<pre class="mermaid">-->
```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]

class additional["Text*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product*"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> product: material

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> defterm: genre, about
```
<!--</pre>-->
#### [material](https://schema.org/material)
Materiaal dat bij de vervaardiging van het werk gebruikt is.
#### [additionalType](https://schema.org/additionalType)
Aanvullende tekstuele beschrijving, of categorisering van het werk. 
#### [DefinedTerm](https://schema.org/DefinedTerm)
Aanvullende relevante termen via relaties genre en about.

<!--
<script type="module">
	import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
	mermaid.initialize({
		startOnLoad: true,
		theme: 'dark'
	});
</script>
-->