# TraitAM, a global spore trait database for arbuscular mycorrhizal fungi

[https://doi.org/10.5061/dryad.6hdr7sr8z](https://doi.org/10.5061/dryad.6hdr7sr8z)

Contact: Dr. V. Bala Chaudhary, [bala.chaudhary@dartmouth.edu](mailto:bala.chaudhary@dartmouth.edu)

**Filenames**: All files have names of the form "DataRecord_(number)*(contents)*(date updated, DDMonYYYY)," for example, "DataRecord_1_CalculatedTraitMetrics_18Jun2024.csv" is a data record #1, contains "calculated trait metrics," and was last updated on June 18th, 2024.

TraitAM contains data on the spore traits of all Arbuscular Mycorrhizal (AM) fungi with available species descriptions through 2023. Data were collected by manually reading species descriptions and extracting relevant information from 2019 to 2024. For full description, methods, and metadata see publication:

Chaudhary, V. B., Gonzalez, J. B., Nokes, L. F., Cooper, P. O., Katula, A. M., Mares, E. C., Limbu, S. P., Robinson, J. N., Aguilar-Trigueros, C. A. (2024). TraitAM, a global spore trait and phylogeny database for arbuscular mycorrhizal fungi. Manuscript submitted for publication.

**Files:**

* DataRecord_1_CalculatedTraitMetrics_18Jun2024.csv: Table containing the calculated trait metrics for all taxa in the database, including spore volume, shape, color, wall investment, and ornamentation height.

- DataRecord_2_TraitAMraw_18Jun2024.csv: Table containing the raw data used to calculate the trait metrics in DataRecord_1. Cells containing "NA" reflect data that was not present in the species descriptions.

* DataRecord_3_TraitMetricsCode_18Jun2024.R: R script containing the annotated code used to calculate the trait metrics in DataRecord_1 from the raw data in DataRecord_2.

- DataRecord_4_SpeciesDescriptions_18Jun2024.csv: Table containing a list of all species in the TraitAM database and the bibliographic information for the paper containing the species description we used to collect data on the species for DataRecord_2.

* DataRecord_5_SpeciesListWithAccnNum_Oct2023.csv: Table containing a list of species used in the creation of the Arbuscular Mycorrhizal fungal phylogeny, with the GenBank accession numbers for the sequences used in the creation of the phylogenetic tree.

- DataRecord_6_LSUseqsLROR-FLR2_28Oct2023.fasta: LSU sequences used in phylogenetic analysis, trimmed to LROR-FLR2 (n=231).

* DataRecord_7_FinalTree_Oct2023.tre: Phylogenetic tree generated from DataRecord_6.

- DataRecord_8_PhyloanalysisCode_28Oct2023.txt: Code used in phylogenetic analysis for Maximum Likelihood and Bayesian Inference approaches used to generate DataRecord_7.

**Metadata for DataRecord_1:**

* species = species binomial nomenclature, followed by “_morpha” for acaulosporoid morphs and “_morphg” for glomoid morphs, if applicable

- order = Taxonomic order of the species

* family = Taxonomic family of the species

- genus = Genus

* vol_mean = Spore volume (μm3)

- shape_mean = Spore shape, aspect ratio of spore length (μm) / spore width (μm)

* color_most = Color mode (see metadata for DataRecord_2)

- investment_mean = Spore wall investment, ratio of wall volume / total spore volume

* orn_height_mean = Mean ornamentation height (μm) (see metadata for DataRecord_2)

**Metadata for DataRecord_2:**

* species = Species binomial nomenclature

- order = Taxonomic order of the species

* family = Taxonomic family of the species

- genus = Genus

* color_low = “Minimum” color: To standardize the color data across the database, we assigned the following ordinal scale for common color along a pigmentation gradient ranging from 0 (hyaline, no pigmentation) to 6 (fully melanized, dark). The intermediate values include 1, white to cream or pink, 2, yellow, 3, green, 4, orange to red, and 5, brown. For each species we include three color data points: minimum, mode, and maximum. If a spore with “yellow to yellow orange” it would have color minimum 2, color mode 2, and color maximum 4.

- color_most = Color mode, see above

* color_high = Color maximum, see above

- orn_height_min = Minimum height of ornamentation, as given in species description. 0 if there is no ornamentation

* orn_height_mean = Mean height of ornamentation, as given or as the average of the minimum and maximum given if not. 0 if there is no ornamentation

- orn_height_max = Maximum height of ornamentation, as given. 0 if there is no maximum ornamentation

* orn_diam_min = Minimum diameter of ornamentation, as given in species description. 0 if there is no ornamentation

- orn_diam_mean = Mean diameter of ornamentation, as given or as the average of the minimum and maximum given if not. 0 if there is no ornamentation

* orn_diam_max = Maximum diameter of ornamentation, as given. 0 if there is no maximum ornamentation

- min_wall_thickness = Minimum wall thickness of the spores

* mean_wall_thickness = Mean wall thickness of the spores

- max_wall_thickness = Maximum wall thickness of the spores

* dim1.min2 = Dimension 1 minimum 2 (lower minimum). Spore dimensions are given for each spore shape as ranges with up to four values describing the distribution of each dimension. The traitAM database includes eight dimension data points for each spore shape described: dimension lower minimum, dimension higher minimum, dimension lower maximum, and dimension higher maximum for two dimensions, length and width.

- dim1.min = Dimension 1 minimum

* dim1.max = Dimension 1 lower maximum

- dim1.max2 = Dimension 1 upper maximum

* dim2.min2 = Dimension 2 lower minimum

- dim2.min = Dimension 2 upper minimum

* dim2.max = Dimension 2 lower maximum

- dim2.max2 = Dimension 2 upper maximum

Changelog: all changes to the TraitAM database and any files will be logged here with a timestamp and a description of changes.



# Provenance 

This section was added after capturing a versioned copy of TraitAM

## for humans 

| label | content digest / fingerprint |
| --- | --- |
| DataRecord_1_CalculatedTraitMetrics_18Jun2024.csv | hash://sha256/dff4a33ec5fe8ade65c2d157048a9a99b537c316dea6329eb4f23775d2e8f79e |
| DataRecord_2_TraitAMraw_18Jun2024.csv.csv | hash://sha256/5a4504cfdaa90e60db6ab0032af4198ae84d2f2c1fb82481d61ac786ce5fdfb0 |
| DataRecord_3_TraitMetricsCode_18Jun2024.R | hash://sha256/163d7d61947cf3d68836ad2af8f3f7cb8d24dff62cd5a7231633da2d6234059c |
| DataRecord_4_SpeciesDescriptions_18Jun2024.csv | hash://sha256/7e4a5b92d12bef0a233afa5b0f877bf93e4f6bdea47f4f11e234b159d35ea7be |
| DataRecord_5_SpeciesListWithAccnNum_Oct2023.csv | hash://sha256/313eaa20cf99ea1dcb5991cd6c3747734a1d68b85cc7f563df452a5cd70d384b |
| DataRecord_6_LSUseqsLROR-FLR2_28Oct2023.fasta | hash://sha256/bf83fa7b986b72be199e6ab8d6d4d9ffa21b778aae56a0965b5b2f7424e6acc8 |
| DataRecord_7_FinalTree_Oct2023.tre | hash://sha256/1221316f6744ac9e00e1374c11a6edfe23032c7e39ab402bd3defca5be3e9013 |
| DataRecord_8_PhyloanalysisCode_28Oct2023.txt | hash://sha256/ea7fcc0f54c8026075442e26c105a7c28e5ca08df7e17cd70447df05a2a2f447 |
| README.md | hash://sha256/de75afb0a7222a5591e3e39869befa2c0fb5d7a2e4ade47d49380e1ccb8b39fb |

as generated via 

```
preston alias https://datadryad.org/api/v2/versions/355108/files\
 | preston cat\
 | jq -c '._embedded["stash:files"][] | { path: .path, digest: ("hash://sha256/" + .digest) }' \
 | mlr --ijsonl --omd cat
```

and files in repository generated via 

```
preston alias https://datadryad.org/api/v2/versions/355108/files \
 | preston cat \
 | jq -c '._embedded["stash:files"][] | { path: .path, digest: ("hash://sha256/" + .digest) }' \
 | mlr --ijsonl --otsvlite reorder -f digest,path \
 | tail -n+2 \
 | sed 's/^/preston cat /g' \
 | tr '\t' '>' \
 | bash
```

## for machines

The ```data/``` folder contains a data package describing the result 

```
preston track https://doi.org/10.5061/dryad.6hdr7sr8z
```

using preston v0.11.7 

with 

```
preston head 
```

producing the unique data package fingerprint - 

```
hash://sha256/5524ed2ea9ab8d55ef1a1669e3208723a625109de9ea3357244a3b7e4569c0b7
```

with associated content 

```
preston alias --anchor hash://sha256/5524ed2ea9ab8d55ef1a1669e3208723a625109de9ea3357244a3b7e4569c0b7
```


```
<https://doi.org/10.5061/dryad.6hdr7sr8z> <http://purl.org/pav/hasVersion> <hash://sha256/b43234aa81db401923b42dc8dc3fd8e053f3105e43ac3089d04e13d453464cf3> <urn:uuid:66f8b485-7bf6-4363-b6cc-9b94f8b9d200> .
<https://datadryad.org/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z/versions> <http://purl.org/pav/hasVersion> <hash://sha256/fd6ca89c70a4893b615a976b02362025d522d27768ab98a1ef138212ddfcdea2> <urn:uuid:edc5cc56-0ff6-4186-9a49-12663455d876> .
<https://datadryad.org/api/v2/versions/355108/files> <http://purl.org/pav/hasVersion> <hash://sha256/e4a3816c222045fa6cb6f75670c3cc5b899b6dcb5309e961b94f0aba9880c46a> <urn:uuid:75ea42cc-a9b7-4190-b168-cc0cd6e36c9a> .
<https://datadryad.org/api/v2/files/3985003/download> <http://purl.org/pav/hasVersion> <hash://sha256/dff4a33ec5fe8ade65c2d157048a9a99b537c316dea6329eb4f23775d2e8f79e> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985003/download> <http://purl.org/pav/hasVersion> <hash://sha256/dff4a33ec5fe8ade65c2d157048a9a99b537c316dea6329eb4f23775d2e8f79e> <urn:uuid:510c2765-e4fd-4708-8f98-4c98f40877fe> .
<https://datadryad.org/api/v2/files/3985013/download> <http://purl.org/pav/hasVersion> <hash://sha256/5a4504cfdaa90e60db6ab0032af4198ae84d2f2c1fb82481d61ac786ce5fdfb0> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985013/download> <http://purl.org/pav/hasVersion> <hash://sha256/5a4504cfdaa90e60db6ab0032af4198ae84d2f2c1fb82481d61ac786ce5fdfb0> <urn:uuid:dd87ded2-b6cb-4791-a0d9-1284f7f8feb1> .
<https://datadryad.org/api/v2/files/3985011/download> <http://purl.org/pav/hasVersion> <hash://sha256/163d7d61947cf3d68836ad2af8f3f7cb8d24dff62cd5a7231633da2d6234059c> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985011/download> <http://purl.org/pav/hasVersion> <hash://sha256/163d7d61947cf3d68836ad2af8f3f7cb8d24dff62cd5a7231633da2d6234059c> <urn:uuid:94fc4661-1ffb-4aad-84e6-4f10efb89666> .
<https://datadryad.org/api/v2/files/3985008/download> <http://purl.org/pav/hasVersion> <hash://sha256/7e4a5b92d12bef0a233afa5b0f877bf93e4f6bdea47f4f11e234b159d35ea7be> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985008/download> <http://purl.org/pav/hasVersion> <hash://sha256/7e4a5b92d12bef0a233afa5b0f877bf93e4f6bdea47f4f11e234b159d35ea7be> <urn:uuid:66329493-e621-4acf-bbc1-c21357b58cbd> .
<https://datadryad.org/api/v2/files/3985009/download> <http://purl.org/pav/hasVersion> <hash://sha256/313eaa20cf99ea1dcb5991cd6c3747734a1d68b85cc7f563df452a5cd70d384b> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985009/download> <http://purl.org/pav/hasVersion> <hash://sha256/313eaa20cf99ea1dcb5991cd6c3747734a1d68b85cc7f563df452a5cd70d384b> <urn:uuid:52fe9827-ac3a-4743-9162-387e9cb12eb3> .
<https://datadryad.org/api/v2/files/3985004/download> <http://purl.org/pav/hasVersion> <hash://sha256/bf83fa7b986b72be199e6ab8d6d4d9ffa21b778aae56a0965b5b2f7424e6acc8> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985004/download> <http://purl.org/pav/hasVersion> <hash://sha256/bf83fa7b986b72be199e6ab8d6d4d9ffa21b778aae56a0965b5b2f7424e6acc8> <urn:uuid:7875627c-96d5-4692-8808-351d38381b7c> .
<https://datadryad.org/api/v2/files/3985005/download> <http://purl.org/pav/hasVersion> <hash://sha256/1221316f6744ac9e00e1374c11a6edfe23032c7e39ab402bd3defca5be3e9013> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985005/download> <http://purl.org/pav/hasVersion> <hash://sha256/1221316f6744ac9e00e1374c11a6edfe23032c7e39ab402bd3defca5be3e9013> <urn:uuid:c94e9172-6120-4254-872f-17f5ae787af4> .
<https://datadryad.org/api/v2/files/3985006/download> <http://purl.org/pav/hasVersion> <hash://sha256/ea7fcc0f54c8026075442e26c105a7c28e5ca08df7e17cd70447df05a2a2f447> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985006/download> <http://purl.org/pav/hasVersion> <hash://sha256/ea7fcc0f54c8026075442e26c105a7c28e5ca08df7e17cd70447df05a2a2f447> <urn:uuid:11b26749-427c-4218-936d-5d141f1ada39> .
<https://datadryad.org/api/v2/files/3985010/download> <http://purl.org/pav/hasVersion> <hash://sha256/de75afb0a7222a5591e3e39869befa2c0fb5d7a2e4ade47d49380e1ccb8b39fb> <urn:uuid:8996dfcc-4bea-4973-975a-3a59f000bcde> .
<https://datadryad.org/api/v2/files/3985010/download> <http://purl.org/pav/hasVersion> <hash://sha256/de75afb0a7222a5591e3e39869befa2c0fb5d7a2e4ade47d49380e1ccb8b39fb> <urn:uuid:510da85f-70d2-4fc4-a0ee-1c062c4520d3> .
```

with datadryad metadata containing the related data files published by https://doi.org/10.5061/dryad.6hdr7sr8z as seen on 2026-07-24 . 


```
preston alias https://datadryad.org/api/v2/versions/355108/files \
 | preston cat \
 | jq .
```

being 

```
{
  "_links": {
    "self": {
      "href": "/api/v2/versions/355108/files"
    },
    "first": {
      "href": "/api/v2/versions/355108/files"
    },
    "last": {
      "href": "/api/v2/versions/355108/files?page=1"
    }
  },
  "count": 9,
  "total": 9,
  "_embedded": {
    "stash:files": [
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985003"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985003/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_1_CalculatedTraitMetrics_18Jun2024.csv",
        "size": 35689,
        "mimeType": "application/vnd.ms-excel",
        "status": "copied",
        "digest": "dff4a33ec5fe8ade65c2d157048a9a99b537c316dea6329eb4f23775d2e8f79e",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985013"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985013/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_2_TraitAMraw_18Jun2024.csv.csv",
        "size": 43484,
        "mimeType": "text/csv",
        "status": "created",
        "digest": "5a4504cfdaa90e60db6ab0032af4198ae84d2f2c1fb82481d61ac786ce5fdfb0",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985011"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985011/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_3_TraitMetricsCode_18Jun2024.R",
        "size": 6084,
        "mimeType": "",
        "status": "copied",
        "digest": "163d7d61947cf3d68836ad2af8f3f7cb8d24dff62cd5a7231633da2d6234059c",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985008"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985008/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_4_SpeciesDescriptions_18Jun2024.csv",
        "size": 66741,
        "mimeType": "text/csv",
        "status": "copied",
        "digest": "7e4a5b92d12bef0a233afa5b0f877bf93e4f6bdea47f4f11e234b159d35ea7be",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985009"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985009/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_5_SpeciesListWithAccnNum_Oct2023.csv",
        "size": 7407,
        "mimeType": "text/csv",
        "status": "copied",
        "digest": "313eaa20cf99ea1dcb5991cd6c3747734a1d68b85cc7f563df452a5cd70d384b",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985004"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985004/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_6_LSUseqsLROR-FLR2_28Oct2023.fasta",
        "size": 191075,
        "mimeType": "",
        "status": "copied",
        "digest": "bf83fa7b986b72be199e6ab8d6d4d9ffa21b778aae56a0965b5b2f7424e6acc8",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985005"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985005/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_7_FinalTree_Oct2023.tre",
        "size": 81480,
        "mimeType": "",
        "status": "copied",
        "digest": "1221316f6744ac9e00e1374c11a6edfe23032c7e39ab402bd3defca5be3e9013",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985006"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985006/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "DataRecord_8_PhyloanalysisCode_28Oct2023.txt",
        "size": 241707,
        "mimeType": "text/plain",
        "status": "copied",
        "digest": "ea7fcc0f54c8026075442e26c105a7c28e5ca08df7e17cd70447df05a2a2f447",
        "digestType": "sha-256"
      },
      {
        "_links": {
          "self": {
            "href": "/api/v2/files/3985010"
          },
          "stash:dataset": {
            "href": "/api/v2/datasets/doi%3A10.5061%2Fdryad.6hdr7sr8z"
          },
          "stash:version": {
            "href": "/api/v2/versions/355108"
          },
          "stash:files": {
            "href": "/api/v2/versions/355108/files"
          },
          "stash:download": {
            "href": "/api/v2/files/3985010/download"
          },
          "curies": [
            {
              "name": "stash",
              "href": "https://github.com/datadryad/dryad-app/blob/main/documentation/apis/link_relations.md#{rel}",
              "templated": "true"
            }
          ]
        },
        "path": "README.md",
        "size": 5802,
        "mimeType": "text/markdown",
        "status": "copied",
        "digest": "de75afb0a7222a5591e3e39869befa2c0fb5d7a2e4ade47d49380e1ccb8b39fb",
        "digestType": "sha-256"
      }
    ]
  }
}
```

# Indexing 

[![GloBI Review by Elton](../../actions/workflows/review.yml/badge.svg)](../../actions/workflows/review.yml) [![GloBI](https://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:globalbioticinteractions/traitam&refutes=true&refutes=false)](https://globalbioticinteractions.org/?accordingTo=globi:globalbioticinteractions/traitam)

Configuration to help Global Biotic Interactions (GloBI, https://globalbioticinteractions.org) index: 

Chaudhary, Bala; Nokes, Liam; Gonzalez, Jennifer et al. (2025). TraitAM, a global spore trait database for arbuscular mycorrhizal fungi [Dataset]. Dryad. https://doi.org/10.5061/dryad.6hdr7sr8z
