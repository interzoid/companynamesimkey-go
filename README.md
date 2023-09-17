## companynamesimkey-go

Go package for generating a similarity key from the input data used to match with other similar company name data. Use the generated similarity key, rather than the actual data itself, to match and/or sort company name data by similarity. This avoids the problems of data inconsistency, misspellings, and name variations when matching within a single dataset, and can also help matching across datasets or for more advanced searching.

The key generation is based on a series of tests, algorithms, AI, and an ever-growing body of Machine Learning-based generated knowledge.

### Usage

To generate the similarity key, you will need the following information:

- an API License key, available at https://www.interzoid.com
- an individual full name to generate the similarity key for

Begin by retrieving the package:

    go get "github.com/interzoid/companynamesimkey-go"

Import the package into your code:

    import "github.com/interzoid/companynamesimkey-go"    

Then, feed the information into the GetSimKey() method:

    simkey, code, credits, err := CompanyNameSimKey.GetSimKey("YOUR-API-KEY","Bank of America")


The return values will be the similarity key, a code (success or failure), how many remaining credits on your API key, and any error messages. The similarity key can be used to search for other similar company names, to sort large datasets by similarity, and perhaps use additional attributes to identify duplicates/redundancy.

Examples:


    Bank of America  ->  wAR3laPfUVvB784_iH0cw7aQbKhr26sophlZ4z7iqtM
    Bank of Amer Corp  ->  wAR3laPfUVvB784_iH0cw7aQbKhr26sophlZ4z7iqtM

    AMAZON.COM  ->   EP88bx0VFDaIh-cOt86c8pOJ6lNkb_TWiKFpmMKXakY
    Amazon Inc.  ->  EP88bx0VFDaIh-cOt86c8pOJ6lNkb_TWiKFpmMKXakY

See Also:

**Individual Name Similarity Keys**: https://github.com/interzoid/fullnamesimkey-go

**Individual Name Match Scoring**: https://github.com/interzoid/fullnamematchscore-go

**Street Address Similarity Keys**: https://github.com/interzoid/streetaddresssimkey-go
