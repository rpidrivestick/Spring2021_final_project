<!---You may see very mixed code in these documents - I learned to code in html before Google was born.-->
# Spring2021_final_project
#### Spring 2021 IA626 Final Project


<center>
    <img src="https://media.gettyimages.com/photos/highway-to-albany-new-york-state-capitol-skyline-and-government-picture-id661898406?s=2048x2048" title="Albany, NY skyline from above the Dunn Memorial Bridge; OSC is the building on the right which looks like a HoJo's" alt="Albany, NY skyline from above the Dunn Memorial Bridge">
    </center>

## Background

I have been an employee of the New York State (NYS) government for over 15 years, including 4 years as a sales and use tax auditor.  NYS is a large and complex state, and it seems that everything they do is large and complex.  The sales taxes in NYS are no exception.

NYS established a statewide sales tax in 1965, and the statewide sales tax rate is currently 4%.  Counties and municipalities can choose to charge an additional sales tax; if they choose to collect more than 3%, it must be re-approved by the state legislature every 2 years (generally).  There is an additional tax that is collected for counties and municpalities in the Metropolitan Commuter Transportation District.

As I've stated, sales tax is a complicated subject; this begins with most tangible items being taxed, but with specific exemptions, and services are generally <i>not</i> taxable unless enumerated.  Clothing items under &#36;110 are currently exempt, yet counties and municipalities can choose whether or not to enact the exemption, often creating 2 tax rates for a single county.  There are 62 counties in NY (including the 5 boroughs of NYC, which are also counties; these are reported as one jurisdiction for sales tax), and many cities which choose to impose their own sales tax (sometimes shown as "pre-empting" cities), along with the multiple taxes and exemptions, creating a great many jurisdictions and forms to report on.

The sales tax year ends in February, with returns due by the 20th of March, which means timely receipts are in hand by the state for their fiscal year end at March 31st.  This means that the sales tax quarters are not the same as calendar year quarters, nor even the state's fiscal year quarters.  Prior to the enactment of the permanent &#36;110 clothing exemption, the legislature was fond of clothing tax "holidays" in the week leading up to Labor Day.  This was a nightmare for retailers, as August was in one sales tax quarter and September was in another!  (And though it was good PR for the legislature, how many families do you know that are doing their school year shopping in the week before schools started?)

Vendors required to report sales tax in NYS may report only on an annual basis, a quarterly basis, a monthly basis, or, for very large retailers, a part-monthly basis.  Included in sales tax reporting is use tax reporting (also called "purchases subject to tax"); this is for vendors to report tax which was not charged on items they use themselves, such as when purchased online or out of state, or items which they generally purchase for resale.

For more information on the NYS sales tax, an easy to read document is this report from the NYS Office of the State Comptroller (OSC).  This includes information on how the sales tax is collected and how it is distributed, and some maps which appear to have been produced in Tableau, for visualization of information.

