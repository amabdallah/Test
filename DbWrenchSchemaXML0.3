USE WaMDaM03;


/************ Remove Foreign Keys ***************/

ALTER TABLE scenarioslinkbridge DROP FOREIGN KEY fk_ScenariosLinkBridge_Scenarios;

ALTER TABLE scenariosnodebridge DROP FOREIGN KEY fk_ScenariosBridge_ScenarioNodeInstanceAttributeData;

ALTER TABLE scenariosnodebridge DROP FOREIGN KEY fk_ScenariosBridge_Scenarios;



/************ Update: Tables ***************/

/******************** Update Table: AttributeNameCV ************************/

ALTER TABLE AttributeNameCV CHANGE COLUMN ObjectName ObjectName VARCHAR(255) 
		COMMENT 'Lists the object name that has the corresponding attribute' NOT NULL;


/******************** Update Table: BinaryDataData ************************/

ALTER TABLE BinaryDataData DROP COLUMN ValueMeaning;

ALTER TABLE BinaryDataData ADD ValueMeaning BINARY(1) NOT NULL;


/******************** Add Table: LinkObjects ************************/

/* Build Table Structure */
CREATE TABLE LinkObjects
(
	LinkObjectID INTEGER AUTO_INCREMENT PRIMARY KEY DEFAULT 'Primary Key' NOT NULL,
	LinkObjectNameCV VARCHAR(255) NOT NULL,
	Description VARCHAR(500) NULL,
	Color VARCHAR(50) NULL,
	Shape VARCHAR(50) NULL,
	LinkObjectCode VARCHAR(50) NULL,
	ProjectID INTEGER NOT NULL,
	LinkObjectCategoryID INTEGER NOT NULL
) ENGINE=InnoDB;


/******************** Add Table: NodeObjectNameCV ************************/

/* Build Table Structure */
CREATE TABLE NodeObjectNameCV
(
	NodeObjectName VARCHAR(255) 
		COMMENT 'Controlled vocabulary term' NOT NULL,
	Definition VARCHAR(500) 
		COMMENT 'Definition of term' NOT NULL
) Holds information about node objects like reservoirs and demand sites ENGINE=InnoDB;

/* Add Primary Key */
ALTER TABLE NodeObjectNameCV ADD CONSTRAINT pkNodeObjectNameCV
	PRIMARY KEY (NodeObjectName);


/******************** Add Table: People ************************/

/* Build Table Structure */
CREATE TABLE People
(
	PersonID INTEGER AUTO_INCREMENT PRIMARY KEY 
		COMMENT 'PrimaryKey' NOT NULL,
	PersonFirstName VARCHAR(255) 
		COMMENT 'First name of the person' NOT NULL,
	PersonMiddleName VARCHAR(255) 
		COMMENT 'Middle name of the perosn' NULL,
	PersonLastName VARCHAR(255) 
		COMMENT 'Last name of the person' NOT NULL
) Describes people ENGINE=InnoDB;


/******************** Add Table: Projects ************************/

/* Build Table Structure */
CREATE TABLE Projects
(
	ProjectID INTEGER AUTO_INCREMENT PRIMARY KEY 
		COMMENT 'Primary key' NOT NULL,
	ProjectName VARCHAR(255) 
		COMMENT 'The project name like "Lower Bear River Watershed"' NOT NULL,
	Description VARCHAR(500) 
		COMMENT 'Project description' NULL,
	ProjectPurpose VARCHAR(500) 
		COMMENT 'The purpose of the project (e.g., simulation of restoration scenation)' NULL,
	Domain VARCHAR(255) NULL,
	DateCreated DATE 
		COMMENT 'The date that the project was careated on ' NULL,
	Status VARCHAR(255) 
		COMMENT 'Status of the project (e.g., active or inactive)' NULL
) Contains networks and link and node objects  ENGINE=InnoDB;


/******************** Add Table: ScenarioLinkInstanceAttributeData ************************/

