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
  * 2025-01-13
* **Version Information**
  * http://w3id.org/cr#
* **Imports**
  * [http://w3id.org/ci](http://w3id.org/ci)
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
[Consumo](#Consumo),
[Cost item to geometry assignment](#Costitemtogeometryassignment),
[Geräteressource](#Gerteressource),
[Relazione tra risorsa e attività](#Relazionetrarisorsaeattivit),
[Resource](#Resource),
[Resource to cost item assignment](#Resourcetocostitemassignment),
[ResourceAssignment](#ResourceAssignment),
[Risorsa materiale](#Risorsamateriale),
[Risorsa umana](#Risorsaumana),
[Zuordnung von Ressourcen zu Kostenbestandteilen](#ZuordnungvonRessourcenzuKostenbestandteilen),
[Zuordnung von Vorgängen zu Geometrieobjekten](#ZuordnungvonVorgngenzuGeometrieobjekten),
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
Restrictions |[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op) **exactly** 1 [cr:AssignmentSet](https://w3id.org/cr#AssignmentSet) (c)<br />
Sub-classes |[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />[cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c)<br />[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />[cr:TaskToCostItemAssignment](https://w3id.org/cr#TaskToCostItemAssignment) (c)<br />[cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c)<br />
In domain of |[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op)<br />
In range of |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op)<br />
### Assignment set
Property | Value
--- | ---
IRI | `https://w3id.org/cr#AssignmentSet`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op) **some** [cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
In domain of |[cr:hasAssignment](https://w3id.org/cr#hasAssignment) (op)<br />
In range of |[cr:isAssignmentOf](https://w3id.org/cr#isAssignmentOf) (op)<br />
### Consumo
Property | Value
--- | ---
IRI | `https://w3id.org/cr#Consumption`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[cterm:parameterSymbol2](https://w3id.org/cterm#parameterSymbol2) **max** 1<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op) **max** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cterm:parameterValue2](https://w3id.org/cterm#parameterValue2) **max** 1<br />[cterm:parameterValue1](https://w3id.org/cterm#parameterValue1) **max** 1<br />[cterm:parameterSymbol1](https://w3id.org/cterm#parameterSymbol1) **max** 1<br />[cterm:parameterType](https://w3id.org/cterm#parameterType) **max** 1<br />
In domain of |[cr:ConsumptionOf](https://w3id.org/cr#ConsumptionOf) (op)<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op)<br />
In range of |[cr:hasConsumption](https://w3id.org/cr#hasConsumption) (op)<br />
### Cost item to geometry assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#CostItemToGeometryAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refParamFormula](https://w3id.org/cr#refParamFormula) (dp) **exactly** 1<br />[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />[cr:refParamQuantity](https://w3id.org/cr#refParamQuantity) (dp) **exactly** 1<br />[cr:refGeometry](https://w3id.org/cr#refGeometry) (op) **exactly** 1 [https://standards.buildingsmart.org/IFC/DEV/IFC4/ADD2/OW#IfcProduct](https://standards.buildingsmart.org/IFC/DEV/IFC4/ADD2/OW#IfcProduct) (c)<br />
In domain of |[cr:refCostItem](https://w3id.org/cr#refCostItem) (op)<br />[cr:refParamFormula](https://w3id.org/cr#refParamFormula) (dp)<br />[cr:refParamQuantity](https://w3id.org/cr#refParamQuantity) (dp)<br />[cr:refGeometry](https://w3id.org/cr#refGeometry) (op)<br />
### Geräteressource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#EquipmentResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifcconstructionequipmentresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfEquipment](https://w3id.org/cterm#FamilyOfEquipment) (c)<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **max** 10 [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 5 [cterm:FunctionOfEquipment](https://w3id.org/cterm#FunctionOfEquipment) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfEquipment](https://w3id.org/cterm#ObjectOfEquipment) (c)<br />[cr:minimunLevelLabourResource](https://w3id.org/cr#minimunLevelLabourResource) (dp) **max** 1<br />[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **max** 10 [cr:PerformanceParameter](https://w3id.org/cr#PerformanceParameter) (c)<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **exactly** 1 [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[cr:accessory](https://w3id.org/cr#accessory) (dp) **exactly** 1<br />[cterm:hasObjectStandard](https://w3id.org/cterm#hasObjectStandard) **max** 1 [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:Use](https://w3id.org/cterm#Use) (c)<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **max** 10 [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **max** 5 [cterm:AspectOfEquipment](https://w3id.org/cterm#AspectOfEquipment) (c)<br />[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **max** 5 [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfEquipment](https://w3id.org/cterm#CategoryOfEquipment) (c)<br />[cr:rent](https://w3id.org/cr#rent) (dp) **exactly** 1<br />
In domain of |[cr:accessory](https://w3id.org/cr#accessory) (dp)<br />[cr:yield](https://w3id.org/cr#yield) (dp)<br />[cr:rent](https://w3id.org/cr#rent) (dp)<br />[cr:cam](https://w3id.org/cr#cam) (dp)<br />[cr:hasConsumption](https://w3id.org/cr#hasConsumption) (op)<br />[cr:minimunLevelLabourResource](https://w3id.org/cr#minimunLevelLabourResource) (dp)<br />
In range of |[cr:ConsumptionOf](https://w3id.org/cr#ConsumptionOf) (op)<br />
### Risorsa umana
Property | Value
--- | ---
IRI | `https://w3id.org/cr#LabourResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifclaborresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfLabour](https://w3id.org/cterm#CategoryOfLabour) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfLabour](https://w3id.org/cterm#ObjectOfLabour) (c)<br />[cterm:hasQualificationLevel](https://w3id.org/cterm#hasQualificationLevel) **max** 1 [cterm:QualificationLevel](https://w3id.org/cterm#QualificationLevel) (c)<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfLabour](https://w3id.org/cterm#FamilyOfLabour) (c)<br />
### Risorsa materiale
Property | Value
--- | ---
IRI | `https://w3id.org/cr#MaterialResource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifcconstructionmgmtdomain/lexical/ifcconstructionmaterialresource.htm
Super-classes |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
Restrictions |[cterm:hasPerformanceParameter](https://w3id.org/cterm#hasPerformanceParameter) **max** 10 [cterm:PerformanceParameter](https://w3id.org/cterm#PerformanceParameter) (c)<br />[cterm:hasCategory](https://w3id.org/cterm#hasCategory) **exactly** 1 [cterm:CategoryOfMaterial](https://w3id.org/cterm#CategoryOfMaterial) (c)<br />[cterm:hasDimensionParameter](https://w3id.org/cterm#hasDimensionParameter) **max** 10 [cterm:DimensionParameter](https://w3id.org/cterm#DimensionParameter) (c)<br />[cterm:hasFinishing](https://w3id.org/cterm#hasFinishing) **max** 5 [cterm:Finishing](https://w3id.org/cterm#Finishing) (c)<br />[cterm:hasFamily](https://w3id.org/cterm#hasFamily) **exactly** 1 [cterm:FamilyOfMaterial](https://w3id.org/cterm#FamilyOfMaterial) (c)<br />[cterm:hasAspect](https://w3id.org/cterm#hasAspect) **max** 5 [cterm:AspectOfMaterial](https://w3id.org/cterm#AspectOfMaterial) (c)<br />[cr:cam](https://w3id.org/cr#cam) (dp) **exactly** 1<br />[cterm:hasObjectStandard](https://w3id.org/cterm#hasObjectStandard) **max** 1 [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasOtherStandard](https://w3id.org/cterm#hasOtherStandard) **max** 5 [cterm:Standard](https://w3id.org/cterm#Standard) (c)<br />[cterm:hasUse](https://w3id.org/cterm#hasUse) **max** 5 [cterm:Use](https://w3id.org/cterm#Use) (c)<br />[cterm:hasMaterial](https://w3id.org/cterm#hasMaterial) **exactly** 1 [cterm:Material](https://w3id.org/cterm#Material) (c)<br />[cterm:hasFurnishing](https://w3id.org/cterm#hasFurnishing) **max** 5 [cterm:Furnishing](https://w3id.org/cterm#Furnishing) (c)<br />[cterm:hasPhysicalParameter](https://w3id.org/cterm#hasPhysicalParameter) **max** 10 [cterm:PhysicalParameter](https://w3id.org/cterm#PhysicalParameter) (c)<br />[cterm:hasFunction](https://w3id.org/cterm#hasFunction) **max** 5 [cterm:FunctionOfMaterial](https://w3id.org/cterm#FunctionOfMaterial) (c)<br />[cterm:hasObject](https://w3id.org/cterm#hasObject) **exactly** 1 [cterm:ObjectOfMaterial](https://w3id.org/cterm#ObjectOfMaterial) (c)<br />
In domain of |[cr:hasConsumption](https://w3id.org/cr#hasConsumption) (op)<br />[cr:cam](https://w3id.org/cr#cam) (dp)<br />[cr:yield](https://w3id.org/cr#yield) (dp)<br />
In range of |[cr:ConsumptionOf](https://w3id.org/cr#ConsumptionOf) (op)<br />
### Resource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#Resource`
Is Defined By | https://standards.buildingsmart.org/IFC/RELEASE/IFC4_1/FINAL/HTML/schema/ifckernel/lexical/ifcresource.htm
Description | <p>This class is used for providing information about a construction resource.</p>
Restrictions |[cr:descriptionGeneral](https://w3id.org/cr#descriptionGeneral) (dp) **exactly** 1<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[cr:law](https://w3id.org/cr#law) (dp) **max** 10<br />[cterm:hasType](https://w3id.org/cterm#hasType) **max** 1 [cterm:Type](https://w3id.org/cterm#Type) (c)<br />[cr:unitPrice](https://w3id.org/cr#unitPrice) (dp) **exactly** 1<br />[cr:descriptionDetail](https://w3id.org/cr#descriptionDetail) (dp) **max** 1<br />[cr:quantityUnitOfMeasure](https://w3id.org/cr#quantityUnitOfMeasure) (dp) **exactly** 1<br />[cr:code](https://w3id.org/cr#code) (dp) **exactly** 1<br />[cr:keywords](https://w3id.org/cr#keywords) (dp) **max** 10<br />
Sub-classes |[cr:LabourResource](https://w3id.org/cr#LabourResource) (c)<br />[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
In domain of |[cr:unitPrice](https://w3id.org/cr#unitPrice) (dp)<br />[cr:escluded](https://w3id.org/cr#escluded) (dp)<br />[cr:subRecourceOf](https://w3id.org/cr#subRecourceOf)<br />[cr:law](https://w3id.org/cr#law) (dp)<br />[cr:techSpecs](https://w3id.org/cr#techSpecs) (dp)<br />[cr:quantityUnitOfMeasure](https://w3id.org/cr#quantityUnitOfMeasure) (dp)<br />[cr:measurementRules](https://w3id.org/cr#measurementRules) (dp)<br />[cr:included](https://w3id.org/cr#included) (dp)<br />[cr:keywords](https://w3id.org/cr#keywords) (dp)<br />[cr:code](https://w3id.org/cr#code) (dp)<br />[cr:hasUnit](https://w3id.org/cr#hasUnit) (op)<br />[cr:descriptionGeneral](https://w3id.org/cr#descriptionGeneral) (dp)<br />[cr:hasSubResource](https://w3id.org/cr#hasSubResource)<br />[cr:descriptionDetail](https://w3id.org/cr#descriptionDetail) (dp)<br />
In range of |[cr:subRecourceOf](https://w3id.org/cr#subRecourceOf)<br />[cr:hasSubResource](https://w3id.org/cr#hasSubResource)<br />[cr:refResource](https://w3id.org/cr#refResource) (op)<br />
### Resource to cost item assignment
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ResourceToCostItemAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refResource](https://w3id.org/cr#refResource) (op) **exactly** 1 [cr:Resource](https://w3id.org/cr#Resource) (c)<br />[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />
In domain of |[cr:refResource](https://w3id.org/cr#refResource) (op)<br />[cr:refParamUtilizationFactor](https://w3id.org/cr#refParamUtilizationFactor) (dp)<br />[cr:refCostItem](https://w3id.org/cr#refCostItem) (op)<br />
### Relazione tra risorsa e attività
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ResourceToTaskAssignment`
Is Defined By | https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refResource](https://w3id.org/cr#refResource) (op) **exactly** 1 [cr:Resource](https://w3id.org/cr#Resource) (c)<br />[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />[cr:refParamUtilizationRate](https://w3id.org/cr#refParamUtilizationRate) (dp) **exactly** 1<br />
Sub-classes |[https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment](https://dtc-ontology.cms.ed.tum.de/ontology#ResourceAssignment) (c)<br />
In domain of |[cr:refParamUtilizationRate](https://w3id.org/cr#refParamUtilizationRate) (dp)<br />[cr:refTask](https://w3id.org/cr#refTask) (op)<br />[cr:refResource](https://w3id.org/cr#refResource) (op)<br />
### Zuordnung von Ressourcen zu Kostenbestandteilen
Property | Value
--- | ---
IRI | `https://w3id.org/cr#TaskToCostItemAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />[cr:refCostItem](https://w3id.org/cr#refCostItem) (op) **exactly** 1 [ci:CostItem](https://w3id.org/ci#CostItem) (c)<br />
### Zuordnung von Vorgängen zu Geometrieobjekten
Property | Value
--- | ---
IRI | `https://w3id.org/cr#TaskToGeometryAssignment`
Super-classes |[cr:Assignment](https://w3id.org/cr#Assignment) (c)<br />
Restrictions |[cr:refGeometry](https://w3id.org/cr#refGeometry) (op) **exactly** 1 [http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct](http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct) (c)<br />[cr:refTask](https://w3id.org/cr#refTask) (op) **exactly** 1 [https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />
In domain of |[cr:refTask](https://w3id.org/cr#refTask) (op)<br />[cr:refGeometry](https://w3id.org/cr#refGeometry) (op)<br />

## Object Properties
[ConsumptionOf](#ConsumptionOf),
[has assignment](#hasassignment),
[hasConsumption](#hasConsumption),
[hasUnit](#hasUnit),
[is assignment Of](#isassignmentOf),
[ref](#ref),
[ref cost item](#refcostitem),
[ref geometry](#refgeometry),
[ref resource](#refresource),
[ref task](#reftask),
[](ConsumptionOf)
### ConsumptionOf
Property | Value
--- | ---
IRI | `https://w3id.org/cr#ConsumptionOf`
Domain(s) |[cr:Consumption](https://w3id.org/cr#Consumption) (c)<br />
Range(s) |[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
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
Domain(s) |[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
Range(s) |[cr:Consumption](https://w3id.org/cr#Consumption) (c)<br />
[](hasUnit)
### hasUnit
Property | Value
--- | ---
IRI | `https://w3id.org/cr#hasUnit`
Domain(s) |[cterm:Parameter](https://w3id.org/cterm#Parameter) (c)<br />[cr:Resource](https://w3id.org/cr#Resource) (c)<br />[cr:Consumption](https://w3id.org/cr#Consumption) (c)<br />
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
[](refcostitem)
### ref cost item
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refCostItem`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />[cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c)<br />
Range(s) |[ci:ProductionResult](https://w3id.org/ci#ProductionResult) (c)<br />
[](refgeometry)
### ref geometry
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refGeometry`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |[cr:CostItemToGeometryAssignment](https://w3id.org/cr#CostItemToGeometryAssignment) (c)<br />[cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c)<br />
Range(s) |[http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct](http://ifcowl.openbimstandards.org/IFC4_ADD2#IfcProduct) (c)<br />
[](refresource)
### ref resource
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refResource`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |[cr:ResourceToCostItemAssignment](https://w3id.org/cr#ResourceToCostItemAssignment) (c)<br />[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />
Range(s) |[cr:Resource](https://w3id.org/cr#Resource) (c)<br />
[](reftask)
### ref task
Property | Value
--- | ---
IRI | `https://w3id.org/cr#refTask`
Super-properties |[cr:ref](https://w3id.org/cr#ref) (op)<br />
Domain(s) |[cr:ResourceToTaskAssignment](https://w3id.org/cr#ResourceToTaskAssignment) (c)<br />[cr:TaskToGeometryAssignment](https://w3id.org/cr#TaskToGeometryAssignment) (c)<br />
Range(s) |[https://dtc-ontology.cms.ed.tum.de/ontology#Task](https://dtc-ontology.cms.ed.tum.de/ontology#Task) (c)<br />

## Datatype Properties
[accessory](#accessory),
[cam](#cam),
[code](#code),
[descriptionDetail](#descriptionDetail),
[descriptionGeneral](#descriptionGeneral),
[escluded](#escluded),
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
Domain(s) |[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />
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
[](escluded)
### escluded
Property | Value
--- | ---
IRI | `https://w3id.org/cr#escluded`
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
Domain(s) |[cr:EquipmentResource](https://w3id.org/cr#EquipmentResource) (c)<br />[cr:MaterialResource](https://w3id.org/cr#MaterialResource) (c)<br />
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