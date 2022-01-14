## GUS/Strategies-WDK
Management of biomedical big data to enable intuitive access, visualization, and mining is an ongoing challenge. Exploiting the GUS/Strategies-WDK system, our group has successfully developed and deployed such a system in support of functional genomics data for diverse user communities, including the NIAID EuPathDB Bioinformatics Resource Center (http://eupathdb.org), the NIDDK Beta Cell Biology Consortium Genomics Resource (http://genomics.betacell.org), and the NIA NIAGADS Genomics database (www.niagads.org/genomics). Although thus far used primarily for functional genomics datasets, our system is inherently generalizable beyond omics data, including clinical records.

<em>Our philosophy for building a web-resource</em>
<ol>
<li>Identify relevant data types for the target community.</li>
<li>Define the information that describes each such data type.</li>
<li>Formulate meaningful data specific questions.</li>
<li>Facilitate discovery and insight through an intuitive interface.</li>
</ol>

Correspondingly: 

<em>In our system</em>
<ol>
<li>Developers define records of interest.</li>
<li>Developers specify each record’s attributes and how to display them.</li>
<li>For each record type, developers specify a list of parameterizable questions.</li>
<li>Users build complex queries (strategies) in a graphical interface.</li>
</ol>

![GUS WDK architecture](https://www.cbil.upenn.edu/sites/default/files/current_architecture-cs-em_0.jpg)

<em>GUS</em>
GUS (Genomics Unified Schema) is a relational database schema that has been deployed in Oracle and PostgreSQL. The schema is modular and has been updated (GUS4) to better cover investigational studies, results from high (and not so high) throughput technologies, technology used, biological sequences, metadata and associated standards, pathways and networks, and data control. In particular, deep phenotyping (e.g epidemiological results) can be easily captured and interpreted through associations to ontology terms. Objectives, study design, protocols, and results are all linked in a manner consistent with established standards (MAGE-TAB, Ontology for Biomedical Investigations).
<p>
The GUS source is now maintained in GitHub by the VEuPathDB Bioinformatics Resource Center: https://github.com/VEuPathDB/GusSchema, https://github.com/VEuPathDB/GusAppFramework.
<p>
<em>Strategies-WDK</em>
Mining the data in GUS can be performed using the Strategies-WDK (Fischer et al. Database 2011) to provide a workspace for generating, combining, saving, and sharing “strategies.” Strategies are graphical workflows of database searches of record types (such as genes, SNPs, studies) that can be selected (favorites, baskets), combined, and transformed (SNPs to genes, genes to pathways, pathways to chemical compounds). This system has proved highly popular and successful in enabling sophisticating data-mining by a diverse group of end users, and has recently been updated so as to provide the ability to browse extensive metadata (e.g., clinical epidemiology variables), inspired by the Harvest data discovery platform (Pennington et. al., JAMIA 2014). Also new is the introduction of an analysis tab for the records returned by Strategy searches. For example, a list of returned genes can be analyzed for Gene Ontology or KEGG pathway enrichment without having to leave the Strategies workspace page. Future plans include refactoring the combined GUS/ Strategies-WDK system so that this package is easier for other projects and communities to install and customize.
