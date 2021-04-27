# Spring2021_final_project
#### Spring 2021 IA626 Final Project


<center>
    <img src="https://media.gettyimages.com/photos/highway-to-albany-new-york-state-capitol-skyline-and-government-picture-id661898406?s=2048x2048" title="Albany, NY skyline from above the Dunn Memorial Bridge; OSC is the building on the right which looks like a HoJo's" alt="Albany, NY skyline from above the Dunn Memorial Bridge">
    </center>

## Background

I have been an employee of the New York State government for over 15 years, including 4 years as a sales and use tax auditor.

[Report from the Office of the State Comptroller: "Understanding Local Government Sales Tax in New York State"](https://www.osc.state.ny.us/files/local-government/publications/pdf/understanding-local-government-sales-tax-in-nys-2020-update.pdf)

[New York State Annual Financial Reports from the Office of the State Comptroller](https://www.osc.state.ny.us/reports/finance)

[NYS Sales Tax Return, Annual reporting, ST-101](https://www.tax.ny.gov/pdf/current_forms/st/st101_fill_in.pdf)

### Planned analysis

* Tax collected by jurisdiction 
    * vs tax distributions by jurisdiction
        * This is a common question, are jurisdictions getting everything that gets collected
        * Taxes remitted for a jurisdiction – the data may show the collections for both the state and local portions, or just the local; if both state and local, some jurisdictions would be 50% for the local portion, some would be ~43% (where the tax rate is only 3% for the local), others would higher than 50%.
    * vs employment statistics by geographic area
        * How do the sales tax remittances correlate to the employment statistics, do they lag/lead?
    * vs corporations established
        * How many corporations are established vs tax remittances – is there a correlation?
* Sales tax collected by industry (NAICS) vs corporate tax credits by industry

I was hoping to compare the sales tax collections to corporation taxes during the pandemic, but corporation taxes are audited on a 3 year lag, and the most recent corporation tax information available from DTF are for the tax year 2017.  The information that is available is the tax credits, not the taxes paid.  Whether or not they sales taxes and the corporate credits correlate would be interesting, even if pre-pandemic information must be used.

<center>
    <img src="https://media.giphy.com/media/3oKIPa2TdahY8LAAxy/giphy.gif" alt="Futurama: Philip J. Fry, somewhere in New New York, 31st Century" title="Futurama: Philip J. Fry, somewhere in New New York, 31st Century" />
</center>

### Known hurdles:

The DOL employment information is based on geographic area, not by county or sales tax jurisdiction.  DOL has a document showing the county breakdown of the various geographic areas here:
https://statistics.labor.ny.gov/lsgeog.shtm

Municipalities other than counties are allowed to impose additional taxes, therefore are more sales tax jurisdictions than the 62 counties.  When comparing sales tax revenues to employment and corporation statistics, these jurisdictions may need to be combined with the county-wide taxes.

Also, NYC is made up of 5 counties (boroughs), but is reported as NYC on the sales tax returns.  NYC imposes tax on some things which the state does not, as opposed to other counties, which generally tax either at the state portion or the state + local portions (a noted exception – clothing, which is reported on a separate form).  Tax forms and information:
* https://www.tax.ny.gov/forms/annual_filer_forms_st101_series.htm
* https://www.tax.ny.gov/pdf/current_forms/st/st101_fill_in.pdf

Sales tax quarters are on a February year end.  This needs to be kept in mind when comparing to the other data sets.  The state operated on a 3/31 fiscal year, and the returns for the sales tax year ended February 28(29) are due by 3/20, before the end of the state’s fiscal year.

Corporate tax information is based on the federal tax year, which may be a company’s fiscal year and not the same as a calendar year or the NYS fiscal year.

## Dataset information

All datasets were found on the NYS data.ny.gov website and were in csv format.  The data is provided by the Department of Taxation and Finance, Department of State, and Department of Labor.  API's are available for some of the datasets.

The largest dataset retrieved was the active corportations, at over 3 million lines of data.

For information on the datasets used, [click here](datasets.md)

### Descriptions of fields

For descriptions of fields in the datasets, [click here](fields.md)

### The Journey

“It does not do to leave a live dragon out of your calculations, if you live near one.” – J.R.R. Tolkien.

A plan was mapped out, but things don't usually work 100% the first time.  [Read about the issues I encountered and how I addressed them.](journey.md)

<center>
    <img src="https://media.gettyimages.com/photos/new-york-state-capitol-building-at-night-albany-picture-id136330095?s=2048x2048" title="NYS Capitol Building at night, from the Empire State Plaza" alt="NYS Capitol Building at night, from the Empire State Plaza">
</center>