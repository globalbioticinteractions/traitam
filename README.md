


# Provenance 

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
