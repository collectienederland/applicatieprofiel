# CollectieNederland.nl Applicatieprofiel 

## Inleiding

In deze documentatie wordt het applicatieprofiel beschreven voor CollectieNederland.nl. Dit profiel beschrijft hoe bronhouders het nieuwe datamodel voor Collectienederland.nl kunnen toepassen. Het applicatieprofiel maakt gebruik van [Schema.org](https://schema.org/) als beschrijvende vocabulaire. Dit applicatieprofiel is een uitbreiding op het [NDE-applicatieprofiel](https://docs.nde.nl/schema-profile/) ([versie 1.4.0](https://docs.nde.nl/schema-profile/#v1.4.0)) en volgt dit applicatieprofiel grotendeels. Dit document vormt de basis voor de aanlevervoorwaarden van [CollectieNederland.nl](https://www.collectienederland.nl/).

Op enkele punten wijkt het applicatieprofiel voor CollectieNederland.nl af van het NDE-applicatieprofiel. Het gaat hier altijd om versoepelingen en aanvullingen ten op zichte van het NDE-applicatieprofiel, nooit om striktere eisen. Deze punten zijn terug te vinden onder <a href="#afwijkingen-ten-opzichte-van-het-nde-applicatieprofiel">Afwijkingen ten opzichte van het NDE applicatieprofiel</a>.

De velden die minimaal nodig zijn om data aan te leveren aan CollectieNederland.nl staan genoteerd onder <a href="#minimale-en-sterk-aanbevolen-velden">Minimale en sterk aanbevolen velden</a>. De thesauri die CollectieNederland.nl aanhoudt zijn terug te vinden onder <a href="#thesauri-gebruik">Thesauri-gebruik</a>.

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
schema:name en schema:description). Deze worden gebruikt om te bepalen
welke entiteiten toegestaan zijn in het applicatieprofiel.

**Verplichtingsniveau:**

- **Verplicht**: de waarden die altijd moeten worden aangeleverd

- **Aanbevolen**: de waarden waarvan wordt aanbevolen dat ze worden aangeleverd

- **Optioneel:** de waarden die mogen worden aangeleverd

## Velden voor CollectieNederland.nl

CollectieNederland.nl is een Nederlands dienstplatform en toont de collectiedata in het Nederlands. Zorg dat de velden een ‘nl’ of ‘nl-NL’ tag hebben waarin de taal van de data wordt aangegeven.

### Velden

Bij delen van collectiedata aan CollectieNederland.nl wordt gekeken of de minimale velden aanwezig zijn in de data en of de inhoud van deze velden in lijn is met het NDE-applicatieprofiel en de aanvullende bepalingen ten behoeve van CollectieNederland.nl. Als er voor een  veld een afwijking of versoepeling geldt, dan is deze leidend ten opzichte van het NDE-applicatieprofiel. Bij overlap tussen de twee profielen verwijst dit document door naar het NDE-applicatieprofiel. Afwijkingen en versoepelingen worden toegelicht bij de properties. 

#### Minimale publicatievoorwaarden

In de onderstaande tabel staat een overzicht van de verplichte velden voor publicatie op CollectieNederland.nl.

| *Entiteit* | *Veld* | *Betekenis* | *Verplicht* | *Type* |
|----|----|----|----|----|
| Schema:CreativeWork | Schema:isPartOf | Beschrijft van welke dataset het object deel uitmaakt | Ja | URI |
| Schema:CreativeWork | schema:sdDatePublished | Datum van publicatie metadata | Ja | date |
| Schema:CreativeWork | schema:name | Titel | Ja | String |
| Schema:CreativeWork | schema:additionalType | Soort object | Ja, als er geen titel beschikbaar is| String of URI |
| Schema:CreativeWork | schema:copyrightNotice | Actuele juridische status |  Alleen Rijksmusea | String |
| Schema:CreativeWork | schema:LEEEG | Conditiestatus | Alleen Rijksmusea| String 

### Thesauri-gebruik

