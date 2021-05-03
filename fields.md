<center>
    <img src="https://media.gettyimages.com/photos/new-york-interior-picture-id817635976?s=2048x2048" title="The Million Dollar Staircase, inside the NYS Capitol Building" alt="The Million Dollar Staircase, inside the NYS Capitol Building">
</center>

# Field descriptions

Information in these tables was obtained from the data.ny.gov pages where the data was downloaded from.  See links for each dataset on [this page](datasets.md).

## Data 1 - Taxable Sales And Purchases Quarterly Data: Beginning Sales Tax Year 2013-2014

| Field | Column Name | Description | Type |
|:---:|:---|:---|:---|
| 0 | Status | Status of Data: P = Preliminary, subject to revision; F = Final | Plain Text |
| 1 | Sales Tax Year | Sales Tax Year: from March 1 to February 28/29 | Plain Text |
| 2 | Selling Period | The sales tax quarters run from: March yyyy – May yyyy, June yyyy – August yyyy, September yyyy – November yyyy, and December yyyy – February yyyy. | Plain Text |
| 3 | Sales Tax Quarter | The sales tax quarter: 1 = March – May; 2 = June – August; 3 = September – November; 4 = December – February. Note: quarter 4 includes March – February for vendors filing annual returns (annual returns generally account for less than 0.5% of sales tax receipts). | Plain Text |
| 4 | Jurisdiction | The State (NY State), Metropolitan Commuter Transportation District (MCTD), New York City and county where the reported sale or use occurred. The MCTD is composed of New York City (Manhattan, Bronx, Kings/Brooklyn, Queens, Richmond/Staten Island), and the counties of Dutchess, Nassau, Orange, Putnam, Rockland, Suffolk, and Westchester. | Plain Text |
| 5 | NAICS Industry Group | The North American Industry Classification System (NAICS) four-digit industry group code, including unclassified. Beginning with sales tax year 2016-2017, the NAICS industry group uses the 2017 NAICS codes. Prior to sales tax year 2016-2017, the NAICS industry group uses the 2012 NAICS codes with the following industries reported only at the three-digit level: 3130, 3140, 4810, 4870, 5620, 6110, 6220, 6230. | Plain Text |
| 6 | Description | The description of the industry group associated with a NAICS code. | Plain Text |
| 7 | Taxable Sales and Purchases | The amount of taxable sales and purchases reported by vendors. Notes: Zero values indicate the vendor reported a zero; a blank indicates that no values were reported or that there are no vendors in that industry. Negative values indicate a credit or refund claimed. | Number |
| 8 | Jurisdiction Sort Order | Sort order on jurisdiction. | Number |
| 9 | Row Update Indicator | Unique field used in the update of new/revised data | Plain Text |

## Data 2 - State and Local Sales Tax Distributions: Beginning Fiscal Years Ended March 31, 1995

| Field | Column Name | Description | Type |
|:---:|:---|:---|:---|
| 0 | Fiscal Year Ended | New York State Fiscal Year Ended March 31 | Number |
| 1 | Taxing Jurisdiction | Name of the jurisdiction imposing a general retail sales and compensating use tax or sales tax on a consumer utilities services or other special commodities or services. | Plain Text |
| 2 | Amount Distributed | Net amount of sales tax distributions to each taxing jurisdiction, in US dollars, during the fiscal year identified. A \$0<!-- escape $ --> value may indicate the city no longer imposed the tax during that period. Refer to <a href="http://www.tax.ny.gov/pdf/publications/sales/pub718a.pdf">Enactment and Effective Dates of Sales and Use Tax Rates – Publication 718-A</a> | Number |
| 3 | Jurisdiction Sort Order | Sort order on the Taxing Jurisdiction | Number |

## Data 3 - Current Employment Statistics: Beginning 1990

| Field | Column Name | Description | Type |
|:---:|:---|:---|:---|
| 0 | Area | Geographic Area Code | Plain Text |
| 1 | Area Name | Geographic Area Name | Plain Text |
| 2 | Series | Code identifying the specific series | Plain Text |
| 3 | Title | Industry Name | Plain Text |
| 4 | Year | Year of Data. Beginning 1990. | Number |
| 5 | Month | Month of Data | Number |
| 6 | Current Employment | Number of Jobs | Number |

## Data 4 - Active Corporations: Beginning 1800

There are 30 fields of this dataset.  The first 6 are detailed here.  The remaining fields are all address-related (for example, agent and CEO addresses).

| Field | Column Name | Description | Type |
|:---:|:---|:---|:---|
| 0 | DOS ID | Unique ID number for each corporation. | Plain Text |
| 1 | Current Entity Name | Current name of corporation. | Plain Text |
| 2 | Initial DOS Filing Date | Date of incorporation. | Date & Time |
| 3 | County | County where entity is incorporated. | Plain Text |
| 4 | Jurisdiction | State or country of jurisdiction. | Plain Text |
| 5 | Entity Type | Type of incorporation. | Plain Text |
| 6 | DOS Process Name | Address: name line for service of process address. | Plain Text |

## Data 5 - New York State Corporate Tax Credits by Major Industry Group: Beginning Tax Year 2001

| Field | Column Name | Description | Type |
|:---:|:---|:---|:---|
| 0 | Tax Year | Tax year of the credit claim; typically, the year preceding the calendar year, although extensions and fiscal years may result in a longer interval. | Number |
| 1 | Tax Article | The dataset only contains data for corporate franchise taxpayers filing under Article 9‐A of the Tax Law. It does not include statistics for taxpayers filing as banks under Article 32*, insurance companies filing under Article 33, or taxpayers filing under any of the various sections of Article 9. Nor does it provide data for taxpayers claiming credits under Article 22, the Personal Income Tax. <i> \*Starting in 2015, banks and general business corporations file under the same tax article – (Article 9‐A).</i> | Plain Text |
| 2 | Credit Type | Profile of credit values consisting of the components credit earned, claimed, used and carried forward. Credit earned is the amount of credit generated in the current tax year. Credit claimed is the amount of credit that taxpayers have available to use and refund during the taxable year. Credit used is the amount of credit that taxpayers actually apply to their tax liability. Credit carried forward is any unused amount of credit that is allowed to offset tax liability in future years. | Plain Text |
| 3 | Credit Name | Name of the credit. For a list of credits with detailed credit information and expiration dates, see the link to Article 9‐A credit provisions, under Additional Resources. | Plain Text |
| 4 | NAICS Description | The major industry group category is based on the North American Industry Classification System (NAICS). Taxpayers report their principal business activity using NAICS codes from their federal tax returns. Therefore, the NAICS code may not be indicative of the type of activities actually being undertaken in New York. The NAICS descriptions provided within the dataset may vary between years because NAICS codes are reviewed every five years (in the years ending in ‘2’ or ‘7’) for potential revisions so that the classification system can keep pace with the changing economy. | Plain Text |
| 5 | Notes | Disclosure identifies whether the data in columns have a value, but is not reported. d/ ‐ Tax Law secrecy provisions prohibit the disclosure of data for instances of less than three taxpayers. 1/ Chapter 56 of the Laws of 2011 created the New York Youth Works Tax Credit Program. Chapter 56 of the Laws of 2015 renamed the program the Urban Youth Jobs Program Tax Credit. Chapter 59 of the Laws of 2017 further renamed the program the New York Youth Jobs Program Tax Credit. 2/ Beginning in 2016 the Beer Production Credit was renamed the Alcoholic Beverage Production Credit and expanded to include wine, liquor and cider. | Plain Text |
| 6 | Number of Taxpayers | Number of taxpayers taking the credit. | Number |
| 7 | Amount of Credit | The amount of the credit generated, claimed, used, refunded, or carried forward in the tax year based on the credit type. | Number | 
| 8 | Percent of Credit | Percentage of the amount of credit by NAICS description within each credit type. | Number | 
| 9 | Median Amount of Credit | The central value representing an equal number of credit values above and below it. | Number | 
| 10 | Mean Amount of Credit | Average amount of credit in a given category. | Number | 
| 11 | Group Sort Order | Indicator to sort by NAICS description. | Number | 
| 12 | Credit Type Sort Order | Indicator to sort the credit type. |  | 

<p align="center">
    <center><h1 style="font-size:1vw">
        <i>
            <a href = "README.md">RETURN TO MAIN MARKDOWN PAGE</a></h1>
    </center>
    </p>


<center>
    <img src="https://media.gettyimages.com/photos/landscape-with-cohoes-falls-picture-id1188990007?s=2048x2048" title="The Cohoes Falls, Cohoes, NY - the Hudson River is actually an estuary and is at sea level until this point" alt="The Cohoes Falls, Cohoes, NY - the Hudson River is actually an estuary and is at sea level until this point">
</center>
