Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# The Construction Resources (CR) Ontology

## Metadata
* **IRI**
  * `http://w3id.org/cr`
* **Creators(s)**
  * [Cassandro, Jacopo](https://orcid.org/0000-0002-1487-8178)
    [[ORCID]](https://orcid.org/0000-0002-1487-8178)
    (<jacopo.cassandro@polimi.it></a>) of [Politecnico di Milano](https://www.dabc.polimi.it/persona/jacopo-cassandro/)
  * [Hagedorn, Philipp](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Politecnico di Milano](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Contributor(s)**
  * [Mirarchi, Claudio](https://orcid.org/0000-0002-9288-8662)
    [[ORCID]](https://orcid.org/0000-0002-9288-8662)
    (<claudio.mirarchi@polimi.it></a>) of [Politecnico di Milano, Dipartimento ABC](https://www.dabc.polimi.it/persona/claudio-mirarchi/)
  * [Sigalov, Katharina](https://orcid.org/0000-0002-3070-0759)
    [[ORCID]](https://orcid.org/0000-0002-3070-0759)
    (<katharina.sigalov@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/katharina_sigalov.html.en)
* **Created**
  * 2024-10-12
* **Modified**
  * 2025-04-07
* **Version Information**
  * 0.2
* **Imports**
  * [http://w3id.org/cterm](http://w3id.org/cterm)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2025 by DABC, PoliMi
* **Ontology RDF**
  * RDF ([resources.ttl](turtle))
### Description
<p>The Construction Resources (CR) Ontology is based on concepts and principles of construction project management to provide a centralized definitiopn of resources that can be used as shared entities with task planning and cost estimation for providing a unified context.</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Assignment](#Assignment),
[Assignment set](#Assignmentset),
[Geräteressource](#Gerteressource),
[Lag Precondition](#LagPrecondition),
[Materielle Ressource](#MaterielleRessource),
[Relazione tra risorsa e attività](#Relazionetrarisorsaeattivit),
[ResourceAssignment](#ResourceAssignment),
[Ressource](#Ressource),
[Risorsa umana](#Risorsaumana),
[Task to cost item assignment](#Tasktocostitemassignment),
[Task to geometry assignment](#Tasktogeometryassignment),
[Verbrauch](#Verbrauch),
[Zuordnung von Kostenbestandteilen zu Geometrieobjekten](#ZuordnungvonKostenbestandteilenzuGeometrieobjekten),
[Zuordnung von Ressourcen zu Kostenbestandteilen](#ZuordnungvonRessourcenzuKostenbestandteilen),
### ResourceAssignment
Property | Value
--- | ---
IRI | `https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment`
Super-classes |[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />
### Assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#Assignment`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op) **some** [cr:AssignmentSet](https://w3id.org/cr#AssignmentSet) (c)<br />
Sub-classes |[cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c)<br />[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />[cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c)<br />[cr:TaskToCostItemAssignment](https://w3id.org/cr#TaskToCostItemAssignment) (c)<br />[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />
In domain of |[cr:ref](https://w3id.org/cr#ref) (op)<br />[cr:refParameter](https://w3id.org/cr#refParameter) (dp)<br />[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op)<br />
In range of |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op)<br />
### Assignment set
Property | Value
--- | ---
IRI | `https://w3id.org/cr#AssignmentSet`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op) **some** [cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
In domain of |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op)<br />
In range of |[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op)<br />
### Verbrauch
Property | Value
--- | ---
IRI | `https://w3id.org/cr#Consumption`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cterm:parameterSymbol1](https://w3id.org/cterm#parameterSymbol1) **only** [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />[cterm:parameterValue1](https://w3id.org/cterm#parameterValue1) **only** [xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />[cterm:parameterType](https://w3id.org/cterm#parameterType) **only** [cterm:ParameterType](https://w3id.org/cterm#ParameterType) (c)<br />[cterm:parameterValue2](https://w3id.org/cterm#parameterValue2) **only** [xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op) **max** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cterm:parameterSymbol2](https://w3id.org/cterm#parameterSymbol2) **only** [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
In domain of |[cr:consumptionOf](https://w3id.org/cr#consumptionOf) (op)<br />
In range of |[cr:hasConsumption](https://w3id.org/cr#hasConsumption) (op)<br />
### Zuordnung von Kostenbestandteilen zu Geometrieobjekten
Property | Value
--- | ---
IRI | `https://w3id.org/cr#CostItemToGeometryAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[cr:refGeometry](https://w3id.org/cr#refGeometry) (op) **exactly** 1 [https://standards.buildingsmart.org/IFC/DEV/IFC4/ADD2/OW#IfcProduct](https://standards.buildingsmart.org/IFC/DEV/IFC4/ADD2/OW#IfcProduct) (c)<br />[cr:refParamQuantity](https://w3id.org/cr#refParamQuantity) (dp) **exactly** 1<br />[cr:refParamFormula](https://w3id.org/cr#refParamFormula) (dp) **exactly** 1<br />
In domain of |[cr:refParamQuantity](https://w3id.org/cr#refParamQuantity) (dp)<br />[cr:refParamFormula](https://w3id.org/cr#refParamFormula) (dp)<br />
### Geräteressource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#EquipmentResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifcconstructionequipmentresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfEquipment](https://w3id.org/cterm#FunctionOfEquipment) (c)<br />[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **some** [cterm:PerformanceParameter](https://w3id.org/cterm#PerformanceParameter) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **some** [cterm:AspectOfEquipment](https://w3id.org/cterm#AspectOfEquipment) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfEquipment](https://w3id.org/cterm#ObjectOfEquipment) (c)<br />[cterm:hasObjectStandard](https://w3id.org/cterm#hasObjectStandard) **only** [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **only** [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[cr:minimunLevelLabourResource](https://w3id.org/cr#minimunLevelLabourResource) (dp) **max** 1<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **some** [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **some** [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfEquipment](https://w3id.org/cterm#TypeOfEquipment) (c)<br />[cr:rent](https://w3id.org/cr#rent) (dp) **exactly** 1<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfEquipment](https://w3id.org/cterm#CategoryOfEquipment) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:Use](https://w3id.org/cterm#Use) (c)<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfEquipment](https://w3id.org/cterm#FamilyOfEquipment) (c)<br />[cr:accessory](https://w3id.org/cr#accessory) (dp) **exactly** 1<br />[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **some** [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />
In domain of |[cr:rent](https://w3id.org/cr#rent) (dp)<br />[cr:accessory](https://w3id.org/cr#accessory) (dp)<br />[cr:minimunLevelLabourResource](https://w3id.org/cr#minimunLevelLabourResource) (dp)<br />
### Risorsa umana
Property | Value
--- | ---
IRI | `https://w3id.org/cr#LabourResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifclaborresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfLabour](https://w3id.org/cterm#FamilyOfLabour) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfLabour](https://w3id.org/cterm#TypeOfLabour) (c)<br />[cterm:hasQualificationLevel](https://w3id.org/cterm#hasQualificationLevel) **only** [cterm:QualificationLevel](https://w3id.org/cterm#QualificationLevel) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfLabour](https://w3id.org/cterm#CategoryOfLabour) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfLabour](https://w3id.org/cterm#ObjectOfLabour) (c)<br />
### Lag Precondition
Property | Value
--- | ---
IRI | `https://w3id.org/cr#LagPrecondition`
Description | <p>A subtype of the DTC Precondition providing information of the lag that needs to be completed before starting a next activity.</p>
Super-classes |[dtc:Precondition](https://dtc-ontology.cms.ed.tum.de/ontology/Precondition) (c)<br />
Restrictions |[cr:hasLagUnit](https://w3id.org/cr#hasLagUnit) (op) **max** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cr:hasLagStart](https://w3id.org/cr#hasLagStart) (op) **max** 1<br />[cr:hasLagDuration](https://w3id.org/cr#hasLagDuration) (op) **max** 1<br />
In domain of |[cr:hasLagDuration](https://w3id.org/cr#hasLagDuration) (op)<br />[cr:hasLagUnit](https://w3id.org/cr#hasLagUnit) (op)<br />[cr:hasLagStart](https://w3id.org/cr#hasLagStart) (op)<br />
### Materielle Ressource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#MaterialResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifcconstructionmaterialresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **some** [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **only** [cterm:ObjectOfMaterial](https://w3id.org/cterm#ObjectOfMaterial) (c)<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **only** [cterm:FamilyOfMaterial](https://w3id.org/cterm#FamilyOfMaterial) (c)<br />[cterm:hasFurnishing](https://w3id.org/cterm#hasFurnishing) **some** [cterm:Furnishing](https://w3id.org/cterm#Furnishing) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **some** [cterm:FunctionOfMaterial](https://w3id.org/cterm#FunctionOfMaterial) (c)<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **some** [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **only** [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **some** [cterm:PerformanceParameter](https://w3id.org/cterm#PerformanceParameter) (c)<br />[cr:cam](https://w3id.org/cr#cam) (dp) **exactly** 1<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **some** [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **only** [cterm:CategoryOfMaterial](https://w3id.org/cterm#CategoryOfMaterial) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **some** [cterm:Use](https://w3id.org/cterm#Use) (c)<br />[cterm:hasType](https://w3id.org/cterm#hasType) **only** [cterm:TypeOfMaterial](https://w3id.org/cterm#TypeOfMaterial) (c)<br />[cterm:hasObjectStandard](https://w3id.org/cterm#hasObjectStandard) **only** [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **some** [cterm:Finishing](https://w3id.org/cterm#Finishing) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **some** [cterm:AspectOfMaterial](https://w3id.org/cterm#AspectOfMaterial) (c)<br />
### Ressource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#Resource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifckernel/lexical/ifcresource.htm
Description | <p>This class is used for providing information about a construction resource.</p>
Restrictions |[cr:quantityUnitOfMeasure](https://w3id.org/cr#quantityUnitOfMeasure) (dp) **exactly** 1<br />[cr:descriptionGeneral](https://w3id.org/cr#descriptionGeneral) (dp) **exactly** 1<br />[cr:descriptionDetail](https://w3id.org/cr#descriptionDetail) (dp) **max** 1<br />[cr:unitPrice](https://w3id.org/cr#unitPrice) (dp) **exactly** 1<br />[cr:code](https://w3id.org/cr#code) (dp) **exactly** 1<br />[cr:keywords](https://w3id.org/cr#keywords) (dp) **some** [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cr:law](https://w3id.org/cr#law) (dp) **some** [xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
Sub-classes |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cr:LabourResource](https://w3id.org/cr#LabourResource) (c)<br />
In domain of |[cr:subRecourceOf](https://w3id.org/cr#subRecourceOf)<br />[cr:included](https://w3id.org/cr#included) (dp)<br />[cr:measurementRules](https://w3id.org/cr#measurementRules) (dp)<br />[cr:quantityUnitOfMeasure](https://w3id.org/cr#quantityUnitOfMeasure) (dp)<br />[cr:techSpecs](https://w3id.org/cr#techSpecs) (dp)<br />[cr:descriptionDetail](https://w3id.org/cr#descriptionDetail) (dp)<br />[cr:law](https://w3id.org/cr#law) (dp)<br />[cr:hasSubResource](https://w3id.org/cr#hasSubResource)<br />[cr:excluded](https://w3id.org/cr#excluded) (dp)<br />[cr:keywords](https://w3id.org/cr#keywords) (dp)<br />[cr:unitPrice](https://w3id.org/cr#unitPrice) (dp)<br />[cr:code](https://w3id.org/cr#code) (dp)<br />[cr:descriptionGeneral](https://w3id.org/cr#descriptionGeneral) (dp)<br />
In range of |[cr:hasSubResource](https://w3id.org/cr#hasSubResource)<br />[cr:subRecourceOf](https://w3id.org/cr#subRecourceOf)<br />[cr:refResource](https://w3id.org/cr#refResource) (op)<br />
### Zuordnung von Ressourcen zu Kostenbestandteilen
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ResourceToCostItemAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[cr:refResource](https://w3id.org/cr#refResource) (op) **exactly** 1 [cr:Resource](https://w3id.org/cr#Resource) (c)<br />
In domain of |[cr:refParamUtilizationFactor](https://w3id.org/cr#refParamUtilizationFactor) (dp)<br />
### Relazione tra risorsa e attività
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ResourceToTaskAssignment`
Is Defined By | https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refParamUtilizationRate](https://w3id.org/cr#refParamUtilizationRate) (dp) **exactly** 1<br />[cr:refResource](https://w3id.org/cr#refResource) (op) **exactly** 1 [cr:Resource](https://w3id.org/cr#Resource) (c)<br />[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />
Sub-classes |[https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment](https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment) (c)<br />
In domain of |[cr:refParamUtilizationRate](https://w3id.org/cr#refParamUtilizationRate) (dp)<br />
### Task to cost item assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#TaskToCostItemAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />
### Task to geometry assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#TaskToGeometryAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />[cr:refGeometry](https://w3id.org/cr#refGeometry) (op) **exactly** 1 [http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct](http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct) (c)<br />

## Object Properties
[consumptionOf](#consumptionOf),
[has assignment](#hasassignment),
[hasConsumption](#hasConsumption),
[hasLagDuration](#hasLagDuration),
[hasLagStart](#hasLagStart),
[hasLagUnit](#hasLagUnit),
[hasUnit](#hasUnit),
[is assignment Of](#isassignmentOf),
[ref](#ref),
[ref cost item](#refcostitem),
[ref geometry](#refgeometry),
[ref resource](#refresource),
[ref task](#reftask),
[](consumptionOf)
### consumptionOf
Property | Value
--- | ---
IRI | `https://w3id.org/cr#consumptionOf`
Domain(s) |[cr:Consumption](https://w3id.org/cr#Consumption) (c)<br />
Range(s) |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />
[](hasassignment)
### has assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasAssignment`
Domain(s) |[cr:AssignmentSet](https://w3id.org/cr#AssignmentSet) (c)<br />
Range(s) |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
[](hasConsumption)
### hasConsumption
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasConsumption`
Domain(s) |([cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c) or [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c))<br />
Range(s) |[cr:Consumption](https://w3id.org/cr#Consumption) (c)<br />
[](hasLagDuration)
### hasLagDuration
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasLagDuration`
Domain(s) |[cr:LagPrecondition](https://w3id.org/cr#LagPrecondition) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasLagStart)
### hasLagStart
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasLagStart`
Domain(s) |[cr:LagPrecondition](https://w3id.org/cr#LagPrecondition) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](hasLagUnit)
### hasLagUnit
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasLagUnit`
Domain(s) |[cr:LagPrecondition](https://w3id.org/cr#LagPrecondition) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasUnit)
### hasUnit
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasUnit`
Domain(s) |([cr:Consumption](https://w3id.org/cr#Consumption) (c) or [cr:Resource](https://w3id.org/cr#Resource) (c) or [cterm:Parameter](https://w3id.org/cterm#Parameter) (c))<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](isassignmentOf)
### is assignment Of
Property | Value
--- | ---
IRI | `https://w3id.org/cr#isAssignmentOf`
Domain(s) |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Range(s) |[cr:AssignmentSet](https://w3id.org/cr#AssignmentSet) (c)<br />
[](ref)
### ref
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ref`
Domain(s) |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Range(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
[](refcostitem)
### ref cost item
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refCostItem`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |([cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c) or [cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c))<br />
Range(s) |[ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c)<br />
[](refgeometry)
### ref geometry
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refGeometry`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |([cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c) or [cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c))<br />
Range(s) |[http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct](http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct) (c)<br />
[](refresource)
### ref resource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refResource`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |([cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c) or [cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c))<br />
Range(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
[](reftask)
### ref task
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refTask`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |([cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c) or [cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c))<br />
Range(s) |[https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />

## Datatype Properties
[accessory](#accessory),
[cam](#cam),
[code](#code),
[descriptionDetail](#descriptionDetail),
[descriptionGeneral](#descriptionGeneral),
[excluded](#excluded),
[included](#included),
[keywords](#keywords),
[law](#law),
[measurement rules](#measurementrules),
[minimunLevelLabourResource](#minimunLevelLabourResource),
[quantityUnitOfMeasure](#quantityUnitOfMeasure),
[ref param formula](#refparamformula),
[quantity](#quantity),
[utilization factor](#utilizationfactor),
[utilization rate](#utilizationrate),
[ref parameter](#refparameter),
[rent](#rent),
[tech specs](#techspecs),
[unit price](#unitprice),
[yield](#yield),
[](accessory)
### accessory
Property | Value
--- | ---
IRI | `https://w3id.org/cr#accessory`
Domain(s) |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](cam)
### cam
Property | Value
--- | ---
IRI | `https://w3id.org/cr#cam`
Domain(s) |([cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c) or [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c))<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](code)
### code
Property | Value
--- | ---
IRI | `https://w3id.org/cr#code`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](descriptionDetail)
### descriptionDetail
Property | Value
--- | ---
IRI | `https://w3id.org/cr#descriptionDetail`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](descriptionGeneral)
### descriptionGeneral
Property | Value
--- | ---
IRI | `https://w3id.org/cr#descriptionGeneral`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](excluded)
### excluded
Property | Value
--- | ---
IRI | `https://w3id.org/cr#excluded`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](included)
### included
Property | Value
--- | ---
IRI | `https://w3id.org/cr#included`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](keywords)
### keywords
Property | Value
--- | ---
IRI | `https://w3id.org/cr#keywords`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](law)
### law
Property | Value
--- | ---
IRI | `https://w3id.org/cr#law`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](measurementrules)
### measurement rules
Property | Value
--- | ---
IRI | `https://w3id.org/cr#measurementRules`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](minimunLevelLabourResource)
### minimunLevelLabourResource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#minimunLevelLabourResource`
Domain(s) |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](quantityUnitOfMeasure)
### quantityUnitOfMeasure
Property | Value
--- | ---
IRI | `https://w3id.org/cr#quantityUnitOfMeasure`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](refparamformula)
### ref param formula
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refParamFormula`
Super-properties |[cr:refParameter](https://w3id.org/cr#refParameter) (dp)<br />
Domain(s) |[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](quantity)
### quantity
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refParamQuantity`
Description | The quantity calculated from the geometrical element that is applied to the cost item and its unitary price.
Super-properties |[cr:refParameter](https://w3id.org/cr#refParameter) (dp)<br />
Domain(s) |[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](utilizationfactor)
### utilization factor
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refParamUtilizationFactor`
Description | The utilization factor of a resource that is applied in a cost item.
Super-properties |[cr:refParameter](https://w3id.org/cr#refParameter) (dp)<br />
Domain(s) |[cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](utilizationrate)
### utilization rate
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refParamUtilizationRate`
Description | The utilization rate of a (equipment) resource that is applied in a task.
Super-properties |[cr:refParameter](https://w3id.org/cr#refParameter) (dp)<br />
Domain(s) |[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](refparameter)
### ref parameter
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refParameter`
Domain(s) |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
[](rent)
### rent
Property | Value
--- | ---
IRI | `https://w3id.org/cr#rent`
Domain(s) |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](techspecs)
### tech specs
Property | Value
--- | ---
IRI | `https://w3id.org/cr#techSpecs`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](unitprice)
### unit price
Property | Value
--- | ---
IRI | `https://w3id.org/cr#unitPrice`
Domain(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](yield)
### yield
Property | Value
--- | ---
IRI | `https://w3id.org/cr#yield`
Domain(s) |([cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c) or [cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c))<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **ci**
  * `https://w3id.org/ci#`
* **cr**
  * `https://w3id.org/cr#`
* **cterm**
  * `https://w3id.org/cterm#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dtc**
  * `https://dtc-ontology.cms.ed.tum.de/ontology/`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **qudt**
  * `http://qudt.org/schema/qudt/`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **vs**
  * `http://www.w3.org/2003/06/sw-vocab-status/ns#`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni