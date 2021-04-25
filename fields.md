# Field descriptions

## Data 1 - Taxable Sales And Purchases Quarterly Data: Beginning Sales Tax Year 2013-2014

| Column Name | Description | Type |
|---|---|---|
| Status | Status of Data: P = Preliminary, subject to revision; F = Final | Plain Text |
| Sales Tax Year | Sales Tax Year: from March 1 to February 28/29 | Plain Text |
| Selling Period | The sales tax quarters run from: March yyyy – May yyyy, June yyyy – August yyyy, September yyyy – November yyyy, and December yyyy – February yyyy. | Plain Text |
| Sales Tax Quarter | The sales tax quarter: 1 = March – May; 2 = June – August; 3 = September – November; 4 = December – February. Note: quarter 4 includes March – February for vendors filing annual returns (annual returns generally account for less than 0.5% of sales tax receipts). | Plain Text |
| Jurisdiction | The State (NY State), Metropolitan Commuter Transportation District (MCTD), New York City and county where the reported sale or use occurred. The MCTD is composed of New York City (Manhattan, Bronx, Kings/Brooklyn, Queens, Richmond/Staten Island), and the counties of Dutchess, Nassau, Orange, Putnam, Rockland, Suffolk, and Westchester. | Plain Text |
| NAICS Industry Group | The North American Industry Classification System (NAICS) four-digit industry group code, including unclassified. Beginning with sales tax year 2016-2017, the NAICS industry group uses the 2017 NAICS codes. Prior to sales tax year 2016-2017, the NAICS industry group uses the 2012 NAICS codes with the following industries reported only at the three-digit level: 3130, 3140, 4810, 4870, 5620, 6110, 6220, 6230. | Plain Text |
| Description | The description of the industry group associated with a NAICS code. | Plain Text |
| Taxable Sales and Purchases | The amount of taxable sales and purchases reported by vendors. Notes: Zero values indicate the vendor reported a zero; a blank indicates that no values were reported or that there are no vendors in that industry. Negative values indicate a credit or refund claimed. | Number |
| Jurisdiction Sort Order | Sort order on jurisdiction. | Number |
| Row Update Indicator | Unique field used in the update of new/revised data | Plain Text |

## Data 2 - State and Local Sales Tax Distributions: Beginning Fiscal Years Ended March 31, 1995


