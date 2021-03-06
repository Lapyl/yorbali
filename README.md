# Yorbali package
## for general-purpose data-processing tools

### How to install

pip install yorbali

### How to upgrade

pip install yorbali --upgrade

### How to use

import yorbali
or
from yorbali import *

### Modules included

CreData(rec=100000, dys=1000, dst='01/01/2017', pof=1):

    Create a dataframe with rec number of records, spread over dys mumber of
    days starting from date dst, including pof percent of offsetting records.
    Two records are offsetting if they have same values for "item" fields;
    and positive "amounts" record is followed by negative "amounts" record.

GetOffs(dfr, cre, cvl, cdt):

    Identify offsetting records in dataframe dfr, with array cre of
    grouping fields, array cvl of amount fields, and date field cdt.

GroupDf(dfr, cgp, cvl):

    Run GroupBy on a datafarme dfr, for all possible combinations of fields
    specified in array cgp, and evaluate Sum for fields in array cvl.

HighCol(col, dct={"z":"white"}):

    Use this as an argument in dataframe.style.apply,
    to highlight columns specified by keys of dictionary dct.

FormDis(dfr, num=5):

    Format and display num number of rows of dataframe dfr,
    with float-type values in 2 decimals and yellow color.

### Version History

- 0.0.2 2020-08-30 Added CreData and GetOffs.

- 0.0.1 2020-08-29 Initial release. Included GroupDf and FormDis.