Wanneer er gebruikt gemaakt wordt van thesaurustermen dan worden de volgende thesauri aangenomen, afhankelijk van metadata veld: Art & Architecture Thesaurus (AAT), Cultuurhistorische Thesaurus (CHT), GeoNames en RKDartists. Al deze thesauri zijn te raadplegen via het [Termennetwerk](https://termennetwerk.netwerkdigitaalerfgoed.nl/nl). Bekijk hier een omschrijving van thesaurustermen in het NDE-applicatieprofiel: [NDE-applicatieprofiel](https://docs.nde.nl/schema-profile/#reference-terms).

## Datamodel

Afwijkingen van het NDE-applicatieprofiel zijn gemarkeerd door middel van een asterisk (\*) en zijn met uitleg terug te vinden in de bovenstaande sectie 1.2.5. Hieronder is een overzicht van het datamodel te zien. Als centrale klasse word [CreativeWork](https://schema.org/CreativeWork) gebruikt.

<!--```mermaid-->
<pre class="mermaid">
---
  config:
    theme: forest
    nodeSpacing: 50
    rankSpacing: 150
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  alternateName xsd:string 
  citation xsd:string 
  copyrightNotice xsd:string
  creditText xsd:string 
  datePublished xsd:string 
  dateCreated xsd:string 
  description xsd:string 
  isPartOf xsd:anyURI 
  license xsd:string 
  name xsd:string 
  publisher xsd:string 
  sdDatePublished xsd:date 
  size xsd:string 
  temporal xsd:string 
  url xsd:anyURI 
}

creativework --> "0..*" creativework: hasPart

class additional["DefinedTerm, URL"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> "0..1" additional: additionalType

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> "0..1" defterm: genre, about, material
class place["Place"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> "0..1" place: locationCreated
place --> "0..1" geocoor: geo
place --> "0..*" adminarea: addressRegion

class person["Person"]{
  name xsd:string 
  sameAs xsd:anyURI 
  deathDate xsd:string  
  birthDate xsd:string 
}
creativework --> "0..1" person: creator
person --> "0..1" place: birthPlace
person --> "0..1" place: deathPlace

class occupation["Occupation"]{
  name xsd:string 
  sameAs xsd:anyURI 
}
person --> "0..1" occupation: hasOccupation

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license xsd:string
  copyrightNotice xsd:string
  encodingFormat* xsd:string
}
creativework --> "0..*" mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> "0..1" person:copyrightHolder
creativework --> "0..1" person:copyrightHolder

class propval["PropertyValue"] {
  propertyID xsd:string
  value xsd:string
  description xsd:string
}

creativework --> "0..*" propval: identifier
</pre>
<!--```-->

### [CreativeWork](http://schema.org/CreativeWork)

De centrale klasse in het CollectieNederland.nl-applicatieprofiel. Met deze klasse worden cultuurhistorische objecten omschreven in dit profiel. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork).

#### [schema:name](https://schema.org/name) (verplicht)
<i>Verplicht, tenzij deze niet aanwezig is, dan is [schema:additionalType](https://schema.org/additionalType) verplicht. </i>
- <b>Beschrijving:</b> titel van het object
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> Zie [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-name) voor meer informatie en voorbeelden.

#### [schema:additionalType](https://schema.org/additionalType) (verplicht)
<i>Verplicht, als [schema:name](https://schema.org/name) niet aanwezig is. </i>
- <b>Beschrijving:</b> Specifiek type van het werk (bijv. schilderij). Als de DefinedTerm een URI bevat, moet die verwijzen naar één van de volgende thesauri: de CHT of AAT.
- <b>Datatype:</b> [DefinedTerm](#DefinedTerm) en[URL](https://schema.org/URL)
- <b>Kardinaliteit:</b> 0..* ???

- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "additionalType": {
    "@type": ["DefinedTerm", "URL"],
    "name": "tekening",
    "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/eb9e1e5b-b319-4519-a4f5-0dd26dbf4524"
  }
}
```

#### [schema:associatedMedia](https://schema.org/associatedMedia)
<i>Optioneel. </i>
- <b>Beschrijving:</b> Gerelateerde media. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#MediaObject)
- <b>Datatype:</b> [MediaObject](#MediaObject)
- <b>Kardinaliteit:</b> 0..* 

#### [schema:material](https://schema.org/material)
<i>Aanbevolen</i><br/>
- <b>Beschrijving:</b> materiaal waaruit het object bestaat. Als de DefinedTerm een URI bevat, moet die verwijzen naar één van de volgende thesauri: de CHT of AAT. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-material)
- <b>Datatype:</b> [DefinedTerm](#DefinedTerm) 
- <b>Kardinaliteit:</b> 0..* 
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "material": {
    "@type": "DefinedTerm",
    "name": "metalen",
    "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/b9fd0887-297b-4bab-bea5-cb288d068816"
  }
}
```

#### [schema:genre](https://schema.org/genre)
<i>Aanbevolen</i><br/>
- <b>Beschrijving:</b> Onderwerp van het afgebeelde op het object. Als de DefinedTerm een URI bevat, moet die verwijzen naar één van de volgende thesauri: de CHT of AAT. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-genre)
- <b>Datatype:</b> [DefinedTerm](#DefinedTerm) 
- <b>Kardinaliteit:</b> 0..* 
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "genre": {
    "@type": "DefinedTerm",
    "name": "bevrijding"@nl,
    "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/ac43187b-02fa-45ab-b1d6-86a02860db1f"
  }
}
```

#### [schema:alternateName](https://schema.org/alternateName)
<i>Optioneel</i><br/>
<br/><i>Uitbreiding NDE-applicatieprofiel om musea de mogelijkheid te geven om objecten meerdere titels mee te geven zoals toegekende titel of originele titel.</i><br/>
- <b>Beschrijving:</b> alternatieve titel van het object
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> 
``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "De Schreeuw"@nl,
  "alternateName": "Skrik"@no,
}
```

#### [schema:copyrightNotice](https://schema.org/copyrightNotice) (verplicht voor Rijksmusea)
- <b>Beschrijving:</b> Actuele juridische status 
- <b>Waarde:</b> *Waarde moet nog bepaald worden*

#### [schema:isPartOf](https://schema.org/isPartOf) (verplicht)
- <b>Beschrijving:</b> Dataset waartoe het werk behoort
- <b>Waarde:</b> Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf)
- <b>Datatype:</b> URI
- <b>Kardinaliteit:</b> 1..1
- <b>Voorbeeld:</b> 
``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "isPartOf": "https://linkeddata.cultureelerfgoed.nl/rce/datacatalog/id/dataset/db6193aa-84af-3edf-90fd-074a0a11248d"
}
```

#### [schema:hasPart](https://schema.org/hasPart) 
<i>Optioneel</i><br/>
<br/><i>Uitbreiding op het NDE-applicatieprofiel voor ensembles.</i><br/>

- <b>Beschrijving:</b> Onderdelen waaruit het object bestaat.
- <b>Datatype:</b> URI
- <b>Kardinaliteit:</b> 0..*
- <b>Voorbeeld:</b> 
``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "hasPart": "MA-2020.001
MA.2020.002
MA.2020.003",
}
```

