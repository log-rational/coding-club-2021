---
tags: [Exercises]
title: Exercise 2.1
created: '2020-12-17T04:45:49.001Z'
modified: '2020-12-17T08:39:33.261Z'
---

# Exercise 2.1

Use the web search to find ArcGIS Pro documentation and using documentation for SpatialReference class find the following:

- [ ] Spatial Reference Name
- [ ] Linear unit of the spatial reference
- [ ] Metres per unit of the spatial reference
- [ ] Factory Code or Well Known Identifier of the Spatial Reference
## Answer
```python
print(desc.spatialReference.Name)
print(desc.spatialReference.linearUnitName)
print(desc.spatialReference.meterPerUnit)
print(desc.spatialReference.factoryCode)
```