[Report from the Office of the State Comptroller: "Understanding Local Government Sales Tax in New York State"](https://www.osc.state.ny.us/files/local-government/publications/pdf/understanding-local-government-sales-tax-in-nys-2020-update.pdf)

For example, the report details how St. Lawrence County's 4% is distributed.  St. Lawrence County has no pre-empting cities.

>First 3.00%: The County retains 50% and distributes 6.437389% to the City of Ogdensburg. The remaining 43.562611% is distributed to towns and villages based on property value and population. <br>Additional 1.00%: The County retains 83.562611% and distributes 6.437389% to the City of Ogdensburg. The remaining 10% is distributed to towns and villages based on property value and population.

NYS Annual Financial Reports from the Office of the State Comptroller can be found here:
<br>[New York State Annual Financial Reports from the Office of the State Comptroller](https://www.osc.state.ny.us/reports/finance)

An example NYS Sales Tax return, for Annual reporting:
<br>[NYS Sales Tax Return, Annual reporting, ST-101](https://www.tax.ny.gov/pdf/current_forms/st/st101_fill_in.pdf)

## Planned analysis

* Tax collected by jurisdiction 
    * vs tax distributions by jurisdiction
        * This is a common question, are jurisdictions getting everything that gets collected
        * Taxes remitted for a jurisdiction – the data may show the collections for both the state and local portions, or just the local; if both state and local, some jurisdictions would be 50% for the local portion, some would be ~43% (where the tax rate is only 3% for the local), others would higher than 50%.
    * vs employment statistics by geographic area
        * How do the sales tax remittances correlate to the employment statistics, do they lag/lead?
    * vs corporations established
        * How many corporations are established vs tax remittances – is there a correlation?
* Sales tax collected by industry (NAICS) vs corporate tax credits by industry
    * <i>I was hoping to compare the sales tax collections to corporation taxes during the pandemic, but corporation taxes are audited on a 3 year lag, and the most recent corporation tax information available from the Department of Taxation and Finance (DTF) are for the tax year 2017.  The information that is available is the tax credits, not the taxes paid.  Whether or not they sales taxes and the corporate credits correlate would be interesting, even if pre-pandemic information must be used.</i>


<p align="center">
<center>
    <img src="https://media.giphy.com/media/3oKIPa2TdahY8LAAxy/giphy.gif" alt="Futurama: Philip J. Fry, somewhere in New New York, 31st Century" title="Futurama: Philip J. Fry, somewhere in New New York, 31st Century" /><br>
<a href="https://giphy.com/gifs/producthunt-shut-up-and-take-my-money-3oKIPa2TdahY8LAAxy">via GIPHY</a>
    </p>
</center>

## Known hurdles:

- [ ] The Department of Labor (DOL) employment information is based on geographic area, not by county or sales tax jurisdiction.  DOL has a document showing the county breakdown of the various geographic areas at [this link](https://statistics.labor.ny.gov/lsgeog.shtm).

- [ ] Municipalities other than counties are allowed to impose additional taxes, therefore there are more sales tax jurisdictions than the 62 counties.  When comparing sales tax revenues to employment and corporation statistics, these jurisdictions may need to be combined with the county-wide taxes.

- [ ] Also, NYC is made up of 5 counties (boroughs), but is reported as NYC on the sales tax returns.  NYC imposes tax on some things which the state does not, as opposed to other counties, which generally tax either at the state portion or the state + local portions (a noted exception – clothing, which is reported on a separate form).  Tax forms and information:
    * https://www.tax.ny.gov/forms/annual_filer_forms_st101_series.htm
    * https://www.tax.ny.gov/pdf/current_forms/st/st101_fill_in.pdf

- [ ] As stated, sales tax quarters are on a February year end.  This needs to be kept in mind when comparing to the other data sets.  The state operates on a 3/31 fiscal year, and the returns for the sales tax year ended February 28(29) are due by 3/20, before the end of the state’s fiscal year.

- [ ] Corporate tax information (such as the tax credits) is based on the federal tax year, which may be a company’s fiscal year and not the same as a calendar year or the NYS fiscal year.

## Dataset information

All datasets were found on the NYS data.ny.gov website and were in csv format.  The data is provided by the Department of Taxation and Finance, Department of State, and Department of Labor.  API's are available for some of the datasets.

The largest dataset retrieved was the active corportations, at over 3 million lines of data.

For information on the datasets used, [see my markdown covering datasets.](datasets.md)

### Descriptions of fields

For descriptions of fields in the datasets, I have created a [fields markdown file with tables for each dataset.](fields.md)

## The Journey

“It does not do to leave a live dragon out of your calculations, if you live near one.” – J.R.R. Tolkien.

A plan was mapped out, but things don't usually work 100% the first time.  [Read about the issues I encountered and how I addressed them.](journey.md)

## What does it mean?

>All your life is Channel 13, Sesame Street, What does it mean?
><br>-"Pressure", Billy Joel

Once the code has been created and run, [what did we learn?](findings.md)

(Channel 13 is the PBS station in NYC.)

<center>
    <img src="https://media.gettyimages.com/photos/new-york-state-capitol-building-at-night-albany-picture-id136330095?s=2048x2048" title="NYS Capitol Building at night, from the Empire State Plaza" alt="NYS Capitol Building at night, from the Empire State Plaza">
</center>