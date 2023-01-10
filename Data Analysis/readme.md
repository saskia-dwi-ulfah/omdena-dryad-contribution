## Findings
* 244 train data rows have no burn_material_amount, 103 validation data rows have no burn_material_amount, 81 test data rows have no burn_material_amount.
* All null values in burn_material_amount (g): from hall venue, with Scott Pine branches in fire bowl material, with manual trigger.
* Most of in_smoke class cases were predicted in hall environment.
* In train and test data, chamber environment shows almost balance distribution for in_smoke and clean_air class.
<br/>

* Overall, train data, validation data, and test data show different distributions.
* gas-scan-0 has more frequencies in last bin.
* gas-scan-1 to gas-scan-9 tend to have more frequencies in left hand side resistances.
<br/>

* There are some patterns in correlation map:
  <br/>All plots in hall venue (train, validation, and test) show encoded_class is + correlated with temperature, + correlated with humid, - correlated with gas_scan.
  <br/>All plots in chamber venue (train, validation, and test) show encoded_class is + correlated with temperature, - correlated with humid, - correlated with gas_scan.
<br/>

* Overall, all temperature boxplots in hall and chamber (train, validation, and test) show in_smoke class has higher mean temperature than clean_air. It matches the findings in correlation map (the higher temperature, the more likely in_smoke).
* All humidity boxplots in hall venue show in_smoke class has higher mean humidity than clean_air. All humidity boxplots in chamber venue show clean_air class has higher mean humidity than in_smoke. 
* Overall, all gas-scan boxplots in hall and chamber (train, validation, and test) show clean_air class has higher mean than in_smoke. It matches the findings in correlation map (the higher gas_scan, the more likely clean_air).
