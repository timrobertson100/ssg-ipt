---
title: IPT Citation Format
drawer: true
category: Documentation
subCategory: User guides
---

# IPT Citation Format

<p class="comment-warning">NB: This page has not been revised</p>
 
## Introduction

Since IPT v2.2 data publishers can choose to let the IPT auto-generate a citation for their dataset. Before publishers had to enter their own citation.

The auto-generated citation format includes the dataset version number and DOI. Human readers can use the DOI to link to the dataset homepage, and can use the version number to locate and download the exact version. This enables reproducing scientific results based on usage of the dataset.

A detailed description of the IPT's citation format is described below. It is important to note that the format is based on DataCite’s preferred citation format, and satisfies the [Joint Declaration of Data Citation Principles](https://www.force11.org/datacitation). For more information about the DataCite format, you can refer to Section 2.2 Citation of their [Metadata Schema](http://schema.datacite.org/meta/kernel-3/doc/DataCite-MetadataKernel_v3.0.pdf). Each part of the citation is described in the table below, with several examples given afterward.

## Citation Format

#### Creators<sup>1</sup> (PublicationYear)<sup>2</sup>: Title<sup>3</sup>. Version<sup>4</sup>. Publisher<sup>5</sup>. ResourceType<sup>6</sup>. Identifier<sup>7</sup>

7 citation parts explained:

| **Citation Part** | **Description** |
|:------------------|:----------------|
| 1.Creators        | One or more individuals, groups, or institutions responsible for the creation of the dataset. All contributors to the dataset should be listed - see [data citation principle #2](https://www.force11.org/datacitation#JDCP2). Creators should be aware, however, that the full list can be truncated by the Journal during typesetting (e.g. According to [Nature’s guidelines](http://www.nature.com/sdata/for-authors/submission-guidelines#references), they will truncate at 6 creators). Creators should be listed last name first, followed by initials of given names. Creators are listed according the importance of the role they played in the creation of the dataset, with the most important creator appearing first. Multiple creators are separated by commas. |
| 2.PublicationYear | Year the dataset version was published/made publicly available. |
| 3.Title           | Title of the dataset. Only the first word of the title should have an initial capital and the title should be written exactly as it appears in the work cited, ending with a full stop. |
| 4.Version         | Dataset version. A new version number gets assigned by the IPT each time the dataset gets published. The version should be written “Version major\_version.minor\_version”. The version number enables “identification of, access to, and verification of the specific data that support a claim” - see [data citation principle #7](https://www.force11.org/datacitation#JDCP7). |
| 5.Publisher       | Institution that published (owns) the dataset. In order to still give credit to the repository hosting the data, the repository name could be listed under creators. |
| 6.ResourceType    | Type of resource published. A description of the type of resource constructed using the ResourceTypeGeneral/ResourceType pair: ResourceTypeGeneral will always be equal to “Dataset”, and the ResourceType is a single term specifying the specific type of dataset, e.g. "Occurrence" or "Checklist".  |
| 7.Identifier      | The DOI (digital object identifier) handle that resolves to the online dataset. If a DOI is lacking, a link to the online IPT dataset page will be used instead. A DOI is highly preferred, since the DOI guarantees persistent access, whereas the IPT URL can change. For citation purposes, DataCite recommends that DOIs are displayed as linkable, permanent URLs. |

## Example Citations

  * Example citation for occurrence dataset, with institutional creator, and DOI:
> Biodiversity Institute of Ontario (2011) Migratory birds of Ontario. Version 2.1. University of Guelph. Dataset/Occurrence. http://dx.doi.org/10.5886/qzxxd2pa
  * Example citation for checklist dataset, with more than 9 creators, and DOI:
> Brouillet L, Desmet P, Coursol F, Meades SJ, Favreau M, Anions M, Bélisle P, Gendreau C, Shorthouse D (2010) Database of vascular plants of Canada. Version 3.1. Université de Montréal Biodiversity Centre. Dataset/Checklist. http://doi.org/10.5886/1bft7W5f
  * Example citation for occurrence dataset with 3 creators, and without DOI:
> Harihar A, Pandav B, Hussein M (2014) Camera trap database of Tigers from Rajaji National Park, Uttarakhand. Version 1.0. Wildlife Institute of India. Dataset/Occurrence Data. http://ibif.gov.in:8080/ipt/resource.do?r=camera_trap_rajaji_np