/* Build Table Structure */
CREATE TABLE ScenarioLinkInstanceAttributeData
(
	ScenarioLinkInstanceAttributeDataID INTEGER AUTO_INCREMENT PRIMARY KEY DEFAULT 'Primary key' NOT NULL,
	AttributeMetaDataID INTEGER NULL,
	LinkInstanceID INTEGER NULL,
	AttributeDataValueID INTEGER NULL
) ENGINE=InnoDB;


/******************** Update Table: ScenariosLinkBridge ************************/

/* Remove Indexes */
DROP INDEX fk_ScenariosLinkBridge_Scenarios ON scenarioslinkbridge;


/******************** Update Table: ScenariosNodeBridge ************************/

/* Remove Indexes */
DROP INDEX fk_ScenariosBridge_ScenarioNodeInstanceAttributeData ON scenariosnodebridge;

DROP INDEX fk_ScenariosBridge_Scenarios ON scenariosnodebridge;


/******************** Update Table: SpatialReference ************************/

ALTER TABLE SpatialReference CHANGE COLUMN IsGeographic IsGeographic BIT NOT NULL;


/******************** Update Table: TimeSeriesMetadata ************************/

ALTER TABLE TimeSeriesMetadata CHANGE COLUMN IsRegular IsRegular BIT NULL;





