# Open Refine Template for University of Tennessee Extension Special Circulars


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells['adminDB'].value}}</identifier>
<identifier type="issn">{{cells["issn"].value}}</identifier>
{{if(isBlank(cells['number#'].value), '', '<identifier type="circular">' + cells['number#'].value + '</identifier>')}}
{{if(isBlank(cells['PID'].value), '', '<identifier type="pid">' + cells['PID'].value + '</identifier>')}}
<titleInfo><title>{{cells["title"].value}}</title></titleInfo>
{{if(isBlank(cells['alternate_title'].value), '', '<titleInfo type="alternative"><title>' + cells['alternate_title'].value + '</title></titleInfo>')}} 
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['author'].value), '', '<name type="personal"' + if(isBlank(cells['author_URI'].value), '', ' authority="naf" valueURI="' + cells['author_URI'].value + '"') + '><namePart>' + cells['author'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['author2'].value), '', '<name type="personal"' + if(isBlank(cells['author2_URI'].value), '', ' authority="naf" valueURI="' + cells['author2_URI'].value + '"') + '><namePart>' + cells['author2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['author3'].value), '', '<name type="personal"><namePart>' + cells['author3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['author4'].value), '', '<name type="personal"><namePart>' + cells['author4'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['author_corp'].value), '', '<name type="corporate"' + if(isBlank(cells['author_corp_URI'].value), '', ' authority="naf" valueURI="' + cells['author_corp_URI'].value + '"') + '><namePart>' + cells['author_corp'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['author_corp2'].value), '', '<name type="corporate"' + if(isBlank(cells['author_corp2_URI'].value), '', ' authority="naf" valueURI="' + cells['author_corp2_URI'].value + '"') + '><namePart>' + cells['author_corp2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
<physicalDescription>
{{if(isBlank(cells['form'].value), '', '<form authority="aat" valueURI="' + cells['form_URI'].value + '">' + cells['form'].value + '</form>')}}
{{if(isBlank(cells['form2'].value), '', '<form authority="aat" valueURI="' + cells['form2_URI'].value + '">' + cells['form2'].value + '</form>')}}
{{if(isBlank(cells['form3'].value), '', '<form authority="aat" valueURI="' + cells['form3_URI'].value + '">' + cells['form3'].value + '</form>')}}
<extent>{{cells['extent'].value}}</extent>
</physicalDescription>
{{if(isBlank(cells['date_year'].value), '', '<originInfo><dateIssued>' + cells['date_year'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes">' + cells['date_full'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
{{if(isBlank(cells['date_start'].value), '', '<originInfo><dateIssued qualifier="inferred">' + cells['date_start'].value + '-' + cells['date_end'].value + '</dateIssued><dateIssued qualifier="inferred" encoding="edtf" keyDate="yes" point="start">' + cells['date_start'].value + '</dateIssued><dateIssued qualifier="inferred" encoding="edtf" keyDate="yes" point="end">' + cells['date_end'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
{{if(isBlank(cells['date_approximate'].value), '', '<originInfo><dateIssued qualifier="approximate">' + cells['date_approximate'].value + '</dateIssued><dateIssued qualifier="approximate" encoding="edtf" keyDate="yes">' + cells['date_approximate'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
{{if(isBlank(cells['subject1'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject1_URI'].value + '"><topic>' + cells['subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo2_URI'].value + '"><geographic>' + cells['subject_geo2'].value + '</geographic></subject>')}}
<classification authority="lcc">{{cells['classification'].value}}</classification>
<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```