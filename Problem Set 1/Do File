// #1
generate TrumpPercentage = (trump/totalvotes) * 100
generate ClintonPercentage = (clinton/totalvotes) * 100
generate trump_margin = TrumpPercentage - ClintonPercentage

// #2
summarize trump_margin white poverty population

// #3
histogram trump_margin

// #4
twoway (scatter trump_margin poverty)
correlate // used to find out the correlation coefficient

// #7
twoway (scatter povery white [aweight = population])

//#6
bysort stname: egen stpopulation = sum(population)
collapse (firstnm) stpopulation white poverty [aw = population], by(stname)
