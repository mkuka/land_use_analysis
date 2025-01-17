# Land Usage Analysis
We compute the land usage for five counties in the state of Iowa; Black Hawk, Butler, Franklin, Carroll, & Webster. In order to do the analysis, we first create a Shapely Point type object for each pixel and use the affine projection matrix to convert them to positions in UTM Zone 15. 

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
             [-96,43.5],
              [-91,43.5],
              [-91,41],
              [-96,41],
              [-96,43.5]
          ]
        ]
      }
    }
  ]
}
```

### Setup for spyder on Windows
Install [miniconda](https://docs.conda.io/en/latest/miniconda.html) as the admin and relevant python modules, such as [geopandas](https://geopandas.org/en/stable/) to access geospatial data and apply spatial operations on geometric types, and [rasterio](https://rasterio.readthedocs.io/en/latest/) to access geospatial raster data.
```
conda create -n spyder-env -y
conda activate spyder-env
conda install spyder-kernels rasterio -y 

conda install matplotlib
conda install shapely

conda config --env --add channels conda-forge
conda config --env --set channel_priority strict
conda install python=3 geopandas

set spyder preference
```
### Sample results

![2004](https://user-images.githubusercontent.com/45642053/209453023-ae31558c-c82f-4043-9237-5b42cfd90b2c.png)
![2008](https://user-images.githubusercontent.com/45642053/209453024-ea2f46ad-5347-4f4e-874c-7a217a2966a6.png)
![2012](https://user-images.githubusercontent.com/45642053/209453025-eab6fcfe-fa19-461e-9e34-2d720137a3f4.png)
![2016](https://user-images.githubusercontent.com/45642053/209453026-94534499-0c23-49bf-a0f1-8d60d890f3d8.png)
![2020](https://user-images.githubusercontent.com/45642053/209453027-4f4de0db-20bd-4d2a-8757-1ef17c5155a0.png)

County boundaries
![county_bdry](https://user-images.githubusercontent.com/45642053/209453058-2ed63a0b-8f6b-4583-90a4-8e86cd0023d9.png)
