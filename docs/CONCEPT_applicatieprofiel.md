# Applicatieprofiel voor CollectieNederland.nl

# Inhoudsopgave

[Applicatieprofiel voor CollectieNederland.nl
[1](#applicatieprofiel-voor-collectienederland.nl)](#applicatieprofiel-voor-collectienederland.nl)

[1.1 Inleiding [2](#inleiding)](#inleiding)

[Definities [3](#definities)](#definities)

[1.2 Velden voor CollectieNederland.nl
[3](#velden-voor-collectienederland.nl)](#velden-voor-collectienederland.nl)

[1.2.1 Minimale en sterk aanbevolen velden
[3](#minimale-en-sterk-aanbevolen-velden)](#minimale-en-sterk-aanbevolen-velden)

[1.2.2 Overzichtstabel minimale en sterk aanbevolen velden
[3](#overzichtstabel-minimale-en-sterk-aanbevolen-velden)](#overzichtstabel-minimale-en-sterk-aanbevolen-velden)

[1.2.3 Aanbevolen en optionele velden
[5](#aanbevolen-en-optionele-velden)](#aanbevolen-en-optionele-velden)

[1.2.4 Overzichtstabel aanbevolen en optionele velden
[6](#overzichtstabel-aanbevolen-en-optionele-velden)](#overzichtstabel-aanbevolen-en-optionele-velden)

[1.2.5 Afwijkingen ten opzichte van het NDE applicatieprofiel
[7](#afwijkingen-ten-opzichte-van-het-nde-applicatieprofiel)](#afwijkingen-ten-opzichte-van-het-nde-applicatieprofiel)

[1.2.6 Thesauri-gebruik [8](#thesauri-gebruik)](#thesauri-gebruik)

[1.3 CollectieNederland.nl-applicatieprofiel
[9](#collectienederland.nl-applicatieprofiel)](#collectienederland.nl-applicatieprofiel)

[1.3.1 Schema:CreativeWork
[9](#schemacreativework)](#schemacreativework)

[1.3.1.1 schema:name (keuzeveld 1)
[9](#schemaname-keuzeveld-1)](#schemaname-keuzeveld-1)

[1.3.1.2 schema:alternateName \*
[9](#schemaalternatename)](#schemaalternatename)

[1.3.1.3 Schema:creditText\* [10](#schemacredittext)](#schemacredittext)

[1.3.1.4 schema:publisher \* [10](#schemapublisher)](#schemapublisher)

[1.3.1.5 schema:datePublished\*
[10](#schemadatepublished)](#schemadatepublished)

[1.3.1.6 Schema:citation\* [11](#schemacitation)](#schemacitation)

[1.3.1.7 schema:dateCreated (keuzeveld 2)
[11](#schemadatecreated-keuzeveld-2)](#schemadatecreated-keuzeveld-2)

[1.3.1.8 schema:temporal \* [12](#schematemporal)](#schematemporal)

[1.3.1.9 schema:license\* [12](#schemalicense)](#schemalicense)

[1.3.1.10 schema:description (keuzeveld 3)
[12](#schemadescription-keuzeveld-3)](#schemadescription-keuzeveld-3)

[1.3.1.11 schema:size (keuzeveld 3)
[13](#schemasize-keuzeveld-3)](#schemasize-keuzeveld-3)

[1.3.1.12 schema:url [13](#schemaurl)](#schemaurl)

[1.3.1.13 schema:isPartOf \>Dataset *of* \>CreativeWork
[13](#schemaispartof-dataset-of-creativework)](#schemaispartof-dataset-of-creativework)

[1.3.1.14 schema:sdDatePublished
[14](#schemasddatepublished)](#schemasddatepublished)

[1.3.1.15 schema:additionalType (Keuzeveld 1)
[14](#schemaadditionaltype-keuzeveld-1)](#schemaadditionaltype-keuzeveld-1)

[1.3.1.16 Schema:material (keuzeveld 3)
[14](#schemamaterial-keuzeveld-3)](#schemamaterial-keuzeveld-3)

[1.3.1.17 schema:genre [15](#schemagenre)](#schemagenre)

[1.3.1.18 schema:about [15](#schemaabout)](#schemaabout)

[1.3.1.19 schema:identifier [16](#schemaidentifier)](#schemaidentifier)

[1.3.1.20 schema:creator [16](#schemacreator)](#schemacreator)

[1.3.1.21 schema:locationCreated (keuzeveld 3)
[17](#schemalocationcreated-keuzeveld-3)](#schemalocationcreated-keuzeveld-3)

[1.3.1.22 Schema:associatedMedia
[17](#schemaassociatedmedia)](#schemaassociatedmedia)

[1.3.1.23 schema:conditionsOfAccess (verplicht voor Rijksmusea)
[17](#schemaconditionsofaccess-verplicht-voor-rijksmusea)](#schemaconditionsofaccess-verplicht-voor-rijksmusea)

[1.3.2 Schema:MediaObject [18](#schemamediaobject)](#schemamediaobject)

[1.3.2.1 schema:contentUrl [18](#schemacontenturl)](#schemacontenturl)

[1.3.2.2 schema:license (verplicht)
[18](#schemalicense-verplicht)](#schemalicense-verplicht)

[1.3.2.3 schema:thumbnailUrl
[19](#schemathumbnailurl)](#schemathumbnailurl)

[1.3.2.4 schema:copyrightHolder\*
[19](#schemacopyrightholder)](#schemacopyrightholder)

[1.3.2.5 Schema:encodingFormat\*
[19](#schemaencodingformat)](#schemaencodingformat)

[1.3.2.6 schema:copyrightNotice
[19](#schemacopyrightnotice)](#schemacopyrightnotice)

[1.3.3 Schema:Person [20](#schemaperson)](#schemaperson)

[1.3.3.1 schema:name [20](#schemaname)](#schemaname)

[1.3.3.2 Schema:sameAs [20](#schemasameas)](#schemasameas)

[1.3.3.3 Schema:hasOccupation
[21](#schemahasoccupation)](#schemahasoccupation)

[1.3.3.4 Schema:birthDate [21](#schemabirthdate)](#schemabirthdate)

[1.3.3.5 Schema:birthPlace [21](#schemabirthplace)](#schemabirthplace)

[1.3.3.6 Schema:deathDate [21](#schemadeathdate)](#schemadeathdate)

[1.3.3.7 Schema:deathplace [22](#schemadeathplace)](#schemadeathplace)

[1.3.4 schema:GeoCoordinates
[22](#schemageocoordinates)](#schemageocoordinates)

[1.3.4.1 schema:latitude [22](#schemalatitude)](#schemalatitude)

[1.3.4.2 schema:longitude [22](#schemalongitude)](#schemalongitude)

[1.3.5. schema:AdministrativeArea\*
[22](#schemaadministrativearea)](#schemaadministrativearea)

[1.3.5.1 Schema:name [23](#schemaname-1)](#schemaname-1)

[1.3.5.2 Schema:sameAs [23](#schemasameas-1)](#schemasameas-1)

[1.3.6 schema:PropertyValue
[23](#schemapropertyvalue)](#schemapropertyvalue)

[1.3.6.1 schema:propertyID [23](#schemapropertyid)](#schemapropertyid)

[1.3.6.2. schema:value [24](#schemavalue)](#schemavalue)

[1.3.6.3 schema:description
[24](#schemadescription)](#schemadescription)

[1.3.7. schema:Place [24](#schemaplace)](#schemaplace)

[1.3.7.1 Schema:addressRegion\*
[24](#schemaaddressregion)](#schemaaddressregion)

[1.3.7.2 Schema:name [24](#schemaname-2)](#schemaname-2)

[1.3.7.3 Schema:sameAs [25](#schemasameas-2)](#schemasameas-2)

[1.3.8 schema:Occupation, schema:DefinedTerm
[25](#schemaoccupation-schemadefinedterm)](#schemaoccupation-schemadefinedterm)

[1.3.8.1 Schema:name [25](#schemaname-3)](#schemaname-3)

[1.3.8.2 Schema:sameAs [25](#schemasameas-3)](#schemasameas-3)

[1.3.9. schema:DefinedTerm [26](#schemadefinedterm)](#schemadefinedterm)

[1.3.9.1 Schema:name [26](#schemaname-4)](#schemaname-4)

[1.3.9.2 Schema:sameAs [26](#schemasameas-4)](#schemasameas-4)

[1.3.10 schema:Product\* [26](#schemaproduct)](#schemaproduct)

[1.3.10.1 Schema:name [27](#schemaname-5)](#schemaname-5)

[1.3.10.2 Schema:sameAs [27](#schemasameas-5)](#schemasameas-5)

[1.3.11 schema:Text\*, schema:DefinedTerm
[27](#schematext-schemadefinedterm)](#schematext-schemadefinedterm)

[1.3.11.1 Schema:name [27](#schemaname-6)](#schemaname-6)

[1.3.11.2 Schema:sameAs [28](#schemasameas-6)](#schemasameas-6)

# 1.1 Inleiding

In deze documentatie wordt het applicatieprofiel beschreven voor
CollectieNederland.nl. Dit profiel is gebaseerd op het [<u>nieuwe
datamodel voor
Collectienederland.nl</u>](https://github.com/collectienederland/schema-profile),
dat schema.org gebruikt als beschrijvende vocabulaire. Dit model is weer
een uitbreiding
op het [<u>NDE-applicatieprofiel</u>](https://docs.nde.nl/schema-profile/)
([versie 1.4.0](https://docs.nde.nl/schema-profile/#v1.4.0)) en volgt
dit applicatieprofiel grotendeels. Dit document vormt de basis voor de
aanlevervoorwaarden van CollectieNederland.nl

Op enkele punten wijkt het applicatieprofiel voor CollectieNederland.nl
af van het NDE-applicatieprofiel. Het gaat hier altijd om versoepelingen
en aanvullingen ten op zichten van het NDE-applicatieprofiel, nooit om
striktere eisen. Deze punten zijn terug te vinden onder 1.2.5.

De velden die minimaal nodig zijn om data aan te leveren aan
CollectieNederland.nl staan genoteerd onder 1.2. De thesauri die
CollectieNederland.nl aanhoudt zijn terug te vinden onder sectie 1.5.

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

# 1.2 Velden voor CollectieNederland.nl

CollectieNederland.nl is een Nederlands dienstplatform en toont de
collectiedata in het Nederlands. Zorg dat de velden een ‘nl’ of ‘nl-NL’
tag hebben waarin de taal van de data wordt aangegeven.

## 1.2.1 Minimale en sterk aanbevolen velden

Bij het aanleveren van collectiedata aan CollectieNederland.nl wordt
gekeken of de volgende minimale en sterk aanbevolen velden aanwezig zijn
in de data en of de inhoud van deze velden in lijn is met het
NDE-applicatieprofiel en de aanvullende bepalingen ten behoeve van
CollectieNederland.nl. Als er voor een veld een afwijking of
versoepeling geldt, dan is deze leidend ten opzichte van het
NDE-applicatieprofiel. Bij overlap tussen de twee profielen verwijst dit
document door naar het NDE-applicatieprofiel.

## 1.2.2 Overzichtstabel minimale en sterk aanbevolen velden

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

| *Entiteit* | *Veld* | *Betekenis* | *Verplicht* | *Type* |  |
|----|----|----|----|----|----|
| MediaObject | Schema:license | Rechtenstatement afbeelding | Ja, als schema:contentUrl aanwezig is | URI |  |
| CreativeWork | schema:copyrightNotice | Actuele juridische status | Ja, voor Rijksmusea | URI |  |
| CreativeWork | Schema:isPartOf\>schema:Dataset | Beschrijft van welke dataset het object deel uitmaakt | Ja | URI |  |
| CreativeWork | schema:sdDatePublished | Datum van publicatie metadata | Ja | date |  |
| CreativeWork | schema:name | Titel | Keuzeveld 1 – schema:name of schema:additionalType | String |  |
| CreativeWork | schema:additionalType | Soort object | Keuzeveld 1 - schema:name of schema:additionalType | String of URI |  |
| CreativeWork | schema:temporal | Periode van vervaardiging | Keuzeveld 2 – sterk aanbevolen | String |  |
| CreativeWork | schema:dateCreated | Vervaardigingsdatum | Keuzeveld 2 – sterk aanbevolen | Date |  |
| CreativeWork | schema:description | Beschrijving van het object | Keuzeveld 3 – sterk aanbevolen | String |  |
| CreativeWork | schema:material | Materiaal | Keuzeveld 3 – sterk aanbevolen | String/URI |  |
| CreativeWork | schema:size | Afmetingen | Keuzeveld 3 – sterk aanbevolen | String/QuantitativeValue |  |
| CreativeWork | schema:locationCreated | Plaats van productie of vervaardiging | Keuzeveld 3 – sterk aanbevolen | String/URI |  |

## 1.2.3 Aanbevolen en optionele velden

In de onderstaande tabel staat een overzicht van de velden die worden
aanbevolen of optioneel zijn om aan te leveren. In sectie 1.3 worden de
velden toegelicht. In sommige gevallen is het zo dat als een optioneel
veld wordt aangeleverd, er een verplicht veld bijkomt – dat aan het
optionele veld verbonden is. Mocht dit zo zijn dan staat dit per veld
aangegeven in de kolom optioneel/aanbevolen.

## 1.2.4 Overzichtstabel aanbevolen en optionele velden

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

## 1.2.5 Afwijkingen ten opzichte van het NDE applicatieprofiel

In de onderstaande tabellen zijn de verschillen terug te vinden tussen
het CollectieNederland.nl-applicatieprofiel en het
NDE-applicatieprofiel. Het gaat hier in de eerste tabel om verschillen
in de aanwezigheid van Classes en Properties. In de tweede tabel worden
de verschillen aangegeven in Classes en Properties die zowel het
NDE-applicatieprofiel als CollectieNederland.nl-applicatieprofiel
kennen, maar waarbij CollectieNederland.nl een ander verplichtingsniveau
hanteert (bijv. optioneel i.p.v. verplicht) of een andere invulling
geeft.

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

## 1.2.6 Thesauri-gebruik

Wanneer er gebruikt gemaakt wordt van thesaurustermen dan worden de
volgende thesauri aangenomen, afhankelijk van metadata veld: Art &
Architecture Thesaurus (AAT), Cultuurhistorische Thesaurus (CHT),
GeoNames en RKDartists. Al deze thesauri zijn te raadplegen via het
[Termennetwerk](https://termennetwerk.netwerkdigitaalerfgoed.nl/nl).
Bekijk hier een omschrijving van thesaurustermen in het
NDE-applicatieprofiel: [<u>https://docs.nde.nl/schema-profile/#reference-terms.</u>](https://docs.nde.nl/schema-profile/#reference-terms.)

# 1.3 CollectieNederland.nl-applicatieprofiel

Afwijkingen van het NDE-applicatieprofiel zijn gemarkeerd door middel
van een asterisk (\*) en zijn met uitleg terug te vinden in de
bovenstaande sectie 1.2.5.

## 1.3.1 Schema:CreativeWork

De centrale klasse in het CollectieNederland.nl-applicatieprofiel. Met
deze klasse worden cultuurhistorische objecten omschreven in dit
profiel.

### 1.3.1.1 schema:name (keuzeveld 1)

- Beschrijving: titel van het object

- Voorbeeld: De nachtwacht

- Verplicht: verplicht - keuzeveld 1

- Technische verwijzing

  - Formaat: string

  - Kardinaliteit: 0..1

  - [<u>https://docs.nde.nl/schema-profile/#CreativeWork-name</u>](https://docs.nde.nl/schema-profile/).

### 1.3.1.2 schema:alternateName \*

- Beschrijving: alternatieve titel van het object

- Voorbeeld:

  - De scheeuw

  - Skrik

- Verplicht: optioneel

- Technische verwijzing

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://schema.org/alternateName>

    - Uitbreiding NDE-applicatieprofiel om musea de mogelijkheid te
      geven om objecten meerdere titels mee te geven zoals toegekende
      titel of originele titel.

### 1.3.1.3 Schema:creditText\*

- Beschrijving: geassocieerde persoon of organisatie die is gerelateerd
  aan het object.

- Voorbeeld:

  - name: Otto Frank

  - sameAs: <http://data.beeldengeluid.nl/gtaa/99929>

- Verplicht: optioneel

- Technische verwijzing:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://schema.org/creditText>

    - Uitbreiding NDE-applicatieprofiel voor generieke
      attributie-/credittekst. Let op: voor het specifieke geval
      eigendomsgeschiedenis is dit veld juist afgeraden (te weinig
      gestructureerd) — hier gaat het om een breder, algemeen gebruik.

### 1.3.1.4 schema:publisher \*

- Beschrijving: uitgever van een boek, tijdschrift of artikel.

- Voorbeeld: Uitgeverij Noordzon

- Verplicht: optioneel

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0.. 1

  - <https://schema.org/publisher>

    - Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die
      ook boeken, artikelen of andere objecten hebben in de
      museumcollectie.

### 1.3.1.5 schema:datePublished\*

- Beschrijving: datum waarop het object is uitgegeven door de uitgever.

- Voorbeeld: 2010-11-02

- Verplicht: optioneel

- Technisch:

  - Formaat: date, conform ISO-8601

  - Kandinaliteit: 0..1

  <!-- -->

  - <https://schema.org/datePublished>

    - Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die
      ook boeken, artikelen of andere objecten hebben in de
      museumcollectie.

### 1.3.1.6 Schema:citation\*

- Beschrijving: referentie naar een publicatie of boek.

- Voorbeeld: van den Boorn, G.P.F. and Van Es, M.J. (1989), Recent
  Acquisitions: II. The Near East. OMROL 69, blz. 13

- Verplicht: optioneel

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0.. \*

  - <https://schema.org/citation>

    - Uitbreiding op het NDE-applicatieprofiel voor verwijzingen naar
      publicaties of boeken die aan een object gerelateerd zijn.

### 1.3.1.7 schema:dateCreated (keuzeveld 2)

- Beschrijving: vervaardigingsdatum van het object.

- Bijvoorbeeld

  - 1955-06-21

  - 1658-05

  - 1658

- Verplicht: sterk aanbevolen, keuzeveld 2

- Technische

  - Formaat: date, conform
    [ISO-8601](http://www.iso.org/iso/catalogue_detail?csnumber=40874)

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-dateCreated>

### 1.3.1.8 schema:temporal \*

- Beschrijving: onzekerheidsaanduiding datering als vrije tekst

- Bijvoorbeeld:

  - Ca.

  - Circa

  - Ongeveer

- Verplicht: sterk aanbevolen

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..\*

  - <https://schema.org/temporal>

    - Toevoeging op het NDE-applicatieprofiel, vanwege collecties die
      geen datering hebben, maar uit een bepaalde periode komen zoals
      archeologische opgravingen.

### 1.3.1.9 schema:license\*<span class="mark"></span>

- Beschrijving: rechtenstatement van het object zelf (URI). Uitsluitend
  rechtenstatements van Rightstatements.org.

- Voorbeeld: http://rightsstatements.org/vocab/InC/1.0/

- Verplicht: aanbevolen

- Technisch:

  - Formaat: URL volgens Rightstatements.org

  - Kardinaliteit: 0..1

  - <https://schema.org/license>

### 1.3.1.10 schema:description (keuzeveld 3)

- Beschrijving: beschrijving van het object.

- Voorbeeld: Schilderij van een ridderzaal met een tafel met buffet. Aan
  beide zijde van de tafel een ridder in harnas.

- Verplicht: sterk aanbevolen, keuzeveld 3.

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-description>.

### 1.3.1.11 schema:size (keuzeveld 3)

- Beschrijving: afmeting van het object in hoogte x breedte x diepte in
  cm als een waarde.

- Voorbeeld: 24,5 × 20,5 x 4 cm

- Verplicht: sterk aanbevolen, keuzeveld 3

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - [<u>https://docs.nde.nl/schema-profile/#CreativeWork-size</u>](https://docs.nde.nl/schema-profile/)

### 1.3.1.12 schema:url 

- Beschrijving: link naar het object bij de website van de bronhouder.

- Voorbeeld:

  - [*http://hdl.handle.net/10934/RM0001.COLLECT.250239*](http://hdl.handle.net/10934/RM0001.COLLECT.250239)

  - <https://muiderslot.adlibhosting.com/details/museum/10000349>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: URL

    - Valide URL

    - Bij voorkeur een PID

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-URI>

### 1.3.1.13 schema:isPartOf \>Dataset *of* \>CreativeWork

- Beschrijving: Dataset of deelcollectie waartoe het object behoort

- Voorbeeld: Rijksmuseum of NK-collectie

- Verplicht: Verplicht in het geval van de Dataset, aanbevolen voor een
  deelcollectie (bij CreativeWork)

- Technisch:

  - Formaat: Dataset (URI) or CreativeWork (URI)

  - Kardinaliteit: 1..\* en 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf>

### 1.3.1.14 schema:sdDatePublished

- Beschrijving: de datum waarop de metadata is gepubliceerd

- Voorbeeld: 2026-01-30

- Verplicht: verplicht

- Technisch:

  - Format: date, conform ISO-8601

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-sdDatePublished>

### 1.3.1.15 schema:additionalType (Keuzeveld 1)

- Beschrijving: soort object

- Voorbeeld:

  - tekening

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/eb9e1e5b-b319-4519-a4f5-0dd26dbf4524>

- Verplicht: verplicht, keuzeveld 1

- Technische verwijzing

  - Formaat: term en/of URI

  - Thesauri: de CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-additionalType>

### 1.3.1.16 Schema:material (keuzeveld 3)

- Beschrijving: materiaal waaruit het object bestaat

- Voorbeeld:

  - metalen

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/b9fd0887-297b-4bab-bea5-cb288d068816>

- Verplicht: sterk aanbevolen, keuzeveld 3

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.1.17 schema:genre 

- Beschrijving: onderwerp van het afgebeelde op het object

- Voorbeeld:

  - bevrijding

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/ac43187b-02fa-45ab-b1d6-86a02860db1f>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-genre>

### 1.3.1.18 schema:about 

- Beschrijving: geassocieerde persoon of concept

- Voorbeeld:

  - Frank, Anne (1929-1945)

  - sameAs: <http://data.bibliotheken.nl/id/thes/p107412225>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

    - Aanbevolen thesauri: CHT, AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-about>

### 1.3.1.19 schema:identifier 

- Beschrijving: identificatienummer of objectnummer.

  - Bij voorkeur een PID

- Bijvoorbeeld:

  - MA-2017-0054

  - Value: http://identifiers.org/viaf:176354386

  - PropertyID:
    [*http://hdl.handle.net/10934/RM0001.COLLECT.250239*](http://hdl.handle.net/10934/RM0001.COLLECT.250239)

- Verplicht: aanbevolen

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-identifier>

    - Versoepeling, waardoor bronhouders een PID, URL of objectnummer
      kunnen aanleveren. Nog niet alle bronhouders hebben de financiële
      middelen om een PID module te implementeren.

### 1.3.1.20 schema:creator 

- Beschrijving: vervaardiger van het object

- Bijvoorbeeld:

  - Gogh, van Vincent

  - <https://data.rkd.nl/artists/351830>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: RKD artist

  - Kandinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-creator>

    - Versoepeling van het NDE-applicatieprofiel, vanwege collecties
      waarbij geen vervaardiger bekend is, zoals archeologische
      collecties.

### 1.3.1.21 schema:locationCreated (keuzeveld 3)

- Beschrijving: plaats van vervaardiging of productie.

- Voorbeeld:

  - Alkmaar

  - sameAs: <https://sws.geonames.org/2759899/>

- Verplicht: sterk aanbevolen, keuzeveld 3

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: GeoNames

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-locationCreated>

### 1.3.1.22 Schema:associatedMedia

- Beschrijving: Afbeeldingen (MediaObjects) die het CreativeWork
  representeren.

- Voorbeeld:
  <https://medialib.naturalis.nl/file/id/RMNH.ART.730/format/large>

- Verplicht: aanbevolen, let op: schema:license is verplicht bij dit
  veld

- Technisch:

  - Format: URI

    - Valide URI.

    - Afbeelding, video, audio en/of 3D model

  - Kardinaltieit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-associatedMedia>

### 1.3.1.23 schema:conditionsOfAccess (verplicht voor Rijksmusea)

- Beschrijving: juridische status voor collecties bij Rijksmusea.

- Voorbeeld: *Waarde moet nog bepaald worden*

- Verplicht: verplicht voor Rijksmusea

- Status: alleen verplicht voor Rijksmusea volgens de Erfgoedwet. Dit
  veld wordt niet getoond op CollectieNederland.nl.

- Technische verwijzing:

  - Formaat: string

  - Kardinaliteit: 1..1

  - <https://schema.org/conditionsOfAccess>

<span class="mark">\
</span>1.3.2 Schema:MediaObject
-------------------------------

Afbeelding, video, audio en/of 3D model die het object of object
representeert. Het aanleveren van afbeeldingen wordt sterk aanbevolen.

### 1.3.2.1 schema:contentUrl 

- Beschrijving: directe URI naar het mediabestand (afbeelding, video,
  audio en/of 3D model), verplicht als valide URI.

- Voorbeeld:
  <https://medialib.naturalis.nl/file/id/RMNH.ART.730/format/large>

- Verplicht: aanbevolen, let op: schema:license en schema:thumbnailUrl
  zijn verplicht bij schema:contentUrl

- Technisch:

  - Format: URI

    - Valide URI.

    - Afbeelding, video, audio en/of 3D model

  - Kardinaltieit: 0..\*

  - <https://docs.nde.nl/schema-profile/#MediaObject-contentUrl>

### 1.3.2.2 schema:license (verplicht)

- Beschrijving: rechtenstatement van de **afbeelding** van
  rightsstatements.org

- Voorbeeld: <http://rightsstatements.org/vocab/InC/1.0/>

- Verplicht: ja, bij schema:contentUrl

- Technisch:

  - Format: URI van rechtenstatements.org

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#MediaObject-license>

### 1.3.2.3 schema:thumbnailUrl

- Beschrijving: verkleind formaat van de afbeelding

- Voorbeeld:
  <https://collectie.wereldmuseum.nl/cc/imageproxy.ashx?filename=images/Images/TM//tm-30057342.jpg>

- Verplicht: Verplicht

- Technisch:

  - Format: URI

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#MediaObject-thumbnailUrl>

### 1.3.2.4 schema:copyrightHolder\*

- Beschrijving: rechthebbende van de afbeelding.

- Voorbeeld: Collectie Centraal Museum Utrecht / foto Adriaan van Dam* *

- Voorbeeld URI: <https://rkd.nl/artists/527987>

- Verplicht: optioneel

- Technisch:

  - Format: string

  - SameAs: URI

  - Kardinaliteit: 0..\*

  - <https://schema.org/copyrightHolder>

###  Schema:encodingFormat\*

- Beschrijving: type media van MediaObject

- Voorbeeld: image/png* *

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..\*

  - <https://schema.org/encodingFormat>

###  schema:copyrightNotice

- Beschrijving: Rechtenstatement vanuit brondata

- Voorbeeld: *©* 2025 Collectie Museum Amsterdam, met toestemming van
  Foto graaf

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#MediaObject-copyrightNotice>

## 1.3.3 Schema:Person

### 1.3.3.1 schema:name

- Beschrijving: naam van vervaardiger als persoon of organisatie

- Voorbeeld:

  - name: Gogh, van V.

  - name: Gazelle b.v.

- Verplicht: aanbevolen

- Technisch:

  - Format: string

  - Kardinaliteit 0..1

  - <https://docs.nde.nl/schema-profile/#Person-name>

    - Afwijking van het NDE-applicatieprofiel. De meeste
      collectieinformatiesystemen registeren vervaardigers in hetzelfde
      veld, maar geven een extra waarde mee als rol van de vervaardiger.

    - Als er een persoon of organisatie
      (**schema:Person** en **schema:Organisation**) aanwezig is en
      geregistreerd in verschillende velden, zijn de volgende velden
      verplicht:

      - <https://docs.nde.nl/schema-profile/#Person-name>

      - <https://docs.nde.nl/schema-profile/#Organization-name>

### Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld: <https://data.rkd.nl/artists/351830>

- Aanbevolen thesauri: RKD artist, CHT, AAT, Geonames

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 1.3.3.3 Schema:hasOccupation

- Beschrijving: rol van de vervaardiger

- Voorbeeld:

  - ontwerper

  - sameAs:
    https://data.cultureelerfgoed.nl/term/id/cht/e8f8e3d0-761f-4dda-b846-64f860cdc670

- Verplicht: optioneel

- Technisch:

  - Format: URI

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit 0.. \*

  - <https://docs.nde.nl/schema-profile/#Person-hasOccupation>

### 1.3.3.4 Schema:birthDate

- Beschrijving: geboortedatum van de vervaardiger

- Voorbeeld: 1890-03-20

- Verplicht: optioneel

- Technisch:

  - Format: date, conform ISO-8601

  - Kardinalietit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-birthDate>

### 1.3.3.5 Schema:birthPlace

- Beschrijving: geboorteplaats van de vervaardiger

- Voorbeeld:

  - Leiden

  - sameAs: <https://www.geonames.org/2751773/leiden.html>

- Verplicht: optioneel

- Technisch:

  - Format: string and URI

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-birthPlace>

### 1.3.3.6 Schema:deathDate

- Beschrijving: sterfdatum van de vervaardiger

- Voorbeeld: 1945-03-02

- Verplicht: optioneel

- Technisch:

  - Format: Date conform ISO-8601

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-deathDate>

### 1.3.3.7 Schema:deathplace 

- Beschrijving: sterfplaats van de vervaadiger

- Voorbeeld:

  - Leiden

  - sameAs: <https://www.geonames.org/2751773/leiden.html>

- Verplicht: optioneel

- Technisch:

  - Format: string and URI

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-deathPlace>

## 1.3.4 schema:GeoCoordinates

Optionele geografische coördinaten van een plek. Onderstaande properties
zijn verplicht als schema:GeoCoordinates aanwezig is.

### 1.3.4.1 schema:latitude

- Beschrijving: breedtegraad van de vindplaats of locatie van
  vervaardiging

- Voorbeeld: 52.379189

- Verplicht: verplicht als GeoCoordinates aanwezig is.

- Technisch:

  - Format: string

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-latitude>

### 1.3.4.2 schema:longitude

- Beschrijving: lengtegraad van de vindplaats of vervaardiging

- Voorbeeld: 4.899431

- Verplicht: verplicht als geoCoordinates aanwezig is.

- Technisch:

  - Format: string

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-longitude>

## 1.3.5. schema:AdministrativeArea\*

Optionele provincie waarin de plek zich bevindt.

<https://schema.org/AdministrativeArea>

### 1.3.5.1 Schema:name

- Beschrijving: naam van de plek

- Voorbeeld: Zuid-Holland

- Verplicht: verplicht als schema:AdministrativeArea aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.5.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames (voor schema:AdministrativeArea)

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.6 schema:PropertyValue

IDs, bijvoorbeeld PIDs of IDs uit het collectiebeheersysteem die voor
context belangrijk zijn, kunnen worden toegevoegd door middel van deze
PropertyValue klasse.

<https://schema.org/PropertyValue>

### 1.3.6.1 schema:propertyID

- Beschrijving: *waarde moet nog bepaald worden*

- Voorbeeld: *waarde moet nog bepaald worden*

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/propertyID>

### 1.3.6.2. schema:value

- Beschrijving: *waarde moet nog bepaald worden*

- Voorbeeld: *waarde moet nog bepaald worden*

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/value>

### 1.3.6.3 schema:description

- Beschrijving: *waarde moet nog bepaald worden*

- Voorbeeld: *waarde moet nog bepaald worden*

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/description>

## 1.3.7. schema:Place

### 1.3.7.1 Schema:addressRegion\*

- Beschrijving: provincie waar het object zich bevindt.

- Voorbeeld:

  - name: Gelderland

  - sameAs: <https://www.geonames.org/2755634/provincie-gelderland.html>

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/AdministrativeArea>

  - <https://schema.org/addressRegion>

<span class="mark"></span>

### 1.3.7.2 Schema:name

- Beschrijving: naam van de plek

- Voorbeeld: Zuid-Holland

- Verplicht: verplicht als schema:Place aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.7.3 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames (voor schema:AdministrativeArea)

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 

## 1.3.8 schema:Occupation, schema:DefinedTerm

De rol van de vervaardiger van het object, bv. ‘schilder’.

### 1.3.8.1 Schema:name

- Beschrijving: naam van de rol

- Voorbeeld: schilder

- Verplicht: verplicht als schema:Occupation aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Person-hasOccupation>

### 1.3.8.2 Schema:sameAs

- Beschrijving: schilder

- Voorbeeld: <http://vocab.getty.edu/page/aat/300025136>

- Aanbevolen thesauri: AAT, CHT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.9. schema:DefinedTerm

Aanvullende relevante termen via relaties genre en about.

<https://docs.nde.nl/schema-profile/#reference-terms>

### 1.3.9.1 Schema:name

- Beschrijving: naam van de plek (als voorbeeld)

- Voorbeeld: Zuid-Holland

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit 0..\*

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.9.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames, AAT, CHT, RKDArtists

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.10 schema:Product\*

Materiaal dat bij de vervaardiging van het object gebruikt is.

<https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.10.1 Schema:name

- Beschrijving: naam van het material

- Voorbeeld: canvas

- Verplicht: verplicht als schema:material aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.10.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://data.cultureelerfgoed.nl/term/id/cht/1040c581-3cbb-48c9-91b1-d529573bed98>

- Aanbevolen thesauri: CHT, AAT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 

## 1.3.11 schema:Text\*, schema:DefinedTerm

Aanvullende tekstuele beschrijving, of categorisering van het object.

### 1.3.11.1 Schema:name

- Beschrijving: Aanvullende tekstuele beschrijving, of categorisering
  van het object.

- Voorbeeld: Canvas

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit 0..\*

  - <https://schema.org/name>

### 1.3.11.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://data.cultureelerfgoed.nl/term/id/cht/1040c581-3cbb-48c9-91b1-d529573bed98>

- Aanbevolen thesauri: CHT, AAT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>
