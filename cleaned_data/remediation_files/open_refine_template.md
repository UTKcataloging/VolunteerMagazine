# Open Refine Template Volunteer Magazine / Smokey's Tale


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["filename"].value}}</identifier>
{{if(isBlank(cells['transcribed_title'].value), '', '<titleInfo><title>' + cells['transcribed_title'].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['supplied_title'].value), '', '<titleInfo supplied="yes"><title>' + cells["supplied_title"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['volume_number'].value), '', '<titleInfo type="alternative"><title>' + cells['volume_number'].value + '</title></titleInfo>')}} 
<abstract>{{cells["abstract"].value}}</abstract>
<tableOfContents>{{cells["tableOfContents"].value}}</tableOfContents>
{{if(isBlank(cells['date'].value), '', '<originInfo><dateIssued>' + cells['date'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes">' + cells['date_edtf'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["extent"].value}}</extent></physicalDescription>
{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject5_URI'].value + '"><topic>' + cells['subject5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject6'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject6_URI'].value + '"><topic>' + cells['subject6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject7'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject7_URI'].value + '"><topic>' + cells['subject7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n79109786">
<geographic>Knoxville (Tenn.)</geographic>
<cartographics>
<coordinates>35.96064, -83.92074</coordinates>
</cartographics>
</subject>
<classification authority="lcc">{{cells['classification'].value}}</classification>
<language>
<languageTerm type="text" authority="iso639-2b">English</languageTerm>
</language>
<typeOfResource>text</typeOfResource>
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