/************ Add Foreign Keys ***************/
/*-----------------------------------------------------------
Warning: Versions of MySQL prior to 4.1.2 require indexes on all columns involved in a foreign key. The following indexes may be required: 
fk_Affiliations_Organization may require an index on table: Affiliations, column: OrganizationID
fk_Affiliations_Peopel may require an index on table: Affiliations, column: PersonID
fk_AttributeData_AttributeFormatCV may require an index on table: AttributeMetadata, column: AttributeFormatCV
fk_AttributeData_Attributes may require an index on table: AttributeMetadata, column: AttributesID
fk_AttributeData_DataTypeCV may require an index on table: AttributeMetadata, column: DataTypeCV
fk_AttributeData_Methods may require an index on table: AttributeMetadata, column: MethodID
fk_AttributeData_Units may require an index on table: AttributeMetadata, column: UnitID
fk_AttributeMetadata_Models may require an index on table: AttributeMetadata, column: ModelID
fk_AttributeMetadata_Samples may require an index on table: AttributeMetadata, column: SampleID
fk_AttributeMetadata_Sources may require an index on table: AttributeMetadata, column: SourceID
fk_Attributes_AttributeNameCV may require an index on table: Attributes, column: AttributeNameCV
fk_BinaryDataData_AttributeDataValues may require an index on table: BinaryDataData, column: AttributeDataValueID
fk_ColumnsData_AttributeDataValues may require an index on table: ColumnsData, column: AttributeDataValueID
fk_FileBasedData_AttributeDataValues may require an index on table: FileBasedData, column: AttributeDataValueID
fk_LinkAttributeCategory_LinkAttributeCategory may require an index on table: LinkAttributeCategory, column: ParentLinkAttributeCategoryID
fk_LinkAttributeCategory_LinkAttributeCategoryCV may require an index on table: LinkAttributeCategory, column: LinkAttributeCategotyCV
fk_LinkInstances_LinkObjects may require an index on table: LinkInstances, column: LinkObjectID
fk_LinkInstances_Networks may require an index on table: LinkInstances, column: NetworkID
fk_LinkInstances_NodeInstances may require an index on table: NodeInstances, column: NodeInstanceID, NodeInstanceID
fk_LinkInstances_NodeInstances may require an index on table: LinkInstances, column: StartNodeInstanceID, EndNodeInstanceID
fk_LinkObjectAttributes_Attributes may require an index on table: LinkObjectAttributes, column: AttributesID
fk_LinkObjectAttributes_LinkAttributeCategory may require an index on table: LinkObjectAttributes, column: LinkAttributeCategotyID
fk_LinkObjectAttributes_LinkObjects may require an index on table: LinkObjectAttributes, column: LinkObjectID
fk_LinkObjectCategory_LinkObjectCategory may require an index on table: LinkObjectCategory, column: ParentLinkObjectCategoryID
fk_LinkObjectCategory_LinkObjectCategoryCV may require an index on table: LinkObjectCategory, column: LinkObjectCategoryCV
fk_LinkObjects_LinkObjectCategory may require an index on table: LinkObjects, column: LinkObjectCategoryID
fk_LinkObjects_LinkObjectNameCV may require an index on table: LinkObjects, column: LinkObjectNameCV
fk_NodeObjects_Projects may require an index on table: LinkObjects, column: ProjectID
fk_Methods_MethodTypeCV may require an index on table: Methods, column: MethodTypeCV
fk_Methods_Organization may require an index on table: Methods, column: OrganizationID
fk_MultiColumnValues_MultiColumns may require an index on table: MultiColumnValues, column: MultiColumnID
fk_MultiColumns_AttributeDataValues may require an index on table: MultiColumns, column: AttributeDataValueID
fk_MultiColumns_Columns may require an index on table: MultiColumns, column: ColumnID
fk_Networks_Networks may require an index on table: Networks, column: ParentNetworkID
fk_Networks_Projects may require an index on table: Networks, column: ProjectID
fk_NodeAttributeCategory_NodeAttributeCategory may require an index on table: NodeAttributeCategory, column: ParentNodeAttributeCategoryID
fk_NodeAttributeCategory_NodeAttributeCategoryCV may require an index on table: NodeAttributeCategory, column: NodeAttributeCategotyCV
fk_NodeInstances_Networks may require an index on table: NodeInstances, column: NetworkID
fk_NodeInstances_NodeObjects may require an index on table: NodeInstances, column: NodeObjectID
fk_NodeInstances_SpatialReference may require an index on table: NodeInstances, column: SpatialReferenceID
fk_NodeObjectAttributes_Attributes may require an index on table: NodeObjectAttributes, column: AttributeID
fk_NodeObjectAttributes_NodeAttributeCategory may require an index on table: NodeObjectAttributes, column: NodeAttributeCategotyID
fk_NodeObjectAttributes_NodeObjects may require an index on table: NodeObjectAttributes, column: NodeObjectID
fk_NodeObjectCategory_NodeObjectCategory may require an index on table: NodeObjectCategory, column: ParentNodeObjectCategoryID
fk_NodeObjectCategory_NodeObjectCategoryCV may require an index on table: NodeObjectCategory, column: NodeObjectCategoryCV
fk_NodeObjects_NodeObjectCategory may require an index on table: NodeObjects, column: NodeObjectCategoryID
fk_NodeObjects_NodeObjectNameCV may require an index on table: NodeObjects, column: NodeObjectCV
fk_NodeObjects_Projects may require an index on table: NodeObjects, column: ProjectID
fk_Organization_Organization may require an index on table: Organization, column: ParentOrganizationID
fk_Organization_OrganizationType may require an index on table: Organization, column: OrganizationTypeCV
fk_ParameterData_AttributeDataValues may require an index on table: ParameterData, column: AttributeDataValueID
fk_PeopleProjects_Projects may require an index on table: PeopleProjects, column: ProjectID
fk_Users_People may require an index on table: PeopleProjects, column: PersonID
fk_PoliticalJurisdictionalNodeInstace_NodeInstances may require an index on table: PoliticalJurisdictionalNodeInstace, column: NodeInstanceID
fk_PoliticalJurisdictionalNodeInstace_PoliticalJurisdictions may require an index on table: PoliticalJurisdictionalNodeInstace, column: PoliticalJurisdictionID
fk_Samples_SampleMediumCV may require an index on table: Samples, column: SampleMediumCV
fk_Samples_SampleType may require an index on table: Samples, column: SampleTypeCV
fk_ScenarioLinkInstanceAttributeData_AttributeData may require an index on table: ScenarioLinkInstanceAttributeData, column: AttributeMetaDataID
fk_ScenarioLinkInstanceAttributeData_AttributeDataValues may require an index on table: ScenarioLinkInstanceAttributeData, column: AttributeDataValueID
fk_ScenarioLinkInstanceAttributeData_LinkInstances may require an index on table: ScenarioLinkInstanceAttributeData, column: LinkInstanceID
fk_ScenarioNodeInstanceAttributeData_AttributeData may require an index on table: ScenarioNodeInstanceAttributeData, column: AttributeMetaDataID
fk_ScenarioNodeInstanceAttributeData_AttributeDataValues may require an index on table: ScenarioNodeInstanceAttributeData, column: AttributeDataValueID
fk_ScenarioNodeInstanceAttributeData_NodeInstances may require an index on table: ScenarioNodeInstanceAttributeData, column: NodeInstanceID
fk_Scenarios_Networks may require an index on table: Scenarios, column: NetworkID
fk_ScenariosLinkBridge_ScenarioLinkInstanceAttributeData may require an index on table: ScenariosLinkBridge, column: ScenarioLinkInstanceAttributeDataID
fk_SeasonalParameterData_AttributeDataValues may require an index on table: SeasonalParameterData, column: AttributeDataValueID
fk_SeasonalParameterData_SeasonNameCV may require an index on table: SeasonalParameterData, column: SeasonNameCV
fk_Sources_Organization may require an index on table: Sources, column: OrganizationID
fk_TextDescriptorControlledData_AttributeDataValues may require an index on table: TextDescriptorControlledData, column: AttributeDataValueID
fk_TextDescriptorControlled_TextValueControlledCV may require an index on table: TextDescriptorControlledData, column: TextValueControlled
fk_TextDescriptorFreeData_AttributeDataValues may require an index on table: TextDescriptorFreeData, column: AttributeDataValueID
fk_TimeSeries_AttributeDataValues may require an index on table: TimeSeries, column: AttributeDataValueID
fk_TimeSeries_CensorCodeCV may require an index on table: TimeSeries, column: CensorCode
fk_TimeSeries_TimeSeriesMetadata may require an index on table: TimeSeries, column: TimeSereisMetadataID
fk_TimeSeriesMetadata_Units may require an index on table: TimeSeriesMetadata, column: TimeUnitID
-----------------------------------------------------------
*/

