# Country Music Open Refine Export Template

## Template

#### Prefix
```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

#### Body
```
<mods xmlns="http://www.loc.gov/mods/v3" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
<titleInfo><title>{{cells["Title"].value}}</title></titleInfo>
<accessCondition>{{cells["AccessRights"].value}}</accessCondition>
<abstract>{{cells["Description"].value}}</abstract>
<subject><topic>{{cells["Subject 1"].value}}</topic></subject>
<subject><topic>{{cells["Subject 2"].value}}</topic></subject>
<subject><topic>{{cells["Subject 3"].value}}</topic></subject>
<subject><topic>{{cells["Subject 4"].value}}</topic></subject>
<subject><topic>{{cells["Subject 5"].value}}</topic></subject>
<subject><topic>{{cells["Subject 6"].value}}</topic></subject>
<subject><topic>{{cells["Subject 7"].value}}</topic></subject>
<subject><topic>{{cells["Subject 8"].value}}</topic></subject>
<subject><topic>{{cells["Subject 9"].value}}</topic></subject>
<subject><topic>{{cells["Subject 10"].value}}</topic></subject>
<subject><topic>{{cells["Subject 11"].value}}</topic></subject>
<subject><topic>{{cells["Subject 12"].value}}</topic></subject>
<subject><topic>{{cells["Subject 13"].value}}</topic></subject>
<subject><topic>{{cells["Subject 14"].value}}</topic></subject>
<subject><topic>{{cells["Subject 15"].value}}</topic></subject>
<subject><topic>{{cells["Subject 16"].value}}</topic></subject>
<subject><topic>{{cells["Subject 17"].value}}</topic></subject>
<subject><topic>{{cells["Subject 18"].value}}</topic></subject>
<subject><topic>{{cells["Subject 19"].value}}</topic></subject>
<subject><topic>{{cells["Subject 20"].value}}</topic></subject>
<subject><topic>{{cells["Subject 21"].value}}</topic></subject>
<subject><topic>{{cells["Subject 22"].value}}</topic></subject>
<subject><topic>{{cells["Subject 23"].value}}</topic></subject>
<subject><topic>{{cells["Subject 24"].value}}</topic></subject>
<subject><topic>{{cells["Subject 25"].value}}</topic></subject>
<subject><topic>{{cells["Subject 26"].value}}</topic></subject>
<subject><topic>{{cells["Subject 27"].value}}</topic></subject>
<subject><topic>{{cells["Subject 28"].value}}</topic></subject>
<name><namePart>{{cells["Creator 1"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 2"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 3"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 4"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 5"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 6"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<name><namePart>{{cells["Creator 7"].value}}</namePart><role><roleTerm>Creator</roleTerm></role></name>
<originInfo><dateCreated encoding="edtf" keyDate="yes">{{cells["Date"].value}}</dateCreated></originInfo>
<recordInfo><recordContentSource>Country Music Hall of Fame</recordContentSource></recordInfo>
<location><url usage="primary" access="object in context">{{cells["CleanIdentifier2"].value}}</url></location>
<location><url usage="primary" access="preview">http://digi.countrymusichalloffame.org/utils/getthumbnail/collection/musicaudio/id/{{cells["id"].value}}</url></location>
<identifier type="local">{{cells["id"].value}}</identifier>
<physicalDescription><form>{{cells["RealFormat 1"].value}}</form></physicalDescription>
<physicalDescription><form>{{cells["RealFormat 2"].value}}</form></physicalDescription>
<physicalDescription><form>{{cells["RealFormat 3"].value}}</form></physicalDescription>
<physicalDescription><form>{{cells["RealFormat 4"].value}}</form></physicalDescription>
</mods>

```

#### Row Separator

Leave blank

#### Suffix

```
</modsCollection>
```