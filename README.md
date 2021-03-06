PseudoNetCDF provides read, plot, and sometimes write capabilities for atmospheric science data formats including:

* CAMx (www.camx.org)
* RACM2 box-model outputs
* Kinetic Pre-Processor outputs
* ICARTT Data files (ffi1001)
* CMAQ Files
* GEOS-Chem Binary Punch/NetCDF files

for a full list of formats see `pncdump --help` and look in the --formats help section.

Lots more available at our [wiki ](http://github.com/barronh/pseudonetcdf/wiki)

Try our:
  * [Install Instructions](http://github.com/barronh/pseudonetcdf/wiki/Install-Instructions)
  * [CAMx Tutorials](http://github.com/barronh/pseudonetcdf/wiki/CAMx-Tutorials)
  * [GEOS-Chem Tutorials](http://github.com/barronh/pseudonetcdf/wiki/GC-Tutorials)
  * [Recipes](Recipes)


Quick tour:
 * [Install](http://github.com/barronh/pseudonetcdf/wiki/Install-Instructions.md):
  * `pip install https://github.com/barronh/pseudonetcdf/archive/v2.0.1.zip` for the most stable version or 
  * `pip install http://github.com/barronh/pseudonetcdf/archive/master.zip` for the latest.
 * Download example icartt file: e.g., [HOx from INTEX-NA](http://www-air.larc.nasa.gov/cgi-bin/enzFile?c16141B08DF7F1ACFBAD5C83F9313E20C792f7075622d6169722f4152435441532f4443385f41495243524146542f4252554e452e57494c4c49414d2f484f785f4443385f32303038303632365f52312e696374)
  * `curl -L ftp://ftp-air.larc.nasa.gov/pub/INTEXA/DC8_AIRCRAFT/BRUNE.WILLIAM/HOX_DC8_20040626_R0.ict`
 * Dump an icartt file in CDL: `pncdump -f ffi1001 HOX_DC8_20040626_R0.ict`
 * Create a netcdf from an icartt file: `pncgen -f ffi1001 HOX_DC8_20040626_R0.ict HOX_DC8_20040626_R0.nc`