#### [schema:publisher](https://schema.org/publisher) 
<i>Optioneel</i><br/>
<br/><i>Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die ook boeken, artikelen of andere objecten hebben in de museumcollectie.</i><br/>
- <b>Beschrijving:</b> uitgever van een boek, tijdschrift of artikel. 
- <b>Datatype:</b> string
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "publisher": "Uitgeverij Noordzon"@nl,
}
```

#### [schema:temporal](https://schema.org/temporal)
<i>Optioneel</i><br/>
<br/><i>Uitbreiding op het NDE-applicatieprofiel, vanwege collecties diegeen datering hebben, maar uit een bepaalde periode komen zoals archeologische opgravingen.</i><br/>
- <b>Beschrijving:</b> onzekerheidsaanduiding datering als vrije tekst, bijvoorbeeld:
  - Ca.
  - Circa
  - Ongeveer
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@id": "https://www.wikidata.org/wiki/Q185372",
  "@type": "CreativeWork",
  "temporal": "circa 1665"@nl
}
```

#### [schema:datePublished](https://schema.org/datePublished)
<i>Optioneel</i><br/>
<br/><i>Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die ook boeken, artikelen of andere objecten hebben in de museumcollectie.</i><br/>
- <b>Beschrijving:</b> datum waarop het object is uitgegeven door de uitgever.
- <b>Datatype:</b> date, conform ISO-8601

