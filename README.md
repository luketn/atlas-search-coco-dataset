# COCO Dataset Transformed for an Atlas Search Demo
A subset of the 2017 Common Objects in Context (COCO) dataset for a demo Atlas Search project and tutorial:  
https://github.com/luketn/atlas-search-coco

### COCO
COCO is an open source large-scale object detection, segmentation, and captioning dataset. You can find it here:
https://cocodataset.org/#explore

There are many facets to this dataset, however this simplified subset of the data only includes the list of objects in each image.

Images linked are licensed as indicated in the LicenseName and LicenseUrl fields of the JSON data. 

### Schema
There are two JSON collections ready to import into MongoDB Atlas (in extended MongoDB JSON format) in the file:  
[AtlasSearchCoco.json.zip](./AtlasSearchCoco.json.zip)

### Atlas Search Index
Here's the JSON for the Atlas Search Index that accompanies it:
```json
{
  "mappings": {
    "fields": {
      "caption": [{"type": "string"}],
      "hasPerson": {"type": "boolean"},
      "accessory": [{"type": "token"}, {"type": "stringFacet"}],
      "animal": [{"type": "token"}, {"type": "stringFacet"}],
      "appliance": [{"type": "token"}, {"type": "stringFacet"}],
      "electronic": [{"type": "token"}, {"type": "stringFacet"}],
      "food": [{"type": "token"}, {"type": "stringFacet"}],
      "furniture": [{"type": "token"}, {"type": "stringFacet"}],
      "indoor": [{"type": "token"}, {"type": "stringFacet"}],
      "kitchen": [{"type": "token"}, {"type": "stringFacet"}],
      "outdoor": [{"type": "token"}, {"type": "stringFacet"}],
      "sports": [{"type": "token"}, {"type": "stringFacet"}],
      "vehicle": [{"type": "token"}, {"type": "stringFacet"}]
    }
  }
}
```