/* Add Foreign Key: fk_Affiliations_Organization */
ALTER TABLE Affiliations ADD CONSTRAINT fk_Affiliations_Organization
	FOREIGN KEY (OrganizationID) REFERENCES Organization (OrganizationID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Affiliations_Peopel */
ALTER TABLE Affiliations ADD CONSTRAINT fk_Affiliations_Peopel
	FOREIGN KEY (PersonID) REFERENCES People (PersonID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeData_AttributeFormatCV */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeData_AttributeFormatCV
	FOREIGN KEY (AttributeFormatCV) REFERENCES AttributeFormatCV (AttributeFormat)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeData_Attributes */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeData_Attributes
	FOREIGN KEY (AttributesID) REFERENCES Attributes (AttributeID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeData_DataTypeCV */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeData_DataTypeCV
	FOREIGN KEY (DataTypeCV) REFERENCES DataTypeCV (DataType)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeData_Methods */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeData_Methods
	FOREIGN KEY (MethodID) REFERENCES Methods (MethodID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeData_Units */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeData_Units
	FOREIGN KEY (UnitID) REFERENCES Units (UnitID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeMetadata_Models */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeMetadata_Models
	FOREIGN KEY (ModelID) REFERENCES Models (ModelID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeMetadata_Samples */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeMetadata_Samples
	FOREIGN KEY (SampleID) REFERENCES Samples (SampleID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_AttributeMetadata_Sources */
ALTER TABLE AttributeMetadata ADD CONSTRAINT fk_AttributeMetadata_Sources
	FOREIGN KEY (SourceID) REFERENCES Sources (SourceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Attributes_AttributeNameCV */
ALTER TABLE Attributes ADD CONSTRAINT fk_Attributes_AttributeNameCV
	FOREIGN KEY (AttributeNameCV) REFERENCES AttributeNameCV (AttributeName)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_BinaryDataData_AttributeDataValues */
ALTER TABLE BinaryDataData ADD CONSTRAINT fk_BinaryDataData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ColumnsData_AttributeDataValues */
ALTER TABLE ColumnsData ADD CONSTRAINT fk_ColumnsData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_FileBasedData_AttributeDataValues */
ALTER TABLE FileBasedData ADD CONSTRAINT fk_FileBasedData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkAttributeCategory_LinkAttributeCategory */
ALTER TABLE LinkAttributeCategory ADD CONSTRAINT fk_LinkAttributeCategory_LinkAttributeCategory
	FOREIGN KEY (ParentLinkAttributeCategoryID) REFERENCES LinkAttributeCategory (LinkCategotyID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkAttributeCategory_LinkAttributeCategoryCV */
ALTER TABLE LinkAttributeCategory ADD CONSTRAINT fk_LinkAttributeCategory_LinkAttributeCategoryCV
	FOREIGN KEY (LinkAttributeCategotyCV) REFERENCES LinkAttributeCategoryCV (LinkAttributeCategoty)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkInstances_LinkObjects */
ALTER TABLE LinkInstances ADD CONSTRAINT fk_LinkInstances_LinkObjects
	FOREIGN KEY (LinkObjectID) REFERENCES LinkObjects (LinkObjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkInstances_Networks */
ALTER TABLE LinkInstances ADD CONSTRAINT fk_LinkInstances_Networks
	FOREIGN KEY (NetworkID) REFERENCES Networks (NetworkID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkInstances_NodeInstances */
ALTER TABLE LinkInstances ADD CONSTRAINT fk_LinkInstances_NodeInstances
	FOREIGN KEY (StartNodeInstanceID, EndNodeInstanceID) REFERENCES NodeInstances (NodeInstanceID, NodeInstanceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjectAttributes_Attributes */
ALTER TABLE LinkObjectAttributes ADD CONSTRAINT fk_LinkObjectAttributes_Attributes
	FOREIGN KEY (AttributesID) REFERENCES Attributes (AttributeID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjectAttributes_LinkAttributeCategory */
ALTER TABLE LinkObjectAttributes ADD CONSTRAINT fk_LinkObjectAttributes_LinkAttributeCategory
	FOREIGN KEY (LinkAttributeCategotyID) REFERENCES LinkAttributeCategory (LinkCategotyID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjectAttributes_LinkObjects */
ALTER TABLE LinkObjectAttributes ADD CONSTRAINT fk_LinkObjectAttributes_LinkObjects
	FOREIGN KEY (LinkObjectID) REFERENCES LinkObjects (LinkObjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjectCategory_LinkObjectCategory */
ALTER TABLE LinkObjectCategory ADD CONSTRAINT fk_LinkObjectCategory_LinkObjectCategory
	FOREIGN KEY (ParentLinkObjectCategoryID) REFERENCES LinkObjectCategory (LinkObjectCategoryID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjectCategory_LinkObjectCategoryCV */
ALTER TABLE LinkObjectCategory ADD CONSTRAINT fk_LinkObjectCategory_LinkObjectCategoryCV
	FOREIGN KEY (LinkObjectCategoryCV) REFERENCES LinkObjectCategoryCV (LinkObjectCategory)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjects_LinkObjectCategory */
ALTER TABLE LinkObjects ADD CONSTRAINT fk_LinkObjects_LinkObjectCategory
	FOREIGN KEY (LinkObjectCategoryID) REFERENCES LinkObjectCategory (LinkObjectCategoryID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_LinkObjects_LinkObjectNameCV */
ALTER TABLE LinkObjects ADD CONSTRAINT fk_LinkObjects_LinkObjectNameCV
	FOREIGN KEY (LinkObjectNameCV) REFERENCES LinkObjectNameCV (LinkObjectName)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Methods_MethodTypeCV */
ALTER TABLE Methods ADD CONSTRAINT fk_Methods_MethodTypeCV
	FOREIGN KEY (MethodTypeCV) REFERENCES MethodTypeCV (MethodType)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Methods_Organization */
ALTER TABLE Methods ADD CONSTRAINT fk_Methods_Organization
	FOREIGN KEY (OrganizationID) REFERENCES Organization (OrganizationID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_MultiColumnValues_MultiColumns */
ALTER TABLE MultiColumnValues ADD CONSTRAINT fk_MultiColumnValues_MultiColumns
	FOREIGN KEY (MultiColumnID) REFERENCES MultiColumns (MultiColumnID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_MultiColumns_AttributeDataValues */
ALTER TABLE MultiColumns ADD CONSTRAINT fk_MultiColumns_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_MultiColumns_Columns */
ALTER TABLE MultiColumns ADD CONSTRAINT fk_MultiColumns_Columns
	FOREIGN KEY (ColumnID) REFERENCES ColumnsData (ColumnID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Networks_Networks */
ALTER TABLE Networks ADD CONSTRAINT fk_Networks_Networks
	FOREIGN KEY (ParentNetworkID) REFERENCES Networks (NetworkID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Networks_Projects */
ALTER TABLE Networks ADD CONSTRAINT fk_Networks_Projects
	FOREIGN KEY (ProjectID) REFERENCES Projects (ProjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeAttributeCategory_NodeAttributeCategory */
ALTER TABLE NodeAttributeCategory ADD CONSTRAINT fk_NodeAttributeCategory_NodeAttributeCategory
	FOREIGN KEY (ParentNodeAttributeCategoryID) REFERENCES NodeAttributeCategory (NodeAttributeCategotyID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeAttributeCategory_NodeAttributeCategoryCV */
ALTER TABLE NodeAttributeCategory ADD CONSTRAINT fk_NodeAttributeCategory_NodeAttributeCategoryCV
	FOREIGN KEY (NodeAttributeCategotyCV) REFERENCES NodeAttributeCategoryCV (NodeAttributeCategoty)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeInstances_Networks */
ALTER TABLE NodeInstances ADD CONSTRAINT fk_NodeInstances_Networks
	FOREIGN KEY (NetworkID) REFERENCES Networks (NetworkID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeInstances_NodeObjects */
ALTER TABLE NodeInstances ADD CONSTRAINT fk_NodeInstances_NodeObjects
	FOREIGN KEY (NodeObjectID) REFERENCES NodeObjects (NodeObjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeInstances_SpatialReference */
ALTER TABLE NodeInstances ADD CONSTRAINT fk_NodeInstances_SpatialReference
	FOREIGN KEY (SpatialReferenceID) REFERENCES SpatialReference (SpatialReferenceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjectAttributes_Attributes */
ALTER TABLE NodeObjectAttributes ADD CONSTRAINT fk_NodeObjectAttributes_Attributes
	FOREIGN KEY (AttributeID) REFERENCES Attributes (AttributeID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjectAttributes_NodeAttributeCategory */
ALTER TABLE NodeObjectAttributes ADD CONSTRAINT fk_NodeObjectAttributes_NodeAttributeCategory
	FOREIGN KEY (NodeAttributeCategotyID) REFERENCES NodeAttributeCategory (NodeAttributeCategotyID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjectAttributes_NodeObjects */
ALTER TABLE NodeObjectAttributes ADD CONSTRAINT fk_NodeObjectAttributes_NodeObjects
	FOREIGN KEY (NodeObjectID) REFERENCES NodeObjects (NodeObjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjectCategory_NodeObjectCategory */
ALTER TABLE NodeObjectCategory ADD CONSTRAINT fk_NodeObjectCategory_NodeObjectCategory
	FOREIGN KEY (ParentNodeObjectCategoryID) REFERENCES NodeObjectCategory (NodeObjectCategoryID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjectCategory_NodeObjectCategoryCV */
ALTER TABLE NodeObjectCategory ADD CONSTRAINT fk_NodeObjectCategory_NodeObjectCategoryCV
	FOREIGN KEY (NodeObjectCategoryCV) REFERENCES NodeObjectCategoryCV (NodeObjectCategory)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjects_NodeObjectCategory */
ALTER TABLE NodeObjects ADD CONSTRAINT fk_NodeObjects_NodeObjectCategory
	FOREIGN KEY (NodeObjectCategoryID) REFERENCES NodeObjectCategory (NodeObjectCategoryID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjects_NodeObjectNameCV */
ALTER TABLE NodeObjects ADD CONSTRAINT fk_NodeObjects_NodeObjectNameCV
	FOREIGN KEY (NodeObjectCV) REFERENCES NodeObjectNameCV (NodeObjectName)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_NodeObjects_Projects */
ALTER TABLE NodeObjects ADD CONSTRAINT fk_NodeObjects_Projects
	FOREIGN KEY (ProjectID) REFERENCES Projects (ProjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Organization_Organization */
ALTER TABLE Organization ADD CONSTRAINT fk_Organization_Organization
	FOREIGN KEY (ParentOrganizationID) REFERENCES Organization (OrganizationID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Organization_OrganizationType */
ALTER TABLE Organization ADD CONSTRAINT fk_Organization_OrganizationType
	FOREIGN KEY (OrganizationTypeCV) REFERENCES OrganizationType (OrganizationTypeCV)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ParameterData_AttributeDataValues */
ALTER TABLE ParameterData ADD CONSTRAINT fk_ParameterData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_PeopleProjects_Projects */
ALTER TABLE PeopleProjects ADD CONSTRAINT fk_PeopleProjects_Projects
	FOREIGN KEY (ProjectID) REFERENCES Projects (ProjectID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Users_People */
ALTER TABLE PeopleProjects ADD CONSTRAINT fk_Users_People
	FOREIGN KEY (PersonID) REFERENCES People (PersonID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_PoliticalJurisdictionalNodeInstace_NodeInstances */
ALTER TABLE PoliticalJurisdictionalNodeInstace ADD CONSTRAINT fk_PoliticalJurisdictionalNodeInstace_NodeInstances
	FOREIGN KEY (NodeInstanceID) REFERENCES NodeInstances (NodeInstanceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_PoliticalJurisdictionalNodeInstace_PoliticalJurisdictions */
ALTER TABLE PoliticalJurisdictionalNodeInstace ADD CONSTRAINT fk_PoliticalJurisdictionalNodeInstace_PoliticalJurisdictions
	FOREIGN KEY (PoliticalJurisdictionID) REFERENCES PoliticalJurisdictions (PoliticalJurisdictionID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Samples_SampleMediumCV */
ALTER TABLE Samples ADD CONSTRAINT fk_Samples_SampleMediumCV
	FOREIGN KEY (SampleMediumCV) REFERENCES SampleMediumCV (SampleMedium)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Samples_SampleType */
ALTER TABLE Samples ADD CONSTRAINT fk_Samples_SampleType
	FOREIGN KEY (SampleTypeCV) REFERENCES SampleType (SampleType)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioLinkInstanceAttributeData_AttributeData */
ALTER TABLE ScenarioLinkInstanceAttributeData ADD CONSTRAINT fk_ScenarioLinkInstanceAttributeData_AttributeData
	FOREIGN KEY (AttributeMetaDataID) REFERENCES AttributeMetadata (AttributeMetaDataID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioLinkInstanceAttributeData_AttributeDataValues */
ALTER TABLE ScenarioLinkInstanceAttributeData ADD CONSTRAINT fk_ScenarioLinkInstanceAttributeData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioLinkInstanceAttributeData_LinkInstances */
ALTER TABLE ScenarioLinkInstanceAttributeData ADD CONSTRAINT fk_ScenarioLinkInstanceAttributeData_LinkInstances
	FOREIGN KEY (LinkInstanceID) REFERENCES LinkInstances (LinkInstanceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioNodeInstanceAttributeData_AttributeData */
ALTER TABLE ScenarioNodeInstanceAttributeData ADD CONSTRAINT fk_ScenarioNodeInstanceAttributeData_AttributeData
	FOREIGN KEY (AttributeMetaDataID) REFERENCES AttributeMetadata (AttributeMetaDataID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioNodeInstanceAttributeData_AttributeDataValues */
ALTER TABLE ScenarioNodeInstanceAttributeData ADD CONSTRAINT fk_ScenarioNodeInstanceAttributeData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenarioNodeInstanceAttributeData_NodeInstances */
ALTER TABLE ScenarioNodeInstanceAttributeData ADD CONSTRAINT fk_ScenarioNodeInstanceAttributeData_NodeInstances
	FOREIGN KEY (NodeInstanceID) REFERENCES NodeInstances (NodeInstanceID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Scenarios_Networks */
ALTER TABLE Scenarios ADD CONSTRAINT fk_Scenarios_Networks
	FOREIGN KEY (NetworkID) REFERENCES Networks (NetworkID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_ScenariosLinkBridge_ScenarioLinkInstanceAttributeData */
ALTER TABLE ScenariosLinkBridge ADD CONSTRAINT fk_ScenariosLinkBridge_ScenarioLinkInstanceAttributeData
	FOREIGN KEY (ScenarioLinkInstanceAttributeDataID) REFERENCES ScenarioLinkInstanceAttributeData (ScenarioLinkInstanceAttributeDataID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_SeasonalParameterData_AttributeDataValues */
ALTER TABLE SeasonalParameterData ADD CONSTRAINT fk_SeasonalParameterData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_SeasonalParameterData_SeasonNameCV */
ALTER TABLE SeasonalParameterData ADD CONSTRAINT fk_SeasonalParameterData_SeasonNameCV
	FOREIGN KEY (SeasonNameCV) REFERENCES SeasonNameCV (SeasonName)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_Sources_Organization */
ALTER TABLE Sources ADD CONSTRAINT fk_Sources_Organization
	FOREIGN KEY (OrganizationID) REFERENCES Organization (OrganizationID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TextDescriptorControlledData_AttributeDataValues */
ALTER TABLE TextDescriptorControlledData ADD CONSTRAINT fk_TextDescriptorControlledData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TextDescriptorControlled_TextValueControlledCV */
ALTER TABLE TextDescriptorControlledData ADD CONSTRAINT fk_TextDescriptorControlled_TextValueControlledCV
	FOREIGN KEY (TextValueControlled) REFERENCES TextValueControlledCV (TextValueControlled)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TextDescriptorFreeData_AttributeDataValues */
ALTER TABLE TextDescriptorFreeData ADD CONSTRAINT fk_TextDescriptorFreeData_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TimeSeries_AttributeDataValues */
ALTER TABLE TimeSeries ADD CONSTRAINT fk_TimeSeries_AttributeDataValues
	FOREIGN KEY (AttributeDataValueID) REFERENCES AttributeDataValues (AttributeDataValueID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TimeSeries_CensorCodeCV */
ALTER TABLE TimeSeries ADD CONSTRAINT fk_TimeSeries_CensorCodeCV
	FOREIGN KEY (CensorCode) REFERENCES CensorCodeCV (CensorCode)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TimeSeries_TimeSeriesMetadata */
ALTER TABLE TimeSeries ADD CONSTRAINT fk_TimeSeries_TimeSeriesMetadata
	FOREIGN KEY (TimeSereisMetadataID) REFERENCES TimeSeriesMetadata (TimeSereisMetadataID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;

/* Add Foreign Key: fk_TimeSeriesMetadata_Units */
ALTER TABLE TimeSeriesMetadata ADD CONSTRAINT fk_TimeSeriesMetadata_Units
	FOREIGN KEY (TimeUnitID) REFERENCES Units (UnitID)
	ON UPDATE NO ACTION ON DELETE NO ACTION;