#### [schema:sdDatePublished](https://schema.org/sdDatePublished) (verplicht)
- <b>Beschrijving:</b> datum van de laatste wijziging van de object-metadata, Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-sdDatePublished).
- <b>Datatype:</b> date, conform ISO-8601

#### [schema:citation](https://schema.org/citation)
<i>Optioneel</i><br/> 
<br/><i>Uitbreiding op het NDE-applicatieprofiel voor verwijzingen naar publicaties of boeken die aan een object gerelateerd zijn.</i><br/>
- <b>Beschrijving:</b> referentie naar een publicatie of boek.
- <b>Datatype:</b> string
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "citation": "van den Boorn, G.P.F. and Van Es, M.J. (1989), Recent Acquisitions: II. The Near East. OMROL 69, blz. 13"@nl,
}
```

#### [schema:url](https://schema.org/url)
<i>Aanbevolen</i><br/> 
- <b>Beschrijving:</b> CollectieNederland.nl toont de gegevens van jouw object. Wanneer een bezoeker meer informatie over het object wil bekijken, kan diegene via deze link naar de webpagina van jouw organisatie gaan. Gebruik bij voorkeur een URI of gebruik een PID als die beschikbaar is.
- <b>Datatype:</b> URI
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b>
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "url": "http://hdl.handle.net/10934/RM0001.COLLECT.250239",
}
```

