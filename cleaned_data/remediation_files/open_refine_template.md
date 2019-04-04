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
<identifier type="local">{{cells["adminDB"].value}}</identifier>
<titleInfo><title>{{cells["title"].value}}</title></titleInfo> 
{{if(isBlank(cells['number'].value), '', '<part>' + cells['number'].value + '</part>')}}
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
<physicalDescription><form authority="aat">{{cells['form'].value}}</form>
{{if(isBlank(cells['form2'].value), '', '<form authority="aat">' + cells['form2'].value + '</form>')}}
<extent>{{cells['extent'].value}}</extent></physicalDescription>
{{if(isBlank(cells['date_year'].value), '', '<originInfo><dateIssued>' + cells['date_year'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes">' + cells['date_year'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
{{if(isBlank(cells['subject1'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject1_URI'].value + '"><topic>' + cells['subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
<classification authority="lcc">{{cells['classification'].value}}</classification>
<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
</mods>

```

#### Suffix

```
</modsCollection>
```