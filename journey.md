<center>
    <img src="https://media.gettyimages.com/photos/road-markers-indicate-directions-for-the-interstate-87-also-known-as-picture-id698001966?s=2048x2048" title="People new to the Capital Region don't understand instructions to go 'south on the Northwy'" alt="NY Seasons: Almost Winter, Winter, Still Winter, and Construction">
</center>

# Potholes encountered along the way

### Iterating through nested loops

Working with the distribution data (dataset 2), the jurisdictions did not match up with the collections data (dataset 1).  To work with this, I created a csv file which designated a "major jurisdiction" for each "sub jurisdiction".  This was generally cities which are distributed to individually, as well as residential utility tax jurisdictions.  Information was obtained from a report issued by the Office of the State Comptroller: ["Understanding Local Government Sales Tax in New York State"](https://www.osc.state.ny.us/files/local-government/publications/pdf/understanding-local-government-sales-tax-in-nys-2020-update.pdf).

In order to create a dictionary with the major jurisdictions and taxes distributed, the python code included nested loops.  But the output returned was only for a handful of major jurisdictions.  It seemed as if something wasn't being reset after success in the inner loop, and then I was only getting success for the first time it went into the inner loop.  After much frustration, I was able to figure out that the file used for the inner loop did in fact need to be reset - once it got to the end, there was nothing left to look when the next outer iteration instructed to loop through.  The reason it had been working on a few major jurisdictions early on was that I was breaking out of the inner loop, leaving some rows to be iterated through.

```
for row in reader :
    j = row[1]
    y = row[0]
    d = row[2]
    # need to reopen the file each time
    reader2 = csv.reader(open(fn2,'r'))
    if y == '2020' and d != '' :
        for line in reader2 :
            jur = line[0]
            tax_jur = line[1]
            if jur in j or j in jur :
                j2 = tax_jur
                if j2 in DistributeHist.keys() :
                    dist = int(DistributeHist[j2])
                    add_dist = int(d)
                    DistributeHist[j2] = dist + add_dist
                    break
                else:
                    DistributeHist[j2] = int(d)
                    ## count items in JurisCount
                    JurisCount += 1
                    break
```

<center>
<img src="https://media.makeameme.org/created/well-that-didnt-uyd8eh.jpg">
</center>
