<center>
    <img src="https://media.gettyimages.com/photos/waterfall-and-bridge-at-watkins-glen-state-park-new-york-picture-id1179601463?s=2048x2048" title="Watkins Glen State Park" alt="Watkins Glen State Park">
</center>


### Dataset 1 -Taxable Sales And Purchases Quarterly Data: Beginning Sales Tax Year 2013-2014

https://data.ny.gov/Government-Finance/Taxable-Sales-And-Purchases-Quarterly-Data-Beginni/ny73-2j3u

* Dataset downloaded April 6, 2021.
    * The data from Dataset 1 only goes through 3Q, 2020-21, or November 2020.  Data was last updated in January 2021, so 4th quarter would theoretically be available in late April 2021.
    * May 2, 2021: checked and found that data was updated on April 29, 2021.  Downloaded updated dateset and re-ran code.
<p>
* The data is on the taxable sales and purchase amounts related to collections/remittances, rather than the tax collected.  This was discovered when I began by finding the total for one county and comparing it to distributions in dataset 2.  The amount needs to have the local sales tax rate applied in order to compare to the distributions.  Because of the various partial exemptions, where something is taxable at the state level but not the local level, or vice versa, that exist - such as clothing, Qualified Empire Zones, and residential utilities, for example - it is unlikely to be a 100% match.
    
* Sales tax year ends in February
    * Quarters end: 
        - 1 - May
        - 2 - August
        - 3 - November
        - 4 - February
    * Final returns for a quarter are generally due by 20 days after the end of the sales tax quarter or year.
<p>
* Dataset 1 is by quarter, so the quarterly amounts must be consolidated in order to reflect annual totals.

### Dataset 2 - State and Local Sales Tax Distributions: Beginning Fiscal Years Ended March 31, 1995

https://data.ny.gov/Government-Finance/State-and-Local-Sales-Tax-Distributions-Beginning-/5g2s-tnb7

* Dataset downloaded April 6, 2021
    
* The data is the distributions of sales tax collected by the state to the counties and muncipalities.  Unlike other states (and you thought NY was bad), vendors report and remit both local and state sales taxes to the state, rather than have to file with each local jurisdiction, and the state sends the sales tax to the smaller jurisdictions.

* Covid shut downs began in NY in March 2020, which was the beginning of the 1st sales tax quarter of the sales tax year 2020-21.

* Though an industry may not make taxable sales, for the most part, such as a manufacturer who only makes wholesale sales, they may report taxable purchases.

* Dataset 2 was last updated in August 2020.

### Dataset 3 - Current Employment Statistics: Beginning 1990

https://data.ny.gov/Economic-Development/Current-Employment-Statistics-Beginning-1990/6k74-dgkb

* Dataset downloaded April 22, 2021

* Dataset 3 was last updated in March 2021.

* This data is on calendar year, so it needs to be translated to sales tax years for comparison.

* DOL areas are not by counties, but by metropolitan areas and counties when they are not designated as a metropolitan area.  A separate file was created in order to match the data to the sales tax data, using [DOL's geographical descriptions].  See [information below.](datasets.md#geographical-areas)

### Dataset 4 - Active Corporations: Beginning 1800

https://data.ny.gov/Economic-Development/Active-Corporations-Beginning-1800/n9v6-gdp6

* Dataset downloaded April 22, 2021

* Dataset 4 was last updated in April 2021.
    
* The information in this dataset is any corporations which are active with the Department of State, created as far back as 1800.  

### Dataset 5 - New York State Corporate Tax Credits by Major Industry Group: Beginning Tax Year 2001

https://data.ny.gov/Government-Finance/New-York-State-Corporate-Tax-Credits-by-Major-Indu/84qh-f5nv

* Dataset 5 was last updated in October 2020.  
    
* As opposed to sales and use tax, this dataset is relate to corporation tax.

* The most recent tax year contained in this dataset is for 2017.
    * I contacted current and former employees of the tax department, but have been unable to determine why this dataset appears to be on a 3-year lag.
<p>
    
* Information about various available corporation tax credits can be [found here.](https://www.tax.ny.gov/bus/ct/article9a_tax_credits.htm)

* Dataset 5 was downloaded on April 29, 2021.

### Geographical Areas
    
I created a csv file for use in comparing data with only geographical areas to data with county designations.  The file name is "DOL_geog_areas.csv".

The source of the information in this file is https://statistics.labor.ny.gov/lsgeog.shtm

### Distributions file

The jurisdictions in the distributions were not just counties, but school districts and municpalities as well.  (School districts sometimes impose additional taxes on residential utilities.)  I created a file "st_distributions_jur.csv" for aligning the data with the sales tax data.
    
### Tax Rates
    
Because the sales tax purchases data is in the gross purchases, rather than the tax remitted, the tax needed to be calculated in order to compare to distributions.  The file "tax_rates_st101.csv" was created using the rates on the ST-101 form to provide rates for calculations.

### Descriptions of fields

For descriptions of fields in the datasets, [click here](fields.md)
</p>    

<p align="center">
    <center><h1 style="font-size:1vw">
        <i>
            <a href = "README.md">RETURN TO MAIN MARKDOWN PAGE</a></h1>
    </center>
    </p>

   <p align="center">
<center>
    <img src="https://media.gettyimages.com/photos/the-power-house-of-boldt-castle-on-heart-island-in-the-saint-lawrence-picture-id842386682?s=2048x2048" alt="Boldt Caslte, Alexandria Bay" title="Boldt Caslte, Alexandria Bay">
    </p>
</center>
