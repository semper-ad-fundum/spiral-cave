# Spiral cave

## Morphing


## Terrain view
Terrain view is possible in both Aven and Loch models. `NASADEM_HGT_N42E019.zip` was downloaded from [NASA DEM](https://urs.earthdata.nasa.gov/home), placed in `~/.terraintool` and unpacked there.

`Aven` requires the HGT file from the unpacked archive loaded through `File > Open Terrain` menu option.

`Loch` requires the terrain data to be compiled into the `.lox` file, which is done with the `surveys/nasdem.th` file generated by [TerrainTool](https://www.ubss.org.uk/terraintool/terraintool.php). In TerrainTool the following settings were used:

* Coordinate System: UTM
* Datum: WGS-84
* Ellipsoid: GRS80
* Therion `cs` name: UTM34

Then select `Create` menu and use the following options:

* Grid Reference: 34T 380713 4711095
* E-W Range: 600
* N-S Range: 600
* Spacing: 20
* Grid Ref at: Centre

NASA DEM download:
 
1.  At https://earthexplorer.usgs.gov` in `Data Sets` tab search for and select `NASADEM_HGT`
2.  In the `Search Criteria` tab go to `Polygon` tab and click `Use Map`
3.  Mark the Montenegro area on the map
4.  Search displays only one result,  `NASADEM_HGT_N42E019.zip` for download

Running TerrainTool under `sway`:

```
env _JAVA_AWT_WM_NONREPARENTING=1 java -jar TerrainTool.jar
```