#### [schema:license](https://schema.org/license)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> rechtenstatement van het object zelf (URI). Uitsluitend rechtenstatements van Rightstatements.org.
- <b>Datatype:</b> URI
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> 
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "license": "http://rightsstatements.org/vocab/InC/1.0/",
}
```

#### [schema:description](https://schema.org/description)
<i>Aanbevolen</i><br/>
- <b>Beschrijving:</b> beschrijving van het object. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-description).
- <b>Voorbeeld:</b>
```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "description": "Schilderij van een ridderzaal met een tafel met buffet. Aan beide zijde van de tafel een ridder in harnas."@nl,
}
```

#### [schema:size](https://schema.org/size)
<i>Aanbevolen</i><br/>
- <b>Beschrijving:</b> afmeting van het object in hoogte x breedte x diepte in
  cm als een waarde.
- <b>Datatype:</b> string
- [Meer informatie](https://docs.nde.nl/schema-profile/#CreativeWork-size)

```
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "size": "24,5 × 20,5 x 4 cm"@nl,
}
```

#### [schema:creditText](https://schema.org/creditText)
<i>Optioneel</i><br/> 
<br/><i>Uitbreiding NDE-applicatieprofiel voor generieke attributie-/credittekst. Let op: voor het specifieke geval eigendomsgeschiedenis is dit veld juist afgeraden (te weinig gestructureerd) — hier gaat het om een breder, algemeen gebruik.</i><br/>

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

#### [schema:creator](https://schema.org/creator)
<i>Aanbevolen</i><br/> 
- <b>Beschrijving</b>: de vervaardiger van het object. Dat kan een persoon of organisatie zijn. , zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#CreativeWork-creator).
- <b>Datatype:</b> [Person](#Person).
- <b>Kardinaliteit:</b> 0..1
<hr/>

### [Person](https://schema.org/Person)

 Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#Person).

#### [schema:name](https://schema.org/name)
<i>Aanbevolen</i><br/>
- <b>Beschrijving:</b>  Naam van de persoon of organisatie
- <b>Datatype:</b> string
- <b>Kardinaliteit:</b> 1..1
- <b>Voorbeeld:</b> Zie [documentatie van het NDE](https://docs.nde.nl/schema-profile/#Person-name) voor meer informatie en voorbeelden.

#### [schema:sameAs](https://schema.org/sameAs)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b>  Relatie naar een thesaurusterm. Aanbevolen thesauri: RKD artist, CHT, AAT, Geonames.
- <b>Datatype:</b> URI
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#CreativeWork-sameAs)

#### [schema:deathDate](https://schema.org/deathDate)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b>  
- <b>Datatype:</b> date
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Person-deathDate)

#### [schema:birthDate](https://schema.org/birthDate)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Geboortedatum van de vervaardiger 
- <b>Datatype:</b> date, conform ISO-8601
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Person-birthDate)

#### [schema:birthPlace](https://schema.org/birthPlace)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Geboorteplaats van de vervaardiger.
- <b>Datatype:</b> [Place](#Place). 
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Person-birthPlace)

#### [schema:deathPlace](https://schema.org/deathPlace)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Sterfplaats van de vervaadiger. 
- <b>Datatype:</b> [Place](#Place). 
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Person-deathPlace)

#### [schema:hasOccupation](https://schema.org/hasOccupation)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Rol van de vervaardiger. Aanbevolen thesauri: CHT of AAT
- <b>Datatype:</b> [Occupation](#Occupation). 
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Person-hasOccupation)
- <b>Voorbeeld:</b>
``` 
{
  "@context": "https://schema.org",
  "@type": "Person",
  "hasOccupation": {
    "@type": "Occupation",
    "name": "ontwerper"@nl,
    "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/e8f8e3d0-761f-4dda-b846-64f860cdc670"
  }
}
```

<hr/>

### [MediaObject](https://schema.org/MediaObject)
Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#MediaObject).

#### [schema:contentUrl](https://schema.org/contentUrl)
<i>Verplicht</i><br/><br/> 
- <b>Beschrijving:</b>  Directe URI naar het mediabestand, verplicht als geldige URI. <https://docs.nde.nl/schema-profile/#MediaObject-contentUrl>
- <b>Datatype:</b>  URI 
- <b>Kardinaliteit:</b> 1..1

#### [schema:thumbnailUrl](https://schema.org/thumbnailUrl)
<i>Verplicht</i><br/><br/> 
- <b>Beschrijving:</b>  Directe URI naar de thumbnail, verplicht als geldige URI. <https://docs.nde.nl/schema-profile/#MediaObject-thumbnailUrl>
- <b>Datatype:</b>  URI 
- <b>Kardinaliteit:</b> 1..1

#### [schema:license](https://schema.org/license)
<i>Verplicht</i><br/><br/> 
- <b>Beschrijving:</b>  Rechtenstatement van de afbeelding, verplicht als URI.
- <b>Datatype:</b>  URI 
- <b>Kardinaliteit:</b> 1..1

#### [schema:copyrightHolder](https://schema.org/copyrightHolder)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b>  Rechthebbende van het mediaobject.
- <b>Datatype:</b>  [Person](#person).
- <b>Kardinaliteit:</b> 0..1

#### [schema:copyrightNotice](https://schema.org/copyrightNotice)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b>  Rechtenstatement van de afbeelding, als tekst beschreven.
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 0..1
<hr/>

### [Place](https://schema.org/Place)
Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/Place).

#### [schema:name](https://schema.org/name)
<i>Aanbevolen</i><br/><br/> 
- <b>Beschrijving:</b> Naam van de plek. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#Place-name)

#### [schema:sameAs](https://schema.org/sameAs)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Relatie naar een thesaurusterm. Aanbevolen thesauri: Geonames.
- <b>Datatype:</b>  URI
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#reference-terms)

#### [schema:addressRegion](https://schema.org/addressRegion)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Provincie waar de plek zich bevindt.
- <b>Datatype:</b>  [AdministrativeArea](#administrativearea)
- <b>Kardinaliteit:</b> 0..1

#### [schema:geo](https://schema.org/geo)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> De coördinaten van de plek. 
- <b>Datatype:</b>  <a href="#geocoordinates">GeoCoordinates</a>
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#GeoCoordinates)
<hr/>

### [GeoCoordinates](https://schema.org/GeoCoordinates)

Geografische coördinaten van een plek. Onderstaande properties zijn verplicht als schema:GeoCoordinates aanwezig is. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#GeoCoordinates).

#### [schema:latitude](https://schema.org/latitude)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Breedtegraad van de vindplaats of locatie van vervaardiging. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#GeoCoordinates-latitude)

#### [schema:longitude](https://schema.org/longitude)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Lengtegraad van de vindplaats of vervaardiging.
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#GeoCoordinates-longitude)
<hr/>

### [AdministrativeArea](https://schema.org/AdministrativeArea)

Provincie waarin de plek zich bevindt.

#### [schema:name](https://schema.org/name)
<i>Optioneel</i><br/>
- <b>Beschrijving:</b> Naam van de plek. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1
- <b>Voorbeeld:</b>

``` 
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "addressRegion": {
                      "@type": "AdministrativeArea",
                      "name": "Zuid-Holland"@nl,
                  } 
}
```

#### [schema:sameAs](https://schema.org/sameAs)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Relatie naar een thesaurusterm. Aanbevolen thesauri: Geonames.
- <b>Datatype:</b>  URI
- <b>Kardinaliteit:</b> 0..1
- [Meer informatie](https://docs.nde.nl/schema-profile/#reference-terms)
<hr/>

### [Occupation](https://schema.org/Occupation)

De rol van de vervaardiger van het object, bv. ‘schilder’. Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#Occupation).

#### [schema:name](https://schema.org/name)
<i>Optioneel</i><br/><br/> 
- <b>Beschrijving:</b> Rol van de vervaardiger. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1

#### [schema:sameAs](https://schema.org/sameAs)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Relatie naar een thesaurusterm. Aanbevolen thesauri: AAT, CHT.
- <b>Datatype:</b>  URI
- <b>Kardinaliteit:</b> 0..1
- <b>Voorbeeld:</b> 

```
{
  "@context": "https://schema.org",
  "@type": "Occupation",
  "name": "Fotograaf",
  "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/fa108e11-e409-4a69-938e-1c1e66927c13",
}
```

<hr/>

### [PropertyValue](https://schema.org/PropertyValue)

IDs, bijvoorbeeld PIDs of IDs uit het collectiebeheersysteem die voor context belangrijk zijn, kunnen worden toegevoegd door middel van deze PropertyValue klasse.

#### [schema:propertyID](https://schema.org/propertyID)
<i>Verplicht bij PropertyValue</i><br/>
- <b>Beschrijving:</b> Uniek kenmerk van het soort identifier. 
- <b>Datatype:</b>  URI of string
- <b>Kardinaliteit:</b> 1..1

#### [schema:value](https://schema.org/value)
<i>Verplicht bij PropertyValue</i><br/>
- <b>Beschrijving:</b> Waarde van de identifier. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1

#### [schema:description](https://schema.org/description)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Beschrijving van het soort identifier. 
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 1..1
<hr/>

### [DefinedTerm](https://schema.org/DefinedTerm)
Zie ook [documentatie van het NDE](https://docs.nde.nl/schema-profile/#reference-terms).

#### [schema:name](https://schema.org/name)
<i>Optioneel</i><br/>
- <b>Beschrijving:</b> Naam van de term, bijvoorbeeld de naam van het genre.  
- <b>Datatype:</b>  string
- <b>Kardinaliteit:</b> 0..1

#### [schema:sameAs](https://schema.org/sameAs)
<i>Optioneel</i><br/> 
- <b>Beschrijving:</b> Relatie naar een thesaurusterm. 
- <b>Datatype:</b>  URI
- <b>Kardinaliteit:</b> 0..1

```
{
  "@context": "https://schema.org",
  "@type": ["DefinedTerm", "URL"]
  "name": "Aquarelverf",
  "sameAs": "https://data.cultureelerfgoed.nl/term/id/cht/152a6b74-0549-4e53-aec0-f8209db88b86",
}
```
<hr/>

<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark'
  });
</script>
